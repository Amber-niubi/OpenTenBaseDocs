# 文档库格式手册

本页面将列出在编写 OpenTenBase 文档时需要注意的格式规范。请您在撰写或者修正文档内容之前仔细阅读本页面，以帮助您撰写更高质量的内容。

## 存储格式与文档链接

1. **文件名以小写字母编写，单词中间以 `-` 分割。** 例如：`docs-format-guide.md`。
2. **英语文档在文件名后加 `.en` 。** 例如：`docs-format-guide.en.md`。英语文档与中文文档存放于同一目录。
3. 站内链接请使用相对路径，例如：`[格式手册](docs-format-guide.md)`、`[常见问题](../faq.md)`。
4. 所有使用的图片均存储到仓库的 `docs/assets` 目录下且拥有有意义的文件名。图片的引用请使用相对路径，例如：`![OpenTenBase favicon](./assets/favicon.png)`。

## 文档基本格式要求

- 除文章开头与文章名称统一的标题外，文章中不应出现 `#` 或者 `<h1>` 形式的一级标题。
- 标题的井号后应有一个英文半角空格。例如：`## 二级标题`。
- 标题后应有一个空行。
- 缩进使用 4 个空格，不要使用 Tab。
- 代码块、表格等块级元素前后应各有一个空行。
- 二级列表应在开头增加 4 个空格缩进。
- 同级列表之间的额外内容前后应各有一个空行，且增加 4 个空格缩进。
- 使用 `???` 或 `!!!` 开头的 Admonitions 语法时，每一行要包括在 Admonitions 语法的文本框的文本，开头必须有 4 个空格缩进。即使是空行，也必须保持与其他行一致的缩进。Admonitions 语法前后应各有一个空行，但内容前后不需要空行。
- ```` ``` ```` 样式的代码块应指定相关语言。例如：```` ``` shell ````。如果代码内容为纯文本，则指定 `text` 作为语言。
- 中文文档撰写过程中应遵循本文结尾的[中文文案排版指北](#中文文案排版指北)。

    !!! note "提示"
        如果需要的话，请参考排版指北的[工具](#工具)部分使用相关工具帮助确保文案排版的正确性。

## 中文文案排版指北

!!! note "提示"
    以下内容更改自 GitHub 用户 sparanoid 的《中文文案排版指北》，其内容使用 MIT 协议授权。[原 GitHub 仓库](https://github.com/sparanoid/chinese-copywriting-guidelines)

### 空格

> 「有研究显示，打字的时候不喜欢在中文和英文之间加空格的人，感情路都走得很辛苦，有七成的比例会在 34 岁的时候跟自己不爱的人结婚，而其余三成的人最后只能把遗产留给自己的猫。毕竟爱情跟书写都需要适时地留白。
>
> 与大家共勉之。」——[vinta/paranoid-auto-spacing](https://github.com/vinta/pangu.js)

#### 中英文之间需要增加空格

正确：

> OpenTenBase 是开源的分布式数据库，可以轻松应对亿级数据的存储、分析和查询。集高扩展性、高SQL兼容度、完整的分布式事务支持、多级容灾能力以及多维度资源隔离等能力于一身，采用无共享的集群架构，适用于PB级海量 HTAP 场景。

错误：

> OpenTenBase是开源的分布式数据库，可以轻松应对亿级数据的存储、分析和查询。集高扩展性、高SQL兼容度、完整的分布式事务支持、多级容灾能力以及多维度资源隔离等能力于一身，采用无共享的集群架构，适用于PB级海量 HTAP场景。
>
> OpenTenBase 是开源的分布式数据库，可以轻松应对亿级数据的存储、分析和查询。集高扩展性、高SQL兼容度、完整的分布式事务支持、多级容灾能力以及多维度资源隔离等能力于一身，采用无共享的集群架构，适用于PB级海量HTAP 场景。

完整的正确用法：

> OpenTenBase 是开源的分布式数据库，可以轻松应对亿级数据的存储、分析和查询。集高扩展性、高SQL兼容度、完整的分布式事务支持、多级容灾能力以及多维度资源隔离等能力于一身，采用无共享的集群架构，适用于PB级海量 HTAP 场景。

#### 中文与数字之间需要增加空格

正确：

> OpenTenBase 有超过 10 年的发展历史。

错误：

> OpenTenBase 有超过10年的发展历史。

#### 数字与单位之间需要增加空格

正确：

> 使用 4k 扇区驱动器时，最大大小为 16 TiB。

错误：

> 使用 4k 扇区驱动器时，最大大小为 16TiB。

例外：度数／百分比与数字之间不需要增加空格：

正确：

> 角度为 90° 的角，就是直角。
>
> 新 MacBook Pro 有 15% 的 CPU 性能提升。

错误：

> 角度为 90 ° 的角，就是直角。
>
> 新 MacBook Pro 有 15 % 的 CPU 性能提升。

#### 全角标点与其他字符之间不加空格

正确：

> chrony 是网络时间协议（NTP）的通用实现。

错误：

> chrony 是网络时间协议（ NTP ）的通用实现。

#### 用 `text-spacing` 来挽救？

CSS Text Module Level 4 的 [`text-spacing`](https://www.w3.org/TR/css-text-4/#text-spacing-property) 和 Microsoft 的 [`-ms-text-autospace`](https://msdn.microsoft.com/library/ms531164(v=vs.85).aspx) 可以实现自动为中英文之间增加空白。不过目前并未普及，另外在其他应用场景，例如 macOS、iOS、Windows 等用户界面目前并不存在这个特性，所以请继续保持随手加空格的习惯。

### 标点符号

### 全角和半角

不明白什么是全角（全形）与半角（半形）符号？请查看维基百科条目『[全角和半角](https://zh.wikipedia.org/wiki/%E5%85%A8%E5%BD%A2%E5%92%8C%E5%8D%8A%E5%BD%A2)』。

#### 使用全角中文标点

正确：

> chrony 是网络时间协议（NTP）的通用实现。

错误：

> chrony 是网络时间协议 (NTP) 的通用实现。
>
> chrony 是网络时间协议(NTP)的通用实现。

#### 数字使用半角字符

正确：

> 使用 4k 扇区驱动器时，最大大小为 16 TiB。

错误：

> 使用 ４k 扇区驱动器时，最大大小为 １６ TiB。

例外：在设计稿、宣传海报中如出现极少量数字的情形时，为方便文字对齐，是可以使用全角数字的。

#### 遇到完整的英文整句、特殊名词，其内容使用半角标点

正确：

> 乔布斯那句话是怎么说的？「Stay hungry, stay foolish.」
>
> 推荐你阅读《Hackers & Painters: Big Ideas from the Computer Age》，非常的有趣。

错误：

> 乔布斯那句话是怎么说的？「Stay hungry，stay foolish。」
>
> 推荐你阅读《Hackers＆Painters：Big Ideas from the Computer Age》，非常的有趣。

### 名词

#### 专有名词使用正确的大小写

大小写相关用法原属于英文书写范畴，不属于本文讨论内容，在这里只对部分易错用法进行简述。

正确：

> 欢迎来到 OpenTenBase 文档库！

错误：

> 欢迎来到 opentenbase 文档库！
>
> 欢迎来到 OPENTENBASE 文档库！
>
> 欢迎来到 openTenBase 文档库！
>
> 欢迎来到 openTenbase 文档库！
>
注意：当网页中需要配合整体视觉风格而出现全部大写／小写的情形，HTML 中请使用标淮的大小写规范进行书写；并通过 `text-transform: uppercase;`／`text-transform: lowercase;` 对表现形式进行定义。

#### 不要使用不地道的缩写

正确：

> 我们需要一位熟悉 TypeScript、HTML5，至少理解一种框架（如 React、Next.js）的前端开发者。

错误：

> 我们需要一位熟悉 Ts、h5，至少理解一种框架（如 RJS、nextjs）的 FED。

### 争议

以下用法略带有个人色彩，即：无论是否遵循下述规则，从语法的角度来讲都是**正确**的。

#### 链接之间增加空格

!!! note "备注"
    此处我们建议将链接内容当作普通内容处理，即：如果前后内容均为中文且链接名称为中文，则不需要在链接前后增加空格。否则，在英语/数字与中文之间增加空格。

用法：

> 请 [提交一个 issue](#) 反馈相关问题。
>
> 访问我们网站的最新动态，请 [点击这里](#) 进行订阅！

对比用法：

> 请[提交一个 issue](#)反馈相关问题。
>
> 访问我们网站的最新动态，请[点击这里](#)进行订阅！

#### 简体中文使用直角引号

!!! note "备注"
    此处我们建议使用普通引号（“” 与 ‘’）。

用法：

> 「老师，『有条不紊』的『紊』是什么意思？」

对比用法：

> “老师，‘有条不紊’的‘紊’是什么意思？”

### 工具

仓库 | 语言
--- | ---
[vinta/paranoid-auto-spacing](https://github.com/vinta/paranoid-auto-spacing) | JavaScript
[serkodev/vue-pangu](https://github.com/serkodev/vue-pangu) | Vue.js (Web Converter)
[huei90/pangu.node](https://github.com/huei90/pangu.node) | Node.js
[huacnlee/auto-correct](https://github.com/huacnlee/auto-correct) | Ruby
[huacnlee/autocorrect](https://github.com/huacnlee/autocorrect) | Rust, WASM, CLI
[huacnlee/go-auto-correct](https://github.com/huacnlee/go-auto-correct) | Go
[sparanoid/space-lover](https://github.com/sparanoid/space-lover) | PHP (WordPress)
[nauxliu/auto-correct](https://github.com/NauxLiu/auto-correct) | PHP
[jxlwqq/chinese-typesetting](https://github.com/jxlwqq/chinese-typesetting) | PHP
[hotoo/pangu.vim](https://github.com/hotoo/pangu.vim) | Vim
[sparanoid/grunt-auto-spacing](https://github.com/sparanoid/grunt-auto-spacing) | Node.js (Grunt)
[hjiang/scripts/add-space-between-latin-and-cjk](https://github.com/hjiang/scripts/blob/master/add-space-between-latin-and-cjk) | Python
[hustcc/hint](https://github.com/hustcc/hint) | Python
[studygolang/autocorrect](https://github.com/studygolang/autocorrect) | Go
[n0vad3v/Tekorret](https://github.com/n0vad3v/Tekorrect) | Python
[VS Code - huacnlee.auto-correct](https://marketplace.visualstudio.com/items?itemName=huacnlee.auto-correct) | VS Code Extension

### 参考文献

- [Guidelines for Using Capital Letters - ThoughtCo.](https://www.thoughtco.com/guidelines-for-using-capital-letters-1691724)
- [Letter case - Wikipedia](https://en.wikipedia.org/wiki/Letter_case)
- [Punctuation - Oxford Dictionaries](https://en.oxforddictionaries.com/grammar/punctuation)
- [Punctuation - The Purdue OWL](https://owl.english.purdue.edu/owl/section/1/6/)
- [How to Use English Punctuation Correctly - wikiHow](https://www.wikihow.com/Use-English-Punctuation-Correctly)
- [格式 - openSUSE](https://zh.opensuse.org/index.php?title=Help:%E6%A0%BC%E5%BC%8F)
- [全形和半形 - 维基百科](https://zh.wikipedia.org/wiki/%E5%85%A8%E5%BD%A2%E5%92%8C%E5%8D%8A%E5%BD%A2)
- [引号 - 维基百科](https://zh.wikipedia.org/wiki/%E5%BC%95%E8%99%9F)
- [疑问惊叹号 - 维基百科](https://zh.wikipedia.org/wiki/%E7%96%91%E5%95%8F%E9%A9%9A%E5%98%86%E8%99%9F)
