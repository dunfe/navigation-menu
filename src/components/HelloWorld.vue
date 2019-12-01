<template>
    <div class="hello">
        <h1>{{ msg }}</h1>
        <div class="container">
            <div class="container-fluid">
                <nav class="navbar navbar-expand-sm navbar-light bg-light">
                    <a class="navbar-brand" href="#">Diện Vô</a>
                    <button class="navbar-toggler d-lg-none" type="button" data-toggle="collapse"
                            data-target="#collapsibleNavId"
                            aria-controls="collapsibleNavId"
                            aria-expanded="false" aria-label="Toggle navigation">
                        <span class="navbar-toggler-icon"></span>
                    </button>
                    <div class="collapse navbar-collapse" id="collapsibleNavId">
                        <ul v-bind:class="active" v-on:click.prevent class="navbar-nav mx-auto mt-2 mt-lg-0">
                            <li class="nav-item">
                                <a class="nav-link home" href="#" v-on:click="makeActive('home')">Home <span
                                        class="sr-only">(current)</span></a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link about" href="#" v-on:click="makeActive('about')">About</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link case-study" href="#" v-on:click="makeActive('case-study')">Case
                                    Study</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link contact" href="#" v-on:click="makeActive('contact')">Contact</a>
                            </li>
                        </ul>
                    </div>
                </nav>
            </div>
            <h1 class="mx-auto pt-3 text-danger">You choose {{ active }}</h1>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'HelloWorld',
        props: {
            msg: String
        },
        data: function () {
            return {
                active: 'home'
            };
        },
        methods: {
          makeActive: function (item) {
            this.active = item
          }
        }
    };

</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    h3 {
        margin: 40px 0 0;
    }

    ul {
        list-style-type: none;
        padding: 0;
    }

    li {
        display: inline-block;
        margin: 0 10px;
    }

    a {
        color: #42b983;
    }
</style>
