<template>
  <p class="logo"><img alt="Vue logo" src="/src/assets/logo.png" /></p>
  <div class="test">
    <ul>
      <li v-for="name in names">
        {{ name }}
      </li>
    </ul>
    <ul>
      <li v-for="pet in pets">
        {{ pet }}
      </li>
    </ul>
  </div>
</template>

<script>
import accounts from "/src/components/name.json";
export default {
  name: 'jsontest',
  computed: {
    names() {
      return accounts.accounts.map((info) => {
        return info.name;
      })
    },
    pets() {
      return accounts.accounts.map((info) => {
        return info.pet;
      })
    }
  }
}
</script>

<style scoped>
.logo {
  position: relative;
  width: 100%;
  margin: 0 auto;
}
</style>