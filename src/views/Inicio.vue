<template>
    <hr>
    <h1>Bienvenido a LOGOSCAN</h1>
    <hr>
    <div class="inicio">
    <b-carousel
        id="carousel-1"
        v-model="slide"
        :interval="4000"
        controls
        indicators
        background="#ababab"
        img-width="1024"
        img-height="480"
        style="text-shadow: 1px 1px 2px #333;"
        @sliding-start="onSlideStart"
        @sliding-end="onSlideEnd"
        >
        <!-- Text slides with image -->
        <b-carousel-slide
            caption="First slide"
            text="Nulla vitae elit libero, a pharetra augue mollis interdum."
            img-src="https://picsum.photos/1024/480/?image=52"
        ></b-carousel-slide>

        <!-- Slides with custom text -->
        <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=54">
            <h1>LOGOSCAN tu aplicación para hacer turismo por la ciudad</h1>
        </b-carousel-slide>

        <!-- Slides with image only -->
        <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=58"></b-carousel-slide>

        <!-- Slides with img slot -->
        <!-- Note the classes .d-block and .img-fluid to prevent browser default image alignment -->
        <b-carousel-slide>
            <template #img>
            <img
                class="d-block img-fluid w-100"
                width="1024"
                height="480"
                src="https://picsum.photos/1024/480/?image=55"
                alt="image slot"
            >
            </template>
        </b-carousel-slide>

        <!-- Slide with blank fluid image to maintain slide aspect ratio -->
        <b-carousel-slide caption="Blank Image" img-blank img-alt="Blank image">
            <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse eros felis, tincidunt
            a tincidunt eget, convallis vel est. Ut pellentesque ut lacus vel interdum.
            </p>
        </b-carousel-slide>
        </b-carousel>

        <p class="mt-4">
        Slide #: {{ slide }}<br>
        Sliding: {{ sliding }}
        </p>
    </div>
    <div>
        <div class="col"></div>
        <div class="col">
            <h4>
                Con LOGOSCAN ahorrate unos pesos cuando salgas de paseo
            </h4>
            <hr>
            <p>
                Lorem ipsum dolor sit amet consectetur, adipisicing elit. Vero esse, ad ipsa atque hic nemo aspernatur minima labore ex libero corporis quis perferendis blanditiis nulla quisquam aperiam, consectetur recusandae dolorum!
            </p>
        </div>
        <div class="col"></div>
    </div>
</template>

<script>
  export default {
    data() {
      return {
        slide: 0,
        sliding: null
      }
    },
    methods: {
      onSlideStart(slide) {
        this.sliding = true
      },
      onSlideEnd(slide) {
        this.sliding = false
      }
    }
  }
</script>
