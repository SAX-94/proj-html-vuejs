<template>
    <div class="container">
        <div class="header_jumbo_container">
            <div class="bg_color">
                <!-- HEADER - NAVBAR -->
                <div class="container_header">
                    <a href="#"><img src="../assets/img/theme_eduprime_logo.png" alt="logo"></a>
                    <nav>
                        <ul>
                            <li v-for="(link, i) in links" :key="i">
                                <a :href="link.url" :class="link.current ? 'active' : ''"
                                    @click="link.current = !link.current">
                                    {{ link.text }}
                                    <font-awesome-icon class="icon_down" icon="fa-solid fa-caret-down" />
                                </a>
                            </li>
                        </ul>
                        <button class="btn_yellow">
                            VIEW COURSES
                        </button>
                    </nav>
                </div>

<!-------   JUMBOTRON   ------->
                <div class="container_jumbo">
                    <h2 class="title_jumbo">
                        Key to your success
                    </h2>

                    <p>EduPrime is the most versatile WordPress theme for educational purposes, showcasting
                        universities, courses, secondary school etc.</p>

                    <div class="btn_container">
                        <button class="btn_yellow">
                            <font-awesome-icon icon="fa-solid fa-magnifying-glass" /> Search courses
                        </button>

                        <button class="btn_white">
                            <font-awesome-icon icon="fa-solid fa-user-plus" /> Apply for university
                        </button>
                    </div>
                </div>

            </div>

        </div>

        <div class="wave_container">
            <img src="../assets/img/Wave-1.png" alt="">
        </div>
    </div>
</template>

<script>
export default {
    name: 'TheHeader',
    data() {
        return {
            links: [
                {
                    text: "Home",
                    url: "#",
                    current: false
                },
                {
                    text: "Courses",
                    url: "#",
                    current: false
                },
                {
                    text: "About Us",
                    url: "#",
                    current: false
                },
                {
                    text: "News",
                    url: "#",
                    current: false
                },
                {
                    text: "Pages",
                    url: "#",
                    current: false
                },
                {
                    text: "Contact",
                    url: "#",
                    current: false
                },
                {
                    text: "Purchase",
                    url: "#",
                    current: false
                }
            ]
        }
    },
}
</script>


<!--******************************
-------      STYLE      -------
*******************************-->


<style scoped lang="scss">
@import '../assets/button.scss';

/* -- CUSTOMIZED YELLOW -- */
$yellow_clr: #E9D758;

/* -- GENERAL -- */
ul {
    display: inline-block;
}

.header_jumbo_container {
    background-image: url("../assets/img/theme_slider2_bg-1.jpg");
    height: 500px;
    background-size: cover;
    background-repeat: no-repeat;
    position: relative;
    font-weight: 700;
    color: white;

    .bg_color {
        background-color: rgba($color: #E56768, $alpha: 0.8);
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
    }

    .container_header {

        display: flex;
        justify-content: space-between;
        align-items: center;
        padding-top: 2rem;
        padding-left: 1.3rem;
        padding-right: 1.7rem;

        img {
            width: 200px;
            margin: 0 20px;
        }
        
        .btn_yellow:hover {
            background-color: white;
            color: #E56768;
        }

        ul {
            list-style-type: none;
            margin: 20px 0;

            li {
                display: inline-block;

                a {
                    color: white;
                    text-decoration: none;
                    padding: 0 10px;
                    font-weight: 800;

                    &.active {
                        color: $yellow_clr;
                    }

                    &:hover {
                        color: $yellow_clr;
                    }
                }
            }
        }

    }

    .icon_down {
        font-size: 10px;
        margin-left: 5px;
        margin-bottom: 2px;
    }
}

.container_jumbo {
    width: 40%;
    margin: 0 auto;
    text-align: center;

    .title_jumbo {
        font-size: 50px;
        margin-top: 30px;
        font-weight: 900;
    }

    p {
        margin: 20px;
        font-weight: 400;
    }
}

.wave_container {
    position: relative;

    img {
        width: 100%;
        display: block;
        position: absolute;
        bottom: 0;
        left: 0;
    }
}
</style>