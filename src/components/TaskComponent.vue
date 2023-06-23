<script setup>
const props = defineProps({
    name:{
        type:String,
        default:'No tengo nombre'
    },
    index:{
        type:Number
    }
})
const emit = defineEmits([
    'deleteTask'
])
const deleteTask = (index) => {
    emit('deleteTask', index)
}
</script>


<template>
  

        <div class="flex justify-between px-4 py-2 bg-gray-200 rounded">
           
            {{ props.name }}
            <span class="inline-block px-2 bg-red-600 hover:bg-red-800 text-white cursor-pointer"
             @click="deleteTask(props.index)">
                X
            </span>
        </div>
</template>