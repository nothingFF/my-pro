<template>
  <div class="hello">
    {{info}}
  </div>
</template>

<script>

import Axios from 'axios'

export default {
  name: 'test',
  data () {
    return {
      info: 'Welcome to Your Vue.js App'
    }
  },
  mounted () {
    Axios
      .get('https://www.runoob.com/try/ajax/json_demo.json')
      .then(response => (this.info = response))
      .catch(function (error) { // 请求失败处理
        console.log(error)
      })
  }
}
</script>
