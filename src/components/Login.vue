<template lang="">
    <div >
        <form class="login">
            <input type="text" v-model="userData.username">
            <input type="password" v-model="userData.password">
            <button @click="login">Login</button>
        </form>
    </div>
</template>

<script>
export default {
    props:{
        userData:{
            username:'',
            password:''
        }
        
    },
    methods:{
        login(e){
            e.preventDefault()
            const user={username:this.username,password:this.password}
            this.$emit('clickedLogin')
        }
    }
}
</script>

<style scoped>

button {
    background-color: #18E084;
    color: #ffffff;
    padding: auto 20px;
    border-radius: 20px;
    cursor: pointer;
    width: 250px;
    left: 150px;
}

form { 
    margin: auto;
    vertical-align: middle;
    width:350px;
}

#login-box {
    padding: 40px 0;
}

input {
    width: 100%;
    padding: 12px 20px;
    margin: 8px 0;
    display: inline-block;
    border: 1px solid #ccc;
    border-radius: 6px;
}

</style>