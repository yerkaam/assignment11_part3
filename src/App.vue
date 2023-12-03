<template>
     <div>
        <h1>Hello world</h1>
        <div class="flex" style="margin-left: -190px;">
            <p>Type your name:</p>
        <input @input="addText" type="text" id="input">
        <button @click="deleteText">Delete</button>
        </div>
        <div  class="">
        <p id="text">Your name:</p>
        </div>
     </div>
</template>
<script>

export default{
    data(){
        return{
            text:'Your name:'
        }
    },
    methods:{
        addText(){
            let te = this.text;
            te += document.getElementById('input').value.trim()
            let t = document.getElementById('text')
            t.textContent = te;
        },
        deleteText(){
         document.getElementById('input').value = '';
 document.getElementById('text').textContent =''
            
    }
    }
    
}
</script>
<style>
body{
    background-color: aqua;
}
#app{
    width: 500px;
    margin: 0 auto;
}
.flex{
    display: flex;
    align-items: center;
    justify-content: center;
}
input{
    background-color: transparent;
    border: 1px solid black;
    height: fit-content;
}
</style>