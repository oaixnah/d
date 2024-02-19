# 基础篇

## SQL (Structured Query Language)

> 结构化查询语言

### 1. 通用语法

- 单行或多行书写，以分号 ++semicolon++ 结尾
- 使用 **空格** ++space++ 缩进增加语句的可读性
- 不区分大小写，关键字建议使用**大写**
- 注释：
    - 单行：`--` 或 `#`
    - 多行：`/* 注释内容 */`

### 2. 分类

| 类型  | 全称                         | 说明                         |
|-----|----------------------------|----------------------------|
| DDL | Data Definition Language   | 数据定义语言，用来定义数据库对象（数据库、表、字段） |
| DML | Data Manipulation Language | 数据操作语言，用来对数据库表中数据进行增删改     |
| DQL | Data Query Language        | 数据查询语言，用来查询数据库表中数据         |
| DCL | Data Control Language      | 数据控制语言，用来创建数据库用户、管理访问权限    |

#### 2.1. DDL

=== "数据库"

    ```mysql
    # 查询所有数据库
    mysql> show databases;

    # 查询当前数据库
    mysql> select database();

    # 创建数据库
    mysql> create database [if not exists] <数据库名> [default charset <字符集>] [collate <排序规则>];

    # 删除数据库
    mysql> drop database [if exists] <数据库名>;

    # 切换数据库
    mysql> use <数据库名>;
    ```

=== "表"

    ```mysql
    # 查询当前数据库所有表
    mysql> show tables;

    # 查询指定表结构
    mysql> desc <表名>;

    # 查询指定表的建表语句
    mysql> show create table <表名>;
    ```
