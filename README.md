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
$sms->templateId = '你的模板id';
$sms->templateCodeKey = '模板中验证码对应占位符';

$bool = $sms->sendCode('18688888888', '1234');

var_dump($bool);
```
