## How to use buriedDot?

### npm install buriedDot

### use buriedDot
``` javascript
import BuriedDot from './utils/buriedDot';
// 这里需要传入 router , callback, 60000 = 预设用户离开时间
BuriedDot(router, (mark, buriedData) => {
  console.log('触发埋点的标记: ', mark)
  console.log('获取到的埋点信息: ', buriedData);
  /**
   * 触发埋点的标记mark: router / click / leave
   * 
   * 埋点信息
   * buriedData: {
   *   currentPagePath: "/home"
   *   currentPageTitle: "首页"
   *   enterTime: "2020-05-09 14:26:26"
   *   formPagePath: "/"
   *   fromPagaTitle: ""
   *   lastTime: 0
   *   pageCount: 1
   * }
  */
}, 60000);
```

### Element plus data-dot Click on element to trigger buried point callback
``` html
<!-- 元素加上data-dot 点击元素触发埋点callback -->
<button data-dot="这里放置埋点信息">这是一个按钮</button>
```