<template>
  <ul>
    <li v-for="country in countries" v-bind:key="country.code">
      {{ country.name }}
    </li>
  </ul>
</template>

<script>
import gql from 'graphql-tag';

export default {
  apollo: {
    countries: gql`query {
      countries {
        code
        name
      }
    }`
  }
}
</script>