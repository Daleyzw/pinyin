# pinyin
汉字转带有声调的汉语拼音，汉字转无声调的汉语拼音，汉字转成汉语拼音首字母，获取英文姓名首字母，获取中文名


#### Install

```
composer require yuzhiwei/pinyin
```

#### Example

```php

//没有声调
$testStr = $pinyin->transformWithoutTone("你好，中国");

var_dump($testStr); //string(13) "nihaozhongguo"

//汉字首字母
$testStr1 = $pinyin->transformUcwords("中国");

var_dump($testStr1);  //string(2) "ZG"

$testStr1 = $pinyin->transformFirstUcwords("北京");

var_dump($testStr1);  //string(2) "B"

//有声调
$testStr2 = $pinyin->transformWithTone("你好，中国");

var_dump($testStr2);  //string(24) "nǐ hǎo ，zhōng guó "

//获取英文名首字母
$testStr3 = $pinyin->getFirstCharacter('peter pang');
var_dump($testStr3);  //string(2) "PP"

//获取中文名
$testStr4 = $pinyin->getFirstName("吴彦祖");
var_dump($testStr4);   //string(6) "彦祖"
    
```
