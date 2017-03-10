
<p align="center"><h1>Easy SMS</h1></p>

<p align="center">:calling: The easiest way to send short message.</p>

<p align="center">
<a href="https://travis-ci.org/overtrue/easy-sms"><img src="https://travis-ci.org/overtrue/easy-sms.svg?branch=master" alt="Build Status"></a>
<a href="https://packagist.org/packages/overtrue/easy-sms"><img src="https://poser.pugx.org/overtrue/easy-sms/v/stable.svg" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/overtrue/easy-sms"><img src="https://poser.pugx.org/overtrue/easy-sms/v/unstable.svg" alt="Latest Unstable Version"></a>
<a href="https://scrutinizer-ci.com/g/overtrue/easy-sms/build-status/master"><img src="https://scrutinizer-ci.com/g/overtrue/easy-sms/badges/build.png?b=master" alt="Build Status"></a>
<a href="https://scrutinizer-ci.com/g/overtrue/easy-sms/?branch=master"><img src="https://scrutinizer-ci.com/g/overtrue/easy-sms/badges/quality-score.png?b=master" alt="Scrutinizer Code Quality"></a>
<a href="https://scrutinizer-ci.com/g/overtrue/easy-sms/?branch=master"><img src="https://scrutinizer-ci.com/g/overtrue/easy-sms/badges/coverage.png?b=master" alt="Code Coverage"></a>
<a href="https://packagist.org/packages/overtrue/easy-sms"><img src="https://poser.pugx.org/overtrue/easy-sms/downloads" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/overtrue/easy-sms"><img src="https://poser.pugx.org/overtrue/easy-sms/license" alt="License"></a>
</p>

# Usage

```php
use Overtrue\EasySms\EasySms;

$config = [
    'default' => 'error-log',
    'signature' => '【xxx公司】',
    'gateways' => [
        /*...*/
        'error-log' => [
            'file' => '/tmp/easy-sms.log',
        ],
        /*...*/
        'yun-pian' => [
            'api_key' => '824f0ff2f71cab52936a13ede3xxxxx',
        ],
    ],
];
$easySms = new EasySms($config);
$easySms->gateway('error-log')->send(1888888888, 'hello world!');
```

# License

MIT