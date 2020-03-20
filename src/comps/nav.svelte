<script>
  let burgerActive = false
  let activeMenu = "home"
</script>
<nav class="navbar is-fixed-top" role="navigation" aria-label="main navigation">
  <div class="container is-flex-desktop">
    <div class="navbar-brand">
      <a class="navbar-item" href="#/">
        <img src="https://bulma.io/images/bulma-logo.png" alt="brand pic" width="112" height="28">
      </a>
      <span class:is-active={burgerActive} role="button" class="navbar-burger" aria-label="menu" aria-expanded="false" on:click={() =>{burgerActive = !burgerActive}}>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </span>
    </div>
    <div class="navbar-menu" class:is-active={burgerActive} on:click={()=>{burgerActive = false}}>
      <div class="navbar-end">
          <a href="#/" class="navbar-item" class:navActive={activeMenu == "home"} on:click={() => {activeMenu="home"}}>Home</a>
          <a href="#/about" class="navbar-item" class:navActive={activeMenu == "about"} on:click={() => {activeMenu="about"}}>About</a>
          <a href="#/booking" class="navbar-item" class:navActive={activeMenu == "booking"} on:click={() => {activeMenu="booking"}}>Booking</a>
          <a href="#/faq" class="navbar-item" class:navActive={activeMenu == "faq"} on:click={() => {activeMenu="faq"}}>FAQ</a>
      </div>
    </div>
  </div>
</nav>

<style>
  .navActive {
    color: blue;
    font-weight: 600;
  }
  .navbar-item:active {
    color: blue;
    background: white;
  }
  .navbar-item:hover {
    color: blue;
  }
  .navbar-item:focus {
    color: blue;
    background: white;
  }
</style>