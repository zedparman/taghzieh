<template>
  <div>
    <nav class="navbar navbar-expand-sm navbar-dark bg-primary">
      <nuxt-link to="/" class="navbar-brand">Home</nuxt-link>

      <div class="collapse navbar-collapse" id="collapsibleNavId">
        <ul class="navbar-nav mr-auto mt-2 mt-lg-0">
          <li class="nav-item active">
            <nuxt-link to="checkuser" class="nav-link">checkuser</nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link to="getauthcode" class="nav-link">getauthcode</nuxt-link>
          </li>
        </ul>
        <form class="form-inline my-2 my-lg-0">
          <input
            class="form-control mr-sm-2"
            type="text"
            placeholder="Search"
          />
          <button class="btn btn-outline-success my-2 my-sm-0" type="submit">
            Search
          </button>
        </form>
      </div>
    </nav>
    <nuxt />
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
</style>