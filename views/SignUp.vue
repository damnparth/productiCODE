<template>
     
     <form @submit.prevent="handleSignUp">
        <h1> Sign Up</h1>
        <label for="">email</label>
        <input type="email" required v-model="email">
        <label for="">password</label>
        <input type="password" requried v-model="password">
        <label for="">confirm password</label>
        <input type="password" required v-model="confirm">
        <br>

        
        
        <div v-if="passwordError" class="error">{{ passwordError }}</div>


        

        <br>
        <br>
        <br>
       <button> <router-link to="/Login" style="color: white;text-decoration: none;">submit</router-link></button>
        <br>
        <br>
        <br>
    



        
        

       
    </form>
    
  
</template>

<script>
export default{
    data(){
        return{
            email:'',            
            password:'',
            confirm:'',
            passwordError:''
        }
    },
    methods:{
        handleSignUp(){
            this.passwordError=this.password == this.confirm ? '': 'passwords do not match'
            if(this.passwordError){
                console.log("email: "+this.email);
                console.log("password: "+this.password);

            }

        
        }


    }
    

    }



</script>



<style>
form{
    max-width: 420px;
    margin: 30px auto;
    background:#B5C0D0;
    text-align: left;
    padding:40px;
    border-radius:20px;
    width: 400px;
    
    
    


}
label{
    display:flex;
    justify-content: center;
    align-items:center;
    color: black;
    display:inline block;
    margin:25px 0 15px;
    text-transform:uppercase;
    letter-spacing: 1px;
    font-weight:bold;
    
    



}
input{
    display:block;
    padding:10px 6px;
    width:300px;
    box-sizing:border-box;
    border:none;
    border-bottom: 1px  solid #ddd;
    color:#474545;
    border-radius: 10px;
    margin: auto;



}
h1{
    display:flex;
    justify-content: center;
    align-items: center;
    color: #2D3250;
}
button{
    display: flex;
    justify-content: center;
    align-items:center;
    border-radius:20px;
    height:50px;
    width:200px;
    margin:auto;
    padding:0;
    border:none;
    cursor:pointer;
    background-color: #2D3250;
    color:white;
    outline: 10cap;
    box-shadow: black;


}
body{
    background-color:#F5E8DD;
}
.error{
    display:flex;
    justify-content: center;
    align-items:center;
    color:red;
    
}




</style>