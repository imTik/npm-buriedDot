## How to use buriedDot?
> This is a buried point plugin based on the vue framework

### npm install buriedDot

### use buriedDot
``` javascript
import BuriedDot from './utils/buriedDot';
// 这里需要传入 router , callback, 60000 = 预设用户离开时间
BuriedDot(router, (mark, buriedData) => {
  console.log('触发埋点的标记: ', mark)
  console.log('获取到的埋点信息: ', buriedData);
  /**
   * 触发埋点的标记mark: router(路由埋点) / click(点击事件埋点) / leave(用户离开/无操作 埋点) / close(关闭页面埋点)
   * 
   * 埋点信息
   * buriedData: {
   *   deviceData: {...}  // 设备信息
   *   dotData:    {...}  // 埋点信息
   *   netData：   {...}  // 网络加载信息
   * }
  */
}, 60000);
```

### Element plus data-dot Click on element to trigger buried point callback
``` html
<!-- 元素加上data-dot 点击元素触发埋点callback -->
<button data-dot="这里放置埋点信息">这是一个按钮</button>
```