<template>
  <div v-if="profile" class="flex flex-col text-sm lg:text-base">
    <div v-if="profile.name" class="flex flex-row border-b-2">
        <div class="pr-4">Name</div>
        <div class="font-bold m-auto mr-2">{{profile.name}}</div>
    </div>
    <div v-if="profile.career" class="flex flex-row pt-2">
        <div class="pr-4">Email</div>
        <div class="font-bold m-auto mr-2">{{profile.email}}</div>
    </div>
    <div v-if="profile.number" class="flex flex-row">
        <div class="pr-4">Number</div>
        <div class="font-bold m-auto mr-2">{{profile.number}}</div>
    </div>
    <div v-if="profile.career" class="flex flex-row">
        <div class="pr-4">Career</div>
        <div class="font-bold m-auto mr-2">{{profile.career}}</div>
    </div>
    <div v-if="profile.location" class="flex flex-row">
        <div class="pr-4">Location</div>
        <div class="font-bold m-auto mr-2" >{{profile.location}}</div>
    </div>
    <div v-if="profile.experience" class="flex flex-row">
        <div class="pr-4">Experience</div>
        <div class='flex flex-col md:flex-row justify-end w-full'>
        <div v-for="exp in profile.experience" :key="exp.name" class="font-bold m-auto mr-2">
          <a class="pr-1 hover:text-blue-500" :href="exp.link" target="_blank">{{exp.name}}</a>
        </div>
        </div>
    </div>
    <div v-if="profile.websites" class="flex flex-row">
        <div class="pr-4">Websites</div>
        <div class='flex flex-col md:flex-row justify-end w-full'>
        <div v-for="exp in profile.websites" :key="exp.link" class="font-bold m-auto mr-2">
          <a class="pr-1 hover:text-blue-500" :href="exp.link" target="_blank">{{exp.name}}</a>
        </div>
        </div>
    </div>
  </div>
</template>
<script>
export default {
  /**
   * @author pat-lego <patrique.legault@gmail.com>
   * @version 1.0
   * @description This component is used to display user profile data
   * @memberof components
   */
  name: 'profile-component',
  props: {
    profile: {
      type: Object,
      note: 'This is the user profile'
    }
  }
}
</script>
