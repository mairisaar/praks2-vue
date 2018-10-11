<template>
  <div>
    <h1>Kaalu teisendamine</h1>
    <h4>Sisesta kaal kilogrammides</h4>
    <input type="number" min="0" v-model="kg">
    <table>
      <tr>
        <td>Grammid</td>
        <td>{{ `${kg * 1000} g` }}</td>
      </tr>
      <tr>
        <td>Naelad</td>
        <td>{{ `${(kg * 2.20462).toFixed(2)} lb` }}</td>
      </tr>
      <tr>
        <td>Untsid</td>
        <td>{{ `${(kg * 35.274).toFixed(2)} oz` }}</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: 'Konverter',
  data () {
    return {
      kg: 0
      }
  },
  methods: { 
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
