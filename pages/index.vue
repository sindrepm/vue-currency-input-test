<template>
  <VContainer>
    <VRow>
      <VCol>
        <h2>Simple Input</h2>
        <CurrencyInput v-model="value" currency="EUR" />
      </VCol>
      <VCol>
        <h2>Vuetify</h2>
        <VCurrencyField v-model="value" :options="{ currency: 'EUR' }" />
      </VCol>
    </VRow>
    <VRow>
      <VCol
        >Number value: <code>{{ value != null ? value : "null" }}</code></VCol
      >
    </VRow>
  </VContainer>
</template>

<script>
import { ref } from "@vue/composition-api";
import VCurrencyField from "@/components/VCurrencyField";
import CurrencyInput from "@/components/CurrencyInput";

export default {
  name: "App",
  components: {
    CurrencyInput,
    VCurrencyField,
  },
  setup() {
    return {
      value: ref(1234),
    };
  },
};
</script>

