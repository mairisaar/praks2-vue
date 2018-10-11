<template>
  <div>
    <h1>Kaalu teisendamine</h1>
    <h4>Sisesta kaal kilogrammides</h4>
    <input type="number" min="0" v-model="kg">
    <table v-if="kg !== ''">
      <tr>
        <td>Grammid</td>
        <td>{{ convertKg(1000) + ' g' }}</td>
      </tr>
      <tr>
        <td>Naelad</td>
        <td>{{ convertKg(2.20462) + ' lb' }}</td>
      </tr>
      <tr>
        <td>Untsid</td>
        <td>{{ convertKg(35.2739316) + ' oz' }}</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: 'Konverter',
  data () {
    return {
      kg: ''
      }
  },
  methods: { 
    convertKg (multiplier) {
      return (this.kg !== 0) ? (this.kg * multiplier).toFixed(2) : 0;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
