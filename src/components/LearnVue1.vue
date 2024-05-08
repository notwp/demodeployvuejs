<template lang="">
    <div class="my-profile">
        <p>My name is{{ name}}</p>
        <p>i'm age {{age}} year old.</p>
        <p>My position is {{position}}</p>
        <p>myFavLang</p>
        <p v-for="myFavLang in myFavLang" ::key="myFavLang.id"> {{myFavLang.name}}</p>
        <button @click="count++">click me {{count}}</button>
        <button @click="name='not123'">change my name</button>
        <button @click="awesome = !awesome">Toggle</button>
        <p v-if="awesome">vue is awesome!</p>
        <p v-else>oh no!</p>
        
    </div>
</template>
<script>
export default {
    data () {
        return {
            name: "notwp",
            age:26,
            position: "dev",
            myFavLang: [
                {
                    name: 'java',
                    id:1
                },
                {
                    name: 'css',
                    id:2
                },
                {
                    name: 'html',
                    id:3
                }
            ],
            count: 0,
            awesome: true
        }
    }
}
</script>
<style scoped>
    .my-profile {
        background-color: aqua;
        border-radius: 5px;
        box-shadow: 3px 3px 10px black;
        padding: 1rem;
    }
</style>