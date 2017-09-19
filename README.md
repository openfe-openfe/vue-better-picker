# vue-better-picker

## 这是什么(What is it)
为vue提供的picker选择器组件

## 代码演示如何使用

```shell
npm install vue-better-picker --save

```

```html
<div class="select" @click="showPicker(1)" ref="select1">{{ selectedText }}</div>
<picker @select="handleSelect(1,arguments)" :data="data"
        ref="picker1" :title="title" :cancelTxt="cancelTxt":confirmTxt="confirmTxt">
</picker>

```
```js
export default {
    data() {
      return {
        data: [
          [['aaa','bbb'], ['ccc','ddd'], ['eee','fff']]
        ],
        title: [
          '三列选择器'
        ],
        selectedText:[
          '三列选择器'
        ]
        cancelTxt: '关闭',
        confirmTxt: '好的'
      }
    },
    methods: {
      showPicker(index) {
        let picker = this.$refs['picker' + index]

        picker.show()
      },
      handleSelect(index, args) {
        alert(`您选中${args[2]}`)
      }
    },
    components: {
      Picker
    }
  }
```


## 组件演示demo

```js
git clone https://github.com/songhaoreact/vue-better-picker.git
cd vue-better-picker
npm install 
npm run dev
```

## 演示效果图

![image](https://github.com/songhaoreact/vue-better-picker/master/blog/demo.gif)

## 说明

vue-better-picker 组件来自better-scroll，底层是better-scroll实现的
















