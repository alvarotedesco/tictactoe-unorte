<template>
  <div class="flex justify-center items-center">
    <qrcode-vue :value="value" :size="size" level="H"/>
  </div>
</template>
<script>
import QrcodeVue from 'qrcode.vue'

export default {
  components: {
    QrcodeVue,
  },

  props: {
    value: {type: String, required: true},
    size: {type: Number, default: 200},
  },
}
</script>