<template>
    <div id="app" class="container">
        <h1>My Counter</h1>
        <hr>
        <p class="count">{{ count }}</p>
        <Btn class="blue" @handleCount="doCount('up')">Up</Btn>
        <Btn class="green" @handleCount="doCount('down')">Down</Btn>
    </div>
</template>

<script>
import Btn from "./components/Btn"

export default {
    components: {
        Btn
    },
    data () {
        return {
            count: 0,
        }
    },
    methods: {
        doCount(countType) {
            this.count += (countType === "up" ? 1 : -1)
        },
    },
}
</script>

<style scope>
.container {
    text-align: center;
    width: 500px;
}

.count {
    font-size: 35px;
    margin: 10px;
}
</style>
