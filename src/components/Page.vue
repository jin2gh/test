<template>
  <main class="page">
    <div class="content">
      <Content class="docs-en" slot-key="en" />
      <Content class="docs-zh" slot-key="zh" />
    </div>
    <PageEdit />

    <PageNav v-bind="{ sidebarItems }" />
  </main>
</template>

<script>
import PageEdit from '@theme/components/PageEdit.vue'
import PageNav from '@theme/components/PageNav.vue'

export default {
  components: {
    PageEdit,
    PageNav
  },
  props: ['sidebarItems']
}
</script>

<style lang="stylus">
@import './Page.styl'
</style>
