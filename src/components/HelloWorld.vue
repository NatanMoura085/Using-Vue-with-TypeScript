<script setup lang="ts">
import { Component, Prop, Vue } from 'vue-facing-decorator';

@Component
export default class HelloWorld extends Vue {
  @Prop({ default: 'Hello, world!' }) readonly msg!: string;
}
</script>

<template>
  <div class="greetings">
    <h1 class="greetings--green">{{ msg }}</h1>
    <h3>
      You’ve successfully created a project with
      <a href="https://vitejs.dev/" target="_blank" rel="noopener">Vite</a> +
      <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a>.
      What's next?
    </h3>
  </div>
</template>

<style scoped lang="scss">
.greetings {
  &--green {
    color: green;
  }
  & h1 {
    font-weight: 500;
    font-size: 2.6rem;
    top: -10px;
  }
  & h3 {
    font-size: 1.2rem;
  }
  h1,
  h3 {
    text-align: center;
  }
  @media (min-width: 1024px) {
    h1,
    h3 {
      text-align: left;
    }
  }
}
</style>