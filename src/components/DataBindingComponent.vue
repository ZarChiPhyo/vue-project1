<template>
    <div>
        <h3>Data Binding</h3>
        <p>Name:{{ name }}</p>
        <p>Mail:{{ mail }}</p>
        <p>Marks:{{ marks[0] }},{{ marks[1] }},{{ marks[2] }}</p>
        <p v-bind:class="levelClass">Levels:html:{{ levels.html }},css:{{levels.css}},js:{{ levels.js }},vue:{{ levels.vue }}</p>
    </div>
</template>

<script>
    export default {
        name: 'DataBinding',
        data(){
            return{
                name:"Thiri Aung",
                mail:"thiri@gmail.com",
                marks:[56,78,90],
                levels:{
                    html:5,
                    css:4,
                    js:4,
                    vue:5
                },
                levelClass:'capital',
            }
        }
    }
</script>

<style scoped>
    .capital{
        text-transform: uppercase;
        font-family: Georgia, 'Times New Roman', Times, serif;
        font-size: 20px;
    }
</style>