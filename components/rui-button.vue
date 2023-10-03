<script setup lang="ts">
type Size = "tiny" | "small" | "default" | "medium" | "large";
type Type = "default" | "primary" | "dashed" | "text" | "link";

type Props = {
  color?: string;
  size?: Size;
  type?: Type;
};

const Types: Record<Type, string> = {
  default: "",
  primary: "",
  dashed: "",
  text: "",
  link: "",
};

const Sizes: Record<Size, string> = {
  default: "",
  tiny: "",
  small: "",
  medium: "",
  large: "",
};

const props = defineProps<Props>();
</script>

<template>
  <button :class="[]">
    <slot />
  </button>
</template>
