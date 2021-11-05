<template>
  <!--  https://dev.to/ayushmanbthakur/how-to-make-tic-tac-toe-in-browser-with-html-css-and-js-28ed-->
  <div class="container">
    <h1>Tic-Tac-Toe</h1>
    <div class="play-area">
      <div id="block_0" class="block">X</div>
      <div id="block_1" class="block">O</div>
      <div id="block_2" class="block"></div>
      <div id="block_3" class="block"></div>
      <div id="block_4" class="block"></div>
      <div id="block_5" class="block"></div>
      <div id="block_6" class="block"></div>
      <div id="block_7" class="block"></div>
      <div id="block_8" class="block"></div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'App',
    components: {
    },
    data() {
      return {
        content: ["", "", "", "", "", "", "", "", ""],
        turn: true,
      }
    },
    methods: {}
  }
</script>

<style>

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, Helvetica, sans-serif;
  }

  .container {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background: #eee;
  }

  h1 {
    font-size: 5rem;
    margin-bottom: 0.5em;
  }

  h2 {
    margin-top: 1em;
    font-size: 2rem;
    margin-bottom: 0.5em;
  }

  .play-area {
    display: grid;
    width: 300px;
    height: 300px;
    grid-template-columns: auto auto auto;
  }

  .block {
    display: flex;
    width: 100px;
    height: 100px;
    align-items: center;
    justify-content: center;
    font-size: 3rem;
    font-weight: bold;
    border: 3px solid black;
    transition: background 0.2s ease-in-out;
  }

  .block:hover {
    cursor: pointer;
    background: #0ff30f;
  }

  .occupied:hover {
    background: #ff3a3a;
  }

  .win {
    background: #0ff30f;
  }

  .win:hover {
    background: #0ff30f;
  }

  #block_0,
  #block_1,
  #block_2 {
    border-top: none;
  }

  #block_0,
  #block_3,
  #block_6 {
    border-left: none;
  }

  #block_6,
  #block_7,
  #block_8 {
    border-bottom: none;
  }

  #block_2,
  #block_5,
  #block_8 {
    border-right: none;
  }

  button {
    outline: none;
    border: 4px solid green;
    padding: 10px 20px;
    font-size: 1rem;
    font-weight: bold;
    background: none;
    transition: all 0.2s ease-in-out;
  }

  button:hover {
    cursor: pointer;
    background: green;
    color: white;
  }

  .playerWin {
    color: green;
  }

  .computerWin {
    color: red;
  }

  .draw {
    color: orangered;
  }

  @media only screen and (max-width: 600px) {

    h1 {
      font-size: 3rem;
      margin-bottom: 0.5em;
    }

    h2 {
      margin-top: 1em;
      font-size: 1.3rem;
    }
  }
</style>
