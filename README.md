### According to [idiotWu/smooth-scrollbar](https://github.com/idiotWu/smooth-scrollbar/tree/7.x#demo)

## init All at once
```JS
Scrollbar.initAll({
    speed: 1,
    damping: 0.1,
    overscrollEffect: 'bounce',
});
```

## init by object
```JS
options = {
    speed: 1,
    damping: 0.1,
    overscrollEffect: 'glow',
    overscrollEffectColor: '#87ceeb'
};
var elem = document.getElementById('myscroll');
Scrollbar.init(elem, options);
```

## Available Options for Scrollbar

| parameter | type | default | description |
| :--------: | :--: | :-----: | :---------- |
| speed | Number | 1 | Scrolling speed scale.|
| damping | Number | 0.1 | Delta reduction damping, a float value between (0, 1), the lower the value is, the more smooth the scrolling will be. |
| thumbMinSize | Number | 20 | Minimal size for scrollbar thumb. |
| syncCallbacks | Boolean | false | Execute listeners in synchronous or asynchronous. |
| renderByPixels | Boolean | true | Render scrolling by integer pixels, set to `true` to improve performance. |
| alwaysShowTracks | Boolean | false | Keep scrollbar tracks visible whether it's scrolling or not. |
| continuousScrolling | Boolean\|String | 'auto' | Whether allow upper scrollable content to continue scrolling when current scrollbar reaches edge. **When set to 'auto', it will be enabled on nested scrollbars, and disabled on first-class scrollbars.** |
| overscrollEffect | Boolean\|String | false | Experimental overscroll effect, `'bounce'` for iOS style effect and `'glow'` for Android style effect. **Be careful when you enable this feature!** |
| overscrollEffectColor | String | '#87ceeb' | Canvas paint color with 'glow' effect. |
| overscrollDamping | Number | 0.2 | The same as `damping`, but for overscrolling. |

## helper
```JS
var testHas = Scrollbar.has(elem) ? true : false; // true
var testGet = Scrollbar.get(document.body) ? true : false; // false
console.log({testHas, testGet});

// Destroy specific
Scrollbar.destroy(elem);
// Destroy all scrollbar
Scrollbar.destroyAll();
```
