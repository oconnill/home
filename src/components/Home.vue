<template>
  <div>

    <div class="container">
      <!-- Nav Bar -->
      <div class="row navbar">
        <div class="col-sm-4 circle-align">
          <div class="linktype logo-align nametype">

          </div>
        </div>
        <div class="col-sm-4 text-center logo-align nametype">
          <h3>Daniel O'Connell</h3>
        </div>
        <div class="col-sm-4 social-icon-align">
          <div class="social-icon-square">
            <a href="https://www.linkedin.com/in/daniel-o-connell-19a85865">
              <img :src="linkedinlogo">
            </a>
          </div>
          <div class="social-icon-rectangle">
            <a href="https://github.com/oconnill">
              <img :src="gitlogo">
            </a>
          </div>
        </div>
      </div>

      <!-- Spacer -->

      <div class="row">
        <div class="col-xs-12 spacer"></div>
      </div>

      <!-- Bio / Logo -->

      <div class="row">
        <div class="col-sm-6 bio">
          <p>
            <br>Starting with an idea and a blank page.
            <br> From pencil to pixel.
            <br> Back-end to front-end.
            <br> I'm always trying to
            <img class="sm-logo" :src="dosmlogo"> more.
          </p>
        </div>
        <div class="col-sm-6">
          <a target="_blank" href="http://www.mrdanieloconnell.com/daniel-oconnell-resume.pdf" download="../assets/daniel-oconnell-resume.pdf">
            <img class="dologo" :src="dologo">
          </a>
        </div>
      </div>

      <!-- Spacer -->

      <div class="row">
        <div class="col-xs-12 spacer"></div>
      </div>



      <!-- Work -->

      <!-- Row One -->

      <div class="row">
        <div class="col-sm-6">
          <div class="content">
            <div class="content-overlay">
              <h1>Build a playlist of songs from the I Tunes API</h1>
            </div>
            <img class="content-image work-image-l" :src="musicSelector">
            <div class="content-details fadeIn-bottom">
              <button class="btn btn-default block-btn">
                <a target="_blank" href="https://vue-music-oconnell.herokuapp.com/">DEMO</a>
              </button>
              <button class="btn btn-default block-btn">
                <a target="_blank" href="https://github.com/oconnill/vue-music-checkpoint">CODE</a>
              </button>
            </div>
          </div>
        </div>
        <div class="col-sm-6">
          <div class="content">
            <div class="content-overlay">
              <h1>Organize work flow with custom boards, lists, tasks, and notes</h1>
            </div>
            <img class="content-image work-image-r" :src="kanban">
            <div class="content-details fadeIn-bottom">
              <button class="btn btn-default block-btn">
                <a target="_blank" href="https://kanban-oconnell.herokuapp.com/">DEMO</a>
              </button>
              <button class="btn btn-default block-btn">
                <a target="_blank" href="https://github.com/oconnill/vue-kanban">CODE</a>
              </button>
            </div>
          </div>
        </div>
      </div>

      <!-- Spacer -->

      <div class="row">
        <div class="col-xs-12 spacer"></div>
      </div>


      <!-- Row Two -->

      <div class="row">
        <div class="col-sm-6" v-scroll-reveal.reset>
          <div class="content">
            <div class="content-overlay">
            </div>
          </div>
        </div>
        <div class="col-sm-6" v-scroll-reveal.reset>
          <div class="content">
            <div class="content-overlay">
              <h1>Personal dashboard for weather, rss feeds, local events, todo lists, photos, and spotify</h1>
            </div>
            <img class="content-image work-image-l" :src="univrss">
            <div class="content-details fadeIn-bottom">
              <!-- <button class="btn btn-default block-btn">
                    <a href="https://vue-music-oconnell.herokuapp.com/">DEMO</a>
                  </button> -->
              <button class="btn btn-default block-btn">
                <a target="_blank" href="https://github.com/oconnill/Univ-Rss">CODE</a>
              </button>
            </div>
          </div>
        </div>
      </div>

      <!-- Spacer -->

      <div class="row">
        <div class="col-xs-12 spacer"></div>
      </div>

      <!-- Row Three -->

      <div class="row">
        <div class="col-sm-6" v-scroll-reveal.reset>
          <img class="content-image work-image-l" :src="poster86">
        </div>
        <div class="col-sm-6" v-scroll-reveal.reset>
          <img class="content-image work-image-l" :src="poster91">
        </div>
      </div>

      <!-- Spacer -->

      <div class="row">
        <div class="col-xs-12 spacer"></div>
      </div>

      <!-- Row Four -->

      <div class="row">
        <div class="col-sm-6" v-scroll-reveal.reset>
          <img class="content-image work-image-l" :src="earlyfront">
        </div>
        <div class="col-sm-6" v-scroll-reveal.reset>
          <img class="content-image work-image-l" :src="earlyback">
        </div>
      </div>

      <!-- Spacer -->

      <div class="row">
        <div class="col-xs-12 spacer"></div>
      </div>

      <!-- Row Five -->

      <div class="row">
        <div class="col-sm-6" v-scroll-reveal.reset>
          <div class="content">
            <div class="content-overlay">
              <h1>Shift Click, an Etch A Sketch inspired font</h1>
            </div>
            <img class="content-image work-image-l" :src="shiftclick">
            <div class="content-details fadeIn-bottom">
              <button class="btn btn-default block-btn">
                <a href="http://www.mrdanieloconnell.com/shiftclick.ttf" download>DOWNLOAD</a>
              </button>
            </div>
          </div>
        </div>
        <div class="col-sm-6" v-scroll-reveal.reset>
          <img class="content-image work-image-l" :src="livingwaters">
        </div>
      </div>

      <!-- Spacer -->

      <div class="row">
        <div class="col-xs-12 spacer"></div>
      </div>

      <!-- Row six -->

      <div class="row">
        <div class="col-sm-6 rev" v-scroll-reveal.reset>
          <img class="content-image work-image-l" :src="magcd">
        </div>
        <div class="col-sm-6 rev" v-scroll-reveal.reset>
          <img class="content-image work-image-l" :src="magcase">
        </div>
      </div>

      <!-- Spacer -->

      <div class="row">
        <div class="col-xs-12 spacer"></div>
      </div>

      <div class="row">
        <div class="col-xs-6 bio2">
          Daniel O’Connell holds a Bachelor of Fine Arts Degree in Graphic Design from Columbia College Chicago. Daniel spent years
          doing freelance work in the field of packaging design. He created memorable packaging for national recording artists
          and an international educational movie series. When not freelancing, Daniel maintained an award winning career
          in beverage hospitality, where he used his attention to detail and creativity to create featured cocktails in publications
          such as Chicago Tribune and Mandarin Quarterly. Daniel is also an invested community member who donates time and
          design work to many local non for profits like The Red Cross, Big Brothers Big Sisters of America, Greater Chicago
          Food Depository, and The Idaho Foodbank. In his free time he enjoys exploring the outdoors with his fiance and
          dog in Boise, Idaho.
          <br>
          <p>
            <br> Freelance Designer: Learning Tree
            <br> Packaging Design: FAK, Alexander Burke, Rich Jones, Magnolia Memoir
            <br> Print Design: Big Brothers Big Sisters of America
            <br>
            <br> Education:
            <br> Boise Code Works - Immersive Full Stack Developer Course
            <br> Columbia College - Chicago Bachelors Fine Arts Graphic Design
          </p>
          <div class="social-icon-square2">
            <a href="mailto:mrdanieloconnellsoffice@gmail.com">
              Contact
              <img :src="mail">
            </a>
          </div>
        </div>
        <div class="col-xs-6 biopic text-right">
          <img :src="headshot" alt="">
        </div>
      </div>

      <!-- Spacer -->

      <div class="row">
        <div class="col-xs-12 spacer"></div>
      </div>

    </div>

  </div>
  </div>
</template>

<script>
  export default {
    name: 'Home',
    data() {
      return {
        // developement
        dologo: require('../assets/do-logo.png'),
        gitlogo: require('../assets/GitHub_Logo.png'),
        instalogo: require('../assets/instagram.png'),
        linkedinlogo: require('../assets/linkedin.png'),
        headshot: require('../assets/headshotcropped.jpg'),
        mail: require('../assets/email-512.png'),
        musicSelector: require('../assets/music-selector-hover.png'),
        univrss: require('../assets/univrss-hover.png'),
        kanban: require('../assets/kanban-hover.png'),
        // design
        poster86: require('../assets/1986crop.jpg'),
        poster91: require('../assets/1991crop.jpg'),
        earlyfront: require('../assets/earlychildhoodfront.jpg'),
        earlyback: require('../assets/earlychildhoodback.jpg'),
        shiftclick: require('../assets/shiftclickalpha.png'),
        livingwaters: require('../assets/lwrecord.jpg'),
        dosmlogo: require('../assets/dosmlogogreen.png'),
        magcd: require('../assets/magnoliacd.jpg'),
        magcase: require('../assets/magnoliamemoirfront.jpg'),
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  body {
    background-color: #FFFFFF;
  }

  .sm-logo {
    height: 23px;
    width: 45px;

  }

  .rev {
    height: 50vh;
  }

  /* Buttons */

  .block-btn {
    border-radius: 0;
    background: white;
    border: none;
    font-family: Arial, Helvetica, sans-serif;
    font-weight: bold;
    font-size: 40px;
    /* color:#16a750; */
    margin: 10px
  }

  a:link {
    color: orangered;
  }

  /* visited link */

  a:visited {
    color: orangered;
  }

  /* mouse over link */

  a:hover {
    color: black;
    text-decoration: none;
  }

  /* Buttons */

  .right-handle {
    display: flex;
    justify-content: flex-end;
  }

  .work-image-l {
    max-width: 100%;
    max-height: 100%;

  }

  .work-image-r {
    max-width: 100%;
    max-height: 100%;
    text-align: right;

  }

  .dologo {
    height: 200px;
    width: 200px;
  }

  .nametype {
    font-family: Arial, Helvetica, sans-serif;
    font-weight: bold
  }

  .linktype {
    font-family: Arial, Helvetica, sans-serif;
    font-weight: bold
  }

  .bio {
    font-family: Arial, Helvetica, sans-serif;
    font-weight: bold;
    text-align: left;
    font-size: 30px
  }

  .bio2 {
    font-family: Arial, Helvetica, sans-serif;
    font-weight: bold;
    text-align: left;
    font-size: 15px;
  }

  .circle {
    width: 18px;
    height: 18px;
    background: #333333;
    -moz-border-radius: 50px;
    -webkit-border-radius: 50px;
    border-radius: 50px;
  }

  .main-image img {
    max-width: 100%;
    overflow: hidden;
    background-size: contain;
  }

  .spacer {
    height: 25px;
    background-color: #FFFFFF;
  }

  .spacer-black {
    height: 25px;
    background-color: #333333;
  }

  .social-icon-align {
    display: flex;
    justify-content: flex-end;
    padding-right: 10px;
    padding-top: 30px;
  }

  .social-icon-square img {
    width: 30px;
    height: 30px;
  }

  .social-icon-square2 img {
    width: 20px;
    height: 20px;
  }

  .social-icon-rectangle img {
    height: 30px;
  }

  .logo-align {
    padding-top: 10px;
  }

  .logo-align img {
    height: 70px;
  }

  .thumbnail-gallery-align {
    display: flex;
    justify-content: space-around;
  }

  .thumbnail-gallery-align img:hover {
    background-color: #798A94;
    cursor: pointer;
  }

  hr {
    border-width: 2px;
    border-color: #798A94;
  }

  .biopic img {
    height: 300px;
  }

  h5 {
    padding-top: 15px;
  }

  h3 {
    font-size: 25px;
    font-weight: bold
  }

  h1 {
    font-size: 40px;
    font-weight: bold;
    font-family: Arial, Helvetica, sans-serif;
    color: #fff
  }



  /* Hover  */

  .content {
    position: relative;
    width: 100%;
    overflow: hidden;
  }

  .content .content-overlay {
    background: orangered;
    position: absolute;
    height: 100%;
    width: 100%;
    text-align: left;
    padding-left: 15px;
    -webkit-transition: all 0.4s ease-in-out 0s;
    -moz-transition: all 0.4s ease-in-out 0s;
    transition: all 0.4s ease-in-out 0s;
  }

  .content:hover .content-overlay {
    opacity: 0;
  }

  .content-image {
    width: 100%;
  }

  .content-details {
    position: absolute;
    text-align: center;
    padding-left: 1em;
    padding-right: 1em;
    width: 100%;
    top: 50%;
    left: 50%;
    opacity: 0;
    -webkit-transform: translate(-50%, -50%);
    -moz-transform: translate(-50%, -50%);
    transform: translate(-50%, -50%);
    -webkit-transition: all 0.3s ease-in-out 0s;
    -moz-transition: all 0.3s ease-in-out 0s;
    transition: all 0.3s ease-in-out 0s;
  }

  .content:hover .content-details {
    top: 50%;
    left: 50%;
    opacity: 1;
  }

  .content-details h3 {
    color: #fff;
    font-weight: 500;
    letter-spacing: 0.15em;
    margin-bottom: 0.5em;
    text-transform: uppercase;
  }

  .content-details p {
    color: #fff;
    font-size: 0.8em;
  }

  .fadeIn-bottom {
    top: 80%;
  }

  .fadeIn-top {
    top: 20%;
  }

  .fadeIn-left {
    left: 20%;
  }

  .fadeIn-right {
    left: 80%;
  }
</style>
