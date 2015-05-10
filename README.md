# 安卓编程风格总结
## java部分

####package命名
包名按照域名的范围从大到小逐步列出，恰好和Internet上的域名命名规则相反.

	域名: example.com
	包名前缀: com.example

包名的后续部分根据不同机构各自内部的命名规范而不尽相同。这类命名规范可能以特定目录名的组成来区分部门 (department) ，项目(project)，机器(machine)，或注册名(login names)。

    com.example.bhs.iqc;
    com.example.iac.imm

####类命名
大驼峰规则, 类名必须使用名词，或名词词组。要求类名简单，不允许出现无意义的单词

####接口命名
同类命名规则

####方法
小驼峰规则, 可以为动词或动词+名词组合; 限制使用下划线.

一些约定:
1. 返回长度的方法，应该命名为length;
2.	布尔型的判断方法一般要求方法名使用单词 is或has 做前缀，如isPersistent()，isString()。或者使用具有逻辑意义的单词，例如equal 或equals
3.	将对象转换为某个特定类型的方法应该命名为toF
4.	构造方法应该用递增的方式写。（参数多的写在后面）。

####变量命名
1. 普通变量采用小驼峰规则; 限制使用下划线, 限制使用美元符号($), 因为这个字符对内部类有特殊的含义.

2. final static常量的名字应该都大写，并且指出完整含义。如果一个常量名称由多个单词组成，则应该用下划线来分割这些单词如:NUM_DAYS_IN_WEEK MAX_VALUE

3. 如果需要对变量名进行缩写时，一定要注意整个代码中缩写规则的一致性

        context=ctx message=msg
4. 通过在结尾处放置一个量词，就可创建更加统一的变量

5. 无论什么时候，均提倡应用常量取代数字、固定字符串。也就是说，程序中除0，1以外，尽量不应该出现其他数字。
6. 索引变量：i、j、k等只作为小型循环的循环索引变量

7. 逻辑变量：避免用flag来命名状态变量，用is来命名逻辑变量。
	if(isClosed){ dosomeworks; return; }

## Android部分
java代码中不要出现中文，所有的中文描述都放在资源文件中
layout文件命名, 全部用小写字母， 单词与单词之间用下划线分割

    如用在activity或fragment中, 则以activity_  fragment_开头
    如用在list的adapter中, 以listitem_开头
    如果是单独的被include的layout, 以该文件的具体用途命名
id的命名以 控件缩写+下划线+控件用途 来命名
java代码中控件的命名, 以 view缩写+下划线+控件用途 来命名



####注释
Java 程序有两类注释：实现注释(implementation comments)和文档注释(document comments).  
实现注释是使用/*...*/和//界定的注释.  
文档注释(被称为"doc comments")由/**...*/界定。文档注释可以通过javadoc工具转换成HTML 文件。


# 参考
android代码贡献者的编程风格指南  
中文翻译:
http://blog.sina.com.cn/s/blog_48d491300100zwzg.html#dont-ignore-exceptions
英文原版:
http://source.android.com/source/code-style.html
