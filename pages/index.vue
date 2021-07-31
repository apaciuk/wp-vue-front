<template>
<div>
<h1>Index</h1>
</div>
</template>

<script>
export default {
  data () {
    return {
      posts: []
    }
  },
  created: function() {
     // GET /someUrl
    this.posts = this.$http.$get('posts').then(response => {
     console.log(response);
    // get body data
    //this.someData = response.body;

  }, response => {
    // error callback
  });
  }
}

</script>
