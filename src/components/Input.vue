<script>
    export default {
        props: {
            changeAmount: {
                type: Function,
                required: true
            },
            convert: {
                type: Function,
                required: true
            },
            favourite: {
                type: Function,
                required: true
            }
        }
    }
</script>

<template>
    <input min="0" type="number" @input="changeAmount($event.target.value)" placeholder="Enter the number">
    <br><button @click="convert()">Convert</button><br>
    <br><button @click="favourite()">Add in Favourites</button><br>
</template>

<style scoped>
    input {
        position: relative;
        outline: none;
        width: 550px;
        border-radius: 3px;
        border: 0;
        padding: 10px 15px;
        background-color: antiquewhite;
        color: black;
        font-size: 1.2em;
        margin-bottom: 40px;
    }

    button {
        position: relative;
        padding: 15px 20px;
        color: aliceblue;
        text-transform: uppercase;
        cursor: pointer;
        background: #1a032d;
        border: none;
        border-radius: 8px;
    }

    button:nth-of-type(2) {
        margin-bottom: 20px;
    }
</style>