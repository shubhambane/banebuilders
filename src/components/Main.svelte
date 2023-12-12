<script>
    let scrollY = 0;
      window.addEventListener("scroll", () => {
      scrollY = window.scrollY;
    });
  </script>
  
  <style>
    .hero {
        position: relative;
    height: 100vh;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    text-align: center;
    }
  
    .parallax-bg {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-size: cover;
    background-position: center;
    transform: translateY(calc(var(--scroll-y) * -0.5));
    z-index: -1;
    }
  </style>
  
  <div class="hero">
    <div class="parallax-bg" style="--scroll-y: {scrollY}px; background-image: url('your-background-image.jpg');"></div>
    <div>
      <h1 class="text-4xl font-bold">Your Hero Title</h1>
      <p>Your hero section content goes here.</p>
    </div>
  </div>
  