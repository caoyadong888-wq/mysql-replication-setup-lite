# MySQL Replication Setup Kit (lite)

## English

### Purpose

A free preview of the primary half of a local replication lab. You get the primary option file, the lab variable names, and the replication-user template. The compose file, the replica option file, the replica `CHANGE REPLICATION SOURCE TO` statement, and the checker are in the full version.

`MYSQL_IMAGE` stays `mysql:CHECK_UPSTREAM_DOCS`. Check upstream docs before you pull any tag. Passwords here are lab placeholders. The sample mailbox used by the full version is `dba@example.com`.

### Deliverables

- `deliverables/PRIMARY_NOTES.md` — primary options only, in English and Chinese.
- `deliverables/primary.cnf` — `server_id` 1, binary log, and GTID options.
- `deliverables/env.example` — lab variable names and placeholder values.
- `deliverables/init/01-repl-user.sql.template` — `REPLICATION SLAVE` grant with unfilled markers.
- `examples/lab.env` — the same placeholders filled for the lab names.

### Quick start

Read `deliverables/PRIMARY_NOTES.md` and compare it with `deliverables/primary.cnf`. Do not start a container from this preview. There is no compose file here.

## 中文

### 用途

本地复制实验里“主库这一半”的免费预览。你得到主库选项文件、实验变量名，以及复制账号模板。compose 文件、从库选项文件、从库的 `CHANGE REPLICATION SOURCE TO` 语句和检查器在完整版里。

`MYSQL_IMAGE` 保持为 `mysql:CHECK_UPSTREAM_DOCS`。拉取任何标签之前请 check upstream docs。这里的口令是实验占位符。完整版示例行使用的邮箱是 `dba@example.com`。

### 交付清单

- `deliverables/PRIMARY_NOTES.md` — 只讲主库选项，中英都有。
- `deliverables/primary.cnf` — `server_id` 为 1，以及二进制日志和 GTID 选项。
- `deliverables/env.example` — 实验变量名和占位值。
- `deliverables/init/01-repl-user.sql.template` — 带未填标记的 `REPLICATION SLAVE` 授权。
- `examples/lab.env` — 按实验名字填好的同一组占位符。

### 快速开始

先读 `deliverables/PRIMARY_NOTES.md`，再对照 `deliverables/primary.cnf`。不要用这个预览启动容器。这里没有 compose 文件。

Full version: GUMROAD_URL
