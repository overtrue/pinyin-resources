汉字拼音相关参考资料
---

此项目为我在开发 [overtrue/pinyin](/overtrue/pinyin) 时所用到的参考的资料收集，旨在方便有同样需求的朋友。

## 汉字的多音字处理

_ 以下内容摘自: [《汉语同音字和多音字处理方法研究》- 杨宪泽,谈文蓉,刘玉萍,张  楠,殷  锋](汉语同音字和多音字处理方法研究.pdf) _

中文是象形文字,字数多,字形复杂。西文是拼音文字，英文只有 26 个字母，加上大写小写及数字符号，总数不超过 128 个，用七位二进制码就可表达。而中文字成千上万,要用十几位二进制码才能把它们区别开来, 这给存储乃至输入方式等都造成困难。

多音字判别方法中技术的关键是基于统计特征， 特征提取使多音字正确判音有效。特征包含在特征词典中, 采用规则描述。共定义了以下特征:

- 词内左右邻接字

    通式为: X<sup>i-1</sup> X<sup>i</sup> 和 X<sup>i</sup> X<sup>i+1</sup>。X<sup>i</sup> 是当前要判断读音的多音字，这是处理多音字在不同的词语中读不同的音的情况 。例如 “人参” 与 “参加”、“银行” 与 “行程”、“重量” 与 “重复” 等等 。

- 左右邻接词

    通式为:W<sup>i-1</sup> X<sup>i</sup> 和 X<sup>i</sup>W<sup>i+1</sup> 。X 是当前要判断读音的多音字，W<sup>i-1</sup> 和 W<sup>i+1</sup> 是多音字 的左右邻接词，这是处理多音字与不同的邻接词读不同的音的情况 。例如“相当长”、“大队长”、“长方形” 等等。

- 当前词的词性

    例如 “数” 作名词的读法和作动词的读法，“更” 作名词的读法和作副词的读法等等。

- 边界条件

    该特征是有的字在句首 、句末或不同位置读音不同，更多地体现在一些语气助词上面 。例如 “了” 在句中和句末时读音往往不会相同 。

## 参考资料

### 文章

- [《汉语转拼音-----带音调和多音字识别》](http://www.cnblogs.com/sunli/archive/2007/11/21/967294.html)
- [《C#分词算法：正向、逆向、双向最大匹配算法》](http://my.oschina.net/u/1270374/blog/164042)

### 统计与分析文档

- [《Frequency statistics 频率统计 - 音素和音节频率》- http://lingua.mtsu.edu](http://lingua.mtsu.edu/chinese-computing/phonology/)
- [《Syllable frequencies with tones 记调音节频率》- http://lingua.mtsu.edu](http://lingua.mtsu.edu/chinese-computing/phonology/syllabletone.php)
- [《Character frequency lists 汉字单字频率列表》- http://lingua.mtsu.edu](http://lingua.mtsu.edu/chinese-computing/statistics/index.html)

### 需求设计

- [汉字转拼音 (hz2py)](https://gist.github.com/erning/1338746)

### 网站

- [CC-CEDICT](http://cc-cedict.org/wiki/)
- [UNICODE CHARACTER DATABASE](http://www.unicode.org/reports/tr44/)
- [lingua.mtsu.edu - 中文文本计算](http://lingua.mtsu.edu/chinese-computing/)
- [汉典](http://www.zdic.net/)
- [开源词典](http://kaifangcidian.com/)

### 论文

- [《汉语同音字和多音字处理方法研究》- 杨宪泽,谈文蓉,刘玉萍,张  楠,殷  锋](汉语同音字和多音字处理方法研究.pdf)

### 开源项目

- [janx/ruby-pinyin](https://github.com/janx/ruby-pinyin)
- [hotoo/node-pinyin](https://github.com/hotoo/node-pinyin)
- [mozillazg/python-pinyin](https://github.com/mozillazg/python-pinyin)
- ["结巴"中文分词](https://github.com/erning/jieba)
- [中文书刊排版相关标准和规范](https://github.com/Haixing-Hu/typesetting-standard)

### License

CC0 1.0 Universal
