<template>
  <div class="m-hcity">
    <dl>
      <dt>{{ title }}</dt>
      <dd v-for="(item, index) in list" 
        :key="index"
        >{{ item }}</dd>
    </dl>
  </div>
</template>

<script>
export default {
  props: ['title','list'],
  data() {
    return {

    }
  },
  methods: {
    
  },
}
</script>

<style lang="scss">
  @import '@/assets/css/changecity/hot.scss';
</style>