<template>
    <div id="app">
        <vueLogoQrcode ref="qrcode"
                       :content="content"
                       :logoSrc="logoSrc"
                       :width="width"
                       :autoGen="true"
                       @click.native="downloadImage"></vueLogoQrcode>
    </div>
</template>

<script>
import vueLogoQrcode from './lib';
import logoSrc from './assets/logo.png'


export default {
    name: 'app',
    components: { vueLogoQrcode },
    data() {
        return {
            content: "shaojiasong",
            width: 200,
            logoSrc,
        }
    },
    methods: {
        downloadImage() {
            this.$refs.qrcode.genQrCodeImageDownload();
        }
    },
  created(){
      console.log(1)

  }
}
</script>

<style lang="scss">
</style>
