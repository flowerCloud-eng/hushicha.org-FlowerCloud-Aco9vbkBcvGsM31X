
**SpringBoot使用properties连接数据库时没有出现问题**


**SpringBoot使用yml连接数据库时出现：Unable to connect to Redis**


**并在报错信息中出现：**
![](https://img2024.cnblogs.com/blog/3516733/202410/3516733-20241003151909711-1958418405.png)


发现是用户或者密码出现问题


**通过查询知道yml是区分数据类型的**，所以如果用户名或者密码是**数字**的话，就要注意


![](https://img2024.cnblogs.com/blog/3516733/202410/3516733-20241003152652876-1788241311.png)


**将密码用双引号括起来，将其识别为字符串就可以正常连接了**
（如果密码有特殊字符也需要单引号或者双引号括起来）
![](https://img2024.cnblogs.com/blog/3516733/202410/3516733-20241003152837027-213439123.png)


MYSQL是同样的
**另外如果是MySQL的话还得注意一下mysql版本和驱动版本对应**




| mysql\-connector\-java | MySQL | jdbc | JDK |
| --- | --- | --- | --- |
| 8\.0\.x | 5\.6、5\.7、8\.0 | 4\.2 | JDK 8\.0或更高版本 |
| 5\.1\.x | 5\.6、5\.7、8\.0 | 3\.0、4\.0、4\.1、4\.2 | JDK 5\.0和JDK 8\.0或更高版本 |


![](https://img2024.cnblogs.com/blog/3516733/202410/3516733-20241003153200949-1297913465.png)


 本博客参考[樱花宇宙官网](https://yzygzn.com)。转载请注明出处！
