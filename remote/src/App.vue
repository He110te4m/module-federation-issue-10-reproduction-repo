<script lang="ts">
import { defineComponent } from "@vue/composition-api";
import Counter from "./components/Counter.vue";
import logoImg from "./assets/logo.svg";

export default defineComponent({
  components: { Counter },
  setup() {
    return { logoImg };
  },
});
</script>

<template>
  <div style="
        background: #1f2124;
        box-shadow: 0 0 20px rgba(0, 0, 0, 0.4);
        border-radius: 5px;
        margin: 20px 20px 20px 20px;
        width: 250px;
        padding: 20px;
        text-align: center;
        color: white;
        float: left;
      " data-e2e="APP__CARD">
    <div className="icon">
      <img :src="logoImg" />
    </div>
    <div style="margin-top: 10px; font-size: 25px">I'm the remote app</div>
    <Counter />
  </div>
</template>
