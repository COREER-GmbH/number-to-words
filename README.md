# number-to-words

- updated for PHP 8

Convert numbers to words in English or German.

Install via Composer
-
```bash
$ composer require coreer/number-to-words
```

How to use
-
English
-
```php
use NumberToWords\NumberToWords;
use NumberToWords\Locale\English;
 
$c = new NumberToWords(new English()); // english
 
// One followed by 3003 zeros
echo $c->nameOfLargeNumber(3003); // outputs "millinillion"
 
echo $n->convert('3043.43'); // outputs "three thousand forty-three point four three"
echo $n->convert('3.1415926535'); // outputs "three point one four one five nine two six five three five"
```

German
-
```php
use NumberToWords\NumberToWords;
use NumberToWords\Locale\German;
 
$c = new NumberToWords(new German()); // german
 
// Eine Eins gefolgt von 6000 Nullen
echo $c->nameOfLargeNumber(6000); // outputs "Millinillion"
 
// Eine Eins gefolgt von 59994 Nullen
echo $c->nameOfLargeNumber(59994); // outputs "Nonillinovenonagintanongentillion"
 
echo $n->convert('509324'); // outputs "fünfhundertneuntausenddreihundertvierundzwanzig"
echo $n->convert('3,1415926535'); // outputs "drei Komma eins vier eins fünf neun zwei sechs fünf drei fünf"
```
