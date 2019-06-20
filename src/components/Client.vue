<template>
  <div class="section">
    <div class="attr">
      <span>{{ names }}</span>
    </div>
    <div class="attr">
      <span>Edad: {{ age }}</span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Evan',
      surname: 'You',
      birthdate: new Date(1990, 5, 11)
    }
  },
  computed: {
    names() {
      return `${this.name} ${this.surname}`
    },
    age() {
      let today = new Date()
      let diff = today - this.birthdate

      // seconds, minutes, hours, days, years
      return Math.floor(diff / (1000 * 60 * 60 * 24 * 365.25))

    }
  }
}
</script>

<style scoped>
.section {
  font-size: 2.4rem;
  background-color: #5FAD56;
  border-radius: 5px;
  margin: 10px;
  padding: 10px;
}

.attr {
  margin: 10px;
}
</style>
