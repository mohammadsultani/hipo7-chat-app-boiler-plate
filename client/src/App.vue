<template>
  <div>
    <h4>Create a simple Vue application to interect with your backend</h4>
    <p>The app is expected to have these basic functionlities.</p>
    <p>
      But you can be creative as a butter fly and turn your app into a piece of
      art.
    </p>
    <ul>
      <li>Your application should have a login page</li>
      <li>A component to show all your messages</li>
      <li>A component to add new messages</li>
      <li>And a delete button to delete a message</li>
    </ul>
    <p>All the required dependencies are already installed for you.</p>
    <p>
      You are advised to go through the codes and read the comments carefully.
    </p>
    <p>
      There are enough hints for you to not get lost inside the boilerplate.
    </p>
    <br />
    <p>Some usefull resources to help you along the way.</p>
    <ul>
      <li>
        Check out
        <a
          href="https://www.digitalocean.com/community/tutorials/vuejs-rest-api-axios"
        >
          this
        </a>
        great article about using axios.
      </li>
      <li>
        if you are curios about socket.io then here is the
        <a href="https://socket.io/">documentation.</a>
      </li>
    </ul>
    <p class="reminder">
      Remember this is meant to be a boiler plate setup to get you up and
      running, not a full functional app.
    </p>
    <p>
      The link to deployed version of the chat app is
      <a href="https://thc-chat-app.herokuapp.com">here</a>.
    </p>
    <p>Feel free to reach out if you face any challenges along the way.</p>
    <p>Enough talks, It is time to start building your app.</p>
    <h3>Happy Coding !!</h3>
  </div>
</template>

<script>
/*eslint-disable*/
import io from "socket.io-client";
const socket = io("http://localhost:5000");
import axios from "axios";
export default {
  name: "App",
  components: {},
  created() {
    // once the app is created and event will be triggered and
    // in the backend we are listening to that event.
    socket.emit("event", "Some data from client side");
  },
};
</script>

<style>
div {
  font-family: sans-serif;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}
p,
li {
  margin: 4px auto;
}
.reminder {
  font-weight: bold;
}
</style>
