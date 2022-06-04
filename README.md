# 监测IP是否被阻断

利用 `PHP socket` 去监测指定 `域名/IP` 的 `TCP` 和 `ICMP` 是否开放.

请开启 `exec()` 函数.

测试环境为:宝塔面板 PHP7.0+ nginx1.15 

请安装 `PHP socket` 扩展(宝塔面板默认是安装的),否则无法使用哦

> 已知问题在Linux下 `socket` 检测 `icmp`,会没有权限.现只能用 `exec()` 函数

## 部署方法

把 `check.php` 分别放到国内服务器和国外服务器.

修改 `index.html` 的GET 请求地址即可.

![教程](https://mjj.today/temp/1910/ec034efc07983847.png "教程")

## 预览

![预览](https://cdn.u1.huluxia.com/g3/M01/E9/0A/wKgBOV2b8heARHU7AAAvxkpyM1M813.png "预览")

## 最后说说

其实可以把这两个请求合并为一个请求...有时间在改改.

![表情](https://cdn.u1.huluxia.com/g3/M02/E9/0B/wKgBOV2b8tSAb9RdAABR3-XN9bs744.jpg "表情")

## 调用API
curl -s https://www.recordaily.com/qiang.php --date 'ip=8.8.8.8&port=53'
