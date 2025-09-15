https://www.nowcoder.com/practice/a37b91f84cdf490b8d8b990794211135?tpId=383&tqId=11210039&sourceUrl=%2Fexam%2Foj%3Fpage%3D1%26tab%3D%25E7%25AE%2597%25E6%25B3%2595%25E5%25AD%25A6%25E4%25B9%25A0%25E7%25AF%2587%26topicId%3D383

全局的::lower_bound和upper_bound二分查找函数在访问Random access iterator的
随机访问迭代器支持所有前向与双向迭代器的操作，包括 ++、--、*、==、!=，此外还支持 +、- 运算、[] 运算符访问、<、>、<=、>= 比较以及两迭代器之间的距离计算，接口非常丰富。
也就是支持类似it+7的访问，
双向迭代器只能支持++ --，
而set容器的迭代器就是双向迭代器，导致了::lower_bound、::upper_bound的性能退化到了O(n)。

#Note: 回顾二分查找算法，会想起来其依赖left, right双指针和mid的随机访问。

而使用set容器自带的lower_bound和upper_bound就可以利用红黑树的性质达成O(log n)的复杂度。