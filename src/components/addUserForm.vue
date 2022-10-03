<template>
    <form @submit.prevent="enviar">
        <div class="formUser">
            <label for="addUser">First Name </label>
            <input type="text" name="addUser" id="addUser" v-model="addUser" />
            <div class="errors">{{addUser}}</div>
        </div>

        <div class="formUser">
            <label for="">Last Name </label>
            <input type="text" name="" id="lasttName" />
        </div>

        <div class="formUser">
            <label for="">Email </label>
            <input type="text" id="email"  />
        </div>
        <button type="submit" class="btn btn-primary">Submeter</button>
    </form>
</template>

<script>
export default {
   name: 'addUserForm',
   data() {
    return {
        addUser:''
        }
    },
}    
</script>

<style scoped>
.formUser{
    padding: 15px;
}
</style>