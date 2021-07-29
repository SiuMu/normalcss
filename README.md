## 序言
&emsp;&emsp;不知道身为后端程序员的你写不写前端代码，反正我是经常写，写的我很烦，尤其是用vue之类的组件式开发，几乎每个vue页面我都要写一些重复性的css，写了一遍又一遍，而且还都是那种非常简单的，margin，padding，font-size之类的东西。毕竟高深的我也不会写。
&emsp;&emsp;所以，我痛定思痛，决定把常用的那些简单的css写成一个文件,并且放在码云上，之后不管是哪个项目我直接复制粘贴进去，全局引用，之后就不用写css了，直接写class就行。
## 使用
&emsp;&emsp;首先是**命名**，命名简单易懂，基本上遵循**属性+值**的命名方式。举个例子来说：mg-left-1-px就是`margin-left: 1px;`而mg-1-1-px就是`margin: 1px 1px;`
所以基本上看到类名就知道它的css代码是啥，给大家展示一下部分代码：
```css
.mg-1-1-px {
    margin: 1px 1px;
}
.mg-right-1-px {
    margin-right: 1px;
}
.mg-bottom-1-px {
    margin-bottom: 1px;
}
.mg-left-1-px {
    margin-left: 1px;
}
.mg-top-1-px {
    margin-top: 1px;
}
.mg-2-2-px {
    margin: 2px 2px;
}
.mg-right-2-px {
    margin-right: 2px;
}
.mg-bottom-2-px {
    margin-bottom: 2px;
}
.mg-left-2-px {
    margin-left: 2px;
}
.mg-top-2-px {
    margin-top: 2px;
}

.pd-1-1-px {
    padding: 1px 1px;
}
.pd-right-1-px {
    padding-right: 1px;
}
.pd-bottom-1-px {
    padding-bottom: 1px;
}
.pd-left-1-px {
    padding-left: 1px;
}
.pd-top-1-px {
    padding-top: 1px;
}

.font-size-1-px {
    font-size: 1px;
}
.font-size-2-px {
    font-size: 2px;
}
.font-size-3-px {
    font-size: 3px;
}
......
......
......
```
&emsp;&emsp;这里面有**margin**，有**padding**，有**font-size**，后续会慢慢添加更多的东西。**根据我写代码的情况来看，距离单位基本都是在两位数以下，用得最多的甚至是10px以下，所以我生成的margin距离都在64px以下，1-64px每个都可以用**。padding距离更短在16px以下。
&emsp;&emsp;本来我用Java代码生成的文件，想着一口气给生成到500px。但是最后生成的文件太大了，不可能用在生产环境的。我就思考了一下结合实际情况，生成到64px。至于更大的距离单位应该会很少用，到时候再定义就行了，估计没几个。
&emsp;&emsp;或许有人问，怎么不用别人写好的css库呢？我也确实找了很多css库，但是人家是专业的，写的又高级，又全，又多，我学起来有点费劲，哪有这复制粘贴来得快。而且很多样式UI库都有，我写的css都是非常简单的那种。用高级css库感觉就像是高射炮打蚊子——我举不动。

## 最后
&emsp;&emsp;这个css库我希望能时常更新，终有把它真的变成面向普通后端程序员的前端通用css代码库