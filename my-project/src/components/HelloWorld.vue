<template>
  <div class="container">

    <form>
      <div class="form-group">
        <button type="button" class="btn btn-primary" v-on:click.stop.prevent="testMethod">てすと</button>
      </div>
    </form>

    <p>{{ hoge }}</p>
    <p>{{ fuga }}</p>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      hoge: '',
    }
  },
  methods: {
    testMethod() {
      this.hoge = 'test message'
      this.fuga = [
        {'id': '111', 'text':'aaa'},
        {'id': '222', 'text':'bbb'},
        {'id': '333', 'text':'ccc'},
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
