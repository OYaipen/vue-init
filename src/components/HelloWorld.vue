<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <alert mode="success">Hola</alert>
    <alert mode="primary">otro componente de vue js</alert>
    <alert mode="secondary">otro componente de vue 2</alert>
    <div>
      <input type="text" v-model="lastName" placeholder="Your nice name?" />
      <p>welcome,{{ lastName }}</p>
    </div>
    <button @click="CleckedMe">Click me</button>
    <input type="text" @keyup.space="doSomenthing" placeholder="Please write you code" />

    <h3>Using loop</h3>
    <ul>
      <li v-for="person in Students" :key="person">{{person}} <br></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data() {
    return {
      lastName: "",
      Students: ["Ali", "Jan", "Willian", "Khan"]
    };
  },
  methods: {
    CleckedMe() {
      console.log("You click on the button");
    },
    doSomenthing() {
      console.log("Code Applied ");
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}

a {
  color: #42b983;
}
</style>
