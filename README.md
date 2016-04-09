# php-syntax

Empty
```php
$empty = ""; // datatype: string
empty($empty); // true
is_null($empty); // false
isset($empty); // true
(bool)$empty; // false
```

NULL
```php
$null = NULL; // datatype: NULL
empty($null); // true
is_null($null); // true
isset($null); // false
(bool)$null; // false
```

Not set
```php
$notSet; // datatype: NULL
empty($notSet); // true
is_null($notSet); // true
isset($notSet); // false
(bool)$notSet; // false
```

Array
```php
$array = array(); // datatype: array
empty($array); // true
is_null($array); // false
isset($array); // true
(bool)$array; // false
(array('a'=>'foo') == array('b'=>'foo')); // false
```

Array merge
```php
$arrOne = array(''=>''); 
$arrTwo = array('9'=>'apple', '15'=>'banana', '20'=>'grapefruit');
$x = array_merge($arrOne, $arrTwo); // $x = array(''=>'', 0=>'apple', 1=>'banana', 2=>'grapefruit');
```

Boolean
```php
$bool = FALSE; // datatype: boolean
empty($bool); // true
is_null($bool); // false
isset($bool); // true
(bool)(-1); // true
```

Datatype
```php
echo ("15" == 15); // true
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

Null coalescing operator (PHP7)
```php
$a = $_GET['a'] ?? 'b'; // return $_GET['a'] if $_GET['a'] exists and is not null, b otherwise
$a = $_GET['a'] ?? $_GET['b'] ?? 'c'; // it can be chained
```

Spaceship operator (PHP7)
```php
echo 1 <=> 1; // 0
echo 1 <=> 2; // -1
echo 2 <=> 1; // 1

echo 1.5 <=> 1.5; // 0
echo 1.5 <=> 2.5; // -1
echo 2.5 <=> 1.5; // 1
 
echo "a" <=> "a"; // 0
echo "a" <=> "b"; // -1
echo "b" <=> "a"; // 1
```
