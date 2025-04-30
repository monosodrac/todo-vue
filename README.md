# ✅ todo-vue - Lista de Afazeres com Vue.js

Este projeto foi desenvolvido com o objetivo de praticar conceitos fundamentais do **Vue.js**, como a ferramenta `reactive`, uso de `props` e a composição de componentes. Trata-se de uma **lista de tarefas** interativa, que permite adicionar, filtrar e atualizar o status de cada afazer.

## ✨ Funcionalidades

- ➕ **Adição de tarefas** com input controlado por `reactive`.
- ✅ **Atualização de status** (pendente ou finalizada) de cada tarefa.
- 🔍 **Filtro de visualização**: permite exibir tarefas **todas**, **pendentes** ou **finalizadas**.
- ♻️ **Componentização**: cabeçalho, formulário e lista de tarefas isolados e reutilizáveis.
- 🧠 Gerenciamento de estado com **reactive()** para reatividade e simplicidade.

## 🛠️ Tecnologias utilizadas

- [Vue.js 3](https://vuejs.org/)
- Composição com `<script setup>` do Composition API
- Reatividade com `reactive`
- Componentes com `props` e comunicação via bindings

## 🚀 Como executar o projeto

1. Clone o repositório:
   ```bash
   git clone https://github.com/monosodrac/todo-vue.git
2. Instale as dependências:
   ```bash
   npm install
   # ou
   yarn install
3. Inicie o servidor de desenvolvimento:
   ```bash
   npm run dev
   # ou
   yarn dev
4. Acesse em seu navegador:
   ```bash
   http://localhost:5173

## 📁 Estrutura do projeto:
   ```bash
   src/
   ├── components/          # Componentes reutilizáveis da interface
   │   ├── Cabecalho.vue    # Exibe o número de tarefas pendentes
   │   ├── Formulario.vue   # Campo para adicionar e filtrar tarefas
   │   └── ListaTarefas.vue # Lista de tarefas com status
   ├── App.vue              # Componente principal com lógica de estado
   └── main.js              # Ponto de entrada da aplicação
   ```
## 🤝 Contribuições:  

Contribuições são bem-vindas! Sinta-se livre para abrir issues, sugerir melhorias ou enviar pull requests.
