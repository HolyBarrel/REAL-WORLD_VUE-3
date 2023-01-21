<template>
  <div class="events">
    <h1>Events For Good</h1>
    <EventCard v-for="event in events" :key="event.id" :event="event"/>
  </div>
</template>

<script>
// @ is an alias to /src
import EventCard from "@/components/EventCard.vue";

export default {
  name: "Home",
  components: {
    EventCard
  },
  data() {
    return {
      events: [
        {
          id: 2010201,
          category: 'Welfare',
          title: 'Cat adoption day',
          description: 'Find feline friend',
          location: 'Meow town',
          date: 'Jan 28, 2022',
          time: '12:00',
          petsAllowed: true,
          organizer: 'Kat Laydee'
        },
        {
        id: 4410201,
          category: 'Protest',
          title: '5G gives corona',
          description: 'Protest and stand together',
          location: 'Capital city',
          date: 'Jan 23, 2022',
          time: '14:00',
          petsAllowed: true,
          organizer: 'Guy Man'
        }
    ]
    }
  }
};
</script>

<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
