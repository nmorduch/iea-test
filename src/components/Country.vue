<script setup>
defineProps({
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
  <tr>
    <th>{{ countryName }}</th>
    <td>{{ region }}</td>
    <td>{{ totalEnergySupply }}</td>
    <td>{{ IEAMember }}</td>
  </tr>
</template>
