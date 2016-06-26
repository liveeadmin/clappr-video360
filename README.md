# clappr-video360


<img src="360.gif" height="480"></img>


[Demo](https://thiago.me/clappr-360)

clappr-video360 is a plugin for playing 360 videos with Clappr.

It's built on top of [Kaleidoscope](https://github.com/thiagopnts/kaleidoscope), so it supports
the same browsers the lib supports.

### Building:

```
$ npm install
$ npm run build
```

### Using:

Add the library with Clappr to your page:
```html
<script type="text/javascript" charset="utf-8" src="node_modules/clappr/dist/clappr.min.js"> </script>
<script type="text/javascript" charset="utf-8" src="node_modules/clappr-video360/dist/clappr-video360.min.js"> </script>
```

Then:
```javascript
var p = new Clappr.Player({
    source: 'your-equirectangular-video.mp4',
    plugins: {
        container: [Video360],
    },
    parentId: '#player',
});
// for better usability, disable clappr's click_to_pause plugin
p.getPlugin('click_to_pause').disable();
```
