# Mysql
## 数据库的相关概念
    Db
      database:存储数据的大仓库，有组织，有规范
    Dbms
      database management system: DB是通过DBMS创建和操作的容器
      分为两大类：
        基于共享文件
        基于客户机
    SQL
      结构化查询语言:与数据库通信的语言
      
## 程序编写(导入+查询)
    Use sakila;
    SELECT *
    FROM customer
    -- where customer_id = 1
    ORDER BY first_name
### SELECT子句
### WHERE子句(用来做判断)
    后面跟AND OR来做同步处理等
    WHERE XXX AND XXX OR XXX
    WHERE XXX NOT IN (XXX)
    WHERE XXX BETWEEN XX AND XX
    WHERE XXX LIKE XX
    % 匹配所有字符 _匹配单个字符
    WHERE XXX REGEXP 'XX' (跟like差不多，不过regexp是正则)
    WHERE XXX IS NULL 缺少值的记录
    用法： 'rose|jack|john'
           '[abc]d' 匹配 ad，bd，cd '[a-c]d'
           '^' beginning
           '$' end
           
 ### 数据排序
    ORDER BY XXX
    ORDER BY XXX DESC 反向排序
### limit
    LIMIT NUM
    LIMIT NUM1,NUM2 num1是偏移量，num2指取多少
### JOIN
    JOIN XXX(表) ON XXXX(条件语句) 
    example：
        SELECT *
        FROM order_items oi
        Join sql_inventory.products p
	        ON oi.product_id=p.product_id
### 
