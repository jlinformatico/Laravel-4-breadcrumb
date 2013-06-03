l4breadcrumb
============

A small and easy customizable breadcrumb generator for Laravel 4.

edit the .json
============

Edit your .json file and add the following line to your "require"

``"mj/breadcrumb": "dev-master"``

After this run the `composer update` to update your framework and get the breadcrumb class loaded into your files.

Setup
============

Open app.php in your config folder

1. Add the line `'Mj\Breadcrumb\BreadcrumbServiceProvider'` to the providers array.

2. To make use of the Facade that comes with Laravel 4, make sure you register the alias in the file 'app/config/app.php'.

Like this: `'Breadcrumb'      => 'Mj\Breadcrumb\Facades\breadcrumb'`

Usage
============

To create breadcrumbs use the following code:

``Breadcrumb::addbreadcrumb('linkname', 'url');``

You can add multiple breadcrumbs by repeating the code above.

To set an seperator you can use:

``Breadcrumb::setSeperator('yourseperator')``

At last send your breadcrumbs to your template (or just generate them) with the following command:

``Breadcrumb::generate()``
