<template>
  <section class="container">
    <h2 class="text-2xl font-semibold mb-8">Features</h2>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 center gap-4">
      <div
        v-for="feature in features"
        :key="feature.name"
        class="transition border p-4 rounded-lg"
      >
        <span class="p-2 rounded-lg inline-block">
          <v-mdi :name="feature.icon" size="34" class="text-gray-100"></v-mdi>
          <p class="text-lg mt-2">{{ feature.name }}</p>
          <p class="text-gray-300">{{ feature.desctription }}</p>
        </span>
      </div>
    </div>
  </section>
</template>
<script setup>
const repository = import.meta.env.VITE_REPOSITORY_URL;
const features = [
  {
    name: 'Keyboard Compatibility',
    icon: 'mdiKeyboardSettingsOutline',
    desctription:
      'Navigate to each page or execute a command only with your keyboard',
  },
  {
    name: 'Command Prompt',
    icon: 'mdiAppleKeyboardCommand ',
    desctription: 'Quick access to your notes and general commands',
  },
  {
    name: 'Export/Import Data',
    icon: 'mdiDatabase',
    desctription:
      'Export or import your data and have full access to your data',
  },
  {
    name: 'Headings Tree',
    icon: 'mdiFileTreeOutline',
    desctription: 'Explore the list of note headings and navigate to it',
  },
  {
    name: 'Focus Mode',
    icon: 'mdiCrosshairsGps',
    desctription:
      'Clear all the distractions and more focus on writing your note',
  },
  {
    name: 'Dark Theme',
    icon: 'mdiWeatherNight',
    desctription:
      'Notething comes with two themes which are light and dark themes.',
  },
];
</script>
