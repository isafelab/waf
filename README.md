iSafeLab 成员主要均为安全研究爱好者，代码可能不是特别好，如有不当，还望斧正。

# 关于
一款基于 PHP 的轻量型 WEB防火墙，旨在于信息安全发展

考虑到性能和简单性，这个脚本只提供了基础的功能防护（简单和误报的均衡)，目标是为了进行最基础的SQL注入和XSS防护。

不要过度依赖本模块，弱密码、代码逻辑错误等不在本防火墙防御内（网络安全不是一个文件就能解决的问题）

 > 本项目为开源项目，未收取任何费用，有问题请借助 Issues 提交 或者通过群友互助
 
 ## 白名单问题
 根据程序逻辑，不建议设置白名单，强烈建议把白名单留空

  如程序中包含 /admin /admin.php /wp-admin /dede 这种路径导致被拦截

  我只想问一句，后台页面不改的吗。。。
 
  ## 安装及使用
  将下载的 isafeLab-Waf.zip 解压后，得到 isafeLab 文件夹，并上传至网站根目录

  在全局加载的文件中( 示例网站根目录下: index.php 或 config.php )，加入如下代码：
  
```php
if(is_file($_SERVER['DOCUMENT_ROOT'].'/isafeLab/isafe-Waf.php')){
    require_once($_SERVER['DOCUMENT_ROOT'].'/isafeLab/isafe-Waf.php');
} //注意文件路径
```
