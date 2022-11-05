<template>
    <p>The User is {{age}}  years old</p>
    <button type="button" @click="onClickAge">Update Age</button>
</template>

<script>
export default{
    name : 'User',
    props:{
        age:{
            type :Number,
            required : true,
            validator(value){
                return value < 130
            }
        }
    },
    emits:['age-change'],
    methods:{
        onClickAge(){
            this.$emit('age-change',3)
        }
    }
}
</script>

<style lang="scss" scoped>

</style>