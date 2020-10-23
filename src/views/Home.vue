<template>
  <div class="home">
    <header>
      <nav class="container">
        <a href="/" class="logo">
          <img src="@/assets/img/logo.png" alt="logo">
        </a>
        <section class="main-menu">
          <ul class="nav">
            <li class="gratis">
              <a href="#">Gratis Testpaket</a>
            </li>
            <li class="flexibles">
              <a href="#">Flexibles Abo</a>
            </li>
            <li class="product">
              <a href="#">Produkte</a>
            </li>
            <li class="magazin">
              <a href="#">Magazin</a>
            </li>
            <li class="uber">
              <a href="#">Über LILLYDOO</a>
            </li>
          </ul>
        </section>
      </nav>
    </header>
    <main>
      <section class="header">
        <div class="info-block">
          <h1 class="h1-center">Dein gratis Testpaket</h1>
          <a href="/" class="button">Wähle Deine Größe</a>
        </div>
      </section>
      <section class="products">
        <div class="container">
          <div class="slider-holder">
            <img src="@/assets/img/oekotex_green_de.svg" alt="logo" class="logobg">
            <div class="slider">
              <img
                  v-for="product in products"
                  v-show="activeProduct === product.value"
                  :src="product.img"
                  :alt="product.value"
              >
            </div>
          </div>
          <div class="right">
            <h2>Entdecke unsere Hautfreundlichkeit</h2>
            <p class="deine-text">Wähle Deine Größe</p>
            <div class="buttons">
              <label class="b" v-for="(product, index) in products">
                <input :value="product.value" type="radio" name="buttons-slider" v-model="activeProduct">
                <p>{{index + 1}}</p>
                <span>({{product.value}})</span>
                <span class="bg"></span>
              </label>
            </div>
            <div class="info-product">
              <p>Teste jetzt unsere hautfreundlichen Windeln und erhalte unsere<br>
                Feuchttücher mit 99 % Wasser zu Größe 1 - 3 oder die Sensitiven<br>
                Feuchttücher zu Größe 4 - 5.</p>
              <ul class="product">
                <li>
                  • Wir zahlen die Produkte, Du nur den Versand.
                </li>
                <li class="color-active">
                  • Automatischer Übergang ins jederzeit kündbare Windel-Abo für <br> 49,50&nbsp;€ pro Lieferung.
                </li>
                <li>
                  • Preise inkl. MwSt., ggf. zzgl.
                  <a href="/" target="/" rel="/">Versandkosten</a>
                </li>
              </ul>
              <button href="/" id="add-to-card">
                <span>In den Warenkorb legen</span>
              </button>
            </div>
          </div>
        </div>
      </section>
      <section class="workFlow">
        <div class="container">
          <div class="stepsContainer">
            <div class="title">
              <h2>Wie es funktioniert</h2>
            </div>
            <div class="steps">
              <div class="step1">
                <img src="@/assets/img/1.png" alt="step" class="first">
                  <h3>DEIN TESTPAKET</h3>
                  <p>Wir zahlen die Produkte,<br> Du nur den Versand.</p>
              </div>
              <div class="step2">
                  <img src="@/assets/img/2.png" alt="step" class="second">
                    <h3>DEINE FLEXIBILITAT</h3>
                    <p>Erste Monatsbox nach 14 Tagen fur 49,50 € erhalten <br> Order noch vor der ersten Lieferung kundigen.</p>
              </div>
              <div class="step3">
                <img src="@/assets/img/3.png" alt="step" class="third">
                  <h3>DEINE MONATSBOX</h3>
                  <p>Jederzeit Windelgobe, Designs und Lieferintervalle <br> anpassen oder weitere Produkte hinzufügen.</p>
              </div>
            </div>
          </div>
          <div class="bottomText">
            <p>Erfahre hier mehr über das <br>LILLYDOO Windel-Abo</p>
          </div>
        </div>
      </section>
      <section class="testPaket">
        <div class="container">
          <div class="title">
            <h2>Test Dein Testpaket enthalt</h2>
          </div>
          <div class="pakets">
            <div class="paket">
              <img src="@/assets/img/test1.png" alt="paket" class="imgPaket">
              <div class="right">
              <h3>10 LILLYDOO WIDELN</h3>
              <star-rating :rating='4.5' :star-size="25" :increment="0.5"></star-rating>
                <ul>
                  <li>
                    • Wir zahlen die Produkte, Du nur den Versand.
                  </li>
                  <li>
                    • Wir zahlen die Produkte, Du nur den Versand.
                  </li>
                  <li>
                    • Wir zahlen die Produkte, Du nur den Versand.
                  </li>
                </ul>
              </div>
            </div>
            <div class="paket">
              <img src="@/assets/img/test2.png" alt="paket" class="paket2">
              <div class="right">
                <h3>10 LILLYDOO WIDELN</h3>
                <star-rating :rating='4.5' :star-size="25" :increment="0.5"></star-rating>
                <ul>
                  <li>
                    • Wir zahlen die Produkte, Du nur den Versand.
                  </li>
                  <li>
                    • Wir zahlen die Produkte, Du nur den Versand.
                  </li>
                  <li>
                    • Wir zahlen die Produkte, Du nur den Versand.
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </section>
      <section class="reviews">
        <div class="container">
          <div class="title">
            <h2>Was andere uber unsere Windeln sagen</h2>
          </div>
          <div class="team">

            <div class="review">
              <img src="@/assets/img/photo1.png" alt="face" class="paket2" width="12%" height="12%">
              <div class="text">
                <p>Teste jetzt unsere hautfreundlichen Windeln und erhalte unsere <br>
                  Feuchttücher mit 99 % Wasser zu Größe 1 - 3 oder die Sensitiven <br> Feuchttücher zu Größe 4 - 5.</p>
                <p class="bold">Uwe Gensheimer-<span>Teste jetzt unsere hautfreundlichen Windeln und erhalte unsere</span></p>
              </div>
            </div>

            <div class="review">
              <img src="@/assets/img/photo2.png" alt="face" class="paket2" width="12%" height="12%">
              <div class="text">
                <p>Teste jetzt unsere hautfreundlichen Windeln und erhalte unsere <br>
                  Feuchttücher mit 99 % Wasser zu Größe 1 - 3 oder die Sensitiven <br> Feuchttücher zu Größe 4 - 5.</p>
                <p class="bold">Uwe Gensheimer-<span>Teste jetzt unsere hautfreundlichen Windeln und erhalte unsere</span></p>
              </div>
            </div>

            <div class="review">
              <img src="@/assets/img/photo3.png" alt="face" class="paket2" width="12%" height="12%">
              <div class="text">
                <p>Teste jetzt unsere hautfreundlichen Windeln und erhalte unsere <br>
                  Feuchttücher mit 99 % Wasser zu Größe 1 - 3 oder die Sensitiven <br> Feuchttücher zu Größe 4 - 5.</p>
                <p class="bold">Uwe Gensheimer-<span>Teste jetzt unsere hautfreundlichen Windeln und erhalte unsere</span></p>
              </div>
            </div>

          </div>
        </div>
      </section>
    </main>
    <footer class="footer">
      <div class="submitButton">
        <div class="title">
          <h2>Uberzeug Dich selbst</h2>
        </div>
        <a href="/" class="button">Wähle Deine Größe</a>
        <img src="@/assets/img/bg.png" alt="bg" class="bg">
      </div>
      <div class="contacts">
        <div class="text">
          <p class="center">Wir wollen mehr für Dich sein, nicht nur Wickeln und Tschüss. Also ruf gerne an oder schreib uns! </p>
        </div>
        <div class="flex">
          <a class="" href="mailto:service@lillydoo.de">service@lillydoo.de</a>
          <a href="tel:+496964357420">+49 (0) 69 - 643 57 420</a>
          <div class="social">
            <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
            <i class="fa fa-facebook" style="font-size:36px"></i>
            <i class="fa fa-instagram" style="font-size:36px"></i>
            <i class="fa fa-youtube" style="font-size:36px"></i>
          </div>
        </div>
        <div class="cardIcons">
          <div class="flexRow">
            <p>Sicher bezahlen mit:</p>
            <div class="left">
              <img src="@/assets/img/visa.svg" alt="bg" class="bg">
              <img src="@/assets/img/mastercard.svg" alt="bg" class="bg">
              <img src="@/assets/img/paypal.svg" alt="bg" class="bg">
              <img src="@/assets/img/rechnung.svg" alt="bg" class="bg">
              <img src="@/assets/img/sepa.svg" alt="bg" class="bg">
            </div>
          </div>
          <div class="row">
            <p>Unser Versandparther:</p>
            <div class="right">
              <img src="@/assets/img/dhl.svg" alt="bg" class="bg">
            </div>
          </div>
        </div>
        <div class="linksLogo">
          <div class="links">
            <p>LILLYDOO App</p>
            <p>Zahlung & Versand</p>
            <p>Karriere</p>
            <p>Presse</p>
            <p>AGB</p>
            <p>Datenschtzeklarung</p>
            <p>Impressum</p>
          </div>
          <div class="logos">
            <img src="@/assets/img/trustmark_120x120.png" alt="bg" class="secondLogo">
            <img src="@/assets/img/reddot-logo.svg" alt="bg" class="firstLogo">
          </div>
          <p class="copywriting">
            © 2020 LILLYDOO GmbH
          </p>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>

import StarRating from 'vue-star-rating'

export default {
  name: 'Home',
  components: {
    StarRating
  },
  data() {
    return {
      products: [
        {
          value: '2-5 KG',
          img: require('@/assets/img/lillydoo-testpaket-10.jpg')
        },
        {
          value: '4-8 KG',
          img: require('@/assets/img/lillydoo-testpaket-20.jpg')
        },
        {
          value: '6-10 KG',
          img: require('@/assets/img/lillydoo-testpaket-30.jpg')
        },
        {
          value: '9-14 KG',
          img: require('@/assets/img/lillydoo-testpaket-40.jpg')
        },
        {
          value: '11-16 KG',
          img: require('@/assets/img/lillydoo-testpaket-50.jpg')
        },
      ],
      activeProduct: '2-5 KG',
    }
  }
}
</script>

<style lang="scss">

  header {
    display: flex;
    justify-content: center;
    background: #f8f8f8;
    width: 100%;
    height: 80px;
    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      .logo {
        img {
          width: 252px;
        }
      }
      ul {
        display: flex;
        list-style: none;
        li {
          margin-left: 40px;
          a {
            text-transform: uppercase;
            text-decoration: none;
            color: #000;
            font-size: 1rem;
            &:hover {
              color: #00afab;
            }
          }
          &.gratis {
            a {
              color: #00afab;
            }
          }
          &.magazin {
            margin-left: 110px;
          }
        }
      }
    }
  }
  main {
    .header {
      background: url('~@/assets/img/header-bg.jpg') no-repeat center center / cover, #f2f0ec;
      min-height: 38rem;
      display: flex;
      align-items: center;
      justify-content: flex-end;
      .info-block {
        padding: 2.5rem 2.5rem 1.5rem 2.5rem;
        width: 31.25rem;
        margin-right: 4rem;
        background: rgba(255,255,255,.7);
        display: flex;
        flex-direction: column;
        align-items: center;
        .h1-center {
          margin-bottom: 1rem;
          text-align: center!important;
        }
        .button {
          display: flex;
          width: 18.1rem;
          margin-top: 1rem;
          margin-bottom: 1rem;
          justify-content: center;
          background-color: #00afab;
          color: #fafafa;
          text-decoration: none;
          line-height: 1.4375rem;
          transition: .3s ease-in-out;
          padding: .5rem 1.25rem .4375rem 1.25rem;
          font-family: cera_proregular,Helvetica,Roboto,Arial,sans-serif;
          text-transform: uppercase;
          font-size: 1rem;
        }
      }
    }
    .products {
      .container {
        display: flex;
        justify-content: space-between;
        align-items: flex-end;
        .slider-holder {
          position: relative;
          width: 50%;
          .logobg {
            position: absolute;
            width: 24%;
            top: 13%;
            left: 9%;
            z-index: 10;
            box-shadow: -2px 2px 6px -3px rgba(0,0,0,.4);
            border-radius: 3px;
          }
          .slider {
            width: 100%;
            img {
              width: 100%;
            }
          }
        }
        .right {
          width: 40%;
          h2 {
            font-size: 1.688rem;
            line-height: 1.2;
            text-transform: none;
            margin-bottom: 10px;
          }
          p {
            margin-bottom: 0.1rem
          }
          span {
            font-size: .8rem;
          }
          .deine-text {
            text-transform: uppercase;
          }
          .buttons {
            display: flex;
            margin-bottom: 30px;
            .b {
              display: flex;
              justify-content: center;
              flex-direction: column;
              align-items: center;
              text-align: center;
              width: 30%;
              padding: 7px 5px 2px 5px;
              color: #7c7c7c;
              margin-right: 10px;
              z-index: 1;
              position: relative;
              cursor: pointer;
              p {
                font-size: 20px;
              }
              .bg {
                position: absolute;
                border-color: #00afab;
                left: 0;
                top: 0;
                width: 100%;
                height: 100%;
                border: 1px solid #7c7c7c;
                z-index: -1;
              }
              &:hover {
                border-color: #00afab;
                background-color: #00afab;
                color: #fff;
              }
              input {
                position: absolute;
                left: 0;
                top: 0;
                width: 100%;
                height: 100%;
                opacity: 0;
                z-index: 1000;
                cursor: pointer;
                &:checked~ {
                  p, span {
                    color: #fff;
                  }
                  .bg {
                    background-color: #00afab;
                  }
                }
              }
            }
          }
          .info-product {
            p {
              margin-bottom: 15px;
            }
            .product {
              margin-bottom: 2rem;
              .color-active {
                color: #00afab;
              }
              a {
                color: #00afab;
                line-height: inherit;
                text-decoration: none;
              }
            }
            #add-to-card {
              display: flex;
              justify-content: center;
              background-color: #00afab;
              color: #fafafa;
              text-decoration: none;
              text-transform: uppercase;
              font-family: cera_proregular,Helvetica,Roboto,Arial,sans-serif;
              font-size: 1rem;
              line-height: 1.4375rem;
              font-weight: 500;
              padding: .5rem 1.25rem .4375rem 1.25rem;
              outline: 0;
              border: 1px solid #00afab;
              transition: .3s ease-in-out;
              margin: .875rem 0 .625rem 0;
              appearance: none;
              position: relative;
              min-width: 16rem;
              cursor: pointer;
            }
          }
        }
      }
    }
    .workFlow {
      background: #f8f8f8;
      .stepsContainer {
        padding-top: 4rem;
        margin: 1.875rem 0;
        .title {
          h2 {
            display: flex;
            justify-content: center;
          }
        }
        .steps {
          display: flex;
          justify-content: space-between;
          margin-top: 50px;
          .step1, .step2, .step3 {
            width: 30%;
            display: flex;
            flex-direction: column;
            align-items: center;
            h3 {
              margin: 0.4rem;
            }
            p {
              text-align: center;
            }
          }
        }
      }
      .bottomText {
        display: flex;
        justify-content: center;
        color: #00afab;
        padding-bottom: 4rem;
        p {
          text-align: center;
        }
      }
    }
    .testPaket {
      .title {
        h2 {
          display: flex;
          justify-content: center;
          margin-top: 50px;
          margin-bottom: 80px;
        }
      }
      .pakets {
        display: flex;
        justify-content: space-between;
        margin-top: 50px;
        padding-bottom: 4.2rem;
        align-items: center;
        .paket {
          display: flex;
          align-items: center;
          ul {
            list-style: none;
          }
          img {
            margin-right: 10px;
          }
        }
      }
    }
    .reviews {
      display: flex;
      justify-items: center;
      padding-top: 4rem;
      margin: 1.875rem 0;
      background: #f8f8f8;
      .container {
        .title {
          h2 {
            display: flex;
            justify-content: center;
          }
        }
        .team {
          display: flex;
          flex-direction: column;
          margin-bottom: 80px;
          .review {
            display: flex;
            justify-content: center;
            align-items: center;
            img {
              margin-top: 45px;
              margin-right: 45px;
            }
            p {
              margin-top: 25px;
              &.bold {
                font-weight: bold;
                span {
                  color: #00afab;
                }
              }
            }
          }
        }
      }
    }
  }
  footer {
    .submitButton {
      display: flex;
      flex-direction: column;
      .title {
        h2 {
          display: flex;
          justify-content: center;
          margin-top: 50px;
          margin-bottom: 80px;
        }
      }
      .button {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 18.1rem;
        margin-top: 1rem;
        margin-bottom: 1rem;
        background-color: #00afab;
        color: #fafafa;
        text-decoration: none;
        line-height: 1.4375rem;
        transition: .3s ease-in-out;
        padding: .5rem 1.25rem .4375rem 1.25rem;
        font-family: cera_proregular,Helvetica,Roboto,Arial,sans-serif;
        text-transform: uppercase;
        font-size: 1rem;
        margin: 0 auto;
        margin-bottom: 50px;
      }
      .bg {
        width: 100%;
      }
    }
    .contacts {
      background-color: #00afab;
      color: white;
      .text {
        text-align: center;
        padding-top: 50px;
      }
      .flex {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 40%;
        margin: 0 auto;
        padding-top: 20px;
        padding-bottom: 20px;
        a {
          color: white;
          text-decoration: none;
          line-height: 1.4375rem;
        }
        .social {
          i {
            margin: 10px 10px 10px;
          }
        }
      }
      .cardIcons {
        display: flex;
        justify-content: space-between;
        color: #000;
        background: #f8f8f8;
        padding: 2.2rem 0;
        padding-left: 25%;
        padding-right: 25%;
        margin: 0 auto;
        p {
          margin-bottom: .5rem;
        }
        img {
          width: 92px;
        }
        .flexRow {
          display: flex;
          flex-direction: column;
          img {
            margin: 0 .5rem .5rem 0;
          }
          .left {
            display: flex;
            justify-content:flex-start;
          }
          .right {
            display: flex;
            justify-content: flex-end;
          }
        }
      }
      .linksLogo {
        display: flex;
        align-items: center;
        flex-direction: column;
        background: #fff;
        color: #000;
        .links {
          display: flex;
          p {
            margin: 1.1rem;
          }
        }
        .logos {
          img {
            height: 92px;
            margin: 10px;
          }
        }
        .copywriting {
          margin: 1.1rem;
        }

      }
    }
  }
</style>
