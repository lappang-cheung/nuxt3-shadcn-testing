<script setup>
  const items = ref([
    {
      title: "Overview",
      path: "/",
      icon: "ri:dashboard-line"
    },
    {
      title: "Transactions",
      path: "/transactions",
      icon: "grommet-icons:transaction"
    },
    {
      title: "Account",
      path: "/account",
      icon: "material-symbols:manage-accounts-rounded"
    },
    {
      title: "Contacts",
      path: "/contacts",
      icon: "mdi:contact"
    },
    {
      title: "Settings",
      path: "/settings",
      icon: "uil:setting"
    }
  ])
</script>

<template>
  <div>
    <header class="flex items-center gap-2 p-4 hover:scale-[101%] transition cursor-pointer">
      <Logo />
      <p class="font-bold">Nuxt Finance</p>
    </header>
    <div class="px-4 grow">
      <div class="grid gap-2">
       <nuxt-link v-for="(item, index) in items"
            :key="index"
            :to="item.path"
            class="flex items-center gap-2 px-2 py-2 transition rounded cursor-pointer hover:bg-neutral-100">
         <Icon size="20" :name="item.icon" color="black"/>
         <span>
           {{item.title}}
         </span>
       </nuxt-link>
      </div>
    </div>
  </div>
</template>
