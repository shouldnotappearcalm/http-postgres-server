# 执行 postgres sql 的服务

## 安装

### 1.使用 npm 仓库安装

```bash
npm install -g http-postgres-server
```

### 2.使用源码 安装

```bash
#a.下载源码
#b.进入源码包、安装依赖
npm install
#c. 链接脚本
npm link

```

## 启动服务器

mysql的用户名、密码、数据库名、数据库的地址、端口、http服务的端口 ，下面罗列的均为默认值，可以不填

```bash
http-postgres-server --user sa --password 123456 --host 127.0.0.1  --database postgres --port 5432 --http_port 5555
#如只指定 数据库端口 其他均用默认值
http-postgres-server  --port 5432
```

## 使用方法

启动服务器后，可对该 HTTP 服务器发起 `POST` 请求，假设服务器访问地址为 `http://127.0.0.1:5555`，那么请求地址为 `http://127.0.0.1:555/api/query`

请求参数如下:

|Name|Descrption|
|------|-------|
|sql|需要查询的 sql 语句|

## 示例

请执行正确的 sql，这里我的 schema 是 db_test，同时我的表名也叫做 db_test，请替换伟你的 schema 和 表名

![image](https://user-images.githubusercontent.com/20592210/71551914-456e3700-2a2c-11ea-8ac7-6f45b3d3fa80.png)
