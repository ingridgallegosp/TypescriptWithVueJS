<script setup lang="ts">
import { reactive } from 'vue';
import type User from './types/User';

const sum = (x: number, y: number) => {
    return x+y
}
//sum(5, "2") // not assignable to parameter number
console.log(sum(8,5))

//Typing reactive data



const user: User = reactive({
    id: 1,
    username: "danielkellyio",
    settings:[]    
})

console.log(user)

</script>

<template>
 {{ user }}
</template>

<style scoped>
header {
  line-height: 1.5;
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
