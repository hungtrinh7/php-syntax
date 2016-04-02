# php-syntax

Empty
```php
$empty = ""; // datatype: string
$x = empty($empty); // true
$x = is_null($empty); // false
$x = isset($empty); // true
$x = (bool)$empty; // false
```

NULL
```php
$null = NULL; // datatype: NULL
$x = empty($null); // true
$x = is_null($null); // true
$x = isset($null); // false
$x = (bool)$null; // false
```

Not set
```php
$notSet; // datatype: NULL
$x = empty($notSet); // true
$x = is_null($notSet); // true
$x = isset($notSet); // false
$x = (bool)$notSet; // false
```

Array
```php
$array = array(); // datatype: array
$x = empty($array); // true
$x = is_null($array); // false
$x = isset($array); // true
$x = (bool)$array; // false
$x = (array('a'=>'foo') == array('b'=>'foo')); // false
```

Array merge
```php
$arrOne = array(''=>'');
$arrTwo = array('9'=>'apple', '15'=>'banana', '20'=>'grapefruit');
$x = array_merge($arrOne, $arrTwo); // $x = array(''=>'', 0=>'apple', 1=>'banana', 2=>'grapefruit');
```

Boolean
```php
$bool = FALSE;
$x = empty($bool); // true
$x = is_null($bool); // false
$x = isset($bool); // true
$x = (bool)(-1); // true
```

Datatype
```php
$x = ("15" == 15); // true
```

Reference
```php
$a = "hello";
$b = &$a;
$b = "world"; 
echo $a; // $a = world

$a = "hello";
$b = &$a;
unset($b);
$b = "world"; 
echo $a; // $a = hello

$a = "hello";
$b = &$a;
unset($b); 
echo $a; // $a = hello

$a = "hello";
$b = &$a;
$b = "world";
unset($b); 
echo $a; // $a = world
```

Pre post increment
```php
$a = 1;
$b = $a++;
echo $b; // 1

$a = 1;
$b = ++$a;
echo $b; // 2 

$a = 1;
$x = &$a;
$b = $a++;
echo $b; // 1

$a = 1;
$x = &$a;
$b = ++$a;
echo $b; // 2
```
