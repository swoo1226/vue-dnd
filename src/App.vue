<template>
  <div id="app">
    <main class="flexbox">
      <Board id="board-1">
        <Card id="card-1" draggable="true">
          <p>Card one</p>
        </Card>
      </Board>
      <Board id="board-2">
        <Card id="card-2" draggable="true">
          <p>Card two</p>
        </Card>
      </Board>
    </main>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import Board from './components/Board.vue';
import Card from './components/Card.vue';
export default Vue.extend({
  name: 'app',
  components: {
    Board,
    Card
  }
});
</script>

<style>
.flexbox {
  display: flex;
  justify-content: space-between;
  width: 100%;
  max-width: 768px;
  height: 100vh;
  overflow: hidden;
}
.flexbox .board {
  display: flex;
  flex-direction: column;
  width: 100%;
  max-width: 300px;
  background-color: #313131;
  padding: 15px;
}
.flexbox .board .card {
  padding: 15px 25px;
  background-color: #f3f3f3;
  cursor: pointer;
  margin-bottom: 15px;
}

</style>
