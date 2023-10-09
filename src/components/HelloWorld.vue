<script setup>
import { ref } from 'vue'

defineProps({
  msg: String,
})

const count = ref(0)
</script>


<template>
<div class="buttons">
  <button class="duplicate">Duplicate!</button>
  <button class="modifytitle">Change Name</button>
  <button id="deletelastcard">Delete</button>
  <button data-toggle-btn>Toggle description</button>
  <button class="colorButton">Change Color</button>
</div>
<div class="wrapper">
  <div class="container">
  <img class="image" src="https://images.unsplash.com/photo-1533738363-b7f9aef128ce?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8M3x8ZnVubnklMjBjYXR8ZW58MHx8MHx8fDA%3D&w=1000&q=80"/>
  <div class="header">
    <h3>Cool Cat</h3>
    <h4>Wicked cool cat</h4>
  </div>
  <details class="details">
    <summary>Description</summary>
    <div>
      <ul>
        <li>Welcome to the description</li>
        <li>hopefully this works when I port it over to openwc</li>
       </ul>
    </div>
    </details>
</div> 
</div>

</template>

<style scoped>
.read-the-docs {
  color: #888;
}

.wrapper {
  width: 300px;
  border: 10px solid lightgreen;
  display: inline-flex;
}

.image {
  width: 300px;
}

.header {
  text-align: center;
  font-size: 2rem;
}

.header h3:hover {
  font-style: bold;
  font-size: 1em;
  color: cyan;
}

.header h3,
.header h4 {
  transition: .3s ease-in-out all;
  margin: 8px;
  font-style: normal;
}

.buttons button:focus,
.buttons button:hover {
  background-color: rgba(100,100,100,.5);
}

.buttons button:active {
  background-color: rgba(0,0,200,.5);
}

.buttons {
  display: block;
}

button {
  padding: 8px;
  font-size: 24px;
}

details {
  margin-left: 24px;
  padding: 10px;
}
.details summary {
  font-size: 20px;
  font-weight: bold;
}


@media only screen and (max-width: 1200px){
  .wrapper {
    background-color: green;
  }
}
@media only screen and (max-width: 600px){
  .wrapper {
    background-color: purple;
  }
}
@media only screen and (max-width: 425px){
  .wrapper {
    font-weight: normal;
  }
  .wrapper .header h3 {
    font-size: 12px;
  }
  .wrapper .header h4 {
    font-size: 10px !important;
  }
  details {
    display: none;
  }
}
</style>
