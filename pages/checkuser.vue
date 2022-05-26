<template>
    <div class="container my-4">
        <form @submit.prevent="handlePhoneNumber">
          <input
            type="text"
            class="form-control mb-2"
            v-model="mobile"
            placeholder="phone number"
          />
          <input class="btn btn-primary w-100" type="submit" value="submit" />
        </form>
    </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      mobile: ""
    };
  },
  methods: {
    async handlePhoneNumber() {
      try {
        let response = await axios.post("http://95.217.96.131:8080/api/checkuser", {
        mobile: this.mobile
      });
        console.log(response);
      } catch (error) {
        console.log(error);
      }
      this.$router.push("/getauthcode");
      localStorage.setItem("mobile", this.mobile);
      this.mobile = "";
    }
  },
  mounted() {
    if (process.client) {
      this.mobile = localStorage.getItem("mobile");
    }
  },
};
</script>

<style scoped>

</style>