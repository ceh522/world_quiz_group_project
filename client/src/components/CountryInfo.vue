<template lang="html">
  <div class="info-container">
    <ul>
      <li id="country-title">{{mapCountryInfo.name}}</li>
      <li>Capital: {{mapCountryInfo.capital}}</li>
      <li>Population: {{mapCountryInfo.population}}</li>
      <li>Region: {{mapCountryInfo.subregion}}</li>
      <li>Area: {{mapCountryInfo.area}}km²</li>
      <li> <img class="small-flag" :src="mapCountryInfo.flag" alt="NoneApplicable"> </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'countryInfo',
  props: ['mapCountryInfo']



}

</script>

<style lang="css" scoped>
.info-container {
  border: solid black 2px;
  width: 80%;
  text-align: left;
  justify-content: space-around;
  background-color: white;
}

@media screen and (max-width: 1050px) {
  .info-container {
    width: 30%;
    margin-bottom: 2em;
  }
}

ul{
  list-style: none;

}

.small-flag {
  height: 30px;
  border: solid black 2px;
}

#country-title {
  text-decoration: underline;
  margin-bottom: 2px;
}
</style>
