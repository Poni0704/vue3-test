<script>
import TitleBar from "@/components/TitleBar.vue";
import ListItem from "@/components/ListItem.vue";
import TimerBox from "@/components/TimerBox.vue";
import EventBack from "@/components/EventBack.vue";
import TemplateRefs from "@/components/TemplateRefs.vue";
import SlotsTitle from "@/components/SlotsTitle.vue";

import { ref } from "vue";
export default {
  components: {
    TitleBar,
    ListItem,
    TimerBox,
    EventBack,
    TemplateRefs,
    SlotsTitle,
  },
  setup() {
    // const isAmin = ref(false);

    const isOpen = ref(true);

    const HandListShow = () => {
      isOpen.value = !isOpen.value;
    };

    const handCallBackFn = (num) => {
      console.log("app=>", num);
    };

    const handTimeOut = (num) => {
      console.log("time is over", num.value);
    };

    return {
      isOpen,
      HandListShow,
      handTimeOut,
    };
  },
};
</script>

<template>
  <!-- 
    <TitleBar :HandListShow="HandListShow" />
    <ListItem :isOpen="isOpen" />
    <TimerBox @TimeOut="handTimeOut" /> 
  -->

  <!-- <EventBack /> -->

  <!-- <TemplateRefs /> -->
  <!-- 如果是該component駝峰式命名，要記得變成小寫，並且透過dash串接 -->
  <slots-title>Poni</slots-title>
  <p>gzdgdhzdhtdzh</p>
  <slots-title>fubon</slots-title>
  <p>gzdgdhzdhtdzh</p>
  <slots-title>heyhey</slots-title>
  <p>gzdgdhzdhtdzh</p>

  <!-- 
    <button>click</button>
    <transition name="fade">
      <div id="box"></div>
    </transition> 
  -->
</template>

<style>
/* .fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
} */

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
html,
body {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;
  background-color: slategray;
}
#app {
  width: 400px;
  overflow: hidden;
  border: 1px solid #42b983;
  border-radius: 10px;
}

/* #box {
  width: 100px;
  height: 100px;
  background-color: red;
} */
</style>
