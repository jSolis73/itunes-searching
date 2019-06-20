<template>
  <div >
    <h1>Search Itunes</h1>
    <br/>
    <div class="form">
      <form @submit.prevent="submit" >
        <v-flex
          xs12
          md3
          >
          <v-text-field
            v-model="search"
            ref="serch"
            label="Enter artist name"
            required
            style="align: center"
          ></v-text-field>
        </v-flex>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      search: ''
    }
  },
  methods: {
    submit(event) {
      this.$router.push(`results/${this.search}`)
    }
  },
}
</script>

<style>
* {
  text-align: center;
}
h1 {
  padding: 20px;
}
.form {
    width: 100%;
    height: 100%;
    position: absolute;
    margin: auto;
    overflow: auto;
    margin-left: 33%;
}
</style>

