<template>
  <div class="wrap"></div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  computed: {
    ...mapGetters('test', ['txt']),
  },
  methods: {
    onSubmit(value) {
      this.$store.dispatch('test/saveTxt', { text: value })
    },
  },
}
</script>

<style lang="scss" scoped>
.wrap {
  max-width: 40rem;
  margin: 0 auto;
}

.txt {
  margin: 10rem 0 2rem;
  text-align: center;
}
</style>
