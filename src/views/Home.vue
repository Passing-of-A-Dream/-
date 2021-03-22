<template>
  <div>
    <search :cont="Gen"></search>
    <Boom :cont="Gen"></Boom>
  </div>
</template>

<script>
// @ is an alias to /src
import Boom from './Boom/Boom'
import Search from './Search/Search'
export default {
  data() {
    return {
      Gen: []
    }
  },
  name: 'Home',
  components: {
    Boom,
    Search
  }
}
</script>

<style>
</style>