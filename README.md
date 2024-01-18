# AntiQQBrowser
基于PHP编写的 简单QQ防红
<p>
    <img width="200" src="https://github.com/Nel1yMinecraft/AntiQQBrowser/QQ.jpg">
</p>

例如这是你的PHP代码

<?php
echo "test";
>

只需要在你逻辑的签名加上这段代码
// 拦截QQ
$conf['qqjump']=1;
if(strpos($_SERVER['HTTP_USER_AGENT'], 'QQ/')||strpos($_SERVER['HTTP_USER_AGENT'], 'MicroMessenger')!==false && $conf['qqjump']==1){
$siteurl='http://'.$_SERVER['SERVER_NAME'].':'.$_SERVER["SERVER_PORT"].$_SERVER["REQUEST_URI"];
echo '<!DOCTYPE html>
<html>
<head>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
    <title>请使用浏览器打开</title>
    <style type="text/css">
        .fk {
            background-color: #FFF;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 180px;
            color: #FF4444;
        }
    </style>
</head>
<body>
<div class="fk">
    安全提示您！该网站安全。<br>
    请按右上角浏览器打开，放心浏览！
</div>
</body>
</html>
';
exit; 
} 

然后你的PHP代码就会变成


<?php

// 拦截QQ
$conf['qqjump']=1;
if(strpos($_SERVER['HTTP_USER_AGENT'], 'QQ/')||strpos($_SERVER['HTTP_USER_AGENT'], 'MicroMessenger')!==false && $conf['qqjump']==1){
$siteurl='http://'.$_SERVER['SERVER_NAME'].':'.$_SERVER["SERVER_PORT"].$_SERVER["REQUEST_URI"];
echo '<!DOCTYPE html>
<html>
<head>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
    <title>请使用浏览器打开</title>
    <style type="text/css">
        .fk {
            background-color: #FFF;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 180px;
            color: #FF4444;
        }
    </style>
</head>
<body>
<div class="fk">
    安全提示您！该网站安全。<br>
    请按右上角浏览器打开，放心浏览！
</div>
</body>
</html>
';
exit; 
} 

echo "test";
>


