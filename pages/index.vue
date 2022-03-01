<template>
  <div class="mt-2">
    <v-card class="pa-2">
      <v-row>
        <v-col cols="6">
          <card-money-received></card-money-received>
        </v-col>
        <v-col cols="6">
          <card-money-pay></card-money-pay>
        </v-col>
      </v-row>
    </v-card>
    <v-divider class="my-5"></v-divider>
    <v-row>
      <v-col cols="12" v-for="(itemLog, i) of list_log_data" :key="i">
        <card-log-list :list="itemLog"></card-log-list>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import CardMoneyPay from "~/components/cardMoneyPay.vue";
import cardMoneyReceived from "~/components/cardMoneyReceived.vue";
export default {
  components: { cardMoneyReceived, CardMoneyPay },
  layout: "emtry",
  data() {
    return {
      list_log_data: [
        {
          amount: "999",
          log_type: "received",
        },
        {
          amount: "999",
          log_type: "pay",
        },
      ],
    };
  },
};
</script>
