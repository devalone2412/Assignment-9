<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <br>
                <button class="btn btn-primary" @click="selectedComponent = 'appBlue'">Load Blue Template</button>
                <button class="btn btn-success" @click="selectedComponent = 'appGreen'">Load Green Template</button>
                <button class="btn btn-danger" @click="selectedComponent = 'appRed'">Load Red Template</button>
                <hr>
                <component :is="selectedComponent">
                    <h1 slot="title">{{ listTemplateData[selectedComponent].title }}</h1>
                    <h3 slot="subtitle">{{ listTemplateData[selectedComponent].subTitle }}</h3>
                </component>
            </div>
        </div>
    </div>
</template>

<script>
    import Blue from './components/Blue.vue';
    import Green from './components/Green.vue';
    import Red from './components/Red.vue';

    export default {
        data() {
            return {
                listTemplateData: {
                    'appBlue': {title: 'Blue Title', subTitle: 'Blue Subtitle'},
                    'appGreen': {title: 'Green Title', subTitle: 'Green Subtitle'},
                    'appRed': {title: 'Red Title', subTitle: 'Red Subtitle'},
                },
                selectedComponent: 'appBlue'
            };
        },
        components: {
            appBlue: Blue,
            appGreen: Green,
            appRed: Red
        }
    }
</script>

<style>
</style>
