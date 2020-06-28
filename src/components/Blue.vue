<template>
    <div>
        <slot name="title"></slot>
        <slot name="subtitle"></slot>
    </div>
</template>

<script>

</script>

<style scoped>
    div {
        border: 1px solid blue;
        background-color: lightblue;
        padding: 30px;
        margin: 20px auto;
        text-align: center
    }

    h1, h3 {
        color: #fff;
    }
</style>