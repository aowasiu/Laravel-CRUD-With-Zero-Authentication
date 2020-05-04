# Laravel 5.4 CRUD app with zero authentication

> A that DOESN'T require a user to be logged-in or authenticated before being able to Create, Retrieve, Update and Delete content. The article content are created using Faker. [tags:crud,laravel-app,laravel-crud-app]


### Table of Contents
* Getting Started
* Prerequisites
* Installation
* Running a test
* Testing your laravel5dot4CRUDAppWithZeroAuthentication
* Contributing
* Author
* Deployment
* Built With
* License
* Acknowledgments


## Getting Started

> These instructions will get you a clone of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.


### Prerequisites

> What things you need to install the software and how to install them
* A computer (desktop or laptop), ofcourse.
* What your system architecture is. (32-bit or 64-bit).
* Apache local development server.
* Git (to be installed locally on your computer first).
* Composer (a package manager).
* Node
* A web browser.
* A Laravel installation.


### Installing

> Steps to get the development env running.

You should find out what system architecture your device is. You can find out from your machine. Mine is:

```
Windows 7 Ultimate, RAM 3GB, Processor Intel(R) Core Duo T2600 2.16GHz, 32-bit Operating System.
```

I found out by, turning the computer on, clicking Windows button on the Taskbar and right-clicking on 'Computer'. An information box with the above info pops out.
* The most vital info is:
```
'32-bit Operating System'.
```

NOTE:	The above vital info implies we should only install softwares designed for such systems. Otherwise, the software won't work.

Next, if you don't already have it on your computer, you need to download and install any of the following Apache local server softwares: XAMPP, WAMP or AMPPS. I installed AMPPS. You can find AMPPS at: https://ampps.com/download.
Download and install the version compatible with your system.

```
I installed the one ideal for a '32-bit Operating System' which is AMPPS Version 3.8. This version has Apache, MySQL, PHP, Perl and Python integrated.
```

All PHP projects will be stored in:

```
C:\Program Files\Ampps\www
```

So we'll be storing the clone in the same location.

I assume you have a web browser installed. If not download and install any of:

```
Mozilla Firefox, Google Chrome, Safari or UC browser.
```

Using any search engine, search for 'Git'. Download and install it.

Now that you're done, click your Windows key, click 'All programs', then 'Git' and select 'Git CMD'. This is Git command-line tool on the.

The Git CMD will display a heading of 'Administrator: Git CMD'. While the prompt may show as 'C:\Users\user>'. While _ blinks. Now let's switch to the root directory intended for the project. In Git CMD, run the command:

```
cd C:/Program Files/Ampps/www
```

Git CMD will now display as:

```
C:/Program Files/Ampps/www>
```

To get the link to the repo, just visit the Github page, https://github.com/aowasiu/laravel_5dot4_crud_app_with_zero_authentication, and click on the green “clone or download” button on the right hand side. Copy and include it in the command to install the clone.

NOTE: The copy text is a URL that ends with '.git'.

To install the clone of the Git repository 'laravel_5dot4_crud_app_with_zero_authentication', run the command:

```
git clone https://github.com/aowasiu/laravel_5dot4_crud_app_with_zero_authentication.git/ laravel5dot4CRUDAppWithZeroAuthentication
```

> 'laravel5dot4CRUDAppWithZeroAuthentication' is the name we're giving 'laravel_5dot4_crud_app_with_zero_authentication' in the directory 'C:/Program Files/Ampps/www>'. Therefore, the clone will be installed inside 'C:/Program Files/Ampps/www/laravel5dot4CRUDAppWithZeroAuthentication>'. 

Switch into the project's folder:

```
cd laravel5dot4CRUDAppWithZeroAuthentication
```

Your location will now be in, as defined by Git CMD:

```
C:/Program Files/Ampps/www/laravel5dot4CRUDAppWithZeroAuthentication>
```

>	Whenever you clone a new Laravel project you must now install all of the project dependencies. This is what actually installs Laravel itself, among other necessary packages to get started.

When we run composer, it checks the composer.json file which is submitted to the github repo and lists all of the composer (PHP) packages that your repo requires. Because these packages are constantly changing, the source code is generally not submitted to github, but instead we let composer handle these updates. So to install all this source code we run composer with the following command.


In Git CMD, run the command:

```
composer install
```

> Using any search engine, search for 'Node'. Download and install it.

Node is required for JavaScript applications. Node has its own package manager, npm (Node Package Manager).


> Install NPM Dependencies

Just like how we must install composer packages to move forward, we must also install necessary NPM packages to move forward. This will install Vue.js, Bootstrap.css and Laravel Mix and any Javascript (or Node) packages required. The list of packages that a repo requires is listed in the packages.json file which is submitted to the GitHub repo.


Now in Git CMD, run the command:

```
npm install
```

> Create a copy of your .env file

'.env' files are not committed to GitHub for security reasons. But there is a .env.example which is a template of the '.env' file that the project expects us to have. So we will make a copy of the '.env.example' file and create a '.env' file that we can start to fill out to do things like database configuration in the next few steps. Now run the command:

```
cp .env.example .env
```

The above command will create a copy of the '.env.example' file in your project and name the copy simply '.env'.

> Generate an app encryption key

Laravel requires an app encryption key which is generally randomly generated and stored in .env file. The app will use this encryption key to encode various elements of your application from cookies to password hashes and more.

Laravel’s command line tools make it to generate this. In the terminal we can run this command to generate that key. 

> NOTE: Make sure that you have already installed Laravel via composer and created an .env file before doing this, of which we have done both.

Run the command:

```
php artisan key:generate
```

> NOTE: If you check the .env file again, you will see that it now has a long random string of characters in the APP_KEY field. We now have a valid app encryption key.


You'll find the database in 'SOURCE' folder of laravel5dot4CRUDAppWithZeroAuthentication. Import the database to your development or production server database.

> Before you test on a local or web server, remember to change your database settings in 'laravel5dot4CRUDAppWithZeroAuthentication/.env' to match the local or web server's settings

```
DB_DATABASE=laravel_5dot4_crud_app_with_zero_authentication
DB_USERNAME=secureuser
DB_PASSWORD=SecurePassworD
```

## Running a test

> Development or local server:
To view a list of news articles

```
http://localhost/repositories/laravel5dot4CRUDAppWithZeroAuthentication/public/api/news
```

> Production or web server:
To view a list of news articles
```
http://your-domain/repositories/laravel5dot4CRUDAppWithZeroAuthentication/public/api/news/23
```


### Testing your laravel5dot4CRUDAppWithZeroAuthentication

> List of news articles
This test shows a paginated list of news articles. 
To view a list of news articles:
```
http://localhost/repositories/laravel5dot4CRUDAppWithZeroAuthentication/public/api/news
```

> View of a news article
This test shows a news article. 
To view a news article with id of 23:
```
http://localhost/repositories/laravel5dot4CRUDAppWithZeroAuthentication/public/api/news
```

> NOTICE:	You can test further by following the routes defined in the application. You can find the routes at:
```
open-news-article/routes/api.php
```


## Deployment

It will be most convenient and safe to deploy the application to a live server using FileZilla. FileZilla is an FTP client.


## Built With

* [Laravel 5](https://laravel.com/5.8/docs/) - The web framework used.
* [Faker](https://github.com/fzaninotto/Faker) - Used to generate dummy content.
* [Postman](https://getpostman.com/) - Used to test dummy-content API.


## Contributing

Please read [CONTRIBUTING.md](https://github.com/aowasiu/laravel_5dot4_crud_app_with_zero_authentication/CONTRIBUTING.md) for details on code of conduct, and the process for submitting pull requests to us.


## Author

* **Wasiu Adisa** - *Initial work* - [aowasiu](https://github.com/aowasiu)


## License

This project is licensed under the GNU Ver 3 License - see the [LICENSE.md](LICENSE.md) file for details


## Acknowledgments

* Thanks to my wife for holding the fort while i go clickety clack on the computer.
* Hat tip to Taylor Otwell for creating Laravel, an awesome and beautiful web framework.
* This project is inspired by Brad Traversy's YouTube video, Laravel 5.5 API From Scratch Using resources.
* Thanks also to the creators of Postman.
* Thanks to DevMarketer for steps to cloning a Git repo. (https://devmarketer.io/learn/setup-laravel-project-cloned-github-com/).
* Thanks to Sublime HQ Pty Ltd for making Sublime Text Basic version free.
* Thanks to Softaculous for providing AMPPS, a robust Apache software.
* Thanks to Mozilla for fast Firefox.
* And thanks to GitHub Inc for making its website free.

