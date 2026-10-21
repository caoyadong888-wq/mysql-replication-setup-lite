# Primary options

## English

This preview is the primary server only. It is a lab file, not a production configuration.

`server_id` must be unique. MySQL documents the range 1 through 4294967295. This file uses 1. The full version uses 2 on the replica. Check upstream docs.

`gtid_mode` and `enforce_gtid_consistency` are both `ON`. MySQL requires the pair to agree when GTID is on. Check upstream docs. `binlog_format` is `ROW`. Check upstream docs before you use another format with GTID.

`bind-address` is `0.0.0.0` so a replica on a lab network can connect. That is a listen address inside a container, not a host publish rule. The full version publishes host ports on `127.0.0.1` only.

`MYSQL_ROOT_PASSWORD` and `MYSQL_DATABASE` are the Docker Official Image variables this lab uses. `MYSQL_USER` is not set. Those variables do nothing when the data directory already holds a database. The image README describes `/etc/mysql/conf.d` for extra option files and `/docker-entrypoint-initdb.d` for first-start SQL. Check upstream docs for the tag you pin.

The account template grants `REPLICATION SLAVE` only. Check upstream docs before you widen it. The full version renders the template and mounts it on the primary.

## 中文

这个预览只有主库。它是实验文件，不是生产配置。

`server_id` 必须唯一。MySQL 文档中的范围是 1 到 4294967295。本文件使用 1。完整版的从库使用 2。请 check upstream docs。

`gtid_mode` 和 `enforce_gtid_consistency` 都是 `ON`。打开 GTID 时 MySQL 要求这一对设置一致。请 check upstream docs。`binlog_format` 是 `ROW`。在 GTID 下改用别的格式之前请 check upstream docs。

`bind-address` 是 `0.0.0.0`，让实验网络上的从库可以连接。这是容器内部的监听地址，不是宿主机的发布规则。完整版只把宿主机端口发布到 `127.0.0.1`。

本实验使用 Docker 官方镜像的 `MYSQL_ROOT_PASSWORD` 和 `MYSQL_DATABASE`。不设置 `MYSQL_USER`。数据目录里已经有库时，这些变量不会再生效。镜像说明用 `/etc/mysql/conf.d` 放额外选项文件，用 `/docker-entrypoint-initdb.d` 放首次启动 SQL。你钉住的标签请 check upstream docs。

账号模板只授予 `REPLICATION SLAVE`。加宽权限之前请 check upstream docs。完整版会渲染模板并把它挂到主库上。
