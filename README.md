# This project is not maintained. Google replaced CityHash with FarmHash and I don't use PHP enough anymore to put time into porting FarmHash

Working on porting Google's CityHash (http://code.google.com/p/cityhash/) to its own PHP PECL Extension.

CityHash is awesome, I'd love to see its adoption spread and I thought that a PECL extension for it might help. I wrote an alpha-version of it and it creates cityhash64/cityhash128 functions.
```
<?php
$test = array("I", "do", "not", "know", "about", "making", "awkward", "rhopalic", "sentences", ".",);
foreach ($test AS $a) {
        echo cityhash64($a)." - $a\n";
        echo cityhash128($a)." - $a\n";
}
```
Just phpize/configure/make to create the extension. It isn't fully polished (missing licenses and comments), but works great and is really just 6 hours away from being 1.0 worthy. I'd love your feedback on this.
