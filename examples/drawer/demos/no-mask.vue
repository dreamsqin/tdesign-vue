<template>
  <div>
    <t-drawer :visible="visible" @close="handleClose" :showOverlay="false" :onConfirm="handleClose" header="抽屉标题">
      <p>抽屉的内容</p>
    </t-drawer>

    <t-button variant="outline" @click="handleClick">打开抽屉</t-button>
  </div>
</template>

<script>
import Vue from 'vue';

export default Vue.extend({
  data() {
    return {
      visible: false,
    };
  },
  methods: {
    setVisible(state) {
      this.visible = state;
    },
    handleClick() {
      this.setVisible(true);
    },
    handleClose() {
      this.setVisible(false);
    },
  },
});
</script>
