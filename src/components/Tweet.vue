<template>
  <div className="tweet">

  <ProfileImage :url="tweet.user.image"/>
    <div className="body">
      <div className="top">
        <span className="user">
          <User :name="tweet.user.name" :handle="tweet.user.handle"/>
        </span>

        <Timestamp :timestamp="tweet.timestamp"/>

      </div>

      <Message :message="tweet.message"/>

      <Buttons/>
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script setup>
import User from "./User.vue"
import ProfileImage from "./ProfileImage.vue";
import Timestamp from "./Timestamp.vue";
import Message from "./Message.vue";
import Buttons from "./Buttons.vue";

import { ref } from 'vue';

const props = defineProps(["tweet"]);

</script>

<style scoped>
a {
  color: #42b983;
}
</style>
