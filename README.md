# Others

## 1. 幂等 ：执行多次的结果和执行一次的结果相同（对一个数套绝对值和对它套一百次绝对值结果是相同的）
###  保证幂等：
   1.1  Token令牌机制---客户端请求页面的时候，服务器会随机生成一个Token保存在session里面并把令牌返回给客户端，客户端下次提交时会带着这个token，服务器会把客户端的token和自己session里面的token比较，相等就是第一次提交，然后更改session里面的token，客户端的token不变，下次提交两个token不相等，客户端提交失败..（不能多次提交订单，多次扣款等） 
   1.2  利用数据库唯一主键---设置一个对应数据库的唯一主键，再次插入就会冲突；
   1.3   版本号version  ????....
