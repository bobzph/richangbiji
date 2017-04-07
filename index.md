## Welcome to GitHub Pages
### Markdown

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/bobzph/richangbiji/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.


###样式兼容

   input:input样式设置兼容


         input{
         	background-color: #006B69;
         	border: none;
         	color: #fff;
         	font-size: 16px;
         	font-family: 微软雅黑;
         	outline: none;
         	appearance: none;
         	-moz-appearance: none;
         	-webkit-appearance: none;
         	text-align: right;
         }
         input::-webkit-input-placeholder{
         	font-size: 12px;
         	font-family: "微软雅黑";
         	color: #007f82;
         }

### 点击效果

图片点击效果 // 点击星星效果

  <div class="pingfen" data-num="0">
            <img data-id="1"data-key="true" src="img/star_in@2x.png"/>
            <img data-id="2"data-key="true" src="img/star_in@2x.png"/>
            <img data-id="3"data-key="true"src="img/star_in@2x.png"/>
            <img data-id="4"data-key="true"src="img/star_in@2x.png"/>
            <img data-id="5"data-key="true"src="img/star_in@2x.png"/>
            <img data-id="6"data-key="true"src="img/star_in@2x.png"/>
            <img data-id="7"data-key="true"src="img/star_in@2x.png"/>
            <img data-id="8"data-key="true"src="img/star_in@2x.png"/>
            <img data-id="9"data-key="true"src="img/star_in@2x.png"/>
            <img data-id="10" data-key="true" src="img/star_in@2x.png"/>
    </div>



    $(".pingfen").find("img").each(function(){
        $(this).click(function(){
            if($(this).attr("data-key")=="true"){
                $(this).attr("src","img/star@2x.png");
                $(this).prevAll().attr("src","img/star@2x.png");
                $(this).prevAll().attr("data-key","false");
                $(this).attr("data-key","false");
                $(".pingfen").attr("data-num",$(this).attr("data-id"))
            }else{
                $(this).attr('src','img/star_in@2x.png')
                $(this).attr('data-key','true')
                $(this).nextAll().attr('src','img/star_in@2x.png');
                $(this).nextAll().attr('data-key','true')
                var num=parseInt($(this).attr('data-id'))-1
                $('.pingfen').attr('data-num',num)
            }
        })
    })
### Jquery
##### text()和html()区别



    html()用为读取和修改元素的HTML标签    对应js中的innerHTML
     .html()是用来读取元素的HTML内容（包括其Html标签）,.html()方法使用在多个元素上时，只读取第一个元素

    .text()用来读取或修改元素的纯文本内容  对应js中的innerText

      text()用来读取元素的纯文本内容，包括其后代元素;.text()方法不能使用在表单元素上

    .val()用来读取或修改表单元素的value值
    .val()是用来读取表单元素的"value"值,.val()只能使用在表单元素上




