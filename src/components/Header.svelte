<script>
  let active = false
  let activeHeader = false
  let iconClass = 'fa-bars'

  $: {
    iconClass = active ? 'fa-times' : 'fa-bars'
  }

  window.onscroll = () => {
    iconClass = 'fa-bars'
    active = false

    if (window.scrollY > 70) {
      activeHeader = true
    } else {
      activeHeader = false
    }
  }
</script>

<header class="{`l-header ${activeHeader && 'active'}`}">
  <a href="#home" class="l-header__logo">LOGO</a>

  <div
    class="{`fas ${iconClass} l-header__menu-button`}"
    on:click="{() => (active = !active)}"
  ></div>

  <nav class="{`l-header__navbar ${active && 'nav-active'}`}">
    <a href="#home" class="l-header__link">home</a>
    <a href="#features" class="l-header__link">features</a>
    <a href="#about" class="l-header__link">about</a>
    <a href="#usage" class="l-header__link">usage</a>
    <a href="#review" class="l-header__link">review</a>
    <a href="#pricing" class="l-header__link">pricing</a>
    <a href="#contact" class="l-header__link">contact</a>
  </nav>
</header>
