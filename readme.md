【用户认证和授权】
	---- 用户认证（Authentication），就是让用户登录，并且在接下来的一段时间内让用户访问网站时可以使用其账户，而不需要再次登录的机制。

	---- 用户授权（Authorization），就是权限控制，指的是规定并允许用户使用自己的权限，例如发布帖子、管理站点等。

【用户认证和sign签名】
	---- 两者是独立的概念，sign签名是为了提高安全性，校验数据的一致性。
	---- 用户认证是用户登录，登录的时候，可以使用sign签名。

【jwt+sign签名】
	---- 用户登录（sign签名，加密数据）---》jwt匹配数据库  ---》成功，返回Token（Token包含用户的id值） 
	---- 用户带着Token发出请求，经过Authenticate中间件判断用户是否已经登陆过 ---》是，则继续操作；否，返回未认证


【相关技术文档】
http://blog.leapoahead.com/2015/09/07/user-authentication-with-jwt/

http://www.infoq.com/cn/minibooks/download/ES6-in-Depth