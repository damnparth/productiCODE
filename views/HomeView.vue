<template>
  <div class="homepage">

  <div class="navbar">
    <div class="container-fluid">
      <h2>ProductiCode</h2>

    </div>
    <div class="navbar-left">
      <button class="login"><router-link to="/Profile" style="color:white; text-decoration: none;font-weight: bold;">Profile</router-link></button>

      
      
      <br>
      <br>
    </div>
    <div class="navbar-right">
      
      <button class="login"> <router-link  to="/SignUp" style="color:white; text-decoration: none; font-weight: bold;">SignUp</router-link></button>

      <button class="login"><router-link to="/Login" style="color:white; text-decoration: none;font-weight: bold;">Login</router-link></button>
     
    </div>
    

  </div>
  <img src="../assets/vue-img.jpeg" alt="">
  
  <div class="dashboard">
    <h1>Dashboard</h1>
    <h4>Important Tip: Studying computer science in college means juggling coursework, side projects, internships, and more. Use this template to help you get organized and stay on top of your school to-dos.</h4>
    <br>
  </div> 
  <br>
  
  <div class="container">
    <div class="grid1">
      <div class="quick-access"><h1>Quick Access</h1>
        <div class="quick-access-pill"><h4>GitHub</h4> <a href="https://github.com/" style="color: white;">www.github.com</a></div>
        <div class="quick-access-pill"><h4>LinkedIn</h4> <a href="https://www.linkedin.com/" style="color:white">www.linkedin.com</a></div>
        <div class="quick-access-pill"><h4>LeetCode</h4><a href="https://leetcode.com/" style="color:white;">www.leetcode.com</a></div>


      </div>
      <div class="habit-tracker"><h1>To Do List</h1>  <input type="ToDoList" required v-model="ToDoList" @keyup="addList" > 
      <div v-for="skill in skills" :key="skill"> {{ skill }}
      </div>
    </div>

      <div class="clock"><h1>calender</h1>
        
      </div>
    
      
    </div>
    <br>

    <div class="internship">
      <h1>Summer internship</h1>
    </div>
    <br>
    <h1>Courses</h1>

    <div class="grid2">
     
      <br>
      <div class="maths4"><h3>  Mathematics 4</h3> <div class="moodle">  <a href="" style="color: white; text-align: center;">Notes</a>   </div>  <br> <div class="moodle" style="text-decoration: underline;color: white;"> <a href="https://youtu.be/T4bE0K14QLU?si=pGGb6ZnlmJNbnWT7" style="color: white;" >Resources</a></div></div>
      <div class="os"><h3>Operating Systems</h3> <div class="moodle">  <a href="" style="color: white; text-align: center;">Notes</a>   </div>  <br> <div class="moodle" style="text-decoration: underline;color: white;"> <a href="https://youtu.be/bkSWJJZNgf8?si=-KqZ83AtAxwF3_-G" style="color: white;">Resources</a></div></div>
      <div class="dbms"><h3>DBMS</h3><div class="moodle">  <a href="" style="color: white; text-align: center;">Notes</a>   </div>  <br> <div class="moodle" style="text-decoration: underline;color: white;">  <a href="https://youtu.be/kBdlM6hNDAE?si=SfJBcYnaZntcuYTO" style="color: white;"> Resources</a></div></div>
      <div class="aoa"><h3>Analysis of Algorithms</h3><div class="moodle">  <a href="" style="color: white; text-align: center;">Notes</a>   </div>  <br> <div class="moodle" style="text-decoration: underline;color: white;">  <a href="https://youtu.be/u8JZ9gU5o4g?si=Y8TQlLCvE5btpXxT" style="color: white;">Resources</a></div></div>
      <div class="mp"><h3>Microprocessor</h3><div class="moodle">  <a href="https://youtu.be/nVumL1rZ768?si=zngsGC_3HanlYnyB" style="color: white; text-align: center;">Notes</a>   </div>  <br> <div class="moodle" style="text-decoration: underline;color: white;"> <a href="https://youtu.be/nVumL1rZ768?si=zngsGC_3HanlYnyB" style="color: white;">Resources</a></div></div>
      


      

      
      
    </div>
    <br>
    


  </div>
  
  

  
 
  


  </div>
</template>

<script>


export default {
  name: 'HomeView',
  components: {
  ToDoList:'',
  skills:[],

  
    
  },
  methods:{
    addList(e){
      
      this.ToDoList=''

    }

  }
}

</script>


<style scoped>


*{
  
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}

.navbar{
  display:flex;
  background-color: #EED3D9;
  padding:10px;
  text-align: right;
}
.navbar-left{
  display:flex;
  margin:auto;
  justify-content: left ;
  align-items: left;
  cursor:pointer;
  
}
.navbar-right{
  display:flex;
  cursor:pointer;

  
  
}
img{
  display: block;
    object-fit: cover;
    border-radius: 0px;
    width: 100%;
    height: 30vh;
    opacity: 1;
    object-position: center;
    height: 250px;
}
.dashboard{
  border-radius:15px;
  background-color: #CCD3CA;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
margin:auto;
margin-left:20px;
margin-right:20px;
}
.grid1{
  display:flex;
  justify-content: space-evenly;
  height:370px;
  

  


}
.quick-access{
  border-radius: 15px;
  width: 300px;
  
  background-color:#CCD3CA

}
.habit-tracker{
  border-radius:15px;
  width:300px;
  
  background-color: #CCD3CA;

}
.clock{
  border-radius:15px;
  width:300px;
  
  
  background-color: #CCD3CA;

}
.internship{
  background-color: #CCD3CA;
  width:500px;
  border-radius:15px;
  margin:auto;
  height:150px;
  


  
}
.grid2{
  display:flex;
  justify-content: space-evenly;
  height:200px;
  
  
  

}
.maths4{
  border-radius: 15px;
  background-color: #CCD3CA;
  width: 200px;

}
.mp{
  border-radius: 15px;
  background-color: #CCD3CA;

  width:200px;
}
.os{
  border-radius: 15px;
  background-color: #CCD3CA;
  width:200px;

}
.dbms{
  border-radius: 15px;
  background-color: #CCD3CA;
  width:200px;

}
.aoa{
  border-radius: 15px;
  background-color: #CCD3CA;
  width: 220px;
  
}
router-link{
  color:black;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}
img{
  height: 300px;

}
input[type='ToDoList']{
  background-color: #EED3D9;
  width: 200px;
height: 30px;

}
.login{
  width: 100px;
  color:white;
  justify-content: space-evenly;
  margin:5%;
  

}
.quick-access-pill{
  border-radius:15px;
  height: 70px;
  background-color: #2D3250;
  color: white;
  margin-left: 10%;
  text-align: center;
  justify-content: center;
  
  margin-right: 10%;
  

  
 

}
.moodle{
  border-radius: 15px;
  height: 45px;
  width: 180px;
  background-color: #2D3250;
  cursor: pointer;
  margin-left: 10%;
  margin-right: 10%;
  margin: auto;
  
}





</style>
