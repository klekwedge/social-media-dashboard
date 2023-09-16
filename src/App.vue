<template>
  <div class="app__wrapper">
    <main class="main">
      <Dashboard></Dashboard>
    </main>
  </div>
</template>

<script>
import Dashboard from "./components/Dashboard.vue";
export default {
  name: "App",
  components: { Dashboard },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@400;700&display=swap");

#app {
  color: var(--textMainColor);
  background-color: var(--bgColor);

  .app__wrapper {
    min-height: 100%;
    display: flex;
    flex-direction: column;
    overflow: hidden;
  }
}

.main {
  flex: 1 1 auto;

  @media (min-width: 1024px) {
    position: relative;
    &::before {
      content: "";
      position: absolute;
      width: 100%;
      height: 33%;
      top: 0;
      left: 0;
      background-color: var(--bgDecorColor);
      border-radius: 0 0 35px 35px;
    }
  }
}
</style>
