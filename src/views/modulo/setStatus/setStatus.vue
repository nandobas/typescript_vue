<template>
  <div class="home">
    <HelloWorld msg="Set Status" />
  </div>
</template>

<script lang="ts">
import { useStore } from "vuex";
import { key } from "../../../store";
import { Options, Vue } from "vue-class-component";
import HelloWorld from "@/components/HelloWorld.vue"; // @ is an alias to /src

@Options({
  components: {
    HelloWorld,
  },
})
export default class Home extends Vue {
  setup() {
    const store = useStore(key);

    store.state.count = 5; // typed as number
  }
}
</script>
