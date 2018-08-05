<template>
    <div class="test">
        <input type="text" v-model = "title">
        <h1>{{title}}</h1>
        <p v-if = "showName">{{user.firstName}}</p>
        <p v-else></p>
        <ul>
            <li v-for = "item in items">{{item.title}}</li>
        </ul>
        <button v-on:click = "greet('hello world')">Say Greeting</button>
        <input type="text" v-model = "stuff">
    </div>
</template>


<script>
export default {
  name: "test",
  data() {
    return {
      title: "Hello World",
      stuff: "",
      user: {
        firstName: "Scott",
        lastName: "Smith"
      },
      showName: false,
      items: [{ title: "Item one" }, {title: "Item two"}, {title: "Item three"}]
    };
  }, 
  methods: {
    greet: function(greeting){
      alert(greeting)
    }
  }
};
</script>

<style scoped>
</style>

