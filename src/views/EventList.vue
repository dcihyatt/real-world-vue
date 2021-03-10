<template>
  <div class="events">
    <h1>Calendar of Events</h1>
    <EventCard
      v-for="event in events"
      :key="event.id"
      :event="event"
    ></EventCard>
  </div>
</template>

<script>
// @ is an alias to /src
import EventCard from "@/components/EventCard.vue";

export default {
  name: "EventList",
  components: {
    EventCard // registered as a child component
  },
  data() {
    return {
      events: [
        {
          id: 5928101,
          category: "riot",
          title: "Offend Nobody Day",
          description: "Lets do the impossible, offend nobody today!",
          location: "City Hall",
          date: "May 3, 2022",
          time: "12:00pm",
          petsAllowed: true,
          organizer: "Fu Man Chu"
        },
        {
          id: 5928102,
          category: "workshop",
          title: "How to Really Wake Up",
          description: "Want to get woke?  Try really waking up.",
          location: "Joe's Coffee Shop",
          date: "May 27, 2022",
          time: "2:00pm-4:00pm",
          petsAllowed: true,
          organizer: "Walter Williams"
        }
      ]
    };
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
