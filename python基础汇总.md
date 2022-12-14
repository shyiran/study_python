1.input输出

~~~python
password = (input("你的密码是："))
print("你的密码是：",password)
~~~

2.输出类型

~~~Python
a = 10
print(type(a))   #int整形，str字符串

#强制类型转换
a = str("123")
print(type(a))

a = 10
print(type(a))   #int整形，str字符串
#强制类型转换
a = str("123")
print(type(a))
~~~

3.if语句：

~~~Python
#if elif else条件判断语句,if语句嵌套，注意缩进
a = 21
if a>1 and a<=15:
    print("是的")
elif a >15 and a<20:
    print("错的")
else:
    a >20 and a<30
    print("哈哈")
~~~

4.导⼊第⼀个库：随机数库

~~~Python
import random
a = random.randint(1,7)
print(a)
~~~

5.经典猜拳游戏，理解随即库与缩进问题

~~~Python
import random
b = random.randint(0,2)
print(b)
#b = int(b)
a = input("输⼊你的数字：")
a = int(a)
if a > 3:
    print("数字错误")
elif  a == b :
    print("平⼿了")
elif a > b :
    print("你输了")
else:
    print("你赢了")
    pass
~~~

6.for语句学习

~~~Python
for i in range(3):
    print(i)
   
for a in range(1,5,1):
    print(a)
    
a = ['aa','bb','cc']
for i in range(len(a)):
    print(i,a[i])
~~~

7.经典联系：求1-100的和

~~~python
n = 100
sum = 0
counter = 1
while counter <= n :
    sum = sum + counter
    counter += 1
    print("1到100的和为：%d"%(sum))
~~~

8.三种结束符的理解：
pass(空字符)  
continue(结束本次循环，但不结束⼤体的如while框架)   
break(结束整个循环，包括while)
9.字符串的转义
a = "nihao \"nihao"   #讲中间双引号转义输出print(a)b = """    nihao    haode"""print(b)   #三引号输出引号内所有字符串包括空格
10.切⽚
a = "wuhan"print(a[0:3:1])    #起始位置：结束位置：跨境值  0下标开始
11.反斜杠与直接显⽰原始字符串
print("nihao\nhaode")print(r"nihao\nhaode")
12.类型的判断
isalnum（字母加数字为真）isalpha（全字母为真）isdigit（全数字为真）isnumeric（只包含数字字符为真）
13.函数必懂知识点
#len(string)返回字符串长度#lstrip()去掉左边的空格#rstript()去掉字符串末尾的空格#encode(usf-8) 默认为UTF-8
14.列表的使⽤，for与while的遍历
a = ["xiaohuang","xiaoliu","xiaowang"]for i in a:    print(i)length = len(a)o =0while o <length:    print(a[o])    o +=1
15.数据的增加（append，extend，insert）
name = ["A","B","C"]zengjia = input("请输⼊:")aa = ["1","2"]name.append(zengjia)   #将整个列表添加，包括列表的【】name.extend(aa)   #讲列表中的元素增
加到另外⼀个⾥⾯name.insert(1,"d")  #在列表的1号位，插⼊数据d#print(name)print(name)
16.数据的删除 （del，pop，remove）
name = ["A","B","C"]#del name[1]   #删除指定下标的对象#name.pop()  #删除数组组后的⼀位name.remove("B")   #删除指定的对象，但是执⾏⼀次后失效prin
t(name)
17.数据的修改
name = ["A","B","C"]name[1]="D"   #指定数据下表修改print(name)
18.数据的查 （in / not in）
name = ["A","B","C"]na= input("输⼊查找的对象：")if na in name:    print("对象存在")else:    print("不存在")
19.数据的查找
#查找对象位置,不在范围内会报错，后⾯通过异常处理错误就⾏a = ["a","b","c","d","e"]b= [1,3,2,4]print(a.index("c",0,4))  #数据的查找
20.元素的操作
print(a.count("c"))a.reverse()#元素反转输出a.sort()  #元素升序输出print(a)a.sort(reverse=True)  #元素降序输出print(a)
21.#列表list取值嵌套
a = [["a","b"],["c","d"]]print(a[0][0])  #第⼀个列表内取值第⼀个值
22.练习：⼋个对象随机分配到三个库，应⽤random库
import randomoffices =[[],[],[]]names = ["a","b","c","d","e","f","g","d"]for name in names:    a = random.randint(0,2)    offices[a].append(name)#i = 1for office i
n offices:    print("分配个数为%d"%(len(office)),"-"*20)    #i += 1    for name in office:        print("对象名字：%s"%name)        #print("\n")        #print("-"*20)
23.#元组tuple的增删改查
a =(1,2,3,"aa")b =(4,)a = a+b   #增print(a)#del a #删除整个元组print(a)#⽆法修改，可以增加print(a[0])  #查询
24.#元组的转换
a = [1,2]a=tuple()print(type(a))
25.#字典知识点：dict 存储形式（key，value）键值对
dict ={"name":"告⽩","age":20}print(dict["name"])#防⽌访问对象不存在print(dict.get("age"))   #noneprint(dict.get("a","22"))   #未找到设定默认值
26.#字典的增加操作
a = {"name":"hsyy","age":"20"}newname=input("请输⼊新的名字:")a["new"]=newname#print(a["new"])print(a)
27.#字典的删除
a = {"name":"hsyy","age":"20"}print("删除前：%s"%a)del a["name"]#删除⼀个键值对print("删除后：%s"%a)del aprint("全部删除后%s"%a)  #清空后输出会报
错不存在a.clear()#清空字典内容print("清空后：%s"%a)
28.#字典的修改
a = {"name":"hsyy","age":"20"}a["name"]="hsyyy"print(a)
29.#字典的查

~~~PYTHON
a = {"name":"hsyy","age":"20"}
print(a.keys()) #得到所有的键 
print(a.values())  #得到所有的值
print(a.items())  #得到所有的键值对
~~~

30.#遍历所有的键值对

~~~PYTHON
for key in a.keys():  #遍历键    
    print(key)
    for value in a.values():   #遍历值   
        print(value)for key,value in a.items():   
            print("输出键值对：%s:%s"%(key,value)) #遍历键值对 
~~~





31.#枚举排序 0,1,2…
a = ("a","b","c")for i,v in enumerate(a):    print(i,v)
32.#乘法表练习
for x in range(1,10):    print("\t")    for y in range(1,x+1):        result = x * y        print("%d * %d = %d"%(x,y,x*y),end="\t")   #打印⼀个不换⾏
33.#函数的定义
def hanshu():    print("-------")    print("   函数的定义与调⽤   ")    print("-------")#函数的调⽤hanshu()
34.#函数带参数的定义
def addnum(a,b):    c = a+b    print(c)addnum(1,2)  #输出3
35.#返回值计算结果
def addnum(a,b):    return a +bvul = addnum(1,2)#print(addnum(1,2))print(vul)
36.#返回多个结果,逗号分割
def num(a,b):    shang = a/b    yushu = a%b    return (shang,yushu)shang,yushu=num(2,1)print("商等于：%d，余数等于：%d"%(shang,yushu))
37.#练习：⾃动输⼊数字，输出特定的长度
def hengxian():    b=int(input("数字："))    print("-" * b)    #return bhengxian()
38.#求三数字和
def num():    a=int(input("第⼀个数:"))    b=int(input("第⼆个数:"))    c=int(input("第三个数:"))    add = (a + b + c)/3    print(add)num()
39.#输出给定长度练习
def num():    print("-"*10)def xiantiao(m):    i = 0    while i<m:        num()        i +=1  #注意先加1再执⾏xiantiao(int(input()))
40.#全局遍历与局部变量，局部变量调⽤全局变量
a = 100def num():    global a    print(a)  #输出100    a=500    print("%d"%a)  #输出500def numm():    print(a)     #输出500，全局变量被修改num()numm()
41.#⽂件的操作知识点
#⽂件的打开⽅式：r：打开  w：没有就创捷，并且覆盖f = open("cms识别/cms/text.txt","r")#f.write("hello,word")#red = f.read(5)reds = f.readlines()  #全部读
取不加s只读⼀⾏print(reds)i = 0for item in reds:    print("%s:%s"%(i,item)) #按照⾏号读取，注意前⾯的readlines的s    i +=1f.close()
42.#⽂件的重命名/删除 os模块
import os#os.rename("textt.txt","cms识别/cms/textt.txt")   #重命名：旧⽂件名的位置，新⽂件以及问价位置#f = open("cms识别/cms/1.txt","w")#f.close()#os.r
emove("cms识别/cms/1.txt")  #删除⽂件os.mkdir("cms识别/hsyy") #创建⽂件os.rmdir("xx")#删除⽂件夹#还有改变⽬录等等操作。。。
43.#错误和异常的处理知识
try:    f = open("cms识别/cms/textt.txt")except IOError:  #打开⽂件异常，属于IO异常后输出pass占位的结果     pass
44.#读取名称异常处理
try:    num = 1    print(num)    f = open("t.txt")#except (NameError,IOError) as t:  #打印错误信息,只会打印第⼀个except Exception as t:  #涵盖所有的报错信息
，便于排查    print("你出错了!")    print(t)
45.#⽂件的强制（finally）执⾏与嵌套try
try:    f = open("cms识别/cms/textt.txt")    try:        f = open("t.txt")    finally:  # 强制执⾏        f.close()        print("强制执⾏")except Exception as t:    print(t)&#10;著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。