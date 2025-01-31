<script setup>
defineProps({
  index: {
    type: Number,
    required: true,
  },
  countryName: {
    type: String,
    required: true,
  },
  region: {
    type: String,
    required: true,
  },
  totalEnergySupply: {
    type: [Number, String],
    default: '—',
  },
  IEAMember: {
    type: Boolean,
    required: true,
  },
})
</script>

<template>
  <tr :aria-rowindex="index">
    <th scope="row">{{ countryName }}</th>
    <td>{{ region }}</td>
    <td>{{ totalEnergySupply == '—' ? '—' : Intl.NumberFormat().format(totalEnergySupply) }}</td>
    <td>{{ IEAMember }}</td>
  </tr>
</template>
