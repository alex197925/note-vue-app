<!-- @format -->
<script setup>
// State
import { ref } from "vue";
const showModal = ref(false); // Open and close Modal window by changing State
const newNote = ref(""); // Adding new note
</script>

<template>
  <main>
    <div v-if="showModal" class="overlay">
      <div class="modal">
        <textarea
          v-model="newNote"
          name="note"
          id="note"
          cols="30"
          rows="10"
        ></textarea>
        <button>Add Note</button>
        <button @click="showModal = false" class="close">Close</button>
      </div>
    </div>
    <div class="container">
      <header>
        <h1>Notes</h1>
        <button @click="showModal = true">+</button>
      </header>

      <div class="card-container">
        <div class="card">
          <p class="main-text">
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Tempora
            assumenda nostrum commodi sequi perspiciatis voluptas?
          </p>
          <p class="date">18.01.2023</p>
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped>
main {
  height: 100vh;
  width: 100vw;
}

.container {
  max-width: 1000px;
  margin: 0 auto;
  padding: 10px;
}

header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

h1 {
  font-weight: bold;
  margin-bottom: 25px;
  font-size: 75px;
}

header button {
  border: none;
  padding: 10px;
  width: 50px;
  height: 50px;
  cursor: pointer;
  background-color: rgb(21, 20, 20);
  color: #fff;
  font-size: 20px;
  border-radius: 100%;
}

.card-container {
  display: flex;
  flex-wrap: wrap;
}
.card {
  width: 225px;
  height: 225px;
  background-color: rgb(237, 182, 44);
  padding: 10px;
  border-radius: 15px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin-right: 20px;
  margin-bottom: 20px;
}

.date {
  font-size: 12.5px;
  font-weight: bold;
}

.overlay {
  position: absolute;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.77);
  z-index: 10;
  display: flex;
  align-items: center;
  justify-content: center;
}

.modal {
  width: 770px;
  position: relative;
  display: flex;
  flex-direction: column;
  background: #fff;
  border-radius: 10px;
  padding: 30px;
}

.modal button {
  padding: 10px 20px;
  font-size: 20px;
  margin-top: 15px;
  width: 100%;
  background-color: blueviolet;
  color: #fff;
  border: none;
}

.modal .close {
  background-color: red;
  margin-top: 7px;
}
</style>
