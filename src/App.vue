<script setup>
import { reactive } from 'vue';
import Cabecalho from './components/Cabecalho.vue';
import Formulario from './components/Formulario.vue';
import ListaTarefas from './components/ListaTarefas.vue';

const estado = reactive({
  filtro: "todas",
  tarefaTemp: '',
  tarefas: [
    {
      titulo: "Estudar ES6",
      finalizada: false,
    },
    {
      titulo: "Estudar SASS",
      finalizada: false,
    },
    {
      titulo: "Ir para a academia",
      finalizada: true,
    },
  ]
});

const getTarefasPendentes = () => {
  return estado.tarefas.filter(tarefa => !tarefa.finalizada);
  // estado.tarefas.filter(tarefa => tarefa.finalizada === false);
};

const getTarefasFinalizadas = () => {
  return estado.tarefas.filter(tarefa => tarefa.finalizada);
  // estado.tarefas.filter(tarefa => tarefa.finalizada === true);
};

const getTarefasFiltradas = () => {
  const { filtro } = estado;
  // const filtro = estado.filtro;

  switch (filtro) {
    case 'pendentes':
      return getTarefasPendentes();
    case 'finalizadas':
      return getTarefasFinalizadas();
    default:
      return estado.tarefas;
  };
};

const cadastraTarefa = () => {
  const tarefaNova = {
    titulo: estado.tarefaTemp,
    finalizada: false,
  };
  estado.tarefas.push(tarefaNova);
  estado.tarefaTemp = '';
};
</script>

<template>
  <div class="container">
    <Cabecalho :tarefas-pendentes="getTarefasPendentes().length" />
    <Formulario
      :trocar-filtro="evento => estado.filtro = evento.target.value"
      :tarefa-temp="estado.tarefaTemp"
      :edita-tarefa-temp="evento => estado.tarefaTemp = evento.target.value"
      :cadastra-tarefa="cadastraTarefa"
    />
    <ListaTarefas :tarefas="getTarefasFiltradas()" />
  </div>
</template>
