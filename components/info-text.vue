<template>
  <v-tooltip right>
    <template v-slot:activator="{ on }">
      <span class="info-text" v-on="on"><slot /></span>
    </template>
    <span>{{ tooltip }}</span>
  </v-tooltip>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'nuxt-property-decorator'

@Component
class InfoText extends Vue {
  @Prop({ default: '' }) tooltip!: string;
}

export default InfoText
</script>

<style lang="scss" scoped>
.info-text {
  border-bottom: 1px dotted aqua;
  display: inline-block;
}

p {
  text-align: left;
}
</style>
