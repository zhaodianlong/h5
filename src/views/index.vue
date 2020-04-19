<template>
  <div class="hello">
    <ul>
      <li v-for="(item, index) of list" :key="index">
        <router-link :to="item.path">{{item.label}}</router-link>
      </li>
      <li>
        <router-link :to="{path: '/register', query: {inviterId: 53}}">注册</router-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      list: [
        {
          label: '关于我们',
          path: '/about'
        }
      ]
    }
  }
}
</script>
<style scoped>
.hello {
  text-align: center;
}
</style>
