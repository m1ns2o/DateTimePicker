<template>
  <div>
    <Datepicker
      uid="auto"
      time-picker
      v-model="date"
      :max-time="{ hours: 22, minutes: 40 }"
      :min-time="{ hours: 7, minutes: 10 }"
      auto-apply
    />
    <hr />
    <pre>
The min-time / max-time is set and also a default time. 

Now when I click on the time-picker,
the value displayed is current time of the browser
not 10:15 as setted by default.

version: 2.3.3 of vue3-date-time-picker
    </pre>
  </div>
</template>

<script>
import { ref } from "vue";
import Datepicker from "vue3-date-time-picker";
import "vue3-date-time-picker/dist/main.css";

export default {
  name: "Demo",
  components: {
    Datepicker,
  },
  setup() {
    const date = ref({ hours: 10, minutes: 15 });

    return {
      date,
    };
  },
};
</script>