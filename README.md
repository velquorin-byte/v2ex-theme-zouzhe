# V2EX 主题 · 奏折（Zouzhe）

宣纸 · 经折 · 红格 · 朱批 · 黄绫。一份 V2EX 自定义 CSS，把页面做成一份奏折：标题前后加「奏为……事」，正文末尾落「谨奏」，帖子头部盖朱批「知道了」，楼主徽章换成「臣」字印。跟随 V2EX 自带的夜间模式切换为「灯下批折」配色。

## 使用方法

打开 V2EX「设置」，开启「使用自定义 CSS」，在 CSS 框里任选一种写法：

### 方式一：引用（推荐，仓库更新后自动生效）

```css
@import url("https://cdn.jsdelivr.net/gh/velquorin-byte/v2ex-theme-zouzhe@main/zouzhe.css");
```

想固定在某个版本、不随仓库变动，把 `@main` 换成标签，例如：

```css
@import url("https://cdn.jsdelivr.net/gh/velquorin-byte/v2ex-theme-zouzhe@v1.0.0/zouzhe.css");
```

### 方式二：粘贴

把 [zouzhe.css](zouzhe.css) 的全部内容复制进去。

## 自定义

`@import` 必须写在最前面，之后可以写自己的覆盖规则，例如关掉彩蛋、换颜色：

```css
@import url("https://cdn.jsdelivr.net/gh/velquorin-byte/v2ex-theme-zouzhe@main/zouzhe.css");

:root {
  --zz-zhupi: "";          /* 不要朱批 */
  --zz-title-before: "";   /* 不要「奏为」 */
  --zz-title-after: "";    /* 不要「事」 */
  --zz-cinnabar: #a8322a;  /* 换朱砂色 */
}
```

所有变量见 `zouzhe.css` 第一节。

没装楷体的系统可以先引入霞鹜文楷（同样放在最前面）：

```css
@import url("https://cdn.jsdelivr.net/npm/lxgw-wenkai-webfont@1.7.0/style.css");
@import url("https://cdn.jsdelivr.net/gh/velquorin-byte/v2ex-theme-zouzhe@main/zouzhe.css");
```

## 更新缓存

jsDelivr 对 `@main` 有最长约 12 小时的缓存。推送新版本后想立即生效，浏览器打开一次：

```
https://purge.jsdelivr.net/gh/velquorin-byte/v2ex-theme-zouzhe@main/zouzhe.css
```
