<script setup lang="ts">
import { CONFIG } from './config.js'
import { SIGNEES } from '../edit-me.js'
</script>

<template>
  <main class="
    min-h-[calc(100vh-10rem)]
    flex
    flex-col
    items-center
    gap-12
    p-8
  ">
    <h1 class="
      text-2xl
      font-bold
    ">
      Theo Browne, please make a video about my tech!
    </h1>

    <img
      src="/assets/theo.jpg"
      class="h-32"
    />


    <div class="
      max-w-[40rem]
      flex
      flex-col
      gap-6
    ">
      <p>
      Aeria is a Prisma-inspired language and HTTP microframework made on top of MongoDB. Terrible idea? Only Theo Browne can say!
      </p>

      <p>
      Here's the official website and documentation: <a href="https://aeria.land/" target="_blank">https://aeria.land/</a>
      </p>

      <p>
      Here's some article I made on MongoDB community forums: <a href="https://www.mongodb.com/community/forums/t/aeria-is-the-new-mongodb-focused-framework/292879/2" target="_blank">https://www.mongodb.com/community/forums/t/aeria-is-the-new-mongodb-focused-framework/292879/2</a>
      </p>
    </div>

    <div>
      <h2 class="font-bold mb-4">
        Signed by:
      </h2>


      <ul>
        <li
          v-for="signee in SIGNEES"
          :key="signee.github"
        >
          {{ signee.github }} - {{ signee.name || 'N/A' }}
        </li>
      </ul>
    </div>

  </main>

  <div class="
      sticky
      bottom-0
      left-0
      border-t
      rounded-t-[2rem]
      h-[10rem]
      bg-white
   ">
    <div class="
      flex
      flex-col
      gap-2
      items-center
      p-6
    ">
      <a :href="CONFIG.repoUrl" target="_blank">
        <button class="
          bg-black
          text-white
          p-6
          rounded-xl
          animate-bounce
        ">
          Fork this repository and add your name to the list!
        </button>
      </a>

      <a
        href="https://github.com/aeria-org/aeria"
        target="_blank"
        class="animate-pulse"
      >
        ...and star Aeria while you're at it! (click here)
      </a>
    </div>
  </div>

    <img
      src="/assets/soyface2.jpg"
      class="
        h-64
        fixed
        right-0
        bottom-0
       "
    />

</template>

