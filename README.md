<h1 align="center">animate-js</h1>

JS 动画

### Usage

```
const JSAnimate = require("animate-js")

JSAnimate(draw, 10000)
```

### Hooks

```
import { easeIn, useAnimate } from 'animate-js'

const [animate] = useAnimate(draw, 10000, {
    count: 1,
    timing: easeIn
})
```

### API

```
JSAnimate(draw, duration, option)
```

| 属性     | 说明             | 类型                       | 默认值 | 必选  | 版本   |
| :------- | :--------------- | :------------------------- | :----- | :---- | ------ |
| draw     | 绘画函数         | (progress: number) => void | -      | true  | v1.0.0 |
| duration | 动画时间（毫秒） | number                     | -      | true  | v1.0.0 |
| option   | 动画参数         | option 对象                | -      | false | v1.0.0 |

### option

| 属性    | 说明                       | 类型                         | 默认值 | 必选  | 版本   |
| :------ | :------------------------- | :--------------------------- | :----- | :---- | ------ |
| timing  | 缓动函数                   | (progress: number) => number | -      | false | v1.0.0 |
| onStart | 开始钩子函数（不包括延迟） | () => void                   | -      | false | v1.0.0 |
| onEnd   | 结束钩子函数               | () => void                   | -      | false | v1.0.0 |
| delay   | 延迟时间（毫秒）           | number                       | 0      | false | v1.0.0 |
| count   | 执行次数                   | number, "infinite"           | 1      | false | v1.0.0 |

### animate 对象

| 属性     | 说明     | 类型                                   | 版本   |
| :------- | :------- | :------------------------------------- | :----- |
| reset    | 重置     | () => void                             | v1.0.0 |
| pause    | 暂停     | () => state                            | v1.0.0 |
| play     | 播放     | () => state                            | v1.0.0 |
| state    | 动画状态 | 'playing' , 'paused' , 'start' , 'end' | v1.0.0 |
| progress | 动画进度 | number                                 | v1.0.0 |
