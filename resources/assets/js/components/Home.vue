<template>
    <div>
        <nav class="panel column is-offset-2 is-8">
            <p class="panel-heading">
                Phone book
                <button class="button is-link is-outlined " @click="openAdd">
                    Add new
                </button>
            </p>
            <div class="panel-block">
                <p class="control has-icons-left">
                    <input class="input is-small" type="text" placeholder="search">
                    <span class="icon is-small is-left">
                        <i class="fa fa-search"></i>

                    </span>
                </p>

            </div>
            <a class="panel-block">
            <span class="column is-9">
                bulma
            </span>
                <span class="panel-icon column is-1">
                <i class="has-text-danger fa fa-trash"></i>
            </span>
                <span class="panel-icon column is-1">
                <i class="has-text-info fa fa-edit"></i>
            </span>
                <span class="panel-icon column is-1">
                <i class="has-text-primary fa fa-eye"></i>
            </span>
            </a>
        </nav>
        <Add :openmodal='addActive' @closeRequest="closeModal"></Add>
    </div>
</template>
<script>
    let Add = require('./Add.vue');
    export default{
        components:{Add},
        data(){
            return{
                addActive: ''
            }
        },
        methods:{
            openAdd(){
                this.addActive = 'is-active';
            },
            closeModal(){
                this.addActive = '';
            }
        }
    }
</script>