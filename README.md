# SQLTools
SQLTools 专门用于测试数据库性能的小工具。

# 性能测试示例
<pre>
3.1.1.多线程插入性能测试
==============================================JDBC测试10.10.11.218=================
java -jar SQLTEST.jar 参数说明
============================================================插入性能===========================================
[0]  -INTEGER  线程个数
[1]  -STRING   操作类型  参数请输query|insert|queryandinsert|insertandquery
[2]  -INTEGER  每次执行的记录数
[3]  -STRING   是否限制查询记录数   unlimit

**********************************======java -jar SQLTEST.jar 20 insert 5000
线程20执行完成，耗时：1227ms,约1s
线程19执行完成，耗时：1946ms,约1s
线程18执行完成，耗时：2745ms,约2s
线程17执行完成，耗时：3628ms,约3s
线程16执行完成，耗时：4353ms,约4s
线程15执行完成，耗时：5827ms,约5s
线程14执行完成，耗时：6588ms,约6s
线程13执行完成，耗时：7337ms,约7s
线程11执行完成，耗时：8161ms,约8s
线程12执行完成，耗时：8908ms,约8s
线程9执行完成，耗时：9829ms,约9s
线程7执行完成，耗时：10640ms,约10
线程6执行完成，耗时：13758ms,约13
线程5执行完成，耗时：15526ms,约15
线程4执行完成，耗时：16393ms,约16
线程3执行完成，耗时：16991ms,约16
线程2执行完成，耗时：17891ms,约17
线程8执行完成，耗时：18898ms,约18
线程10执行完成，耗时：19728ms,约1
线程1执行完成，耗时：20692ms,约20
线程运行完成，共计耗时：20699ms
**********************************======java -jar SQLTEST.jar 10 insert 10000
线程10执行完成，耗时：1767ms,约1s
线程9执行完成，耗时：3326ms,约3s
线程7执行完成，耗时：4773ms,约4s
线程8执行完成，耗时：6540ms,约6s
线程6执行完成，耗时：7962ms,约7s
线程5执行完成，耗时：9634ms,约9s
线程4执行完成，耗时：11377ms,约11s
线程3执行完成，耗时：12514ms,约12s
线程2执行完成，耗时：14116ms,约14s
线程1执行完成，耗时：15692ms,约15s
线程运行完成，共计耗时：15694ms

**********************************======java -jar SQLTEST.jar 5 insert 20000
线程5执行完成，耗时：2930ms,约2s
线程1执行完成，耗时：4906ms,约4s
线程4执行完成，耗时：6916ms,约6s
线程3执行完成，耗时：9016ms,约9s
线程2执行完成，耗时：10661ms,约10s
线程运行完成，共计耗时：10666ms


**********************************======java -jar SQLTEST.jar 2 insert 50000

线程2执行完成，耗时：6022ms,约6s
线程1执行完成，耗时：10487ms,约10
线程运行完成，共计耗时：10490ms

**********************************======java -jar SQLTEST.jar 1 insert 50000

线程1执行完成，耗时：15230ms,约15s
线程运行完成，共计耗时：15235ms

3.1.2.多线程读取性能测试

============================================================读取性能===========================================
[0]  -INTEGER  线程个数
[1]  -STRING   操作类型  参数请输query|insert|queryandinsert|insertandquery
[2]  -INTEGER  每次执行的记录数
[3]  -STRING   是否限制查询记录数   unlimit


SELECT * FROM mycat_hsae_db.t_location t LEFT JOIN data_number.t_vehicle v ON t.F_VEHICLE_ID=v.F_ID

**********************************======java -jar SQLTEST.jar 20 query 5000
数据库已连接:true
线程1执行完成，耗时：193ms,约0s
线程18执行完成，耗时：338ms,约0s
线程14执行完成，耗时：502ms,约0s
线程10执行完成，耗时：672ms,约0s
线程6执行完成，耗时：847ms,约0s
线程19执行完成，耗时：1004ms,约1s
线程17执行完成，耗时：1163ms,约1s
线程13执行完成，耗时：1323ms,约1s
线程11执行完成，耗时：1487ms,约1s
线程9执行完成，耗时：1651ms,约1s
线程20执行完成，耗时：1818ms,约1s
线程16执行完成，耗时：1977ms,约1s
线程12执行完成，耗时：2137ms,约2s
线程8执行完成，耗时：2318ms,约2s
线程4执行完成，耗时：2482ms,约2s
线程7执行完成，耗时：2650ms,约2s
线程5执行完成，耗时：2810ms,约2s
线程15执行完成，耗时：2975ms,约2s
线程3执行完成，耗时：3133ms,约3s
线程2执行完成，耗时：3297ms,约3s
线程运行完成，共计耗时：3299ms

**********************************======java -jar SQLTEST.jar 10 query 10000
线程1执行完成，耗时：345ms,约0s
线程10执行完成，耗时：675ms,约0s
线程6执行完成，耗时：1001ms,约1s
线程9执行完成，耗时：1323ms,约1s
线程5执行完成，耗时：1643ms,约1s
线程8执行完成，耗时：1966ms,约1s
线程7执行完成，耗时：2307ms,约2s
线程4执行完成，耗时：2670ms,约2s
线程3执行完成，耗时：2992ms,约2s
线程2执行完成，耗时：3326ms,约3s
线程运行完成，共计耗时：3328ms


**********************************======java -jar SQLTEST.jar 5 query 20000
线程1执行完成，耗时：671ms,约0s
线程5执行完成，耗时：1333ms,约1s
线程4执行完成，耗时：1982ms,约1s
线程3执行完成，耗时：2690ms,约2s
线程2执行完成，耗时：3339ms,约3s
线程运行完成，共计耗时：3342ms

**********************************======java -jar SQLTEST.jar 2 query 50000
线程1执行完成，耗时：1638ms,约1s
线程2执行完成，耗时：3258ms,约3s
线程运行完成，共计耗时：3260ms


**********************************======java -jar SQLTEST.jar 1 query 100000
线程2执行完成，耗时：3211ms,约3s
线程运行完成，共计耗时：3218ms

3.1.3.单线程读写性能测试

============================================================单线程读写性能（读取不限条数-unlimit）===========================================
============================================================读取性能===========================================
[0]  -INTEGER  线程个数
[1]  -STRING   操作类型  参数请输query|insert|queryandinsert|insertandquery
[2]  -INTEGER  每次执行的记录数
[3]  -STRING   是否限制查询记录数   unlimit


**********************************======java -jar SQLTEST.jar 1 queryandinsert 10000  unlimit
线程2执行完成，耗时：1721ms,约2s


**********************************======java -jar SQLTEST.jar 1 queryandinsert 20000  unlimit
线程2执行完成，耗时：3627ms,约4s


**********************************======java -jar SQLTEST.jar 1 queryandinsert 30000  unlimit
线程2执行完成，耗时：5176ms,约5s


**********************************======java -jar SQLTEST.jar 1 queryandinsert 40000  unlimit
线程2执行完成，耗时：6736ms,约7s

**********************************======java -jar SQLTEST.jar 1 queryandinsert 50000  unlimit
线程2执行完成，耗时：9596ms,约10s

**********************************======java -jar SQLTEST.jar 1 queryandinsert 60000  unlimit
线程2执行完成，耗时：11642ms,约12s


**********************************======java -jar SQLTEST.jar 1 queryandinsert 70000  unlimit
线程2执行完成，耗时：15830ms,约16s

**********************************======java -jar SQLTEST.jar 1 queryandinsert 80000  unlimit
线程2执行完成，耗时：21860ms,约22s

**********************************======java -jar SQLTEST.jar 1 queryandinsert 90000  unlimit
线程2执行完成，耗时：30311ms,约30s

**********************************======java -jar SQLTEST.jar 1 queryandinsert 100000  unlimit
线程2执行完成，耗时：37585ms,约38s

</pre>
