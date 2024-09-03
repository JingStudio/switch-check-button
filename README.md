# switch-check-button

## Install 
```js
npm install switch-check-button --save
```

## Usage
```vue
<template>
    <SwitchButton v-model="checked1" @change="changeHandler"></SwitchButton>
    <SwitchButton :value="checked2" @input="inpChangeHandler"></SwitchButton>
</template>

import SwitchButton from 'switch-check-button'

export default {
  // ...
  components: { SwitchButton },
  data() {
    return {
      checked1: false,
      checked2: false
    }
  },
  methods: {
    changeHandler(val) {
      console.log(val)
    },
    inpChangeHandler() {
      this.checked2 = !this.checked2
    }
  }
  // ...
}

```

## API 
| key      | value   | information |
| -------- | ------- | ----------- |
| value    | Boolean or String or Number | Default value is false. When Boolean(value) is true, checked.  |
| name     | String  | Default is value null. |
| label    | String | Default value is null. If it is not empty, it will show the label. |
| classes  | String  | Default value is null. Customer className.  |
| disabled | Boolean | Default value is false. When disabled value is true, it could not be clicked. |
| checkedText | Array | Default value is ['close', 'open'], index=0 is false text, index=1 is true text. When showText prop is true, it will be shown. |
| showText | Boolean | Default value is false. When it is true, the text will be shown. |
| checkedColors | Array | Default ['red', 'green']|
| @change | Function | Function that could get the checked status. |
