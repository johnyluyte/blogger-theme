## What is this?

This is the theme for my [blog](http://blog.chunnorris.cc/).

It is based on the default "Picture Window" template from [blogger](https://www.blogger.com/home), with some modification:

- Added a neat Dropdown menu tabs modified from [helplogger](http://helplogger.blogspot.in/2014/02/add-a-neat-css-dropdown-menu-in-blogger.html).

- Added [google-code-prettify](https://code.google.com/p/google-code-prettify) code highlight, and a customized CSS snippet modified from [this blog](http://eric0806.blogspot.tw/2014/04/blogger-google-code-prettify.html).

- Added customized CSS(Table, Blockquote) modified from [Bootstrap](http://getbootstrap.com/).

- Added related articles widget from [WFU blog](http://www.wfublog.com/2014/05/blogger-related-posts-2-custom-thumbnail.html).

- `<a>` links in posts will be opened at new tabs. TOCs will not be effected. As described in [this article](http://stackoverflow.com/questions/4425198/markdown-target-blank).

- The width, layout, font-size, font-family, and others have also been modified based on my own preference.


## Customized Neat-Menu

Customized CSS **Neat-Menu** is just above `]]></b:skin>`, or you can search for: `<!-- neatMenu CSS starts -->`

To modify items of neat-menu(e.g. add tabs, add dropdown lists), go to `Layout`, click `Neat Menu`, then edit HTML.

```html
<div id='contact-links'>
    <div id='menu-container'>
        <nav id='neat-menu'>
          <ul>
            <li><a href='/'>Home</a></li>
            <li><a href='linkToYourPage'>My Page</a></li>
            <li><a>Dropdown lists ▼</a>
                <ul>
                    <li><a href='#'>Item 1</a></li>
                    <li><a href='#'>Item 2</a></li>
                    <li><a href='#'>Item 3</a></li>
                </ul>
            </li>
            <li><a href='#'>Another Page</a></li>
          </ul>
        </nav>
    </div>
</div>
```

![](demo/neat-menu.png)


## Customized Google Code Prettify

Customized **Google Code Prettify** can be located under:

- `<!-- googleCodePrettify CSS starts -->`
- `<!-- googleCodePrettify javascript starts -->`

![](demo/google-code-prettify.png)


## Customized Bootstrap-Style CSS

Customized **Bootstrap-Style Table** can be located under:

- `<!-- bootstrapTable javascript starts -->`

It uses the style from `bootstrap-table.css` in this repository.

![](demo/bootstrap-table.png)

![](demo/blockquote.png)

## Related Articles Widget

CSS: search for `/* 相關文章2 */`

js: search for `<!-- 相關文章2 start -->`

## Open links in new tabs

```javascript
    // 將所有在 .post-body.entry-content 文章內的連結都設定為 target = _blank
    $(&quot;.post-body.entry-content a&quot;).attr(&#39;target&#39;, &#39;_blank&#39;);
    // 但是目錄 TOC 的連結不要
    $(&quot;.toc a&quot;).attr(&#39;target&#39;, &#39;&#39;);
```

## Other Modification Notes

.post-body {
  font-size: 130%;
}

.content-outer{
  font-size: 90%;
}
