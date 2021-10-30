<template>
    <div class="inputBox shadow">
        <input type="text" v-model="newTodoitem" placeholder="할 일을 적으세요" v-on:keyup.enter="addTodo" />
        <span class="addContainer" v-on:click="addTodo">
            <font-awesome-icon class="addBtn" icon="plus" aria-hidden="true" />
        </span>

        <modal v-if="showModal" @close="showModal = false">
            <h3 slot="header">경고</h3>
            <span slot="body">할 일 선택</span>
            <button slot="footer" @click="showModal = false">닫기</button>
        </modal>
    </div>
</template>

<script>
    export default{};
</script>

<style scoped>

</style>