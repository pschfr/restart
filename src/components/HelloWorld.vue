<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h1>{{ time }}</h1>
    <h1>{{ date }}</h1>
  </div>
</template>

<script>
// Import any dependencies needed before my app
import dayjs from 'dayjs'

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  computed: {
    time() {
      return dayjs().format('h:mm:ss A')
    },
    date() {
      return dayjs().format('dddd, MMMM DD, YYYY')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
