---
layout:     post
title:      SpringBoot整合Elasticsearch
subtitle:   SpringBoot整合Elasticsearch
date:       2023-03-22
author:     Bamboo
header-img: img/post-bg-e2e-ux.jpg
catalog: true
tags:
    - SpringBoot
    - Elasticsearch
---

>我们写数据库设计文档时，总是需要以Excel的格式写数据库结构。

# 1、在Navicat中新建查询，运行以下命令
```sql
SELECT
COLUMN_NAME `字段名称`,
COLUMN_TYPE `数据类型`,
IF(IS_NULLABLE='NO','√','×') AS '不是null',
COLUMN_DEFAULT `默认值`,
COLUMN_COMMENT `注释`
FROM
INFORMATION_SCHEMA.COLUMNS
where
-- databaseName为数据库名称
table_schema ='databaseName'
AND
-- tableName为表名 不写会查询出所有的表
table_name = 'tableName'
```

# 2、复制到Excel表格

在导出的结果中，先ctrl+a，选中所有的查询结果，然后`右击`->​​`复制为`​​​->`​​制表符分隔值(字段名和数据)`​​。
复制完成后直接到Excel表格中粘贴就可以了。

![](/img-post/2023-03-24-a-001.png)


# 3、Navicat也可以直接导出为Excel表格
    
运行语句，然后点击`导出结果`->`到处当前结果`->`选择Excel数据表/文件`，然后一直点击`下一步`就可以了。

![](/img-post/2023-03-24-a-002.png)