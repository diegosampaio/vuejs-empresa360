<template>
  <div>
    <h2>Detalhes do Lead</h2>
    
    
  </div>
</template>

<script>
export default {
  name: 'Lead',
  data: () => ({
    dados: null
  }),
  created() {
    this.getDadosApi()
  },
  methods: {
    getDadosApi() {
      fetch('http://localhost:3000/leads')
        .then(response => response.json())
        .then(response => {
          console.log(response)
          this.dados = response
        })
    }
  }
}
</script>