### mysql引擎类型
- 常见的 myisam innodb
    - myisam是最简单的引擎,不支持事务,但是读写速度快,主要依靠3个后缀的文件来实现存储(frm MYD MYI)
    - innodb是常用的引擎,支持事务,支持外键,支持自增列,读写性能相比前者慢一些,有共享表空间和多表空间两种存储方式,但是表结构都是放在.frm后缀的文件中
- 还有memory merge rdb等
    - memory是基于内存的,
    - merge是多张myisam引擎的表的集合

### mysql的索引
- mysql有唯一索引(BTree,hash等) 全文索引 空间索引几种类型
- myisam和innodb均使用BTree索引(索引的数据结构),部分版本支持全文索引(fulltext),myisam支持空间索引(spatial)
- mysql也可以使用前缀索引,即对索引字段的前N个字符创建索引
- 索引的设计是有原则的
    - 搜索的索引列(即where关键字后的列,连接子句中指定的列)
    - 使用唯一索引
    - 使用短索引
    - 利用最左前缀(即使用N列索引中最左边的列集来匹配,成为最左前缀)
    - 不要过度索引