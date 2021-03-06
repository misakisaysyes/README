README
===========================
该文件用来测试和展示书写README的各种markdown语法。GitHub的markdown语法在标准的markdown语法基础上做了扩充，称之为`GitHub Flavored Markdown`。简称`GFM`，GFM在GitHub上有广泛应用，除了README文件外，issues和wiki均支持markdown语法。

另外本文记录了基于mermaid插件的常见流程图语法，虽然目前github的GFM解析器并不支持流程图语法(nor does MarkdownPad)，但可以在vscode中安装markdown和mermaid两个插件，便可在vscode中编辑支持流程图的*.md文件。

若要传代码写的流程图上github，可以通过preview截图再按照GFM语法插入*.md中，即便这样，还是觉得代码写图比拖拽制图要方便且快很多，不过因人而异吧~

Anyway, happy reading!

****
	
|原作 |果冻虾仁|
|---|---|
|E-mail|Jelly.K.Wang@qq.com|
|原项目地址|https://github.com/dengzhehou/README|

Amber 补充了流程图部分

****
## 目录
* [1横线](#1横线)
* [2标题](#2标题)
* [3文本](#3文本)
    * 3_1普通文本
    * 3_2单行文本
    * 3_3多行文本
    * 3_4文字高亮
    * 3_5换行
    * 3_6斜粗体和删除线
* [4图片](#4图片)
* [5链接](#5链接) 
    *  5_1链接外部URL
    *  5_2链接本仓库里的URL
    * [5_3图片链接](#5_3图片链接)
    *  5_4锚点
* [6列表](#6列表)
    * 6_1无序列表
    * 6_2多级无序列表
    * 6_3一级有序列表
    * 6_4多级有序列表
    * 6_5复选框列表
* [7块引用](#7块引用)
* [8代码高亮](#8代码高亮)
* [9表格](#9表格) 
* [10表情](#10表情)
* [11diff语法](#11diff语法)
* [12流程图](#12流程图)
  * 12_1流程图
  * 12_2状态图  


### 1横线

---

##### 语法
```
    ***
    ---
    ___
```

##### 效果

***
---
___

<br/>


### 2标题

---

##### 语法
```
    # 一级标题  
    ## 二级标题  
    ### 三级标题  
    #### 四级标题  
    ##### 五级标题  
    ###### 六级标题  
```

##### 效果

# 一级标题  
## 二级标题  
### 三级标题  
#### 四级标题  
##### 五级标题  
###### 六级标题  

<br/>


### 3文本

---

#### 3_1普通文本

这是一段普通的文本

#### 3_2单行文本
##### 语法
```
    //在行开头加1个Tab或4个空格
        Hello,大家好，我是果冻虾仁。
```

##### 效果

    Hello,大家好，我是果冻虾仁。

#### 3_3文本块
##### 语法
```    
    //在连续几行的文本开头加入1个Tab或者4个空格。
        欢迎到访
        很高兴见到您

    //使用一对各三个的反引号
    ```
    我是C++码农
    你可以在知乎、CSDN、简书搜索【果冻虾仁】找到我
    ```
```

##### 效果

    欢迎到访
    很高兴见到您

```
我是C++码农
你可以在知乎、CSDN、简书搜索【果冻虾仁】找到我
```

该语法也可以实现代码高亮，见[8_代码高亮](#8_代码高亮)

#### 3_4文字高亮

##### 语法
```
    `linux` `网络编程` `socket` `epoll` 
```

##### 效果

`linux` `网络编程` `socket` `epoll`

适合给内部文本做高亮，也适合做一篇文章的tag

#### 3_5换行

##### 语法
```
    //上行文本末尾两个空格
    欢迎到访  //two space
    很高兴见到你

    //行与行之间直接加一个空行
    欢迎到访

    很高兴见到你

    //使用html标签
    欢迎到访<br/>很高兴见到你
```

##### 效果

//空格效果
欢迎到访  
很高兴见到你

//加行效果
欢迎到访

很高兴见到你

//html效果
欢迎到访<br/>很高兴见到你

#### 3_6斜体、粗体、删除线
|语法|效果|
|----|-----|
|`*斜体1*`|*斜体1*|
|`_斜体2_`| _斜体2_|
|`**粗体1**`|**粗体1**|
|`__粗体2__`|__粗体2__|
|`~~删除线~~`|~~删除线~~|
|`***斜粗体1***`|***斜粗体1***|
|`___斜粗体2___`|___斜粗体2___|
|`***~~斜粗体删除线1~~***`|***~~斜粗体删除线1~~***|
|`~~***斜粗体删除线2***~~`|~~***斜粗体删除线2***~~|
斜体、粗体、删除线可混合使用
<br/>


### 4图片

---

##### 语法
```    
    ![alt](URL title)
```

alt和title即对应HTML中的alt和title属性（都可省略）：
- alt表示图片显示失败时的替换文本
- title表示鼠标悬停在图片时的显示文本（注意这里要加引号）

URL即图片的url地址，如果引用本仓库中的图片，直接使用**相对路径**就可了，如果引用其他github仓库中的图片要注意格式，即：`仓库地址/raw/分支名/图片路径`，如：
```
    https://github.com/guodongxiaren/ImageCache/raw/master/Logo/foryou.gif
```

注意：在github的GFM解析器认为大小写是严格有别的。例如：weibo.png和weibo.PNG后缀大小写不同，在托管存储时会被看作是一张图，但github的GFM解析器会认为这些分别表示两张不同的图，而vscode的markdown语法解析器又认为这些都表示一张图。

|#|语法|效果|
|:----|:----|:----|
|1|`![baidu](http://www.baidu.com/img/bdlogo.gif "百度logo")`|![baidu](http://www.baidu.com/img/bdlogo.gif "百度logo")|
|2|`![][code-past]` <br/> `[code-past]:https://img-blog.csdnimg.cn/201908060004034.png`|![][code-past]|

注意例2的写法使用了**URL标识符**的形式，在[5_链接](#5_链接)一节有介绍。
<br/>


### 5链接

---

#### 5_1链接外部URL

|语法|效果|
|----|-----|
|`[我的博客](http://blog.csdn.net/guodongxiaren "悬停显示")`|[我的博客](http://blog.csdn.net/guodongxiaren "悬停显示")|
|`[我的知乎][zhihu] ` <br/> `[zhihu]:https://www.zhihu.com/people/jellywong "悬停显示"`|[我的知乎][zhihu] |


#### 5_2链接本仓库里的URL

|语法|效果|
|----|-----|
|`[我的简介](/example/profile.md)`|[我的简介](/example/profile.md)|
|`[example](./example)`|[example](./example)|

#### 5_3图片链接
图片加链接 = 图片显示语法 + 普通的链接语法。
普通的链接中[ ]内部是链接要显示的文本，而图片链接[ ]里面则是要显示的图片。  

|#|语法|效果|
|---|----|:---:|
|1|`[![](/img/weibo.png "图片悬停")](http://weibo.com/linpiaochen "链接悬停)`|[![](/img/weibo.png "图片悬停")](http://weibo.com/linpiaochen "链接悬停")|
|2|`[![weibo-logo]](http://weibo.com/linpiaochen)`<br/>`[weibo-logo]:/img/weibo.png "点击图片进入我的微博"`|[![weibo-logo]](http://weibo.com/linpiaochen)|
|3|`[![](/img/zhihu.png "我的知乎，欢迎关注")][zhihu]`<br/>`[zhihu]:https://www.zhihu.com/people/jellywong`|[![](/img/zhihu.png "我的知乎，欢迎关注")][zhihu]|
|4|`[![csdn-logo]][csdn]`<br/> `[csdn-logo]:/img/csdn.png "我的CSDN博客"` <br/> `[csdn]:http://blog.csdn.net/guodongxiaren "我的博客"`|[![csdn-logo]][csdn]|

#### 5_4锚点
其实呢，每一个标题都是一个锚点，和HTML的锚点（`#`）类似，比如我们 

|语法|效果|
|---|---|
|`[回到顶部](#readme)`|[回到顶部](#readme)|

不过要注意，标题中的英文字母都被转化为**小写字母**了。
> 以前GitHub对中文支持的不好，所以中文标题不能正确识别为锚点，但是现在已经没问题啦！

<br/>


### 6_列表

---

#### 6_1无序列表
##### 语法
```
    * 昵称：果冻虾仁
    - 别名：隔壁老王
    * 英文名：Jelly
```

##### 效果

* 昵称：果冻虾仁
- 别名：隔壁老王
* 英文名：Jelly

#### 6_2多级无序列表
##### 语法
```
    * 编程语言
        * 脚本语言
            * Python
```

##### 效果

* 编程语言
    * 脚本语言
        * Python

#### 6_3一级有序列表
##### 语法

就是在数字后面加一个点，再加一个空格。不过看起来起来可能不够明显。 
```
    面向对象的三个基本特征：

    1. 封装
    2. 继承
    3. 多态
```

##### 效果

面向对象的三个基本特征：

1. 封装
2. 继承
3. 多态

#### 6_4多级有序列表
和无序列表一样，有序列表也有多级结构。
##### 语法
```
      1. 这是一级的有序列表，数字1还是1
         1. 这是二级的有序列表，阿拉伯数字在显示的时候变成了罗马数字
            1. 这是三级的有序列表，数字在显示的时候变成了英文字母
```

#### 效果

1. 这是一级的有序列表，数字1还是1
   1. 这是二级的有序列表，阿拉伯数字在显示的时候变成了罗马数字
      1. 这是三级的有序列表，数字在显示的时候变成了英文字母
	 
#### 6_5复选框列表
##### 语法

```
- [x] 需求分析
- [x] 系统设计
- [x] 详细设计
- [ ] 编码
- [ ] 测试
- [ ] 交付
```

##### 效果

- [x] 需求分析
- [x] 系统设计
- [x] 详细设计
- [ ] 编码
- [ ] 测试
- [ ] 交付

您可以使用这个功能来标注某个项目各项任务的完成情况。
> Tip:
在GitHub的**issue**中使用该语法是可以实时点击复选框来勾选或解除勾选的，而无需修改issue原文。

<br/>


### 7块引用

---

##### 语法
```
    > 数据结构
    >> 树
    >>> 二叉树
    >>>> 平衡二叉树
    >>>>> 满二叉树
```

##### 效果
> 数据结构
>> 树
>>> 二叉树
>>>> 平衡二叉树
>>>>> 满二叉树

<br/>


### 8代码高亮

---

##### 语法
```    
    ```Java
    public static void main(String[]args){} //Java
    ```
    ```c
    int main(int argc, char *argv[]) //C
    ```
    ```Bash
    echo "hello GitHub" #Bash
    ```
    ```javascript
    document.getElementById("myH1").innerHTML="Welcome to my Homepage"; //javascipt
    ```
    ```cpp
    string &operator+(const string& A,const string& B) //cpp
    ```
```

##### 效果

```Java
public static void main(String[]args){} //Java
```
```c
int main(int argc, char *argv[]) //C
```
```Bash
echo "hello GitHub" #Bash
```
```javascript
document.getElementById("myH1").innerHTML="Welcome to my Homepage"; //javascipt
```
```cpp
string &operator+(const string& A,const string& B) //cpp
```
<br/>


### 9表格

---

##### 语法
    
    | 表头1  | 表头2|
    | --------- | ---------- |
    |`***~~斜粗体删除线1~~***`|***~~斜粗体删除线1~~***|
    |`~~***斜粗体删除线2***~~`|~~***斜粗体删除线2***~~|

    //指定对齐方式
    | 左对齐 | 居中  | 右对齐 |
    | :------------ |:---------------:| -----:|
    | col 3 is      | some wordy text | $1600 |
    | col 2 is      | centered        |   $12 |
    | zebra stripes | are neat        |    $1 |

##### 效果

| 表头1  | 表头2|
| --------- | ---------- |
|`***~~斜粗体删除线1~~***`|***~~斜粗体删除线1~~***|
|`~~***斜粗体删除线2***~~`|~~***斜粗体删除线2***~~|

| 左对齐 | 居中  | 右对齐 |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |

表格单元中的内容可以和其他大多数GFM语法配合使用，如在表格中放链接图片等。 
<br/>


### 10表情

---

##### 语法
```
    //:符号名称:
    :blush: :sun_with_face:
```

##### 效果

:blush: :sun_with_face:

具体每一个表情的符号码，可以查询GitHub的官方网页[http://www.emoji-cheat-sheet.com](http://www.emoji-cheat-sheet.com)。

但是这个网页每次都打开**奇慢**。。所以我整理到了本repo中，大家可以直接在此查看[emoji](./emoji.md)。
<br/>


### 11diff语法

---

版本控制的系统中都少不了diff的功能，即展示一个文件内容的增加与删除。
GFM中可以显示的展示diff效果。绿色表示新增，红色表示删除。

##### 语法
```
    ```diff
    + 人闲桂花落， //新增
    - 夜静春山空。 //删除
    ! 月出惊山鸟， //其他
    # 时鸣春涧中。 //其他
    ```
```

##### 效果

```diff
+ 人闲桂花落，
- 夜静春山空。
! 月出惊山鸟，
# 时鸣春涧中。
``` 
<br/>


### 12流程图

---

这里只介绍流程图和状态图的常用语法，更多请见[mermaid项目地址](https://github.com/mermaid-js/mermaid)

#### 12_1流程图
流程图语法描述内容包括：方向、节点、连线、子图4个部分。

##### 12_1_1方向语法
```
    ```mermaid
        graph TB    %% graph [方向值]
            id1[节点1] --> id2(节点2)
    ```
```
注意：`%%` 为mermaid语法中的注释号

| 值   | 全称   | 释义  |
| :-----: | :-----: | :-----: |
| TB(或TD) | Top Bottom  | ↓ |
| BT(或DT) | Bottom Top  | ↑ |
| LR | Left Right  | →  |
| RL | Right Left  | ←  |

##### 12_1_1方向效果
  
 | TB | BT | LR | RL |
 | --- | --- | --- | --- | 
 |![TB](/img/TB.PNG)|![BT](/img/BT.PNG)|![LR](/img/LR.PNG)|![RL](/img/RL.PNG)| 


##### 12_1_2节点语法
```
    ```mermaid
        graph TB    
            id1[矩形]   %% idx为节点名，括号描述节点形状，括号内为节点文本
            id2(圆角矩形)
            id3((圆形))
            id4>不对称矩形]
            id5{菱形}
            id6[\平行四边形\]
    ```
```

注意：直接定义idx不加括号说明形状时默认为矩形。

##### 12_1_2节点效果

![nodes](/img/nodes.PNG)

##### 12_1_3连线语法
```
    ```mermaid
        graph LR
            id1[节点1] --- id2(节点2) 
            id3[节点3] --注释--- id4(节点4)
            id5[节点5] --> id6(节点6) 
            id7[节点7] --注释--> id8(节点8)
            id9[节点9] -.-> id10(节点10) 
            id11[节点11] -.注释.-> id12(节点12)
            id13[节点13] ==> id14(节点14)
            id15[节点15] ==注释==> id16(节点16)
    ```
```

注意：连线的"-"数必须严格按照语法示例的个数来，连线两端空格无严格要求。

##### 12_1_3连线效果

|#|无注释|带注释|
|:------:|:------:|:------:|
|`---` 无方向连线|![](/img/link1.png)|![](/img/link2.png)|
|`-->` 带方向连线|![](/img/link3.png)|![](/img/link4.png)|
|`-.->` 虚线|![](/img/link5.png)|![](/img/link6.png)|
|`==>` 加粗线|![](/img/link7.png)|![](/img/link8.png)|

##### 12_1_4子图语法
```
    ```mermaid
        graph TB
            c1 --> a2
            subgraph one    %% subgraph [子图名]
                a1 --> a2
            end
            subgraph two
                b1 --> b2
            end
            subgraph three
                c1 --> c2
            end
    ```
```

##### 12_1_4子图效果

![subgraph](/img/subgraph.PNG)

#### 12_2状态图
状态图语法描述内容主要有：状态、转化、起止、合成状态4个部分。

##### 12_2_1状态语法
```
    ```mermaid
        stateDiagram    %% 两种状态定义方式
            s1             
            s2:state s2    
    ```
```

##### 12_2_1状态效果

![state](/img/state.PNG)

##### 12_2_2转化语法
```
    ```mermaid
        stateDiagram    %% 两种转化描述方式
            s1 --> s2
            s3 --> s2:转化注释       
    ```
```

##### 12_2_2转化效果

![state_trans](/img/state_trans.PNG)

##### 12_2_3状态起止描述语法
```
    ```mermaid
        stateDiagram
            [*] --> s1
            s1 --> [*]
    ```
```

##### 12_2_3状态起止效果

![begin_end](/img/begin_end.PNG)

##### 12_2_4合成状态语法
```
    ```mermaid
        stateDiagram
            [*] --> First
            First --> Second
            First --> Third
        
            state First{  
                fir --> [*]
            }
            state Second{  
                sec --> [*]
            }
            state Third{  
                th --> [*]
            }
    ```
```

##### 12_2_4合成状态效果

![com_trans](/img/com_trans.PNG)

--------------------------------
[csdn]:http://blog.csdn.net/guodongxiaren "我的博客"
[zhihu]:https://www.zhihu.com/people/jellywong "悬停显示"
[weibo]:http://weibo.com/linpiaochen
[baidu-logo]:http://www.baidu.com/img/bdlogo.gif "百度logo"
[weibo-logo]:/img/weibo.png "点击图片进入我的微博"
[csdn-logo]:/img/csdn.png "我的CSDN博客"
[code-past]:https://img-blog.csdnimg.cn/201908060004034.png
