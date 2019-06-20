<template>
  <div id="app" class="principal">
    <span>{{ titulo }}</span>
    <entry></entry>
  </div>
</template>

<script>
import Entry from '@/views/Entry.vue'

export default {
  name: 'App',
  data() {
    return {
      titulo: 'Tickets'
    }
  },
  components: {
    Entry
  }
}
</script>

<style>
html {
  font-size: 62.5% !important;
}

.principal {
  background-color: #F78154;
  padding: 10px;
  color: white;
  border-radius: 5px;
  width: 400px;
  font-size: 3rem;
  text-align: center
}
</style>
