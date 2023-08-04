# Python-21-
Python学习笔记(21)
# p68 元组的创建方式
'第一种，使用()'
t=('Python','hello',98)
print(t)
print(type(t))

t2='Python','world',98  #这样也是可以的
#当包含一个元组的元素，需要使用逗号和小括号
t=(10,)

'第二种创建方式，使用内置函数tuple()'
t1=tuple(('Python','world',98))
print(t1)
print(type(t1))

'空元组的创建方式'
lst=[]
lst1=list()

d={}
d2=dict()

#空元组
t4=()
t5=tuple()

print('空列表',lst,lst1)
print('空字典',d,d2)
print('空元组',t4,t5)



# p69 为什么要将元组设计成不可变序列
t=(10,[20,30],9)
print(t)
print(type(t))
print(t[0],type(t[0]),id(t[0]))
print(t[1],type(t[1]),id(t[1]))
print(t[2],type(t[2]),id(t[2]))
'尝试将t[1]修改为100'
print(id(100))
t[1]=100  #报错，元组是不允许修改元素的
'由于[20,30]为列表，而列表是可变序列，所以可以向列表中添加元素，而列表的内存地址不变'
t[1],append(100)  #向列表添加元素
print(t,id(t[1]))  #id是不变的，元组中的对象本身不可变，元组的对象是可变对象，允许更改



# p70 元组的遍历
'元组的遍历'
t=('Python','world',98)
'使用第一种获取元组的方式，使用索引'
print(t[0])
print(t[1])
print(t[2])
'获取元组的第二种方式，遍历元组'
for item in t:
    print(item)
