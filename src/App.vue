<template>
  <div id="app">
    <main>
      <div class="search-box">
        <input type="text"
               class="search-bar"
               placeholder="Recherche..."
               v-model="search"
        />
      </div>

      <div class="weather-wrap">
        <div class="location-box">
          <div class="location">Thiès, SN</div>
          <div class="date">February 11th 2020</div>
        </div>
      </div>

      <div class="weather-box">
        <div class="temp">22°c</div>
        <div class="weather">Ensoleillé</div>
      </div>

      <div class="footer">
        <p>CopyRight @mdwade 2020</p>
      </div>
    </main>


  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {
      api_key: '',
      search: ''
    }
  },
  methods() {

  }

}
</script>

<style lang="scss">
*
{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

main
{
  font-family: 'montserrat', sans-serif;
}

#app
{
  background-image: url('/assets/logo.png');
  background-size: cover;
  background-position: bottom;
  transition: 0.6s;
}

main
{
  min-height: 100vh;
  padding: 50px;
  background-image: linear-gradient(to bottom, rgba(0, 0, 0, 0.25), rgba(0, 0, 0, 0.75));
}

.search-box
{
  width: 100%;
  margin-bottom: 30px;
}

.search-box .search-bar
{
  display: block;
  width: 100%;
  padding: 20px;

  color: #313131;
  font-size: 20px;

  appearance: none;
  border: none;
  outline: none;
  box-shadow: 0 0 8px rgba(0, 0, 0, 0.25);
  background: rgba(255, 255, 255, 0.45) none;
  border-radius: 0 16px 0 16px;
  transition: 0.6s;
}

.search-box .search-bar:focus
{
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.25);
  background-color: rgba(255, 255, 255, 0.75);
  border-radius: 16px 0 16px 0;
}

.location-box .location
{
  color: #ffffff;
  font-size: 32px;
  font-weight: 500;
  text-align: center;
  text-shadow: 1px 3px rgba(0, 0, 0, 0.25);
}

.location-box .date
{
  color: #ffffff;
  font-size: 20px;
  font-weight: 300;
  text-align: center;
  font-style: italic;
  text-shadow: 1px 3px rgba(0, 0, 0, 0.25);
}

.weather-box
{
  text-align: center;
  font-size: 36px;
  font-weight: 600;
  font-style: italic;
  text-shadow: 3px 6px rgba(0, 0, 0, 0.25);
}

.weather-box .temp
{
  display: inline-block;
  padding: 10px 25px;
  color: #ffffff;
  font-size: 102px;
  font-weight: 900;

  text-shadow: 2px 4px rgba(0, 0, 0, 0.25);
  background-color: rgba(255, 255, 255, 0.25);
  border-radius: 16px;
  margin: 30px 0;

  box-shadow: 3px 6px rgba(0, 0, 0, 0.25);
}

.weather-box .weather
{
  color: #ffffff;
}

.footer
{
  position: fixed;
  width: 100%;
  left: 0;
  bottom: 20px;
  color: #ffffff;
  font-size: 12px;
  text-align: center;
}
</style>
