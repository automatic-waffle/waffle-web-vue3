<script>
import { NConfigProvider, NGlobalStyle } from "naive-ui";
import { defineComponent } from "vue";
import { darkTheme } from "naive-ui";

/**
 * @type import('naive-ui').GlobalThemeOverrides
 */
const themeOverrides = {
  common: {
    fontFamily: "JetbrainsMono, sans-serif",
    fontFamilyMono: "JetbrainsMono, sans-serif",
  },
};

export default defineComponent({
  themeOverrides,

  components: {
    NConfigProvider,
    NGlobalStyle,
  },
  setup() {
    return {
      darkTheme,
    };
  },
});
</script>

<template>
  <n-config-provider :theme-overrides="$options.themeOverrides">
    <n-global-style />
    <slot />
  </n-config-provider>
</template>
