<template>
    <div>
            <h1>Name</h1>

            <p class="Error">{{Error}}</p>
            
            <v-text-field class="vInput"
                v-model="Name"
                label="Full Name"
                placeholder="">
            </v-text-field>
            <v-text-field class="vInput"
                v-model="Id"
                label="Id"
                placeholder="">
            </v-text-field>
            
            <v-btn @click="Accept()">Accept</v-btn>
    </div>
    
</template>

<script>
export default {
    name: 'Step1',
    data: function(){
        return{
            Name: "",
            Id: "",
            Error: ""
        }
    },
    methods:{
        Accept: function(){
            if((this.name == "")||(this.Id == ""))
                this.Error = "Enter first or last name"
            else{
                this.Error = "",
                this.$emit('Accept',this.Id, this.name)
            }
        }
        
    }
}
</script>

<style scoped>
.vInput{
    width: 50%;
}
.Error{
    color: rgb(255, 68, 68);
}
</style>