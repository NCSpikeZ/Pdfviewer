<template>
  <div id="app">
    <PDFJSViewer :path="path" :fileName="name" />
  </div>
</template>

<script>
import PDFJSViewer from './components/PDFJSViewer';

export default {
  name: 'app',
  components: {
    PDFJSViewer,
  },
  data() {
    return {
      name: '50MB-TESTFILE.ORG.pdf', // change which pdf file loads
      path: 'lib/pdfjs-4.0.379-dist/web/viewer.html', // path of the PDF.js viewer.html
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
