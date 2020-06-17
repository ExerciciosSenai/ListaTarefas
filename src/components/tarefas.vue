<template>
  <div id="caixa">
<div class="tarefas" v-for="(tarefa, index) in tarefas" :key="index" :style="tarefa.cor" >
            {{tarefa.descricao}}
        </div>
  </div>
</template>

<script>
export default {
  name: "caixa",
    props: ['tarefas']
}
</script>

<style>
#caixa{
        color: #FFF;
        display: flex;
        width: 800px;
        height: 200px;
        border: 1px solid #FFF;
        margin: 50px auto 0 auto;
        flex-wrap: wrap;
    }
    .tarefas{
        width: 150px;
        height: 30px;
        border: 1px solid #FFF;   
        margin: 10px 0 0 10px;
        text-align: center;
        line-height: 30px;
        user-select: none;
        cursor: pointer;
    }
</style>