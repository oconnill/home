<template>
    <div class="container">
        <!-- Nav Bar -->
        <div class="row content-spacing">
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

        <!-- Bio / Logo -->

        <div class="row content-spacing" v-scroll-reveal.reset>
            <div class="col-sm-6 bio">
                <p>
                    <br>Starting with an idea and a blank page.
                    <br> From pencil to pixel.
                    <br> Back-end to front-end.
                    <br> I'm always trying to
                    <img class="sm-logo" :src="dosmlogo"> more.
                </p>
            </div>
            <div class="col-sm-6 do-cont">
                    <img class="dologo" :src="dologo">
            </div>
        </div>

        <!-- Work -->

        <!-- Row One -->

        <div class="row content-spacing" v-scroll-reveal.reset>
            <div class="col-sm-6 live-projects" v-for="liveProject in liveProjects">
                <div class="content">
                    <div class="content-overlay">
                        <h1>{{ liveProject.description }}</h1>
                    </div>
                    <img class="content-image work-image-l" :src="liveProject.image">
                    <div class="content-details fadeIn-bottom">
                        <button v-if="liveProject.demoLink" class="btn btn-default block-btn">
                            <a v-bind:href="liveProject.demoLink" target="_blank">DEMO</a>
                        </button>
                        <button v-if="liveProject.gitHubLink" class="btn btn-default block-btn">
                            <a v-bind:href="liveProject.gitHubLink" target="_blank">CODE</a>
                        </button>
                    </div>
                </div>
            </div>
        </div>

        <div class="row content-spacing">
            <div class="work-skills">
                <div class="col-sm-6" v-scroll-reveal.reset v-for="projectImage in projectImages">
                    <div v-if="!projectImage.shiftclick">
                        <img class="content-image work-image-l" :src="projectImage">
                    </div>
                    <div v-else>
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
                </div>
            </div>
        </div>

        <div class="row content-spacing" v-scroll-reveal.reset>
            <div class="col-sm-12 bio-copy bio2 content-spacing">
                <p>
                    Daniel O’Connell holds a Bachelor of Fine Arts Degree in Graphic Design from Columbia College
                    Chicago. Daniel currently works as a web developer at Port One Five in Boise, Idaho. He has
                    spent years
                    doing freelance work in the field of packaging design. He created memorable packaging for
                    national
                    recording artists
                    and an international educational movie series. When not freelancing, Daniel maintained an award
                    winning career
                    in mixology and hospitality, where he used his attention to detail and creativity to create featured
                    cocktails in publications
                    such as Chicago Tribune and Mandarin Quarterly. Daniel is also an invested community member who
                    donates time and
                    design work to many local non for profits like The Red Cross, Big Brothers Big Sisters of
                    America,
                    Greater Chicago
                    Food Depository, and The Idaho Foodbank. In his free time he enjoys exploring the outdoors with
                    his
                    fiance and
                    dog.
                </p>
            </div>
            <div class="col-sm-6 bio2">
                <br>
                <p>
                    <br> Web Developer: Port One Five
                    <br> Freelance Designer: Learning Seed
                    <br> Packaging Design: FAK, Alexander Burke, Rich Jones, Magnolia Memoir
                    <br> Print Design: Big Brothers Big Sisters of America
                    <br>
                    <br> Education:
                    <br> Boise Code Works - Immersive Full Stack Developer Course
                    <br> Columbia College - Chicago Bachelors Fine Arts Graphic Design
                </p>
                <div class="social-icon-square2">
                    <a href="mailto:mrdanieloconnellsoffice@gmail.com">
                        <img :src="mail">
                    </a>
                </div>
            </div>
            <div class="col-sm-6">
                <div class="row bio22" v-for="skill in workSkills" v-scroll-reveal.reset>
                    <div class="col-sm-4 skill-name">{{ skill.name }}</div>
                    <div class="col-sm-8">
                        <div class="progress" style="height: 4px;">
                            <div class="progress-bar" role="progressbar"
                                 v-bind:style="{ width: skill.skillLevel + '%' }" aria-valuenow="25"
                                 aria-valuemin="0" aria-valuemax="100"></div>
                        </div>
                    </div>
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
                projectImages: {
                    poster86: require('../assets/1986crop.jpg'),
                    poster91: require('../assets/1991crop.jpg'),
                    earlyfront: require('../assets/earlychildhoodfront.jpg'),
                    earlyback: require('../assets/earlychildhoodback.jpg'),
                    livingwaters: require('../assets/lwrecord.jpg'),
                    magcd: require('../assets/magnoliacd.jpg'),
                    magcase: require('../assets/magnoliamemoirfront.jpg'),
                    blackLine: require('../assets/blacklinelogo.png')
                },
                workSkills: {
                    javascript: {
                        name: 'Javascript',
                        skillLevel: 78
                    },
                    php: {
                        name: 'PHP',
                        skillLevel: 75
                    },
                    vueJs: {
                        name: 'Vuejs',
                        skillLevel: 70
                    },
                    cSharp: {
                        name: 'C#',
                        skillLevel: 35
                    },
                    mySQL: {
                        name: 'mySQL',
                        skillLevel: 55
                    },
                    noSQL: {
                        name: 'noSQL',
                        skillLevel: 65
                    },
                    laravel: {
                        name: 'Laravel',
                        skillLevel: 70
                    },
                    nodeJs: {
                        name: 'Nodejs',
                        skillLevel: 60
                    },
                    wordPress: {
                        name: 'WordPress',
                        skillLevel: 85
                    },
                    html5: {
                        name: 'Html5',
                        skillLevel: 85
                    },
                    css: {
                        name: 'CSS',
                        skillLevel: 81
                    },
                    adobeCreativeSuite: {
                        name: 'Adobe Creative Suite',
                        skillLevel: 74
                    },
                },
                liveProjects: {
                    rvidaho: {
                        name: 'RV Idaho',
                        image: require('../assets/rvidaho_hover.png'),
                        description: 'Built with a development team, a form for brochure sign-up.  All entries could be exported by admin to a .csv file type. Laravel, Javascript, and WordPress were used in the development.',
                        demoLink: 'https://rvidaho.org/free-camping-guide/',
                    },
                    brundage: {
                        name: 'Brundage',
                        image: require('../assets/brundage_hover.png'),
                        description: 'Updated homepage weather widget and worked to bring in a graph displaying snow data for base and summit depth',
                        demoLink: 'https://brundage.com/',
                    },
                    kanban: {
                        name: 'Kanban',
                        image: require('../assets/kanban-hover.png'),
                        description: 'Organize work flow with custom boards, lists, tasks, and notes',
                        demoLink: "https://kanban-oconnell.herokuapp.com/",
                        gitHubLink: 'https://github.com/oconnill/vue-kanban'
                    },
                    musicSelector: {
                        name: 'Music Selector',
                        image: require('../assets/music-selector-hover.png'),
                        description: 'Build a playlist of songs from the I Tunes API',
                        demoLink: 'https://vue-music-oconnell.herokuapp.com/',
                        gitHubLink: 'https://github.com/oconnill/vue-music-checkpoint'
                    },
                    univrss: {
                        name: 'Univ-Rss',
                        image: require('../assets/univrss-hover.png'),
                        description: 'Personal dashboard for weather, rss feeds, local events, todo lists, photos, and spotify',
                        demoLink: '',
                        gitHubLink: 'https://github.com/oconnill/Univ-Rss'
                    },
                    shiftClick: {
                        name: 'Shift Click',
                        image: require('../assets/shiftclickalpha.png'),
                        description: 'Shift Click, an Etch A Sketch inspired font',
                        demoLink: 'http://www.mrdanieloconnell.com/shiftclick.ttf',
                        gitHubLink: ''
                    },
                },
                dosmlogo: require('../assets/dosmlogogreen.png'),
                dologo: require('../assets/do-logo.png'),
                gitlogo: require('../assets/GitHub_Logo.png'),
                instalogo: require('../assets/instagram.png'),
                linkedinlogo: require('../assets/linkedin.png'),
                headshot: require('../assets/headshotcropped.jpg'),
                mail: require('../assets/email-512.png'),
                resume: '../assets/daniel-oconnell-resume.pdf'
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

    .do-cont {
        display: flex;
        justify-content: center;
    }

    .progress-bar {
        background: #16a750;
    }

    .live-projects {
        padding-bottom: 25px;
    }

    .bio-copy {
        text-align: left;
    }

    .content-spacing {
        padding-bottom: 25px;
    }

    .work-skills {
        padding-bottom: 50px;
    }

    /* Buttons */

    .block-btn {
        border-radius: 0;
        background: white;
        border: none;
        font-family: Arial, Helvetica, sans-serif;
        font-weight: bold;
        font-size: 40px;
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

    .work-image-l {
        max-width: 100%;
        max-height: 100%;

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

    .bio22 {
        font-family: Arial, Helvetica, sans-serif;
        font-weight: bold;
        text-align: left;
        font-size: 15px;
        border-left: solid grey 1px;
    }

    .main-image img {
        max-width: 100%;
        overflow: hidden;
        background-size: contain;
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
        font-size: 30px;
        font-weight: bold;
        letter-spacing: 1.3px;
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
        background: #808080;
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

    .skill-name {
        text-align: left;
    }

    @media only screen and (max-width: 480px) {

        body {
            text-align: center;
        }

        .content-overlay {
            display: none;
        }

        .block-btn {
            pointer-events: none;
        }

    }

    @media only screen and (max-width: 320px) {
        .container {
            text-align: center;
        }
    }

</style>
