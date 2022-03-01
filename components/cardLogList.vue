<template>
  <div>
    <v-card :color="color" dark>
      <v-card-actions>
        <h4>{{ log_type }}</h4>
      </v-card-actions>
    </v-card>
  </div>
</template>

<script>
export default {
  props: ["list"],
  data() {
    return {
      color: null,
    }
  },
  computed: {
    log_type() {
      if (this.list.log_type == "received") {
        this.color = "green";
        return "รายรับ"
      } else {
        this.color = "red";
        return "รายจ่าย"
      }
    },
  },
};
</script>
