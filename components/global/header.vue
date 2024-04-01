<template>
  <div class="w-full bg-primary-50 h-20 flex items-center">
    <div class="flex justify-between max-w-5xl mx-auto w-full">
      <div>
        <img src="/favicon.ico" alt="" />
      </div>
      <nav>
        <ul class="flex flex-row space-x-4">
          <li v-for="nav in navItems" :key="nav.index">
            <NuxtLink :to="nav.to">
              {{ nav.title }}
            </NuxtLink>
          </li>
        </ul>
      </nav>
      <div>
        <NuxtLink to="https://github.com/notcan">Github</NuxtLink>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import type { NavItemInterface } from "@/types/interfaces"
import navigation from "../../content/header/header.json"
const navItems: NavItemInterface[] = navigation
</script>

<style></style>
