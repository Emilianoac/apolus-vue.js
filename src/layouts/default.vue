<template>
    <div class="main-container">
        <TheMenuSuperior/>
        <main class="main">
            <slot> </slot>
        </main>
        <TheMenuLateral/>
        <BarraControl/>
    </div>
</template>

<script>
    import TheMenuSuperior from '../components/TheMenuSuperior.vue'
    import TheMenuLateral  from '../components/TheMenuLateral.vue'
    import BaseReproductor from '../components/BaseReproductor.vue'
    import BarraControl    from '../components/BarraControl.vue'
    export default {
        name: 'Default',
        components: {
            TheMenuSuperior,
            TheMenuLateral,
            BarraControl
        }
    }
</script>


<style lang="scss">

    .main-container {
        height: 100%;
        position: relative;
        display: grid;
        grid-template-columns: 70px 1fr;
        grid-template-rows: min-content;
        padding-bottom: 4em;
    }

    .main {
        width: 100%;
        max-width: 1820px;
        grid-column: 2/4;
        position: relative;
        padding: 2em 3.4em;
        padding-top: 6em;
        margin: 0 auto;
        padding-bottom: 8em;
        z-index: 1;
        overflow-x: hidden;
        overflow-y: auto;
    }

    @media(max-width:991px) {
    
        body {
            height: auto;
        }

        .main-container {
            grid-template-columns: 1fr;
            height: auto;
        }

        .main {
            padding: 2rem;
            padding-top: 9rem;
            padding-bottom: 6rem;
            grid-column: 1/2;
        }
    }

    @media(max-width:650px) {

        .main {
            padding-left: 1rem;
            padding-right: 1rem;
        }
    }
</style>
