<template>
    <div class="svg-loader">
        <svg :xmlns="xmlns"
             :width="config.width"
             :height="config.height"
             :viewBox="getViewBox">
            <path :fill="config.pathFill"
                  :fill-rule="fillRule"
                  :d="config.d"></path>
        </svg>
    </div>
</template>

<script>
    export default {
        name: 'home',
        props: {
            config: Object
        },
        computed: {
          getViewBox() {
              return `0 0 ${this.config.width} ${this.config.height}`
          }
        },
        data: function () {
            return {
                xmlns: "http://www.w3.org/2000/svg",
                fillRule: "evenodd"
            }
        }
    }
</script>

<style scoped
       lang="scss">
    .svg-loader {
        display: flex;
    }
</style>
