<script setup>
defineProps({
	control: Object,
	model: Object,
})
</script>

<template>
	<div>{{ model[control.id] }} </div>
</template>
