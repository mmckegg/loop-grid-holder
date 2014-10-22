loop-grid-holder
===

Beat stutter/looper transform for [loop-grid](https://github.com/mmckegg/loop-grid).

## API

```js
var Holder = require('loop-grid-holder')
```

### `var holder = Holder(transform)`

Pass `loopGrid.transform` to this constructor.

### `holder.setLength(length)`

Choose the length (in beat decimal) of the stutter effect.

### `holder.start(position[, indexes, done])`

Loop events in specified `indexes` (or all if not specified) from `position` to `position + length`. Ensure each event length is no longer than specified `length` (truncating if necessary).

Automatically calls `holder.stop()` first if there is a current hold in progress.

### `holder.stop()`

Release `transform` and call `done` if specified.