<template>
    <div>
        <p>Counter: {{ counterStore.count }}</p>
        <button @click="add">increment</button>
        <button @click="minus">dicrement</button>

    </div>
</template>

<script>
import { useFriendStore } from '@/stores/counter.js'

export default defineComponent({
    setup() {
        const counterStore = useFriendStore()
        return { counterStore }
    },
    methods:{
        add(){
            this.counterStore.increment()
        },
        minus(){
            this.counterStore.dicrement()
        }
    }
})
</script>