<template>
  <v-layout row justify-center align-center wrap class="mt-4 pt-2">
    <v-flex xs12 sm12 md5 lg6 xl6 class="mt-4 pt-4">
      <h2 class="mb-4 pl-4 pt-2">Education</h2>
      <v-card-text class="py-0">
        <v-timeline align-top dense>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">SEP 2013 -</div>
                <div class="caption font-weight-bold green--text">JUN 2019</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Egerton University , </strong>
                <div class="caption mb-2">Bsc. Computer Science </div>
                <div class="caption mb-2">Second Class Upper Division</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">FEB 2010 -</div>
                <div class="caption font-weight-bold green--text">NOV 2013</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>High School</strong>
                <div class="caption mb-2">Njiiri School</div>
                <div class="caption mb-2">A-</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
          
        </v-timeline>
      </v-card-text>
    </v-flex>
    <v-flex xs12 sm12 md4 lg6 xl6 class="mt-4 pt-2">
      <h2 class="mb-4 pl-4">Experience</h2>
      <v-card-text class="py-0">
        <v-timeline align-top dense>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">JULY 2022 -</div>
                <div class="caption font-weight-bold green--text">PRESENT</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Dynasoft Business Solutions</strong><br>
                <strong>Software Developer</strong>
                <div class="caption mb-2">Full Time</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">DECEMBER 2021 -</div>
                <div class="caption font-weight-bold green--text">June 2022</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Damu Sasa System Limited</strong><br>
                <strong>Software Developer</strong>
                <div class="caption mb-2">Full Time</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">FEB 2019 -</div>
                <div class="caption font-weight-bold green--text">November 2021</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Avanet Technologies</strong><br>
                <strong>Software Developer , Technical Support Engineer</strong>
                <div class="caption mb-2">Full Time</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">MAY 2021 -</div>
                <div class="caption font-weight-bold green--text">NOV 2021</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Liorra Teaching Limited</strong><br>
                <strong>Data Science Instructor</strong>
                <div class="caption mb-2">Part Time</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
        </v-timeline>
      </v-card-text>
    </v-flex>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-flex xs12 sm12 md4 lg5 xl5 class="mx-2 pt-4">
        <h2>
          <span>Technical</span>

          <span class="green--text">Skills</span>
        </h2>
        <br>
        <strong>.Net Fremework | .Net Core [C#]</strong>
        <v-progress-linear v-model="buffer1" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
        <strong>C/AL</strong>
        <v-progress-linear v-model="buffer1" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
        <strong>JavaScript</strong>
        <v-progress-linear v-model="buffer2" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
        <strong>Azure</strong>
        <v-progress-linear v-model="buffer3" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
      </v-flex>
      <v-flex xs12 sm12 md4 lg5 xl5 class="mx-2 pt-4">
        <br> 
        <br>
        <strong>SQL</strong>
        <v-progress-linear v-model="buffer1" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
        <strong>AL</strong>
        <v-progress-linear v-model="buffer4" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
        <strong>PHP</strong>
        <v-progress-linear v-model="buffer5" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
        <strong>Docker & Kubernetes</strong>
        <v-progress-linear v-model="buffer6" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
      </v-flex>
      <div class="mt-4 pt-2">
        <v-btn
          href="https://drive.google.com/file/d/1mIo7mJ3acgKUDQUXOtM2ejJRziHFOKlT/view?usp=sharing"
          target="_blank"
          color="green"
          dark
          large
        >
          Download Resume
          <v-icon right dark>fas fa-file-download</v-icon>
        </v-btn>
      </div>
    </v-layout>
  </v-layout>
</template>

<script>
export default {
  metaInfo: {
    title: "Resume",
    titleTemplate: "%s ← Orina's Space",
    // meta: [
    //   { name: "viewport", content: "width=device-width, initial-scale=1" },
    //   {
    //     name: "description",
    //     content:
    //       "Vue NUXT HTML CSS JavaScript Design Adobe XD Photoshop Coding Skills Resume Work Web Developer Front-End"
    //   },
    //   { charset: "utf-8" },
    //   { property: "og:title", content: "Eldin' Space" },
    //   { property: "og:site_name", content: "Eldin' Space" },
    //   { property: "og:type", content: "website" },
    //   { property: "og:url", content: "https://eldin.space" },
    //   {
    //     property: "og:image",
    //     content: "https://i.imgur.com/Dcz2PGx.jpg"
    //   },
    //   {
    //     property: "og:description",
    //     content:
    //       "Vue NUXT HTML CSS JavaScript Design Adobe XD Photoshop Coding Skills Resume Work Web Developer Front-End"
    //   }
    // ]
  },
  data() {
    return {
      value: 0,
      buffer1: 0,
      buffer2: 0,
      buffer3: 0,
      buffer4: 0,
      buffer5: 0,
      buffer6: 0,
      bufferValue: 100,
      interval: 0
    };
  },
  mounted() {
    this.startBuffer();
  },

  beforeDestroy() {
    clearInterval(this.interval);
  },

  methods: {
    startBuffer() {
      this.interval = setInterval(() => {
        this.buffer1 = 100;
        this.buffer2 = 100;
        this.buffer3 = 100;
        this.buffer4 = 100;
        this.buffer5 = 100;
        this.buffer6 = 100;
      }, 800);
    }
  }
};
</script>
<style >
</style>

