<template>
  <div>
    <div>ادهم</div>
    <input type="text" v-model="number" @keyup="onNumberWrite" />
  </div>
</template>

<script>
import slugify from 'slugify'
export default {
  name: 'IndexPage',
  data: () => ({
    number: '',
  }),
  methods: {
    onNumberWrite() {
      this.number = slugify(this.number)
    },
  },
}
</script>
