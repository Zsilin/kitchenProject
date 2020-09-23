# kitchenProject
数据库文件：kcdatabase.sql

数据库默认配置：kitchen_server/config/config/default.js

```
exports.mysql = {
  client: {
    host: 'localhost',
    port: '3306',
    user: 'root',
    password: 'admin',
    database: 'kcdatabase',
  },
};
```

服务器默认端口:7001  kitchen_server/config/config/default.js

```
exports.cluster = {
	listen: {
		path: "",
		port: 7001
	}
}
```

axios请求地址修改 :kitchen_front/src/axios/index.js

```
axios.defaults.baseURL='http://127.0.0.1:7001';
```



server的图片上传路径profileService  shareService中的路径存储默认都是http://127.0.0.1:7001



防止上传文件过大，数据库多数图片资源使用的网上资源，少数图片存储在服务器中。如果服务器的ip和端口号改变，数据库相关的图片资源的路径也需要改变。

