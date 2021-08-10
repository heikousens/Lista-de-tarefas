<template>
  <div id="app" class="table">
    <div class="titulo">
      <h3>ID</h3>
      <h3>Descrição</h3>
    </div>
    <div class="itensLista" v-for="tarefa in tarefas" v-bind:key="tarefa.id">
      <span v-if="tarefa.estaCompleta = !tarefa.estaCompleta" class="completaEstilo">
        <p>{{ tarefa.id }}</p>
        <p>{{ tarefa.descricao }}</p>
      </span>
      <span v-else v-bind:style="{textDecoration: lineThrough}">
        <p>{{ tarefa.id }}</p>
        <p>{{ tarefa.descricao }}</p>
      </span>
    </div>
  </div>
</template>

<script>
export default {
data: function() {
  return {
    tarefas: [
      {
          id: 1,
          descricao: 'Varrer a casa',
          estaCompleta: false
      },
      {
          id: 2,
          descricao: 'Lavar a louça',
          estaCompleta: true
      },
      {
          id: 3,
          descricao: 'Passear com os cachorros',
          estaCompleta: false
      },
      {
          id: 4,
          descricao: 'Fazer feira',
          estaCompleta: true
      },
      {
          id: 5,
          descricao: 'Pagar conta de luz',
          estaCompleta: false
      },
      {
          id: 6,
          descricao: 'Ir à farmácia',
          estaCompleta: false
      },
      {
          id: 7,
          descricao: 'Marcar médico',
          estaCompleta: true
      },
      {
          id: 8,
          descricao: 'Botar roupa suja de molho',
          estaCompleta: true
      },
    ]
  }
},
}
</script>

<style>
  @import './assets/estilos/estilos.css';
</style>
