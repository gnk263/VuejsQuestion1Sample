<template>
  <div class="container">

    <form>
      <div class="form-group">
        <button type="button" class="btn btn-primary" v-on:click.stop.prevent="testMethod">てすと</button>
      </div>

      <div class="form-group">
        <select multiple v-model="userSelected">
          <option v-for="(group, key, index) in groups" :key="index" v-bind:value="group.id">
            {{ group.text }}
          </option>
        </select>
      </div>
    </form>

    <p>{{ hoge }}</p>
    <p>{{ fuga }}</p>
    <p>userSelected: {{ userSelected }}</p>

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
      fuga: '',
      userSelected: '',
      groups: [],
    }
  },
  methods: {
    testMethod() {
      this.hoge = 'test message'

      const groups = [
        {'id': '111', 'text':'aaa'},
        {'id': '222', 'text':'bbb'},
        {'id': '333', 'text':'ccc'},
      ]

      this.groups = groups
      this.fuga = groups
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
