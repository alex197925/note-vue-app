<!-- @format -->

<template>
  <main>
    <div class="container">
      <header>
        <h1>Notes</h1>
        <button>+</button>
      </header>

      <div class="card-container">
        <div class="card">
          <p class="main-text"></p>
          <p class="date"></p>
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

button {
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
</style>
