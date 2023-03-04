<template>
  <div class="flex flex-col">
    
    <!-- Preview card: What's happening -->
    <SidebarRightPreviewCard title="What's happening">
      <SidebarRightPreviewCardItem 
        v-for="whatsHappening in whatsHappenningItems"
      >

        <div>
          <h2 class="font-bold text-gray-800 text-md dark:text-white">{{ whatsHappening.title }}</h2>
          <p class="text-xs text-gray-400">
            {{ whatsHappening.count }}
          </p>
        </div>

      </SidebarRightPreviewCardItem>
    </SidebarRightPreviewCard>

    <!-- Preview card: Whom to follow -->
    <SidebarRightPreviewCard title="Whom to follow">
      <SidebarRightPreviewCardItem
        v-for="whomToFollow in whomToFollowItems"
      >
      <div class="flex flex-row items-center justify-between p-2">
        <div class="flex flex-row">
          <img class="w-10 h-10 rounded-full" :src="whomToFollow.image" alt="user avatar">

          <div class="flex flex-col ml-2">
            <h1 class="text-sm font-bold text-gray-900 dark:text-white">{{ whomToFollow.name }}</h1>
            <p class="text-xs text-gray-400">{{ whomToFollow.handle }}</p>
          </div>

        </div>

        <div class="flex h-full">
          <button class="px-4 py-2 font-bold text-xs text-white bg-black dark:text-black dark:bg-white rounded-full">Follow</button>
        </div>
      </div>

      </SidebarRightPreviewCardItem>

    </SidebarRightPreviewCard>
  </div>
</template>

<script setup>
const whatsHappenningItems = ref([
  {
    title: 'SpaceX',
    count: '18.8k tweets',
  },
  {
    title: '#GuitarWorld',
    count: '21.3k tweets',
  },
  {
    title: '#BraveNuts',
    count: '14.5k tweets',
  }
])

const whomToFollowItems = ref([
  {
    name: 'Joe Biden',
    handle: '@joebiden',
    image: 'https://picsum.photos/200/200'
  },
  {
    name: 'James Hetfield',
    handle: '@jameshetfield',
    image: 'https://picsum.photos/200/200'
  },
  {
    name: 'Light Yagami',
    handle: '@yourlight',
    image: 'https://picsum.photos/200/200'
  },
])
</script>

<style lang="scss" scoped>

</style>