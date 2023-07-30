<template>
  <div>
    <h1 class="text-primary text-center mt-5">All Todos</h1>
    <div class="container">
      <div class="row">
        <div class="col-md-4 mt-5" v-for="todo in myTodos" :key="todo.id">
               <b-card  bg-variant="primary" text-variant="white" class="text-center">
                <b-card-text>{{todo.title}}</b-card-text>
              </b-card>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { mapActions, mapGetters } from 'vuex'
export default {
  name : "TodoVue",
  methods : {
    ...mapActions([
      "getTodos"
    ])
  },
  computed: {
    ...mapGetters([
      "myTodos"
    ])
  },
  mounted(){
    this.getTodos()
  }
}
</script>

<style>

</style>