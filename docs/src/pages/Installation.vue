<template>
  <div>
    <div class="center-c">
      <a href="https://nodei.co/npm/vue2-dropzone/">
        <img src="https://nodei.co/npm/vue2-dropzone.png?downloads=true&downloadRank=true&stars=true">
      </a>
    </div><br>
    <hr>
    <h1>Installation & Usage</h1>
    <pre v-pre data-lang="bash"><code class="lang-bash">npm install vue2-dropzone</code></pre>
    <pre data-lang="js"><code class="lang-js">{{ example }}</code></pre>
    <h2>Alternate installation</h2>
    <p>If required you clone the Git repository of this library and build it.</p>
    <pre v-pre data-lang="bash"><code class="lang-bash">git clone https://github.com/rowanwins/vue-dropzone.git
  cd vue-dropzone
  npm install
  npm run build</code></pre>
    <edit-doc :link="'Installation.vue'"></edit-doc>
  </div>
</template>
<script>
import editDoc from '../components/DocEditLink.vue';
var e = `
<vue-dropzone ref="myVueDropzone" id="dropzone" :options="dropzoneOptions"></vue-dropzone>
import vue2Dropzone from 'vue2-dropzone'
import 'vue2-dropzone/dist/vue2Dropzone.min.css'
export default {
  name: 'app',
  components: {
    vueDropzone: vue2Dropzone
  },
  data: function () {
    return {
      dropzoneOptions: {
          url: 'https://httpbin.org/post',
          thumbnailWidth: 150,
          maxFilesize: 0.5,
          headers: { "My-Awesome-Header": "header value" }
      }
    }
  }
}`
export default {
  data() {
    return {
      ok: true,
      example: e,
    }
  },
  components: {
    'edit-doc': editDoc
  }
}
</script>
<style>
.center-c {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 10px;
}
</style>
