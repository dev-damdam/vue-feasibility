<template>
  <div class="markdown-sample-wrapper">
    <textarea v-model="markdown" />
    <span>마크다운 결과</span>
    <div v-html="markdownRes" />
  </div>
</template>

<script>
import { marked } from "marked";
export default {
  name: "markdown-sample",
  data() {
    return {
      markdown: "",
    };
  },
  computed: {
    markdownRes: {
      set(value) {
        this.markdown = value;
      },
      get() {
        return marked(this.markdown, {
          sanitize: true,
        });
      },
    },
  },
  mounted() {},
};
</script>
<style scoped lang="scss">
.markdown-sample-wrapper {
  width: 100%;
  display: flex;
  flex-direction: column;

  gap: 10px;
}
</style>
