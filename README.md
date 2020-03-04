# Clockwork

Clockwork is a browser extension, providing tools for debugging and profiling your PHP applications, including request data, application log, database queries, routes, visualisation of application runtime and more.


# Installation

This readme contains installation and usage instructions for the Laravel framework, for other integrations check out the Clockwork website.

Install the Clockwork library via Composer.

$ composer require itsgoingd/clockwork  


If you are running the latest Laravel version, congratulations you are done!

For Laravel versions older than 5.5, you'll need to register the service provider, in your config/app.php:

'providers' => [
	...
	Clockwork\Support\Laravel\ClockworkServiceProvider::class
]
By default, Clockwork will only be available in debug mode, you can change this and other settings in the configuration file. Use the vendor:publish Artisan command to publish the configuration file into your config directory.

Clockwork comes with a clock() helper function, which provides an easy way to add records to the Clockwork log and events to the timeline.

If you prefer to use a Facade, add following to your config/app.php:

'aliases' => [
	...
	'Clockwork' => Clockwork\Support\Laravel\Facade::class,
]
