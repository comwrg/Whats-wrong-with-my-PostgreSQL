# Whats-wrong-with-my-PostgreSQL

## user 关键字坑
比如 `select * from table where user='123';` 并不会像别的数据库那样执行

试一下 `select user` 你便知道, 这里的`user`是指的当前用户名

所以, 要将`user`转义, 变成 `select * from table where "user"='123';`

