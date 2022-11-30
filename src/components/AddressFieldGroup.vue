<template>
  <section class="address">
    <h1>{{msg}}</h1>
    <h2>{{ label }}</h2>
    <div>
        <input type="text" v-model.trim.lazy="value">
        <p>Value: {{value}}</p>
    </div>
    <div class="address__field">
      <label for="streetName">Street name</label>
      <input
        type="text"
        id="streetName"
        :value="streetName"
        @input="$emit('update:streetName', $event.target.value)"
        required
      />
      <label for="street">Display:</label>
      <p id="street">{{streetName}}</p>
    </div>
    <div class="address__field">
      <label for="streetNumber">Street number</label>
      <input
        type="text"
        id="streetNumber"
        :value="streetNumber"
        @input="$emit('update:streetNumber', $event.target.value)"
        required
      />
    </div>
    <div class="address__field">
      <label for="city">City</label>
      <input
        type="text"
        id="city"
        :value="city"
        @input="$emit('update:city', $event.target.value)"
        required
      />
    </div>
    <div class="address__field">
      <label for="postcode">Postcode</label>
      <input
        type="text"
        id="postcode"
        :value="postcode"
        @input="$emit('update:postcode', $event.target.value)"
        required
      />
    </div>
  </section>
</template>

<script setup>
import {ref} from "vue";
const value = ref("");

// export default {
//   name: "AddressFieldGroup",
//   props: {
//     msg: String,
//     label: {
//       type: String,
//       default: "",
//     },
//     streetName: {
//       type: String,
//       default: "",
//     },
//     streetNumber: {
//       type: String,
//       default: "",
//     },
//     city: {
//       type: String,
//       default: "",
//     },
//     postcode: {
//       type: String,
//       default: "",
//     },
//   },
// };
</script>