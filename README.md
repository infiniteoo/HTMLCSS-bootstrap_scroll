# Bootstrap with Scrolling Animation

### Live Demo:

https://b00tstrap.netlify.app/

### About:

Simple product landing page utilizing the Bootstrap framework which includes some jQuery for smooth scrolling and a third party application, Scroll Reveal, to animation elements on our page when they enter the viewport.

![example_gif](./example.gif)

### Plug In:

This projected utilized the power of Scroll Reveal

https://github.com/jlmakes/scrollreveal

```
window.sr = ScrollReveal();

sr.reveal(".navbar", {
    duration: 2000,
    origin: "bottom",
});

```

### Relevant Code:

jQuery code block to enable smooth scrolling:

```
<script>
      $(function () {
        // Smooth Scrolling
        $('a[href*="#"]:not([href="#"])').click(function () {
          if (
            location.pathname.replace(/^\//, "") ==
              this.pathname.replace(/^\//, "") &&
            location.hostname == this.hostname
          ) {
            var target = $(this.hash);
            target = target.length
              ? target
              : $("[name=" + this.hash.slice(1) + "]");
            if (target.length) {
              $("html, body").animate(
                {
                  scrollTop: target.offset().top,
                },
                1000
              );
              return false;
            }
          }
        });
      });
    </script>

```

### Acknowlegement:

Thanks to Traversy Media for this great tutorial.
