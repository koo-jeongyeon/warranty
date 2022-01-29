<template>
  <div class="hello">
    test 입니다. test컴포넌트
  </div>
</template>

<script>
import axios from 'axios';
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  mounted() {
    console.log("testeeeee");
    this.testF();
    axios.get('/api/hello').then(res => { console.log(res.data) });//백엔드 통신
  },
  methods: {
    testF(){
      console.log("test");
      return 
    },
  },
  
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
