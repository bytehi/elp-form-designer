<script setup>
defineProps({
	control: Object,
	model: Object,
})
</script>

<template>
	<el-input v-if="model" :type="control.props.type" :show-password="control.props.showPassword"
		v-model="model[control.id]" :placeholder="control.props.placeholder" :clearable="control.props.clearable"
		:disabled="control.props.disabled" :readonly="control.props.readonly" :show-word-limit="control.props.showWordLimit"
		:maxlength="control.props.showWordLimit ? control.props.maxlength : undefined"></el-input>
	<el-input v-else :type="control.props.type" :show-password="control.props.showPassword"
		v-model="control.props.defaultValue" :placeholder="control.props.placeholder" :clearable="control.props.clearable"
		:disabled="control.props.disabled" :readonly="control.props.readonly" :show-word-limit="control.props.showWordLimit"
		:maxlength="control.props.showWordLimit ? control.props.maxlength : undefined"></el-input>
</template>
