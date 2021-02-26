<template>
    <div class="container">
        <input type="text" placeholder="enter a color..." v-model="colorInput">
        <button class="validate" @click="changeClass">OK</button>
        <h1 :class="classname">Bienvenue</h1>
    </div>
    
</template>

<script>
export default {
    name:'Welcome',
    data: function(){
        return {
            classname:"title--",
            colorInput: "",
            colorList: ["red", "green", "blue"]
        }
    },
    methods:{
        changeClass: function() {
            if(this.colorList.includes(this.colorInput)){
                this.classname = "title--"+this.colorInput;
            }
            else{
                this.classname = "title";
            }
        }
    }
}
</script>

<style lang="scss">
    .container{
        margin-top: 30px;
    }

    .validate{
        margin-left: 20px;
    }

    .title{
        color: black;

        &--red{
            color: red;
        }

        &--green{
            color: green;
        }

        &--blue{
            color: blue;
        }
    }


</style>