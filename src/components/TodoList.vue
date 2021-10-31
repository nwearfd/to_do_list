<template>
    <section>
        <transition-group name="list" tag="ul">
            <li v-for="(todoItem, index) in propsdata" v-bind:key="todoItem" class="shadow">
                <font-awesome-icon class="checkBth" icon="check" aria-hidden="true"></font-awesome-icon>
                {{todoItem}}
                <span class="removeBtn" type="button" @click="removeTodo(todoItem, index)">
                    <font-awesome-icon icon="trash" aria-hidden="true"></font-awesome-icon>
                </span>
            </li>
        </transition-group>
    </section>
</template>

<script>
    export default{
        props: ["propsdata"],
        methods: {
            removeTodo(todoItem, index) {
                this.$emit("removeTodo", todoItem, index);
            }
        },
    };
</script>

<style scoped>

</style>