<script setup>
defineProps({
    title: {
        type: String,
        required: true
    },
    visible: {
        type:Boolean,
        required: true
    },
})
defineEmits(['update:visible'])
</script>

<template>
    <div class="panel-wrap">
       <div class="panel">
        <div>
            <button class="btn error--outline">Close
         </button>
         <h2>{{ tittle }}></h2>
        </div>
        <slot name="content"></slot>
       </div> 

    </div>
</template>



<style lang="scss" scoped>
.panel{
    position: absolute;
}
</style>