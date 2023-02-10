<template>
  <div>
    <section
      class="max-w-md p-4 mx-auto bg-white border border-gray-200 dark:bg-gray-800 left-12 bottom-16 dark:border-gray-700 rounded-2xl"
    >
      <h2 class="font-semibold text-gray-800 dark:text-white">Question 1</h2>

      <p class="mt-4 text-sm text-gray-600 dark:text-gray-300">
        There are more than 10,000 different types of cells in your body.
      </p>

      <p class="mt-3 text-sm text-gray-600 dark:text-gray-300">Select Answer</p>

      <select
        v-model="this.question1"
        id="countries"
        class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
      >
        <option>True</option>
        <option>False</option>
        <option>Not sure</option>
      </select>
    </section>
  </div>

  <div class="mt-5">
    <section
      class="max-w-md p-4 mx-auto bg-white border border-gray-200 dark:bg-gray-800 left-12 bottom-16 dark:border-gray-700 rounded-2xl"
    >
      <h2 class="font-semibold text-gray-800 dark:text-white">Question 2</h2>

      <p class="mt-4 text-sm text-gray-600 dark:text-gray-300">The number of mitochondria in a given cell varies with the cell's energy demands
      </p>

      <p class="mt-3 text-sm text-gray-600 dark:text-gray-300">Select Answer</p>

      <select
        v-model="this.question2"
        id="countries"
        class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
      >
        <option>True</option>
        <option>False</option>
        <option>Not sure</option>
      </select>
    </section>
  </div>

  <div class="mt-5">
    <section
      class="max-w-md p-4 mx-auto bg-white border border-gray-200 dark:bg-gray-800 left-12 bottom-16 dark:border-gray-700 rounded-2xl"
    >
      <h2 class="font-semibold text-gray-800 dark:text-white">Question 3</h2>

      <p class="mt-4 text-sm text-gray-600 dark:text-gray-300">
        The amount of ATP generated during glycolysis is very small compared to the amount generated from breaking down pyruvate
      </p>

      <p class="mt-3 text-sm text-gray-600 dark:text-gray-300">Select Answer</p>

      <select
        v-model="this.question3"
        id="countries"
        class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
      >
        <option>True</option>
        <option>False</option>
        <option>Not sure</option>
      </select>
    </section>
  </div>

  <div class="mt-4">
    <button
      class="group relative h-12 w-48 overflow-hidden rounded-lg bg-white text-lg shadow"
    >
      <div
        class="absolute inset-0 w-3 bg-amber-400 transition-all duration-[250ms] ease-out group-hover:w-full"
      ></div>
      <span
        class="relative text-black group-hover:text-white"
        @click="check_answer"
        >Submit answer</span
      >
    </button>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },

  data() {
    return {
      score: 0,
      question1: 0,
      question2: 0,
      question3: 0,
      modal: false,
    };
  },

  methods: {
    check_answer() {
      if (this.question1 == "False"){
        this.score = this.score + 1
      }
      if (this.question2 == "True"){
        this.score = this.score + 1
      }
      if (this.question3 == "True"){
        this.score = this.score + 1
      }
      alert("Congratulations Your score is: " + this.score)
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
