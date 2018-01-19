# vue-tagger


> Simple tagging component for Vue with built-in autocomplete. It supports tag prefix, multiple delimeters and Awesomplete's label/value array

## Install
```js
$ yarn add vue-tagger
```
_or_

```js
$ npm install AlexCarmel/vue-tagger --save
```

## Usage

```js
<template>
  <div class="my-component">
    <vue-tagger :tags="tags" @change="logTags" :placeholder="'Enter a tag...'" :delimiter="', '" :prefix="'#'"></vue-tagger>
  </div>
</template>
<script>
import VueTagger from 'vue-tagger'
export default {
  components: {
    VueTagger
  },
  data() {
    return {
      tags: [
        { name: 'JavaScript', selected: true },
        { name: 'Ruby', selected: false },
        { name: ['PHP','PHP 7+'], selected: true },
        { name: 'Crystal', selected: true },
        { name: 'Python', selected: false }
      ]
    }
  },
  methods: {
    logTags (tags) {
      console.log(tags)
    }
  }
}
</script>
```

## License

MIT © [Collin Henderson](https://github.com/syropian)
