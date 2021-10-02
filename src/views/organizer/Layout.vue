<template>
  <div v-if="GStore.organizer">
    <h1>{{ GStore.organizer.name }}</h1>
    <div id="nav">
      <router-link :to="{ name: 'OrganizerDetails' }">Details</router-link>
    </div>
    <router-view :organizer="GStore.organizer" />
  </div>
</template>
<script>
export default {
  inject: ['GStore']
}
</script>
