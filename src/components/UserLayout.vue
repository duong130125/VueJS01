<template>
    <div class="user-layout">
      <header class="header">Header</header>
      <nav class="navigation">Navigation</nav>
      <div class="content">
        <aside class="menu">Menu</aside>
        <main class="main">
          <div class="card-grid">
            <div class="card" v-for="i in 16" :key="i">Card</div>
          </div>
        </main>
        <aside class="article">Article</aside>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'UserLayout'
  }
  </script>
  
  <style scoped>
  .user-layout {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }
  
  .header, .navigation {
    background-color: #091ce9e4;
    padding: 10px;
  }
  
  .content {
    display: flex;
    flex: 1;
  }
  
  .menu {
    background-color: #bd5858;
    width: 200px;
    padding: 20px;
  }
  
  .main {
    flex: 1;
    padding: 20px;
  }
  
  .article {
    background-color: #e6addd;
    width: 200px;
    padding: 20px;
  }
  
  .card-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 20px;
  }
  
  .card {
    background-color: #8b8889;
    border: 1px solid #ddd;
    padding: 20px;
    text-align: center;
  }
  </style>