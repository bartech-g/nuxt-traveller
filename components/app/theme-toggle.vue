<script setup lang="ts">
const colorMode = useColorMode();

const isDark = computed({
  get: () => colorMode.value === "dark",
  set: (value) => {
    colorMode.preference = value ? "dark" : "light";
  },
});
</script>

<template>
  <div class="mx-2">
    <label class="swap swap-rotate">
      <!-- this hidden checkbox controls the state -->
      <input v-model="isDark" type="checkbox">

      <!-- sun icon -->
      <Icon
        name="tabler:sun"
        size="24"
        class="swap-on fill-current w-10 h-10"
      />
      <!-- moon icon -->
      <Icon
        name="tabler:moon"
        size="24"
        class="swap-off fill-current w-10 h-10"
      />

    </label>
  </div>
</template>

<style scoped></style>
