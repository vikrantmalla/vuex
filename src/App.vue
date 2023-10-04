<template>
  <main class="container">
    <div>
      <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />
    </div>
    <div class="counter">{{ $store.state.counter }}</div>
    <div class="btn-container">
      <button @click="$store.commit('addToCounter')">Add</button>
      <button @click="$store.commit('subToCounter')">Sub</button>
    </div>
  </main>
  <RouterView />
</template>


<style scoped>
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 2rem;
}

.counter {
  color: black;
  font-size: 50px;
}

.btn-container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  gap: 2rem;
}

.btn-container button {
  padding: 1rem 3rem;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
