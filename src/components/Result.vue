<template>
    <p>Counter is: {{ counter }}</p>
</template>

<script>
    import { mapGetters } from 'vuex';
    import * as types from '../store/types'

    export default {
        computed: {
            //... SPREAD Operator: An es6 solution to put an object immediately inside an object. It pulls out all properties and methods in the object and create seperate key value pairs for each of them
            ...mapGetters({
                counter: types.DOUBLE_COUNTER,
            })
        }
    }
</script>