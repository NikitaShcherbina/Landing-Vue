<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang="scss">
  @import "scss/fonts";

#app {
  background: #fff;
  color: #000;
  cursor: auto;
  font-family: cera_proregular,Helvetica,Roboto,Arial,sans-serif;
  font-style: normal;
  font-weight: 400;
  line-height: 1.5;
  margin: 0;
  padding: 0;
  position: relative;
  font-size: 100%;
  .container {
    max-width: 80rem;
    width: 100%;
    margin: 0 auto;
  }
}
body {
    margin: 0;
    font-size: 16px;
}
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
h1 {

  font-family: 'Museo 300', sans-serif;
    font-size: 2.625rem;
    line-height: 1.1;
}
h2 {
  font-family: cera_proregular,Helvetica,Roboto,Arial,sans-serif;
  font-size: 1.688rem;
    line-height: 1.2;
    text-transform: none;
    margin-bottom: 10px;
    font-style: normal;
    font-weight: 400;
    color: #000;
}
h3 {
  font-size: 0.9rem;
  font-style: normal;
  font-weight: 550;
}
ul {
  list-style: none;
}
p {
  font-family: cera_proregular,Helvetica,Roboto,Arial,sans-serif;
  font-size: .938rem;
  font-weight: 400;
  line-height: 1.4;
  text-rendering: optimizeLegibility;
}
  @media screen and (max-width: 1350px) {
    #app {
      font-size: 13px;
      .container {
        max-width: 70rem;
      }
    }
  }
  @media screen and (max-width: 1023px) {
  #app {
    .container {
      max-width: 100%;
      width: 87%;
    }
    header {
      background: url("~@/assets/img/burger.png") no-repeat 5% center , url("~@/assets/img/shop.png") no-repeat 95% center;
      nav {
        .logo {
          margin: 0 auto;
          img {
            width: 200px;
          }
        }
      }
      .main-menu {
        display: none;
      }
    }
    main {
      .header {
        display: flex;
        justify-content: flex-end;
        align-items: flex-end;
        min-height: 30rem;
        background-size: auto 120%;
        background-position: 12% 100%;

        .info-block {
          margin-right: 0rem;
          padding: 2.1rem 1rem 0.7rem 1rem;
          width: 100%;
          .h1-center {
            font-size: 2.025rem;
          }
        }
      }
      .products {
        margin-top: 30px;
        .container {
          position: relative;
          .slider-holder {
            position: absolute;
            top: 225.5px;
            width: 100%;
          }
          .right {
            width: 100%;
            h2 {
              font-size: 1.288rem;
            }
            .info-product {
              #add-to-card {
                margin: 0 auto;
                min-width: 22rem;
              }
            }
            .buttons {
              flex-wrap: wrap;
              margin-bottom: 363px;
              .b {
                margin-top: 10px;
              }
            }
          }
        }
      }
      .testPaket {
        .pakets {
          display: flex;
          flex-direction: column;
          padding-bottom: 0;
          .paket {
            margin-bottom: 40px;
            padding-bottom: 0;
            .imgPaket {
              margin-left: 30px;
              margin-right: 42px;
            }
          }
        }
      }
      .workFlow {
        .stepsContainer {
          padding-top: 2rem;
          .steps {
            display: flex;
            flex-direction: column;
            margin-top: 0;
            .step1, .step2, .step3 {
              width: 100%;
              margin-top: 30px;
            }
          }
        }
      }
      .reviews {
        padding-top: 1.3rem;
        .container {
          .title {
            h2 {
              font-size: 1.188rem;
            }
          }
          .team {
            .review {
              p {
                font-size: 0.738rem;
              }
              span {
                font-size: 0.638rem;
              }
              img {
                width: 20%;
                margin-right: 33px;
                margin-top: 15px;
              }
            }
          }
        }
      }
    }
    footer {
      .submitButton {
        align-items: center;
        overflow: hidden;
        .button {
          width: 20.5rem;
          font-size: 0.8rem;
        }
        .bg {
          width: auto;
          height: 150px;
        }
        .title {
          h2 {
            margin-top: 0px;
            margin-bottom: 20px;
          }
        }
        .cardIcons {
          flex-direction: column;
          .left {
            flex-direction: column;
          }
        }
        .linksLogo {
          .links {
            flex-direction: column;
          }
        }
      }
      .contacts {
        .flex {
          display: flex;
          flex-direction: column;
          a {
            margin-bottom: 20px;
          }
          .social {
            i {
              font-size: 25px!important;
            }
          }
        }
        .linksLogo {
          img {
            height: 50px;
          }
          .copywriting {
            font-size: 0.638rem;
          }
          .links {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            p {
              font-size: 0.638rem;
            }
          }
        }
      }
      .cardIcons {
        flex-direction: column;
        padding: 0;
        align-items: center;
        .flexRow {
          margin-top: 20px;
          align-items: center;
          .left {
            flex-wrap: wrap;
            justify-content: center;
          }
        }
        .row {
          display: flex;
          flex-direction: column;
          align-items: center;
          margin-bottom: 20px;
        }
      }
    }
  }
  }

</style>
