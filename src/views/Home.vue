<template>
  <v-layout column justify-center align-center class="mt-4 pt-2">
    <VueCompareImage
      class="hidden-md-and-down"
      hover
      :style="{ minWidth: '1300px' }"
      :sliderLineWidth="sliderLine"
      :handleSize="hSize"
      :leftImage="leftImage"
      :rightImage="rightImage"
      :sliderPositionPercentage="sliderPosition"
    />
    <VueCompareImage
      class="hidden-lg-and-up"
      hover
      :style="{ maxWidth: '400px' }"
      :sliderLineWidth="sliderLine"
      :handleSize="hSize"
      :leftImage="leftImage2"
      :rightImage="rightImage2"
      :sliderPositionPercentage="sliderPosition"
    />

    <br>

    <vue-typer class="headline" :repeat="0" text="Brian Orina"></vue-typer>
    <vue-typer
      :text="text1"
      :repeat="Infinity"
      :shuffle="false"
      initial-action="erasing"
      :pre-type-delay="70"
      :type-delay="70"
      :pre-erase-delay="1980"
      :erase-delay="150"
      erase-style="select-back"
      :erase-on-complete="false"
      caret-animation="smooth"
    ></vue-typer>
    <br>
    <v-flex xs12 sm6 md4 lg4 xl4>
      <v-card flat color="transparent" max-width="500">
        <v-card-title primary-title>
          <div>
            <h3 class="headline mb-0">
              <span>About</span>
              <span class="green--text">Me</span>
            </h3>
            <div>
              <p>
                Hello! I’m Brian Orina. I'm a software engeneer who
                is passionate about
                <span
                  class="green--text font-weight-bold"
                >Data Driven Technologies</span>, building great user experiences,
                fighting for simplicity over complexity and constantly learning.
                When I'm not coding, you'll find me watching football.
              </p>
            </div>
          </div>
        </v-card-title>

        <v-card-actions class="hidden-sm-and-down">
          <v-btn
            v-for="icon in icons"
            :key="icon.icon"
            fab
            dark
            outline
            color="green"
            :href="icon.href"
            target="_blank"
          >
            <v-icon dark>{{icon.icon}}</v-icon>
          </v-btn>
        </v-card-actions>

        <v-card-actions class="hidden-md-and-up justify-center">
          <v-btn
            v-for="icon in icons"
            :key="icon.icon"
            small
            fab
            dark
            outline
            color="green"
            :href="icon.href"
            target="_blank"
          >
            <v-icon dark>{{icon.icon}}</v-icon>
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
import { VueTyper } from "vue-typer";
import VueCompareImage from "vue-compare-image";

export default {
  metaInfo: {
    title: "Home",
    titleTemplate: "%s ← Orinas's Space",
    // meta: [
    //   { name: "viewport", content: "width=device-width, initial-scale=1" },
    //   { name: "description", content: "Brian Orinas's Portfolio" },
    //   { charset: "utf-8" },
    //   { property: "og:title", content: "Orinas' Space" },
    //   { property: "og:site_name", content: "Eldin' Space" },
    //   { property: "og:type", content: "website" },
    //   { property: "og:url", content: "https://eldin.space" },
    //   {
    //     property: "og:image",
    //     content: "https://i.imgur.com/Dcz2PGx.jpg"
    //   },
    //   { property: "og:description", content: "Eldin Zaimovic's Portfolio" }
    // ]
  },
  components: {
    "vue-typer": VueTyper,
    VueCompareImage
  },
  data() {
    return {
      icons: [
        { href: "https://github.com/Brianorinah", icon: "fab fa-github" },
        {
          href: "https://stackoverflow.com/users/11765163/brian-the-guru",
          icon: "fab fa-stack-overflow"
        },        
        {
          href: "https://www.linkedin.com/in/brian-orina-666b0416b/",
          icon: "fab fa-linkedin-in"
        },
       
      ],
      text1: ["Full Stack web Developer", "Microsoft Dynamics 365", "APIs", "Docker & Kubernetes"],
      leftImage: "https://i.postimg.cc/VLChcHLg/test1.jpg",
      rightImage: "https://i.postimg.cc/6pwxbNLn/test2.jpg",
      leftImage2: "https://i.postimg.cc/CLdpzR33/portfolio.jpg",
      rightImage2: "https://i.postimg.cc/CLdpzR33/portfolio.jpg",
      // leftImage2: "https://i.imgur.com/SXBitjh.jpg",
      // rightImage2: "https://i.imgur.com/Dcz2PGx.jpg",
      sliderLine: 0,
      hSize: 0,
      sliderPosition: 0.5
    };
  }
};
</script>
<style>
@keyframes rocking {
  0%,
  100% {
    transform: rotateZ(-10deg);
  }

  50% {
    transform: rotateZ(10deg);
  }
}

.vue-typer {
  font-family: Arial, "Helvetica Neue", Helvetica, sans-serif;
}
.vue-typer .custom.char.typed {
  color: green;
}
.vue-typer .custom.char.selected {
  color: #e91e63;
}

.vue-typer .custom.caret {
  animation: rocking 1s ease-in-out 0s infinite;
}
.vue-typer .custom.caret.typing {
  background-color: green;
}
.vue-typer .custom.caret.selecting {
  display: inline-block;
  background-color: #e91e63;
}
</style>

