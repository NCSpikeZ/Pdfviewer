<template>
  <div>
    <iframe height="100%" width="100%" :src="getFilePath"></iframe>
  </div>
</template>

<script>
export default {
  name: 'PDFJSViewer',
  props: {
    fileName: String,
    path: String,
  },
  computed: {
    getFilePath() {
    /* @type {URI|String} url */
      console.log({ SRC: this.fileName })
      console.log({ PATH: this.path })
      const timestamp = new Date().getTime();
      const url = `${this.path}?file=${this.fileName}&v=${timestamp}#page=1`;
      console.log({ URL: url })
      return encodeURI(url);
    }
  },
};
</script>

<style scoped>
div {
  margin-top: -10px;
  width: 100%;
  height: 100vh;
  min-width: 400px;
}
</style>
