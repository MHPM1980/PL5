<template>
    <form @submit.prevent="onSubmitHandler">
        <div class="formUser">
            <label for="addUser">First Name </label>
            <input type="text" name="addUser" id="firstName" v-model="addUser.firstName" />
            <div class="errors">{{addUser.user}}</div>
        </div>

        <div class="formUser">
            <label for="">Last Name </label>
            <input type="text" name="addUser" id="lastName" v-model="addUser.lastName" />
        </div>

        <div class="formUser">
            <label for="">Email </label>
            <input type="text" nme="addUser" id="email" v-model="addUser.email"  />
        </div>
        <button type="submit" class="btn btn-primary">Submeter</button>
    </form>
</template>

<script>
import addUser from '../models/addUser';

export default {
   name: 'addUserForm',
   data() {
    return {
        addUser : new addUser()
        }
    },
    methods:{
        onSubmitHandler(){
            console.log(this.addUser.firstName)
        }
    }
}    
</script>

<style scoped>
.formUser{
    padding: 15px;
}
</style>