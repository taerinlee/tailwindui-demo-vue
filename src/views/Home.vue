<template>
  <div id="home">
    <div v-if="!loading">
      <temp-card 
        class="ml-2 mr-2 mt-4" 
        v-for="index in 3" :key="index"
      />
    </div>
    <div v-else>
      <temp-card-skeleton 
        class="ml-2 mr-2 mt-4" 
        v-for="index in 3" :key="index"
      />
    </div>
  </div>
</template>

<script>
import tempCard from '@/components/TempCard.vue'
import tempCardSkeleton from '@/components/TempCardSkeleton.vue'

export default {
  data() {
    return {
      loading: true
    }
  },
  components: {
    tempCard,
    tempCardSkeleton
  },
  mounted() {
      this.init()
  },
  methods: {
      async init() {
          setTimeout(() => {
            this.loading = false
          }, 4000)
      }
  }
}
</script>