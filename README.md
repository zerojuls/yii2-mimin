Yii2 Mimin
===============
Simple RBAC Manager fo Yii 2.0. Minify of yii2-admin extension

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist hscstudio/yii2-mimin "*"
```

or add

```
"hscstudio/yii2-mimin": "*"
```

to the require section of your `composer.json` file.


Usage
-----

Once the extension is installed, simply use it in your code by  :

in config
```php
'as access' => [
     'class' => 'hscstudio\mimin\components\AccessControl',
     'allowActions' => [
		'site/login', 
		'site/error'
	],
],
...,
'modules' => [
	'mimin' => [
		'class' => 'hscstudio\mimin\Module',
	],
	...
],
'components' => [
	'authManager' => [
		'class' => 'yii\rbac\PhpManager', // or use 'yii\rbac\DbManager'
	],	
],
```
You can then access Auth manager through the following URL:

```
http://localhost/path/to/index.php?r=mimin/user
http://localhost/path/to/index.php?r=mimin/role
http://localhost/path/to/index.php?r=mimin/route
```



