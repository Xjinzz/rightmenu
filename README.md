# rightMenu
- Right click menu
- [git](https://github.com/JinZhenZon/rightmenu.git)

## Install
```shell
npm install rightmenu --save-dev
```

## Quick Start
```javascript
import vue from "vue";
import rightMenu from "rightMenu";
vue.use(rightMenu);
```
## Example
```javascript
<template>
    <div>
        <button v-rightMenu = "menudata">
            {{
                text
            }}
        </button>
    </div>
</template>
<script>
    export default {
        name:"demo",
        data(){
            return {
                menudata:{
                    // 菜单box的样式   Menu box style
                    boxStyle:"width:150px;background:#f55;",
                    // 菜单选项的样式 Style of menu options
                    optionStyle:"color:#fff;line-height:30px;font-size:15px;",
                    menus:[
                        {
                        /**
                         * content 菜单显示的文字 <支持html> 
                         * callback：菜单点击要触发函数  需要在methods定义 
                         * style ： 本项菜单的单独样式 可以覆盖掉optionStyle  
                         * icon : icon图片地址
                         * iconStyle: icon 图片的样式（例如大小等 直接作用于图片）
                         * iconPosition : 支持left / right (其余全部按照left处理);
                         * content The text displayed on the menu(can use html)
                         * callback: Menu clicks to trigger functions need to be defined in methods
                         * style :  The single style of this menu can override option Style
                         * icon : your icon's url
                         * iconStyle : you icon's style ,is image's style
                         * iconPosition :you can use left or right ;The rest are all processed according to left
                         */
                        /**
                         * 字段(field)           类型(type)                 是否可以为空(is can null)    默认值
                         * content            [ html | text ]                       Y                   ""
                         * callback           [  methods function ]                 Y                   return false
                         * style                   [ css ]                          Y                   ""
                         * icon                   [ url ]                           Y                   ""
                         * iconStyle              [ css ]                           Y                   ""
                         * iconPosition           [string]                          Y                   "left"
                        */
                        content:"menu content",
                        callback:"callbackMethods",
                        style:"border-bottom:1px solid #fff;background:#333;line-height:30px;",
                        icon:"https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=2310514390,3580363630&fm=27&gp=0.jpg",
                        iconStyle:"width:20px;height:20px;",
                        iconPosition:"left",
                        },
                        {
                        content:"右键菜单二",
                        callback:"otherMethods"
                        }
                    ],
                },
            }
        },
        methods:{
            callbackMethods(){
                // do something
            },
            otherMethods(){
                // do something
            }
        }
    }
</script>
```

## other Explain
```text
    本插件旨在实现的是灵活 + 低配置 + 扩展性高 + 指令调用的快速右键菜单，正如你看到的我只需要一个指令，一个json，仅此而已。本插件对于新人还是老手均能适用，因为本插件是一款扩展性极高的插件，支持你配置菜单总样式、菜单选项样式、点击的回调函数、菜单选项的icon 甚至你能定义每一单独选项的样式以及icon。最后感谢大家的支持，如果喜欢的话请到github（https://github.com/JinZhenZon/rightmenu）为本插件点个star吧。本人因工作原因，目前已知了一个bug ： 使用icon图片时候 因为css兼容原因，导致icon比文字垂直略微高了一些，将在不久后的下个版本修复此bug，推荐视觉要求较高的项目可以使用字体图标，毕竟我已经扩展了每一项content支持写入html；使用中如有问题，请联系我的QQ:421217189


    This plug-in is designed to achieve a flexible + low configuration + high scalability + fast right-click menu for instruction invocation. As you can see, I only need one instruction, a json, that's all. This plug-in is suitable for both new and veteran users, because it is a highly extensible plug-in, which supports you to configure the general menu style, menu option style, click callback function, menu option icon and even you can define the style of each individual option as well as icon. Finally, thank you for your support. If you like, please go to GitHub (https://github.com/JinZhenZon/rightmenu) and order a start for this plug-in. Because of my work, I have known a bug: when using icon pictures, because of CSS compatibility, icon is slightly higher than text verticality. I will fix this bug in the next version in the near future. I recommend font icons for projects with higher visual requirements. After all, I have expanded every content support. Write to html; if you have any questions in use, please contact my QQ: 421217189
```

## update history
- 2018/11/28 1.0.1 更新redeme文档 