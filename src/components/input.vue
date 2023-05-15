<template>
  <input
    :type="type"
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"
    class="bg-[#ececef] w-[400px] p-[15px] text-[#131313] font-medium text-[16px] rounded-lg outline-none border-[1px]"
  />
</template>

<script setup>
import { defineProps } from "vue";
const props = defineProps(["modelValue", "type", "allstyle"]);
</script>
