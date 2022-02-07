<script>
  const initializedSwiper = () => {
    new window.Swiper(document.querySelector('.image-slider'), {
      effect: 'coverflow',
      grabCursor: true,
      centeredSlides: true,
      slidesPerView: 'auto',
      coverflowEffect: {
        rotate: 0,
        stretch: 0,
        depth: 100,
        modifier: 2,
        slideShadows: true,
      },
      loop: true,
      autoplay: {
        delay: 2000,
        disableOnInteraction: false,
      },
    })
    swiper()
  }
</script>

<svelte:head>
  <script
    src="https://unpkg.com/swiper/swiper-bundle.min.js"
    on:load="{initializedSwiper}"></script>
</svelte:head>

<section class="l-home" id="home">
  <div class="l-home__content">
    <h3 class="l-home__title">Landing Page for App</h3>
    <p class="l-home__description">
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Neque nihil,
      quaerat iure nobis ducimus ea quod sapiente officia! Reprehenderit commodi
      corrupti officiis cumque amet unde, velit libero minus hic repellat.
    </p>
    <a href="#features" class="c-button">get started</a>
  </div>

  <div class="swiper-container image-slider">
    <div class="swiper-wrapper">
      <div class="swiper-slide">
        <img src="images/shot-01.jpg" alt="" class="swiper-image" />
      </div>
      <div class="swiper-slide">
        <img src="images/shot-02.jpg" alt="" class="swiper-image" />
      </div>
      <div class="swiper-slide">
        <img src="images/shot-03.jpg" alt="" class="swiper-image" />
      </div>
      <div class="swiper-slide">
        <img src="images/shot-04.jpg" alt="" class="swiper-image" />
      </div>
      <div class="swiper-slide">
        <img src="images/shot-05.jpg" alt="" class="swiper-image" />
      </div>
    </div>
  </div>
</section>
