layout: post
title: "Google SEO Page Optimization"
description: ""
category:
tags: [google, seo]
---


- [A Visual Guide to Keyword Targeting and On-Page SEO - Moz](https://moz.com/blog/visual-guide-to-keyword-targeting-onpage-optimization)
- [On-Page SEO: Anatomy of a Perfectly Optimized Page](http://backlinko.com/on-page-seo)

### 网页标题规则 Page Title

- 由 50-55 个字母组成
- 搜索关键词靠前和在标题中的占比较大有利于排名优化。
- 标题要人性化，避免关键词堆砌。
- 避免 `Welcome to our official ...` 在标题中出现。

### Meta Description

Meta Keywords 的不影响 Google 排名。Meta Descript 也不会直接影响排名，但会影响 CTR(点击率)，间接影响排名。

    Description -> CTR(LP, Design) -> Convertion/Goal

### Heading

    <h1>Balance bike for Kids</h1>

### Image

    <img src="image url" alt="alt of image">

`alt` 为 alternative 的缩写，让图面能够被搜索引擎收入。

- <FileName>.jpg
- ALT
- Nearby Text
- Anchor Text
- Highlight - Bold, Italic
- Size，不宜太大

### Page Rank

- PR, Page Rank
- Static Rank(Microsoft)
- Webrank(Yahoo)
- MozRank(Linkscape's) 用来取代 PR 值，目前普遍使用这个工具。可以 Chrome Web Store 下载。

可以通过 <http://www.prchecker.net> 或者 <http://www.aizhan.com> 查看网站的 PR。目前买卖链接已无意义，PR 从 2013 年后停止更新。

### 锚文本

    <a href="http://www.baidu.com">Anchor Text</a>

锚文本的匹配：

1. Extract Match，完全匹配。如 Balance Bike
2. Partial Match，部分匹配。如 kids bike, kids learning bike
3. Branded，使用皮牌做锚文本。如 Mocha。
4. Random，随机的。如 clich me, Get this One Today.
5. URL Match，URL 匹配，如 mocha.com

对于目前的搜索引擎而言，大概 30% 使用 Extract Match 和 Partial Match 的锚文本，70% 使用 Brand 和 Random 的锚文本。

### 关键词(Keywords)

关键词分为主关键词(Main Keywords)和长尾关键词(Longtail Keywords)，主关键词的竞争比较大，长尾关键词通常由三个以上的词组组成。

主关键词的特点：

- High Competition
- Low Conversion

长尾关键词的特点：

- Low Competition
- High Convertion

在 Google 中可以通过 Google 索引量来判断搜索词的竞争力(Competition)。通过 Google Planner 来判断搜索词的商业价值(Commercial Value)。竞争度大商业价值不一定高，如 `click here`。

主关键词一般是一个 Sentence，而非关键词的堆砌。在主页中，Title, H1, 正文，甚至图片的 ALT 都要出现主关键词。

长尾关键词可以用于：

- Google Adwords。
- WebPage，如主页、内页。
- 可以使用关键词工具、Google Analytics 来分析关键词。

### Keywords Buying Cycle

Attention   ->      Intrest     ->      Desire      ->          Action

iphone5 -> iphone5 vs iphone4 -> is iphone5 worth purchase -> purchase iphone5 online china

### nofollow

```html
<!-- 用于链接 -->
<a href="" rel="nofollow"></a>

<!-- 用于页面。告知搜索引擎，无需抓取本页面，分散权重。也可以设置 content="noindex" 告知搜索引擎不要收录。 -->
<meta name="robots" content="nofollow" />
```

noflow 作用是告知搜索引擎不用把当前页的权重分散给指定的链接，不要对指定的链接投票。对于外链（如广告、外链内容）或者内容不丰富(不重要)的链接可以使用 noframe，避免分散页面的权重。具体应用于：

- Paid Link
- Content not trust（或者不想分散链接）
- Comments of Blog
- Form
- Login
- 文章归档

See <http://www.dx.com>

主页的权重最大，但是内容丰富的内页，如产品页面应，主页应该分配这类链接权重。

Nofollow  Links 插件可以罗列网站的所有外部链接，通过 Links/Nofollow Links 可以设置外链是否需要设置为 nofollow。

Platinum SEO 插件中可以设置文章归档、文章分类、Login、Register、关键词云等链接为 nofollow。

noindex 主要用于：

- Duplicated Page
- Email Promotion
- Goal Page/Form，如 imiker.com/thanks.html，设置为 noindex。因为该页面被搜索引擎收入，不利于统计转换率。
- Others

### Sitemap

```
User-agent: *
Allow: /
Disallow: /index3.php
Disallow: /new/*.php

Sitemap: http://www.imiker.com/sitemap.xml
```

See <http://www.imiker.com/sitemap.xml> 。

上传到站长工具的 Sitemap 文件不能超过 50k 条，文件大小不能超过 10M。

1. 可以使用 <http://www.web-site-map.com> 制作 Sitemap，但是限制在 500 条一下。也可以使用 WordPress 插件。
2. 上传 sitemap.xml 到站点根目录
3. Google Master Tool，提交 Sitemap 文件。

通过 Google Master Tools 可以查看收录情况：

- indexed
- submited

如果这两个数据出路比较大，说明 Google 并没有收入网站的所有页面，则可能是因为网站结构可能有问题，路径太深，也可能是 Robots 文件的误操作。

对于大站点如果页面没有全部被收入，则可以尝试以下方法：

1. 广度优先。分别把每层链接制作成 sitemap 文件，添加到 robots 中。
2. 深度优先。可以把二级导航作为一棵数，分别制作 sitemap，添加到 robots 中。
3. 添加只把没有收入的页面添加到 Sitemap，添加到 robots 中。

对于 Sitemap.xml 文件，不一定非得是严格的 xml 格式，也可以是链接列表。

### 重复内容解决方案

如 <http://www.inesoi.com>、<http://inesoi.com> 、<http://inesoi.com/index.php> 等对应的都是主页，如果没有做 301 等处理，就会造成重复页面。

解决方法：

- 301 重定向。如果我们期望主域名是 <http://www.inesoi.com>，其他的域名都应该 301 重定向到到这个域名。【推荐】
- Webmaster Tool。Setting/Site Setting，可以设置目标市场，主域名，不过需要把其他的域名也加入到站长工具中。

在域名更换的时候，主域名和所有内页的都需要重定向。

对于 Tags 或者 Categories，也可能导致重复页面。通常不建议使用 Tags。如：
<http://www.inesoi.com/tt/faqs.com> 和 <http://www.inesoi.com/faqs.com> 就是重复页面。解决办法是使用 robos 文件，为内页添加相应的 noindex/nofollow。

做网站内容时，我们通常可以做行业内的 checklist，如 How to Import Oil Painting in China 或 Checklist of Importing Oil Paiting in China。如：

- Canvas Material 画布材料
- Who Paint it?
- Copyright
- Packing
- Services

对于这样的内容，我们可以提供打印功能，有利于吸引用户。打印页面和原页面可能导致重复页面，如 <www.example.com/how-to-import> 和 <www.example.com/how-to-import/print>。解决方案为：

- 在 print 页面中设置 meta 为 noindex。
- 在页面中添加 `rel=Canonical`。