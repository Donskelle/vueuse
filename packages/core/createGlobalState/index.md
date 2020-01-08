# createGlobalState

> Keep state in global scope to be reused across Vue instances

## Usage

```js
// store.js
import { createGlobalState, useStorage } from '@vueuse/core'

export const useGlobalState = createGlobalState(
  () => useStorage('vue-use-locale-storage'),
)
```

```js
// app.js
import { useGlobalState } from './store'

new Vue({
  setup () {
    const state = useGlobalState()
    return { state }
  },
})
```