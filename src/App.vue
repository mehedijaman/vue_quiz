<script setup>
  import Question from './components/Question.vue'

  import {ref,reactive} from 'vue'

  const questions = [
    {
      question:'What is capital of Bangladesh?',
      options:[
        {
          text:'Dhaka',
          status:true
        },
        {
          text:'Khulna',
          status:false
        },
        {
          text:'Barishal',
          status:false
        },
        {
          text:'Chittagonj',
          status:false
        },
      ]
    },
    {
      question:'What is currency of Bangladesh?',
      options:[
        {
          text:'INR',
          status:false
        },
        {
          text:'BDT',
          status:true
        },
        {
          text:'USD',
          status:false
        },
        {
          text:'MDT',
          status:false
        },
      ]
    },
  ]

  let userAnswers = reactive([
    {}
  ])
  let totalAnsweredQuestions = ref(0)
  let currentQuestion = ref(0)
  let progress = ref(0)

  const submit = function(){
    currentQuestion++
    totalAnsweredQuestions++
    progress = `(questions.length * totalAnsweredQuestions)/100 %`
  }

  const finalSubmit = function(){

  }
</script>

<template>
  <Question/>
</template>

<style scoped>
</style>
