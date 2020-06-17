<template>
  <div id="app">
   <todo-form :tarefas="tarefas" @AdicionarTexto="Adicionar($event)"/>
   <tarefas :tarefas="tarefas" />
  </div>
</template>

<script>
import tarefas from "./components/tarefas.vue"
import TodoForm from "./components/TodoForm.vue"
export default {
  name: 'App',
  components: {
    TodoForm , tarefas
  } , data: function() {
   return{
     tarefas: [{
          descricao: "lavar carro",
          cor: "background: green"
        }]
   }
  } , methods :  {
    Adicionar: function(event) {
      this.tarefas.push({
        descricao: event.nome,
        cor: event.cor
      })
      }
    }
}
</script>

<style>

</style>
