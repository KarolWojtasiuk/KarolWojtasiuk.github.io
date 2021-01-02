<template>
  <v-container>
    <header class="d-flex justify-center align-center pa-5">
      <v-avatar size="128">
        <img src="https://via.placeholder.com/256" alt="Avatar" />
      </v-avatar>
      <div class="pa-5">
        <Command name="echo $USER" result="Karol Wojtasiuk (Drakonter)" />
      </div>
    </header>
    <Command
      name="help"
      result="Click command to execute it"
      style="text-align: center"
    />
    <main class="d-flex">
      <Command name="whatis $USER" :result="userName" requireClick />
      <Command name="whereis $USER" :result="userLocation" requireClick />
      <Command name="groups" :result="userGroups" requireClick />
    </main>
  </v-container>
</template>

<script>
import Command from "~/components/Command.vue";

export default {
  components: {
    Command,
  },
  data() {
    return {
      userName: "Karol Wojtasiuk (Drakonter)",
      userLocation: "Zamość, Poland",
      userGroups: "programmers, csharp, dotnet, vue",
    };
  },
};
</script>
