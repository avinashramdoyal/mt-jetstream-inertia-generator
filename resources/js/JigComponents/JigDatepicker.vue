<template>
    <flat-pickr :config="config" class="border-gray-100 bg-gray-50 disabled:opacity-25 focus:border-indigo-300 focus:ring focus:ring-indigo-200 focus:ring-opacity-50 rounded-md shadow-sm" id="next_action_scheduled_date" v-model="modelValue" @input="$emit('update:modelValue', $event.target.value)" ref="input"></flat-pickr>
</template>

<script>
import flatPickr from "vue-flatpickr-component";
import 'flatpickr/dist/flatpickr.css';
export default {
    name: "JigDatepicker",
    components: {flatPickr},
    props: {
        'modelValue': {},
        'config': {
            type: Object,
            default: () => {return {}}
        },
    },
    emits: ['update:modelValue'],
}
</script>

<style scoped>

</style>
