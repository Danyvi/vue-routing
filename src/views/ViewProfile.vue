<template>
  <div class="view-profile">
    <h1>Profile Page for {{ userId }}</h1>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'ViewProfile',
  components: { 
  },
  data(){
    return {
      userId: this.$route.params.user_id 
    }
  },
  methods: {
    updateId(){
       this.userId = this.$route.params.user_id  
    }
  },
  watch:{
    $route: 'updateId'
  }
}
</script>
