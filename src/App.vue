<template>
  <div>
    <button @click="increment">+</button>
    <button @click="decrement">-</button>
    <button @click="incrementIfOdd">{{$store.state.count}}</button>
    <button @click="incrementAsync">{{$store.state.count}}</button>

    <!-- <button @click="increment">+</button>
    <button @click="decrement">-</button>
    <button @click="incrementIfOdd">{{$store.state.count}}</button>
    <button @click="incrementAsync">{{$store.state.count}}</button>-->

    <!-- <button @click="increment">+</button>
    <button @click="decrement">-</button>
    <button @click="incrementIfOdd">{{$store.state.count}}</button>
    <button @click="incrementAsync">{{$store.state.count}}</button>-->

    <!-- <button @click="increment">+</button>
    <button @click="decrement">-</button>
    <button @click="incrementIfOdd">{{count}}</button>
    <button @click="incrementAsync">{{count}}</button>-->
  </div>
</template>
<script type="text/ecmascript-6">
import { mapMutations, mapActions, mapGetters } from "vuex";
export default {
  methods: {
    increment() {
      this.$store.dispatch("increment"); //emit 都代表分发
    },
    decrement() {
      this.$store.dispatch("decrement"); //emit 都代表分发
    },
    incrementIfOdd() {
      this.$store.dispatch("incrementIfOdd"); //emit 都代表分发
    },
    incrementAsync() {
      this.$store.dispatch("incrementAsync"); //emit 都代表分发
    }

    // increment() {
    //   this.$store.dispatch("increment");
    // },
    // decrement() {
    //   this.$store.dispatch("decrement");
    // },
    // incrementIfOdd() {
    //   this.$store.dispatch("incrementIfOdd");
    // },
    // incrementAsync() {
    //   this.$store.dispatch("incrementAsync");
    // }
  },

  // methods:{
  //   increment(){
  //     this.$store.dispatch('increment')
  //   },
  //   decrement(){
  //     this.$store.dispatch('decrement')
  //   },
  //   incrementIfOdd(){
  //     this.$store.dispatch('incrementIfOdd')
  //   },
  //   incrementAsync(){
  //     this.$store.dispatch('incrementAsync')
  //   }
  // }

  // methods: {
  //   increment() {
  //     this.$store.commit("increment");
  //   },
  //   decrement() {
  //     this.$store.commit("increment");
  //   },
  //   incrementIfOdd() {
  //     this.$store.dispatch("incrementIfOdd");
  //   },
  //   incrementAsync() {
  //     this.$store.dispatch("incrementAsync");
  //   }
  // }
  // computed: {
  //   count(){
  //     return this.$store.getters.currentCount
  //   }
  // },

  methods: {
    ...mapMutations(["increment", "decrement"]),
    ...mapActions(["incrementIfOdd", "incrementAsync"])
  }
};
</script>
<style scoped></style>



