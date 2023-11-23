<template>
  <div>
    <h2>Detalhes do Lead</h2>
    
    <div class="row mb-3">
      <label for="id" class="col-sm-2 col-form-label">ID</label>
      <div class="col-sm-10">
        <input type="text" class="form-control" :value="dados.id" readonly>
      </div>
    </div>
    
    <div class="row mb-3">
      <label for="id" class="col-sm-2 col-form-label">NOME</label>
      <div class="col-sm-10">
        <input type="text" class="form-control" :value="dados.nome" readonly>
      </div>
    </div>
    
    <div class="row mb-3">
      <label for="id" class="col-sm-2 col-form-label">FONE</label>
      <div class="col-sm-10">
        <input type="text" class="form-control" :value="dados.telefone" readonly>
      </div>
    </div>

    <div class="col-auto">
      <button class="btn btn-primary">Atualizar</button>
    </div>
    
  </div>
</template>

<script>
import ApiMixin from '../../mixins/ApiMixin'

export default {
  name: 'Lead',
  mixins: [ApiMixin],
  created() {
    this.getDadosApi(`http://localhost:3000/leads/${this.$route.params.id}`)
  }
}
</script> 