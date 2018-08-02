<template>
    <div class="test">
        <h1>{{title}}</h1>
        <p v-if = "showName">{{user.firstName}}</p>
        <p v-else></p>
        <ul>
            <li v-for = "item in items">{{item.title}}</li>
        </ul>
    </div>
</template>


<script>
export default {
  name: "test",
  data() {
    return {
      title: "Hello World",
      user: {
        firstName: "Scott",
        lastName: "Smith"
      },
      showName: false,
      items: [{ title: "Item one" }, {title: "Item two"}, {title: "Item three"}]
    };
  }
};
</script>

<style scoped>
</style>

