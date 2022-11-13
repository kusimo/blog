<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## Laravel Requirement

See all the requirements, for example, you need to have PHP version that is equal to or greater than 7.25. [See more on installation by visiting Laravel site](https://laravel.com/docs/7.x/installation).

I'm using Mac, the process will be different on Windows. Please visit [Laravel Installation Guide](https://laravel.com/docs/8.x/installation#installation-via-composer)

Once your system meets all the requirement, install [Composer](https://getcomposer.org/) as Laravel use this to manage its dependencies. 
 

Download the Laravel installer using Composer:

```
composer global require laravel/installer
```

Edit the bash profile by placing composer system-wide vendor bin directory in your $PATH so laravel executable can be located by the system. You can do this by placing this code in your bash_profile.

```
nano ~/.bash_profile
```

Add the code below to the file that is opened

```
export PATH="$PATH:$HOME/.composer/vendor/bin"
```

Update the the current terminal to detect the changes or open another terminal

```
source ~/.bash_profile
```


## Create a new project
Run the below command to create new project. project-name is the name in the command is the name of your project name or folder that Laravel will be installed.

```
laravel new the-project-name
```
Navigate to the the project you just created
```
cd project-name
```

## Run the project
```
php artisan serve
```

## Getting to know Laravel

Open up the foler that contains your Laravel project, you will see that there are lots of folder there. When you run the <code>php artisan serve</code>, the folder that holds the html can be found under resources/views.

Inside the views folder you will find a file 'welcome.blade.php', this is called blade template. This is the file that generate our view, the one we see on the homepage. Every blade template will have 'blade.php' extension. 

If you open this up, you will see that it just look like normal HTML file. You can change a piece of text and reload the page to view your changes. 

We will come back to view, but let's start with Routing.

### Routing
Expand the 'routes' folder, we are going to be working in the web.php for the most part. You will see that there is an api.php file as well this is used when creating an API project.

In the web.php file, we are going to be loading all our views and controllers. The route is what handles all the requests and return the views - accepts a request and redirect it to a function. 

```
Route::get('/', function () {
    return view('welcome');
});
```

The example above shows that the route accepts a get request with path of root ('/') and returns a welcome page view. Another way of saying this is if the page is home, return a page that is called welcome (welcome.blade.php). This is how we load a view.
> Note the welcome in the name of the file and the welcome in the view function parameter, this needs to match. No need to put '.blade.php'. 


Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework.

You may also try the [Laravel Bootcamp](https://bootcamp.laravel.com), where you will be guided through building a modern Laravel application from scratch.

If you don't feel like reading, [Laracasts](https://laracasts.com) can help. Laracasts contains over 2000 video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

## Laravel Sponsors

We would like to extend our thanks to the following sponsors for funding Laravel development. If you are interested in becoming a sponsor, please visit the Laravel [Patreon page](https://patreon.com/taylorotwell).

### Premium Partners

- **[Vehikl](https://vehikl.com/)**
- **[Tighten Co.](https://tighten.co)**
- **[Kirschbaum Development Group](https://kirschbaumdevelopment.com)**
- **[64 Robots](https://64robots.com)**
- **[Cubet Techno Labs](https://cubettech.com)**
- **[Cyber-Duck](https://cyber-duck.co.uk)**
- **[Many](https://www.many.co.uk)**
- **[Webdock, Fast VPS Hosting](https://www.webdock.io/en)**
- **[DevSquad](https://devsquad.com)**
- **[Curotec](https://www.curotec.com/services/technologies/laravel/)**
- **[OP.GG](https://op.gg)**
- **[WebReinvent](https://webreinvent.com/?utm_source=laravel&utm_medium=github&utm_campaign=patreon-sponsors)**
- **[Lendio](https://lendio.com)**

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
