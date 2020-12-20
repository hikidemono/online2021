<template>
  <v-app>
    <div class="bg"> 
      <v-app-bar
        app
        dark
        color="transparent"
      >
        <v-toolbar-title>forget-me-not / hikidemono plus pink</v-toolbar-title>
        <v-spacer />
        <v-btn href="https://soundcloud.com/hikidemono" class="text-lowercase">
          <v-icon>mdi-soundcloud</v-icon>
          <pre> soundcloud</pre>
        </v-btn>
      </v-app-bar>
      <v-main>
        <v-contaier>
        <v-layout justify-center align-center column >
          <v-card
            dark
            width="600px"
            color="rgba(119,184,218,0.5)"
          >
            <v-card-title>
              forget-me-not / hikidemono plus pink
            </v-card-title>
            <v-card-subtitle>
              Feelin' Free OB's Regular Concert 2021 Online.
            </v-card-subtitle>
            <div>
              <vuetify-audio :file="mp3path" :ended="audioFinish"></vuetify-audio>
            </div>
          </v-card>
        </v-layout>
        </v-contaier>
      </v-main>
      <v-footer
        app
        dark
        absolute
        tile
        color="transparent"
      >
        <div class="footer">
          © 2020 hikidemono all rights reserved.
        </div>
      </v-footer>
    </div>
  </v-app>
</template>

<style>
  .v-application{
    font-family: "Century Gothic","Meiryo","Helvetica Neue","	Hiragino Sans","Helvetica","Arial",sans-serif !important;
  }
  .bg {
    background-image: url("~@/assets/forgetmenot.jpg");
    background-size: cover;
    background-attachment: fixed;
    background-position: center;
    width: 100%;
    height: 100%;
  }
  .v-enter-active, .v-leave-active {
    transition: opacity .5s;
  }
  .v-enter, .v-leave-to {
    opacity: 10;
  }
  .footer {
    margin: auto;
  }
  h3 {
    font-weight: normal;
    text-decoration: underline;
  }
  pre {
    font-family: "Century Gothic","Meiryo","Helvetica Neue","	Hiragino Sans","Helvetica","Arial",sans-serif !important;
  }
  .centering {
    text-align: center;
  }
  .skeleton{
    opacity:0.9;
  }
  .lyrics {
    text-align: left;
    line-height: 1.2em;
    font-size: small;
  }
  .track-credit {
    text-align: right;
    line-height: 1.2em;
    font-size: x-small;
  }
</style>

<script>
import VuetifyAudio from 'vuetify-audio';

export default {
  name: 'App',
  data: () => ({
    mp3path: "https://github.com/hikidemono/online2021/blob/main/tmp/forget_inst.mp3?raw=true"
  }),
  components: {
    'vuetify-audio': VuetifyAudio
  },
  methods: {
    audioFinish () {
      console.log('You see this means audio finish.');
    }
  },
};
</script>
