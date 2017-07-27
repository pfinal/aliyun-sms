# Http

阿里云短信SDK

## 使用composer 安装

```
composer require pfinal/aliyun-sms
```

## 示例

```php
<?php

require_once __DIR__ . '/vendor/autoload.php';

date_default_timezone_set('PRC');

$sms = new \PFinal\Aliyun\AliyunSMS();

$sms->accessKeyId = '你的accessKeyId';
$sms->accessKeySecret = '你的accessKeySecret';
$sms->signName = '你的签名';

$sms->templateId = '验证码模板id';
$sms->templateCodeKey = '模板中验证码对应占位符';

//发验证码
$bool = $sms->sendCode('18688888888', '1234');
var_dump($bool);

//发普通模板短信
$bool = $sms->templateSMS('18688888888','你的模板id',['var1'=>'value1','var2'=>'value2']);
var_dump($bool);

```
