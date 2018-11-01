>关于统计之都的介绍、目标和组织结构请参见[**关于我们**](http://cos.name/about/)


# 0. 责任和义务

1. 任何会员都 **没有绝对的责任和义务** 帮助其他会员解决问题或提供帮助，无人回答的帖子为合理情况，请理解。
2. 本网站非商业机构，无任何营利目的，请各位会员不要利用论坛进行商业活动或者为自身谋取利益（包括但不限于发布广告，赚取其它网站积分的链接）。若有涉及商业活动的帖子需要发布，请事先与我们联系：contact@cos.name；否则视作广告帖删除。
3. 管理人员、版主以及广大会员的一项共同责任是：在出现矛盾或不和谐的情况时，在遵守网站规章制度的前提下换位三思，互相理解。

# 1. 发帖要求

珍爱生命，有效求助。节省别人的时间，才能快速得到帮助。以下为本站发帖的具体要求：

## 1.1 错误的发帖姿势

以下列举本站不提倡的发帖姿势，请尽可能避免。（~~删除可能：高~~）

1. **不要在这里问你的作业答案**，你的作业是你自己的事情，我们相信大多数老师都会要求作业独立完成；若有例外，请按照老师的要求寻求适当的帮助。
2. 有问题尽管问，但 **不要重复发帖**，这样只会让人更加不愿意回复，它也给版主带来了额外的删帖劳动。提问之前请先花两分钟浏览或搜索一下别人相关帖子，看看有没有类似的问题。
3. 疑问再大也不要使用 **多于三个的问号**，感情再强烈也不要使用三个以上的叹号。
4. 新问题请另开新帖， **不建议搭车问问题**
5. 帖子标题严禁 **只使用“求助”“问个问题”“请教”这样的短语**，请把您的问题 用简短的语言阐述清楚，**不写清楚标题的帖子很可能会被删除**。
6. R语言相关问题 **没有样本数据和代码，没有可重复例子**。本条具体规范详见 **1.2**部分。

以下社区礼仪希望大家遵守：

1. **不要特意强调自己是新手**，也不要加急；我们只关心问题能否问好，是否是新手、是否着急，与别人是否会回答问题无关。
1. 建议 **不要点名**让谁回答你的问题，因为这里是大家参与、公开讨论的场所。
1. **一般不建议留邮箱/QQ等私下交流**。因为论坛可以记录你的问题和解决方案，在未来也许会帮到其他人（或者六个月之后的你自己）。


## 1.2 正确的发帖姿势

发帖求助时，提问者请把自己的问题交代清楚，节省大家的时间，不要没有前因后果、没有上下文，让别人看了你的问题还得继续追问。很差的问题如“我的R出错了，请问我该怎么办？”；你得告诉别人在怎样的情况下出错了以及出了什么错。

一个好的问题应当包括以下两个部分：

- 问题描述，
- 预期结果，  
- 相关样本数据和代码  

下面提供一个提问帖的样板，改编自[这篇帖子](https://d.cosx.org/d/420238--)，供参考（斜体内为解说）：

---

标题： ~~如何将数字转化为时间格式~~  
修改后标题： 如何将 5, 930, 2235  这样格式的数字转换为 0:05, 9:30, 22:35  这样格式的时间

> (*从原标题看不出这究竟是个提问帖还是个经验总结帖。修改后，即使不用看正文，也一眼就看清具体问题是什么*)


正文：

~~大家好
我有一列从0-2355的数字，我希望把它们转换成0:00， 23:55这样的时间格式
尝试了 times <- format(otter$time, format = "%h-%m")
或是运算otter$time <- as.numeric(substr(otter[,3],1,2))*60 + as.numeric(substr(otter[3,],3,4))
都没有成功，请问有什么方法可以实现转换？
谢谢。~~

修改后正文：

> (*以markdown进行排版，分为条理清楚的三个小段*)

### 问题描述 

我有一列格式为一到四位数的数字，如 0, 2355 等，我希望把它们转换成 0:00， 23:55 这样的时间格式，但没有成功。
> (*简单描述清楚问题和预期结果即可，如果可能，请尽量提供上下文方便理解*)

### 我的代码、数据和运行结果

为了解决这个问题，我进行了如下测试，得到的都不是预期结果：

``` r
mydata = read.csv("data.csv")
format(mydata, format = "%h-%m")
as.numeric(substr(mydata,1,2))*60 + as.numeric(substr(mydata,3,4))
dput(mydata) 
sessionInfo()
```

> (*按markdown格式提供代码即可，另外R的代码可使用`dput()`函数分享数据或reprex包的`reprex::reprex()`函数创建可重复例子, 具体见`#5 扩展阅读`部分的[求助帖该怎么写，才能吸引别人来帮忙](https://d.cosx.org/d/420240--)*)

### 我的系统环境

``` r
sessionInfo()
#> R version 3.5.1 (2018-07-02)
#> Platform: x86_64-w64-mingw32/x64 (64-bit)
#> Running under: Windows 7 x64 (build 7601) Service Pack 1
#> 
#> Matrix products: default
#> 
#> locale:
#> [1] LC_COLLATE=Chinese (Simplified)_People's Republic of China.936 
#> [2] LC_CTYPE=Chinese (Simplified)_People's Republic of China.936   
#> [3] LC_MONETARY=Chinese (Simplified)_People's Republic of China.936
#> [4] LC_NUMERIC=C                                                   
#> [5] LC_TIME=Chinese (Simplified)_People's Republic of China.936    
#> 
#> attached base packages:
#> [1] stats     graphics  grDevices utils     datasets  methods   base     
#> 
#> loaded via a namespace (and not attached):
#>  [1] compiler_3.5.1    magrittr_1.5      htmltools_0.3.6  
#>  [4] tools_3.5.1       yaml_2.2.0        Rcpp_0.12.18     
#>  [7] stringi_1.2.4     rmarkdown_1.10.13 knitr_1.20       
#> [10] htmldeps_0.1.1    digest_0.6.17     stringr_1.3.1    
#> [13] evaluate_0.11
```

> (*在 R 里运行 `sessionInfo()` 函数，将返回的信息贴出来。目的是提供更多运行环境的信息以更好地定位问题所在。*)

---

# 2 Markdown排版

本站使用markdown语法进行排版。发帖之前我们建议花几分钟学习基本的markdown语法，以使你的帖子有更好的观感。
 
请参阅[github 的markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet),
 
下面仅列举发帖中常用的markdown语法

- **标题** - 
```
# 一级标题
## 二级标题
### 三级标题
```
效果：
# 一级标题
## 二级标题
### 三级标题


- **超级链接** - 如`[统计之都](https://cosx.org)`，效果：[统计之都](https://cosx.org)
- **贴图** - 如 `![](https://d.cosx.org/assets/logo-adex5ots.png)`
效果： ![](https://d.cosx.org/assets/logo-adex5ots.png)
- **引用** - 如`> 不想当裁缝的司机就不是一个好厨子！`，效果：
> 不想当裁缝的司机就不是一个好厨子！

- **句内代码** - 如`` `lm(y ~ x, data = mydata)` ``，效果：`lm(y ~ x, data = mydata)`

- **代码块** - 如
````markdown
```r
plot(cumsum(rnorm(100)), xlab = 'i', ylab = 'Brownian Motion')
```
````
效果
```r
plot(cumsum(rnorm(100)), xlab = 'i', ylab = 'Brownian Motion')
```


- **斜体** - 如`*Emphasize this!*`，效果：*Emphasize this!*
- **粗体** - 如`**我是粗体文字**`，效果：**我是粗体文字**
- **无序列表条目**
```
- 无序列表条目
- 无序列表条目
- 无序列表条目
```
- **有序列表**
```
1. 有序列表条目
1. 有序列表条目
1. 有序列表条目
```

- **数学公式** 支持latex公式语法，可以用`\( \)`或`$$ $$`将公式围起来，注意中间不能有空格或换行
    + 行内公式 - `\(\alpha + \beta\)` 效果： \(\alpha + \beta\)
    + 段落公式
```
$$\alpha+\beta$$
```
效果：
$$\alpha+\beta$$


# 3 文件分享

本站不支持文件上传。

## 图片

如果您想贴图，请先将图片上传到图床，然后使用`# 2 Markdown排版`中markdown语法进行贴图。
可供考虑的图片上传网站有 https://imgur.com , https://weibo.com, https://github.com

## 文件

文件可以通过 Dropbox, github 或（百度）网盘分享链接。

## 代码

有时候一些发帖者会把代码以图片的形式贴出来，这是错误的做法。代码应该以文本的方式发布，否则他人无法直接运行（没人喜欢对着代码图片把代码重新敲一遍）。

如果代码过长不宜放入帖子，或需要分享的代码包含多个文件，建议以github的方式分享。

# 4 捐赠 

如果您在本站受到过帮助并想为本站的发展贡献自己的力量，可以采取[自愿捐赠](https://cosx.org/donate/)的方式。另外需要声明的是，本站并非营利性网站，捐赠纯属自愿行为。


# 5 推荐阅读

- [求助帖该怎么写，才能吸引别人来帮忙](https://d.cosx.org/d/420240--)

- [我在论坛发帖提问求助，为何没有人帮我解答？](https://d.cosx.org/d/419256)
