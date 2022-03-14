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
