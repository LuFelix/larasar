<template>
  <q-page class="flex flex-center">
    <div class="text-center">
      <div class="*col-12">
        <h4 v-if="user">{{$t('you_are_logged_in')}}</h4>
      </div>
      <div class="*col-12">
        <a  target="_blank" href="https://github.com/modemb/larasar"><i class="fab fa-github fa-3x q-mr-lg"/></a>
        <a  target="_blank" href="https://www.facebook.com/modemb.dev"><i class="fab fa-facebook fa-3x q-mr-lg"/></a>
        <a  target="_blank" href="https://www.linkedin.com/in/mohamed-dembele-85051197/"><i class="fab fa-linkedin fa-3x q-mr-lg"/></a>
        <a  target="_blank" href="https://www.patreon.com/modemb"><i class="fab fa-patreon fa-3x q-mr-lg"/></a>
        <form action="https://www.paypal.com/cgi-bin/webscr" method="post" target="_top">
          <input type="hidden" name="cmd" value="_s-xclick" />
          <input type="hidden" name="hosted_button_id" value="CZ6J25TKMVQ42" />
          <button><i class="fab fa-paypal fa-3x *q-mr-lg"/></button>
        </form>
      </div>
      <div class="*col-12">
        <a target="_blank"  href="https://quasar.dev" class="logo">
          <img alt="Larasar logo" src="~assets/quasar-logo-full.svg">
        </a>
      </div>
      <div class="*col-12">
        <a target="_blank"  href="https://laravel.com" class="logo q-mr-lg">
            <img class="mark" src="https://laravel.com/img/logomark.min.svg" alt="Laravel">
            <img class="type" src="https://laravel.com/img/logotype.min.svg" alt="Laravel">
        </a>
        <a target="_blank" id="logo" href="https://vuejs.org">
            <img src="https://vuejs.org/images/logo.png" alt="vue logo" width=50>
        </a>
      </div>
    </div>
  </q-page>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  name: 'PageIndex',
  computed: mapGetters({
    user: 'users/authGetter'
  })
}
</script>

<style lang="css" scoped>
  form {
      display: inline-block;
  }
  button {
      cursor: pointer;
  }
</style>
