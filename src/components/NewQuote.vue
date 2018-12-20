<template>
    <div class="row">
        <form class="col-6 m-auto">
            <div class="col form-group">
                <label>Quote</label>
                <textarea class="form-control" rows="3" v-model="quote"></textarea>
            </div>
            <div class="col form-group">
                <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
            </div>
        </form>
    </div>
</template>

<script>
export default {
    data(){
        return{
            quote: ''
        }
    },
    methods: {
        createNew(){
            this.$emit('quoteAdded', this.quote)
            this.quote = ''
        }
    }
}
</script>

<style>

</style>
