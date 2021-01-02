<template>
  <v-container>
    <div v-if="requireClick" @click="clicked = true">
      <h2 class="clickable">
        <code>> {{ name }}</code>
      </h2>
    </div>
    <div v-else>
      <h2>
        <code>> {{ name }}</code>
      </h2>
    </div>

    <div v-show="clicked || !requireClick">
      <h2>{{ result }}</h2>
    </div>
  </v-container>
</template>

<script>
export default {
  props: {
    name: String,
    result: String,
    requireClick: Boolean,
  },
  data() {
    return {
      clicked: false,
    };
  },
};
</script>

<style scoped>
.clickable {
  cursor: pointer;
}

.clickable:hover {
  color: gold;
}
</style>
