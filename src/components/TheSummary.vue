<script>
export default {
  props: {
    data: {
      required: true,
      type: Number
    }
  }
}
</script>

<template>
  <section class="summary">
    <h1 class="red">Who Is At Mars Today?</h1>

    <h2>There {{  data !== 1 ? 'are' : 'is'  }} <span class="count">{{  data  }}</span> operational
      {{  data !== 1 ? 'robots' : 'robot'  }} at Mars today</h2>
    <p>(still no humans)</p>
  </section>
</template>

<style scoped lang="scss">
.summary {
  text-align: center;

  h1 {
    font-size: 3rem;
    margin: 0 0 2rem 0;

    &.red {
      color: var(--color-accent);
    }
  }

  .count {
    color: var(--color-accent);
    font-size: 1.6rem;
    font-weight: bold;
  }
}
</style>
