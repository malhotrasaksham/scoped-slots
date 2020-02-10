<template>
  <div id="app">
    <Contacts v-slot="{contact}">
      <div class="item">
        <!-- slot-scope="{contact}">-->
        <!--We are destructuring props to accept contact directly
        the slot-scope attribute cannot be added to the component tag directly
        We can omit this extra element by using v-slot
        
        Keep in mind v-slot can only be used on components and template tags, but not in plain HTML tags
        SHorthand is #contact but in beta
        -->
        <div class="name">{{contact.name}}</div>
      </div>
    </Contacts>
  </div>
</template>

<script>
import Contacts from "./components/Contacts";

export default {
  name: "App",
  components: {
    Contacts
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  color: #2c3e50;
  text-align: center;
}
</style>
<style scoped>
.item {
  box-shadow: 1px 1px 1px #EEE;
  margin: 10px;
  width: 200px;
  padding: 10px;
  cursor: pointer;
}
</style>
