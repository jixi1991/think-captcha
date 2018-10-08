# think-captcha
thinkphp5 验证码类库

## 安装
> composer require stylecc/think-captcha


## 使用

```php
$captcha = new \think\captcha\Captcha([
    'imageW'=> 150,
    'imageH'=> 50,
    'length'=> 4,
    'useCurve'=> false,
    'useNoise'=> true,
    'useImgBg'=> false,
    'fontSize'=> 20,
    'fontttf'=> "7.ttf",
    'bg'=> [mt_rand(157,255), mt_rand(157,255), mt_rand(157,255)]
]);
return $captcha->entry('sign_in');
```

```php
$captcha = new \think\captcha\Captcha();
if (!$captcha->check('q2mj','sign_in')) {
    // 验证失败
}
```