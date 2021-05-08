<template>
  <div>
    <div class="hero">
      <div class="hero-title">
        <span class="hero-name">Ella Luhtasaari</span>
      </div>
      <div class="hero-certs">
        <span>M Mus; ArtDip Guildhall School of Music and Drama</span>
      </div>
      <div class="tagline">
        <span class="tagline-item">Pianist </span>
        <span class="tagline-divider">/ </span>
        <span class="tagline-item">Répétiteur </span>
        <span class="tagline-divider">/ </span>
        <span class="tagline-item">Teacher</span>
      </div>
      <div class="location">
        <div>
          <span>Canberra</span> <span>City</span> - <span>Australia</span>
        </div>
      </div>
      <div class="contact">
        <button class="show-contact" v-on:click="toggleContact">Show contact details</button>
        <div v-if="showContactDetails">
          <div class="p"><a href="tel:0435738743">0435 738 743</a></div>
          <div class="e"><a href="mailto:enquiries@ellaluhtasaari.com">enquiries@ellaluhtasaari.com</a></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
      showContactDetails: false
    }
  },
  methods: {
    toggleContact: function () {
      this.showContactDetails = !this.showContactDetails
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  a {
    color: inherit;
    text-decoration: none;
    border-bottom: 2px dotted;
  }

  .hero {
    margin: 100px auto;
  }

  .hero-name {
    font-size: 58px;
  }

  .hero-certs {
    font-style: italic;
    font-size: 75%;
    line-height: 1;
  }

  .tagline {
    margin-top: 30px;
  }

  .tagline-divider {
    color: #d3d3d3;
    font-size: 200%;
    vertical-align: middle;
    margin-left: 0.25em;
  }

  .location {
    margin-top: 40px;
  }

  .show-contact {
    border: none;
    background: none;
    color: #617181;
    font-weight: 600;
    text-decoration: underline;
    cursor: pointer;
    margin: 20px 0 0px;
  }

  .p, .e {
    margin: 0.5em 0;
  }
</style>
