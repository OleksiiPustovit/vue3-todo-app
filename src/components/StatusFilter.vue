<script>
  export default {
    props: {
      modelValue: String,
    },
    emits: ['update:modelValue'],
  };
</script>

<template>
  <nav class="filter" data-cy="Filter">
    <a
      data-cy="FilterLinkAll"
      href="#/"
      class="filter__link"
      :class="{ selected: modelValue === 'all'}"
      @click="$emit('update:modelValue', 'all')"
    >
      All
    </a>

    <a
      data-cy="FilterLinkActive"
      href="#/active"
      class="filter__link"
      :class="{ selected: modelValue === 'active'}"
      @click="$emit('update:modelValue', 'active')"
    >
      Active
    </a>
    <a
      data-cy="FilterLinkCompleted"
      href="#/completed"
      class="filter__link"
      :class="{ selected: modelValue === 'completed'}"
      @click="$emit('update:modelValue', 'completed')"
    >
      Completed
    </a>
  </nav>
</template>

<style></style>