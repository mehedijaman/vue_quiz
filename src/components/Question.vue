<script setup>

</script>

<template>
  
  <div class="col col-md-6 offset-md-3">
    <div class="card">
      <div class="card-header">
        <h4 class="text-center">Vue Quiz</h4>
      </div>
      <div class="card-body">
        <h5 class="card-title"><strong>{{ questions[currentQuestion].question }} </strong></h5>
        <div class="form-check" v-for="(option,index) in questions[currentQuestion].options" :key="index">
          <input class="form-check-input" type="radio" name="flexRadioDefault" id="flexRadioDefault1">
          <label class="form-check-label" for="flexRadioDefault1">
            {{ option }}
          </label>
        </div>
        <div class="col col-md-4 offset-md-4">
          <a href="#" class="btn btn-primary btn-sm mt-3" @click="submit">Submit Answer</a>
        </div>
      </div>
      <div class="card-footer text-muted">
        0/0 Questions answered
        <div class="progress">
          <div class="progress-bar progress-bar-striped progress-bar-animated" role="progressbar" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100" :style="progress"></div>
        </div>
      </div>
    </div>
  </div>

  
</template>

<style scoped>
</style>
