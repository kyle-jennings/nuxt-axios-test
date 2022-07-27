<template>
  <Tutorial />
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'IndexPage',
  async beforeMount () {
  try {
    const results = await this.api('me');
    console.log(results);
  } catch (e) {
    console.log(e);
  }
}
})
</script>
