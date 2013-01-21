static-combiner-php
===================

Script that combines static files (JS/CSS), with a file cache functionality. Implemented with PHP.

It is originally based on the code on this URL:
http://rakaz.nl/2006/12/make-your-pages-load-faster-by-combining-and-compressing-javascript-and-css-files.html

Thanks, -ashiina (https://github.com/ashiina)

Usage
------------

1) Configure the directory settings in combine.php:
```
 29 
 30 >   $ROOT_DIR = '/path/to/staticfiles';
 31 >   $cache    = true;
 32 >   $cachedir = $ROOT_DIR . '/_cache';
 33 >   $cssdir   = $ROOT_DIR . '/css';
 34 >   $jsdir    = $ROOT_DIR . '/js';
 35 
```

2) Put it whereever you want (e.g. your DocumentRoot):
```

[root@localhost /]# cd /var/www/html/
[root@localhost /]# ls
combine.php

```

3) Hit the URL with whatever CSS/JS files you want to combine,
in the format below.
If any of the files do not exist, it will return a 404 error.
 * type : type of file (css|js)
 * files : list of files, each separated with a comma. Can also specify files under directories too

```
wget http://localhost/combine.php?type=css&files=common.css,bootstrap.css,lib/more.css
```

License
------------

Please refer to the license stated in the source code.



