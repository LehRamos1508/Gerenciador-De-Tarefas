# Relatório: Aplicação de Gerenciamento de Tarefas

## Descrição Geral
Essa aplicação é um **gerenciador de tarefas** desenvolvido com **React Native** e **Axios** para integração com uma API REST. O objetivo principal é permitir que os usuários possam listar, criar, editar e excluir tarefas de maneira prática, com uma interface estilizada e amigável.

---

## Funcionalidades
### 1. **Listar Tarefas**
   - Exibe uma lista de tarefas provenientes da API.
   - As tarefas podem ser filtradas por status:
     - **Todos** 📝
     - **Pendentes** ⏰
     - **Feito** ✅

### 2. **Criar Nova Tarefa**
   - Através da navegação, o usuário pode criar uma nova tarefa, que será adicionada automaticamente à lista.

### 3. **Editar Tarefa**
   - O usuário pode editar a descrição e o status de uma tarefa existente.

### 4. **Deletar Tarefa**
   - Tarefas podem ser removidas definitivamente da lista.

### 5. **Atualização Automática**
   - A lista de tarefas é atualizada automaticamente após criar, editar ou excluir uma tarefa, sem necessidade de atualizar manualmente.

---

## Tecnologias Utilizadas
- **React Native**: Para a criação da interface do aplicativo.
- **Axios**: Para realizar as requisições HTTP com a API.
- **React Navigation**: Para gerenciar as transições entre as telas.

---

## Estrutura de Código
### **Tela Principal (`HomeScreen`)**
- **Responsável por**: 
  - Exibir a lista de tarefas.
  - Permitir a navegação para criação e edição de tarefas.
- **Destaques do Código**:
  - Uso de `FlatList` para renderização eficiente.
  - Lógica de filtragem de tarefas por status.
  - Atualização automática da lista ao retornar à tela principal.

### **Tela de Criação e Edição**
- **Nova Tarefa**:
  - Tela para adicionar uma nova tarefa com campos para descrição e status.
- **Editar Tarefa**:
  - Tela para editar uma tarefa existente com validação para campos obrigatórios.

### **API**
- **URL da API**: Configurada como `http://10.68.152.255:3000`.
- **Endpoints Utilizados**:
  - `GET /tarefas`: Retorna todas as tarefas.
  - `POST /tarefas`: Cria uma nova tarefa.
  - `PUT /tarefas/:id`: Atualiza uma tarefa existente.
  - `DELETE /tarefas/:id`: Remove uma tarefa.

---

## Estilização
- A aplicação foi estilizada para ser visualmente agradável:
  - **Filtros**: Botões destacados e responsivos.
  - **Lista de Tarefas**:
    - Cores que indicam o status: 
      - **Verde** para "Feito".
      - **Vermelho** para "Pendente".
    - Elementos com espaçamento adequado e cantos arredondados.
  - **Botões**:
    - Ações (Editar/Deletar) possuem estilos diferenciados.
    - Botão de "Nova Tarefa" com cor de destaque.

---

## Atualização Automática
Para garantir a atualização automática da lista, foi implementado:
1. **Centralização da Lógica**:
   - Função `buscarTarefas()` para carregar os dados da API.
2. **Listener de Navegação**:
   - Usado `navigation.addListener("focus")` para recarregar a lista ao voltar à tela principal.

---

## Pontos de Melhoria
1. **Feedback Visual**:
   - Exibir animações ou mensagens de carregamento durante as requisições.
2. **Autenticação**:
   - Adicionar autenticação de usuários para gerenciar tarefas individuais.
3. **Tratamento de Erros**:
   - Implementar mensagens de erro mais amigáveis para problemas na API.

---

## Conclusão
A aplicação oferece uma interface intuitiva e funcional para gerenciar tarefas, com atualização automática e estilização moderna. Ela pode ser expandida com novas funcionalidades e integrações para atender a diferentes necessidades dos usuários.
