<script>
export default {
  data: function () {
    return {
      newProductParams: {},
    };
  },
  methods: {
    handleSubmit: function () {
      this.$emit("createProduct", this.newProductParams);
      this.newProductParams = {};
      console.log("testing submit")
    },
  },
};

</script>

<template>
  <div>
    <h1>New Product</h1>
    <form v-on:submit.prevent="handleSubmit">
      <div>
        Name:
        <input name="name" type="text" v-model="newProductParams.name"/>
      </div>
      <div>
        Category:
        <input name="category" type="text" v-model="newProductParams.category"/>
      </div>
      <div>
        Price:
        <input name="price" type="number" v-model="newProductParams.price"/>
      </div>
      <button type="submit">Create Product</button>
    </form>
  </div>
</template>

<style></style>