<script>
export default {
    data() {
        return {
            cardArray:"",
        }
    },
    methods:{
        callApi:function () {
            
        },
        callApiTV:function () {
            
        },
    }
}
</script>
<template>
    <header>
        <div class="title">
            <div>
                <h1>Boolflix</h1>
            </div>
        </div>
        <div>
            <div class="search-bar">
                <input v-on:keyup.enter="$emit('callApi');$emit('callApiTv')" v-model="cardArray" @keyup="printArray" @change="$emit('select',cardArray)"  placeholder="cerca qui il tuo film" >
            </div>
        </div>
    </header>
    <AppMain />
</template>
<style lang="scss">
    *{
        align-items: center;
        padding: 2px;
    }
    header{
        background-color: rgba(0, 0, 0, 0.897);
        height: 100px;
        display: flex;
        justify-content: space-around;

        h1{
            color: red;
            font-size: 80px;
        }

        .search-bar input{
            width: 500px;
            height: 40px;
            
        }
    }
  
</style>