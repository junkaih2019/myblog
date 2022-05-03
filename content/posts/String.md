---
title: "C++字符串基础操作"
date: 2022-05-03T10:36:01+08:00
draft: false
toc: false
images:
tags: 
  - C++
---

# 字符串

## 输入

```cpp
char s[100];
//读到空格、回车为止
cin << s;
scanf("%s", s);
//读入空格，回车
fgets(s,10000,stdin); //注意：会把回车读进来
cin.getline(s,1000)
```

## 输出

``` cpp
printf("%s\n",s);
puts(s);
```

## 常用函数

```cpp
# inlude <cstring>
strlen(s);//不包含‘\0'
strcmp(a,b);//字典序比较，相等为0，a<b返回-1，a>b返回10
strcpy(a,b);//把后面的复制给前面的
```

## String类

```cpp
#include <string>
```

### 初始化

```cpp
string s1; //默认的空字符串
string s2 = s1; //s2是s1的一个副本
string s3 = "hiya";
string s4(10, 'c'); //s4内容：cccccccccc
```

### 输入

```cpp
cin >> s1;//读入空格、回车、换行前的字符串
getline(cin, str);//读入整行
/*注意：string不能用scanf()读入*/
```

### 输出

```cpp
printf("%s", s1.c_str()); //c_str():返回string数组首地址
puts(s1.c_str());
cout << s1;
```

### 常用函数

```cpp
s1.empty(); //当前string是否为空，返回0、1
s1.size(); //当前字符的长度，O(1)速度
s1 > s2; //> < >=  <= == !=
s1 + s2; //"abc"拼接"def"得"abcdef"
s1 += s3;  //支持累加
s1 += "yes"; s1 + '!';//'+'运算符两侧至少有一个string变量
```

### 遍历

```cpp
string s1;
for (int i = 0; i < s1.size(); i++){}
for (auto c : s1){}
for (auto &c : s1){}//遍历得同时改变原string
```



## Trick

```cpp
# 遍历字符串
char str[101];
for(int i = 0, len = strlen(str); i < len; i++){}
for(int i = 0; str[i]; i++){}
```

添加一行信息 再来一次 again

