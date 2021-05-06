<template>
  <v-app>
    <v-navigation-drawer
      class="mx-auto"
      v-if="drawer"
      app
      style="background-color: #0f131e"
      width="auto"
      height="auto"
      permanent
    >
      <v-list>
        <!-- <center><b>Пиши:</b></center> -->
        <v-list-item v-for="(item, i) in items" :key="i" link>
          <v-list-item-icon>
            <v-icon style="color:white">{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title style="color:white"
              ><a
                :href="item.url"
                target="_blank"
                style="color: white;text-decoration: none;"
                >{{ item.title }}</a
              ></v-list-item-title
            >
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar style="background-color: #0f131e" dense dark app>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title
        ><v-img
          :src="require('@/assets/logo_frendex.png')"
          max-height="50px"
          max-width="80px"
        ></v-img
      ></v-toolbar-title>

      <v-spacer></v-spacer>
    </v-app-bar>

    <v-sheet
      id="scrolling-techniques-3"
      class="overflow-y-auto"
      style="background-color: #15172e"
    >
      <v-container style="height: auto;margin-top: 50px;">
        <v-card-text style="color:white;font-size: 15px;"
          ><p style="text-align:center;font-size: 39px;line-height: 1.1;">
            ФРЕНДЕКС, МОЖНО ЛИ ЗАРАБОТАТЬ?
          </p>
        </v-card-text>

        <v-row dense>
          <v-col
            cols="3"
            style="min-width: 100px; max-width: 100%;"
            class="flex-grow-1 flex-shrink-0"
          >
            <v-card
              class="mx-auto"
              max-width="344"
              style="background-color: #151821;color:white;box-shadow: 0 0 10px rgb(0 0 0);"
            >
              <v-img
                :src="require('@/assets/ainur.png')"
                height="400px"
              ></v-img>

              <v-card-title>
                Меня зовут Айнур
              </v-card-title>

              <v-card-subtitle
                style="color:white;font-style: italic;font-size: 15px;line-height: 1.6;"
              >
                Если вам интересен пассивный доход, инструмент, который будет
                приносить деньги, даже когда вы сидите дома, то вам думаю, будет
                интересен проект ФРЕНДЕКС
              </v-card-subtitle>
            </v-card>
          </v-col>
          <v-col
            cols="8"
            style="min-width: 100px; max-width: 100%;margin-left:20px;margin-right:20px;"
            class="flex-grow-1 flex-shrink-0"
          >
            <v-card
              class="mx-auto"
              style="background-color: #151821;color:white;box-shadow: 0 0 10px rgb(0 0 0);"
            >
              <v-card-title style="font-size: 19px;">
                Frendex - закрытый инвестиционный клуб, благодаря которому
                каждый желающий<br />может начать зарабатывать от 0,7% до 2%
                ежедневно.
              </v-card-title>
              <hr />
              <v-card-subtitle
                style="line-height: 2;font-size: 16.4px;color:white;"
                >Из множества компаний с высокой доходностью я выбрал именно эту
                по следующим причинам:<br />

                - Компания довольно свежая. Дата старта август 2020г.<br />

                - Нет негативных отзывов. Все выплаты вкладчики получают вовремя
                и благополучно.<br />

                - Большая доходность. От 30% в месяц, от вложенной суммы. (То
                есть, вложенные средства оправдываются уже за 3 месяца, затем
                выходишь на чистую прибыль).<br />

                - Нет комиссии за вывод средств. К примеру, в других подобных
                компаниях везде существует комиссия за вывод.<br />

                - Можно внести любую сумму, начиная от 100 долларов.<br />

                - И лично для меня, существенным плюсом компании является
                возможность реинвестирования средств. Можно создать
                капитализацию средств своего счета Френдекс. Можно добавлять
                полученные дивиденды к своему депозиту и уже будет работать
                общая сумма (изначальный депозит-плюс полученные дивиденды).<br />

                - Считаю важным плюсом открытость основателя Френдекс -
                <b>Руслана Пичугина</b>. Он ездит по городам и рассказывает про
                свое детище.
              </v-card-subtitle>
            </v-card>
          </v-col>
        </v-row>
        <v-row dense>
          <v-col
            cols="6"
            style="min-width: 100px; max-width: 100%;margin-top: 30px;"
            class="flex-grow-1 flex-shrink-0"
          >
            <v-card
              class="mx-auto"
              style="background-color: #151821;color:white;box-shadow: 0 0 10px rgb(0 0 0);"
            >
              <v-card-title>
                Деньги инвесторов<br />трейдеры компании<br />Френдекс
                вкладывают<br />в такие направления как:
              </v-card-title>
              <hr />
              <v-card-subtitle
                style="line-height: 1.7;font-size: 16px;color:white"
              >
                - Выкуп с торгов недвижимости банкротов по выгодной цене<br />-
                Эффективные сделки на Московской бирже и валютном рынке<br />-
                Строительный бизнес<br />- Развитие стартапов<br /><br />Доходность
                компании составляет<br />3-5 % в день.<br />Из полученных денег
                почти треть идет на выплату партнерам, то есть НАМ!<br />Остальное
                тратят на хозяйственные нужды, зарплату сотрудникам компании и
                формирование резерва.
              </v-card-subtitle>
            </v-card>
          </v-col>
          <v-col
            cols="5"
            style="min-width: 100px; max-width: 100%;margin-top: 30px;margin-left:20px;margin-right:20px;"
            class="flex-grow-1 flex-shrink-0"
          >
            <v-carousel
              cycle
              style="box-shadow: 0 0 10px rgb(0 0 0);border-radius: 5px;"
              height="auto"
              hide-delimiter-background
              show-arrows-on-hover
            >
              <v-carousel-item v-for="(slide, i) in slides" :key="i">
                <center>
                  <img
                    :lazy-src="slide.src"
                    :src="slide.src"
                    style="margin-bottom: -7px;"
                    width="100%"
                    heigth="100%"
                    :alt="slide.src"
                  />
                </center>
              </v-carousel-item>
            </v-carousel>
          </v-col>
        </v-row>
        <v-row dense>
          <v-col
            cols="12"
            style="min-width: 100px; max-width: 100%;"
            class="flex-grow-1 flex-shrink-0"
          >
            <v-card
              class="mx-auto"
              style="background-color: #151821;box-shadow: 0 0 10px rgb(0 0 0);margin-top: 30px;"
            >
              <v-card-subtitle
                style="color:white;
                font-size:16px;
                line-height:1.8;"
              >
                Масштабность и успех закрытого инвестиционного клуба Frendex
                видна в открытии офисов и получении автомобилей. Также
                проводятся конференции, планируют открыть офис в Москве и многих
                городах бывшего СНГ.<br />Реальные отзывы о Френдекс появляются
                на Youtube и в общем Telegram чате. Люди вкладывают большие
                деньги. Веской причиной добавления проекта в портфель стал
                переход лидеров из разных инвестиционных программ.<br />Просто
                так происходить такие процессы не могут. Это значит, что в
                будущем будут строить мощные команды, а главное, что в интернете
                информации еще практически о клубе нет. Если будет ребрендинг,
                тогда только начнется основная раскачка.
              </v-card-subtitle>
            </v-card>
          </v-col>
        </v-row>

        <v-row dense>
          <v-col
            cols="5"
            style="min-width: 100px; max-width: 100%;margin-top: 30px;margin-right:10px;"
            class="flex-grow-1 flex-shrink-0"
          >
            <v-card
              class="mx-auto"
              style="background-color: #151821;color:white;box-shadow: 0 0 10px rgb(0 0 0);"
            >
              <v-img :src="require('@/assets/auto.png')" height="auto"></v-img>
            </v-card>
          </v-col>
          <v-col
            cols="6"
            style="min-width: 200px; max-width: 100%;margin-top: 30px;margin-left:10px;"
            class="flex-grow-1 flex-shrink-0"
          >
            <v-card
              class="mx-auto"
              style="background-color: #151821;color:white;box-shadow: 0 0 10px rgb(0 0 0);"
            >
              <v-card-title>
                Auto за часть от ее стоимости
              </v-card-title>
              <hr />

              <v-card-title style="line-height: 2;font-size: 16px;color:white"
                >В компании так же есть возможность приобрести поддержанное или
                новое авто за часть от ее стоимости.<br /><br />⦁ Взнос 30% —
                130 дней ожидания — 2% вознаграждение<br /><br />⦁ Взнос 35% —
                120 дней ожидания — 3% вознаграждение<br /><br />⦁ Взнос 40% —
                110 дней ожидания — 4% вознаграждение
              </v-card-title>
            </v-card>
          </v-col>
        </v-row>
        <v-row dense style="margin-top:30px;margin-bottom:30px;">
          <v-col
            cols="12"
            style="min-width: 100px; max-width: 100%;"
            class="flex-grow-1 flex-shrink-0"
          >
            <v-card
              class="mx-auto"
              style="background-color: #151821;color:white;box-shadow: 0 0 10px rgb(0 0 0);"
            >
              <v-img :src="require('@/assets/result.png')"></v-img>

              <v-card-title>
                Мое личное мнение, в проект Френдекс можно вложиться смело.
              </v-card-title>

              <v-card-subtitle
                style="color:white;font-size: 18px;line-height: 2;"
              >
                По всем признакам она еще проживет достаточно долго. Мой
                результат на скрине с личного кабинета.<br />
                <b>Для начала я вложил 4000 долларов.</b><br />
                <v-btn
                  class=""
                  :loading="loading2"
                  :disabled="loading2"
                  style="max-width: 100%;"
                  color="success"
                  href="https://frendex.org/I/7805659"
                  target="_blank"
                  @click="loader = 'loading2'"
                >
                  РЕГИСТРАЦИЯ ФРЕНДЕКС
                  <template v-slot:loader>
                    <span style="color: grey;">Переход...</span>
                  </template>
                </v-btn>
              </v-card-subtitle>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-sheet>
    <v-footer padless style="background-color: #0f131e">
      <v-divider></v-divider>
      <!-- <v-col class="text-center" cols="12"> -->
      <v-card-text class="py-2 white--text text-center">
        <strong style="text-decoration: none;">
          <a
            href="https://frendex.org/I/7805659"
            target="_blank"
            style="color: white;text-decoration: none;font-size: 18px;"
            >FrendeX</a
          >
          {{ new Date().getFullYear() }}</strong
        >
      </v-card-text>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      items: [
        {
          title: "Мой telegram",
          icon: "mdi-telegram",
          url: "https://t.me/ainur134dd"
        },
        {
          title: "Регистрация Френдекс",
          icon: "mdi-view-dashboard",
          url: "https://frendex.org/I/7805659"
        }
      ],
      drawer: false,
      // tab: null,
      // itemsTab: ["Главная страница", "О компании"],
      slides: [
        { src: require("@/assets/slide.png") },
        { src: require("@/assets/slide1.png") },
        { src: require("@/assets/slide2.png") }
      ],
      loader: null,
      loading2: false
    };
  },
  watch: {
    loader() {
      const l = this.loader;
      this[l] = !this[l];

      setTimeout(() => (this[l] = false), 1500);

      this.loader = null;
    }
  }
};
</script>

<style>
#app {
  color: #15172e;
}
.navigation {
  color: #15172e;
}
.bar {
  color: #15172e;
}
img {
  /* box-shadow: 0 0 10px rgb(0 0 0);
  border-radius: 10px; */
}
</style>
