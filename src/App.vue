<template>
  <div class="container">
    <div class="card card-body mt-5 p-5 text-center border-secondary">
        <div>
          <i class="fa fa-star text-warning fa-6x" @click="setRating(1)"></i>
          <i class="fa fa-star text-warning fa-6x" @click="setRating(2)"></i>
          <i class="fa fa-star text-warning fa-6x" @click="setRating(3)"></i>
          <i class="fa fa-star text-warning fa-6x" @click="setRating(4)"></i>
          <i class="fa fa-star text-warning fa-6x" @click="setRating(5)"></i>
        </div>
        <p class="display-4">{{rating}} Star rating</p>
        <h1 v-if="rating == 1">Sorry to hear that</h1>
        <h1 v-if="rating == 2">We will try to imrpove</h1>
        <h1 v-if="rating == 3">Thank you!! We will try to improve</h1>
        <h1 v-if="rating == 4">Glad to hear that!!</h1>
        <h1 v-if="rating == 5">Great!!</h1>
    </div>
  </div>
</template>

<script>
export default {
  name:"App",
  data()
  {
    return{
       rating: "NULL"
    }
  },
  methods:{
    setRating(rating)
    {
      this.rating = rating
    }
  }
}
</script>

<style>
body{
  background-color: black;
}
</style>