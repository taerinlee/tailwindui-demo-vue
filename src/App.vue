<template>
  <div id="app">
    <the-nav class="mb-6"/>
    <router-view/>
  </div>
</template>

<script>
import theNav from '@/components/TheNav.vue'

export default {
  components: {
    theNav
  }
}
</script>