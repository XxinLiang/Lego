<template>
    <input
        type="text"
        class="input"
        :id="id"
        :disabled="disabled"
        :placeholder="placeholder"
        :style="{
            width: width + 'px',
            height: height + 'px'
        }"
    />
</template>

<script>
    export default {
        name: 'LgInput',
        props: {
            id: String,
            disabled: Boolean,
            width: {
                type: Number,
                default: 260
            },
            height: {
                type: Number,
                default: 30
            },
            placeholder: String
        }
    }
</script>

<style lang="scss" scoped>
@import "../../common.scss";

.input {
    display: inline-block;
    box-sizing: border-box;
    padding: 0 9px;
    color: #333;
    font-size: 12px;
    border: 1px solid $border;
    transition: all .15s ease;
    outline: none;
    &:focus {
        border-color: $main;
    }
    &:disabled {
        background-color: #f5f5f5;
        color: #b7b7b7;
    }
}
</style>
