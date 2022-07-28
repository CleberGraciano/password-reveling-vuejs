<template lang="">
    <div>
        Password
       <input 
            :type="inputType" 
            :value="value"
            :id="id" 
            :placeholder="placeholder"
            @input="$emit('input', $event.target.value)">
            <div @click="tooglePassword">
                <img v-if="isPassword" src="../assets/olho_fechado.png" height="30"/>
                <img v-else src="../assets/olho_aberto.png" height="30"/>
            </div>  
    </div>
</template>
<script>
export default {
    name: 'PasswordReveling',

    props: {
        value: {
            type: String,
            default: '',
        },
        id: {
            type: String,
            default: '',
        },
        placeholder: {
            type: String,
            default: '',
        }
    },

    data() {
        return {
            inputType: 'password'
        };
    },

    computed: {
        isPassword(){
            return this.inputType === 'password'
        },

    },

    methods: {
        tooglePassword(){
            this.inputType = this.isPassword ? 'text' : 'password'
        }
    },

}
</script>
<style lang="">
    
</style>