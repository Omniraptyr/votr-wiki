<template>
    <div class="container">
    <!-- START NAV -->
    <nav class="navbar is-white">
      <div class="navbar-brand">
                      <nuxt-link to="/" class="navbar-item brand-text">Home</nuxt-link>

        <div class="navbar-burger burger" data-target="navMenu">
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>
      <div id="navMenu" class="navbar-menu">
        <div class="navbar-start">
          
              <nuxt-link to="/legendaries" class="navbar-item">Legendaries</nuxt-link>
              <nuxt-link to="/dungeons" class="navbar-item">Dungeons</nuxt-link>

          
        </div>
      </div>
    </nav>
    <!-- END NAV -->
    <section class="articles">
        <div class="column is-8 is-offset-2">

          <!-- START PROMO BLOCK -->
          <section class="hero is-danger is-bold is-small promo-block">
            <div class="hero-body">
              <div class="container">
                <h1 class="title">
                  <i class="fa fa-bell-o"></i> 
                   Furious Gauntlet
                </h1>
                <h2 class="subtitle">
                  No fear shall be shown.
                </h2>
              </div>
            </div>
            
          </section>
                    <div class="card article">
            <div class="card-content">
             
            <div class="content article-body">
                <img src="https://i.imgur.com/oUQeiOo.png" class="image is-128x128" alt="furious gauntlet">
                <h3>Stats.</h3>
                <p>
                    <li>+20 RESTORATION</li>
                    <li>+18 DEFENSE</li>
                    <li>+25 VITALITY</li>
                    <li>+10 SPEED</li>
                    <li>+10 DEXTERITY</li>
                    <li>Fame Bonus: 8%</li>
                </p>
                <h3>How to obtain.</h3>
                <p>
                    <li> This accessory is forged with the Shard of Cosmic Collapse.</li>
                </p>    
                <h3>Usage.</h3>
                <p> 
                    <li class="is-center"> The passive of this ring can be used effeciently to weaken strong mobs, making them easier to defeat. </li>
                </p>    
              </div>
            </div>
          </div>

          </div>
          
</section>
</div>

</template>

<script>
import axios from '~/plugins/axios'
export default {
  async asyncData () {
    let { data } = await axios.get('/users')
    return { users: data }
  },
  head () {
    return {
      title: 'Votr | Legendaries'
    }
  }
}
</script>

<style scoped>
</style>
