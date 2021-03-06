# README

## Example

### Default

```js
import { createElement, mount } from '@divlook/chain-element'
import { addStyle } from '@divlook/chain-element/action'

const black = addStyle({ color: '#000' })
const app = createElement('div').use(black)

mount(document.body, app)
mount('#app', app)

app.toString()
// <div style="color: #fff"></div>
```

### Compose

```js
import { createElement, compose } from '@divlook/chain-element'
import { addStyle } from '@divlook/chain-element/action'

const white = addStyle({ color: '#fff' })
const bold = addStyle({ textWeight: 600 })
const options = compose(white, bold)

createElement('span').use(options)
```
