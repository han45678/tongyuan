<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue';

const splideRef1 = ref(null)
const no1 = ref(0);

const goPrev1 = () => {
  splideRef1.value?.splide.go('-1')
  no1.value = splideRef1.value?.splide.index;
}

const goNext1 = () => {
  splideRef1.value?.splide.go('+1')
  no1.value = splideRef1.value?.splide.index;
}


const splideRef2 = ref(null)
const no2 = ref(0);

const goPrev2 = () => {
  splideRef2.value?.splide.go('-1')
  no2.value = splideRef2.value?.splide.index;
}

const goNext2 = () => {
  splideRef2.value?.splide.go('+1')
  no2.value = splideRef2.value?.splide.index;
}


const splideRef3 = ref(null)
const no3 = ref(0);

const goPrev3 = () => {
  splideRef3.value?.splide.go('-1')
  no3.value = splideRef3.value?.splide.index;
}

const goNext3 = () => {
  splideRef3.value?.splide.go('+1')
  no3.value = splideRef3.value?.splide.index;
}


onMounted(() => {
  if (splideRef1.value) {
    splideRef1.value.splide.on('moved', () => {
      no1.value = splideRef1.value?.splide.index;
    });
  }

  if (splideRef2.value) {
    splideRef2.value.splide.on('moved', () => {
      no2.value = splideRef2.value?.splide.index;
    });
  }

  if (splideRef3.value) {
    splideRef3.value.splide.on('moved', () => {
      no3.value = splideRef3.value?.splide.index;
    });
  }
});

onBeforeUnmount(() => {
  if (splideRef1.value) {
    splideRef1.value.splide.off('moved');
  }

  if (splideRef2.value) {
    splideRef2.value.splide.off('moved');
  }

  if (splideRef3.value) {
    splideRef3.value.splide.off('moved');
  }
});

</script>

<template>
  <article class="s3 relative" id="s3">

    <div class="weapper">
      <div class="title font-['Noto_Sans_TC'] text-[#fff]">
        西區門戶 國門首席 璀璨時代 極刻啟程
      </div>
      <div class="content">
        <div class="item">

          <div class="pic">
            <Splide ref="splideRef1" :options="{
              type: 'slide',       // 使用 slide 模式而非 fade
              autoplay: true,     // 不自動播放
              interval: 5000,      // 可省略，因為 autoplay 是 false
              speed: 1000,         // 切換速度
              arrows: false,        // 顯示左右箭頭 ✅
              pagination: false,    // 顯示下方小點 ✅
              drag: true,          // 可拖曳
              perPage: 1,          // 每頁一張
              rewind: true         // 可循環播放
            }">
              <SplideSlide class="slide">
                <div class="slide_item">
                  <div class="item_pic"><img src="@/section/s3/l_pic01.webp" alt="pic">
                    <span class="font-['Noto_Sans_TC'] text-[#fff]">雙子星3D透視圖</span>
                  </div>

                </div>
              </SplideSlide>
              <SplideSlide class="slide">
                <div class="slide_item">
                  <div class="item_pic"><img src="@/section/s3/l_pic02.webp" alt="pic">
                    <span class="font-['Noto_Sans_TC'] text-[#fff]">雙子星3D透視圖</span>
                  </div>

                </div>
              </SplideSlide>
              <SplideSlide class="slide">
                <div class="slide_item">
                  <div class="item_pic"><img src="@/section/s3/l_pic03.webp" alt="pic">
                    <span class="font-['Noto_Sans_TC'] text-[#fff]">雙子星3D透視圖</span>
                  </div>
                </div>
              </SplideSlide>

              <SplideSlide class="slide">
                <div class="slide_item">
                  <div class="item_pic"><img src="@/section/s3/l_pic04.webp" alt="pic">
                    <span class="font-['Noto_Sans_TC'] text-[#fff]">西區門戶意象</span>
                  </div>
                </div>
              </SplideSlide>
              <SplideSlide class="slide">
                <div class="slide_item">
                  <div class="item_pic"><img src="@/section/s3/l_pic05.webp" alt="pic">
                    <span class="font-['Noto_Sans_TC'] text-[#fff]">一橋北市 (忠孝橋/中興橋)意象</span>
                  </div>
                </div>
              </SplideSlide>
            </Splide>

            <div class="_btn_">
              <div class="splide_btn prev" @click="goPrev1">
                <img src="@/section/s3/prev.svg" alt="prev">
              </div>
              <div class="splide_btn next" @click="goNext1">
                <img src="@/section/s3/next.svg" alt="next">
              </div>
            </div>
          </div>
          <div class="text">
            <h3 class="font-['Noto_Sans_TC'] text-[#EEBA51]">GATEGATEWAY TO THE NATION</h3>
            <h4 class="font-['Noto_Sans_TC'] text-[#fff]">六鐵共構  台北中央車站</h4>
            <p class="font-['Noto_Sans_TC'] text-[#fff]">
              台北中央車站-雙子星國門特區，高級住宅、國際商務、購物休閒、<br>
              五星級飯店一應俱全，台鐵、捷運、高鐵、機場捷運，四通八達，<br>
              國家門戶之首，西區崛起。
            </p>
          </div>

        </div>
        <div class="item">

          <div class="pic">
            <Splide ref="splideRef2" :options="{
              type: 'slide',       // 使用 slide 模式而非 fade
              autoplay: true,     // 不自動播放
              interval: 5000,      // 可省略，因為 autoplay 是 false
              speed: 1000,         // 切換速度
              arrows: false,        // 顯示左右箭頭 ✅
              pagination: false,    // 顯示下方小點 ✅
              drag: true,          // 可拖曳
              perPage: 1,          // 每頁一張
              rewind: true         // 可循環播放
            }">
              <SplideSlide class="slide">
                <div class="slide_item">
                  <div class="item_pic">
                    <img src="@/section/s3/r_pic01.webp" alt="pic">
                    <span class="font-['Noto_Sans_TC'] text-[#fff]">台北車站實景圖</span>
                  </div>

                </div>
              </SplideSlide>
              <SplideSlide class="slide">
                <div class="slide_item">
                  <div class="item_pic"><img src="@/section/s3/r_pic02.webp" alt="pic">
                    <span class="font-['Noto_Sans_TC'] text-[#fff]">台北車站實景圖</span>
                  </div>

                </div>
              </SplideSlide>
              <SplideSlide class="slide">
                <div class="slide_item">
                  <div class="item_pic"><img src="@/section/s3/r_pic03.webp" alt="pic">
                    <span class="font-['Noto_Sans_TC'] text-[#fff]">台北車站實景圖</span>
                  </div>
                </div>
              </SplideSlide>

              <SplideSlide class="slide">
                <div class="slide_item">
                  <div class="item_pic"><img src="@/section/s3/r_pic04.webp" alt="pic">
                    <span class="font-['Noto_Sans_TC'] text-[#fff]">台北車站實景圖</span>
                  </div>
                </div>
              </SplideSlide>
              <SplideSlide class="slide">
                <div class="slide_item">
                  <div class="item_pic"><img src="@/section/s3/r_pic5.webp" alt="pic">
                    <span class="font-['Noto_Sans_TC'] text-[#fff]">台北車站實景圖</span>
                  </div>
                </div>
              </SplideSlide>
              <SplideSlide class="slide">
                <div class="slide_item">
                  <div class="item_pic"><img src="@/section/s3/r_pic06.webp" alt="pic">
                    <span class="font-['Noto_Sans_TC'] text-[#fff]">台北車站實景圖</span>
                  </div>
                </div>
              </SplideSlide>
            </Splide>

            <div class="_btn_">
              <div class="splide_btn prev" @click="goPrev2">
                <img src="@/section/s3/prev.svg" alt="prev">
              </div>
              <div class="splide_btn next" @click="goNext2">
                <img src="@/section/s3/next.svg" alt="next">
              </div>
            </div>
          </div>
          <div class="text">
            <h3 class="font-['Noto_Sans_TC'] text-[#EEBA51]">DRAWS GLOBAL ATTENTION</h3>
            <h4 class="font-['Noto_Sans_TC'] text-[#fff]">首都璀璨  台北雙子星</h4>
            <p class="font-['Noto_Sans_TC'] text-[#fff]">
              西區即刻顛覆，東軸西轉，台北雙子星大樓，挹注建設金額達606億，<br>
              規模超越台北101，西區嶄新門戶，萬眾焦點，舉世矚目。
            </p>
          </div>

        </div>
      </div>

      <img src="@/section/s3/MRT.webp" alt="MRT">

      <div class="content_b">
        <div class="item">

          <div class="text">
            <h3 class="font-['Noto_Sans_TC'] text-[#fff]">極速交通</h3>
            <h4 class="font-['Noto_Sans_TC'] text-[#fff]">A2機捷三重站 新蘆線三重站雙捷匯聚</h4>
            <p class="font-['Noto_Sans_TC'] text-[#fff]">
              1站直達台北車站，快速接軌高鐵與全台捷運網絡，通勤無憂。一線直通桃園國際機場，隨時啟程，連結世界零時差。便捷交通，讓繁華與國際盡在轉瞬之間！
            </p>
          </div>

          <Splide ref="splideRef3" :options="{
            type: 'slide',       // 使用 slide 模式而非 fade
            autoplay: true,     // 不自動播放
            interval: 5000,      // 可省略，因為 autoplay 是 false
            speed: 1000,         // 切換速度
            arrows: false,        // 顯示左右箭頭 ✅
            pagination: false,    // 顯示下方小點 ✅
            drag: true,          // 可拖曳
            perPage: 3,          // 每頁一張
            rewind: true,         // 可循環播放
            gap: '15px'
          }">
            <SplideSlide class="slide">
              <div class="slide_item">
                <div class="item_pic"><img src="@/section/s3/b_pic00.webp" alt="pic">
                  <span class="font-['Noto_Sans_TC'] text-[#fff]">總統府</span>
                </div>

              </div>
            </SplideSlide>
            <SplideSlide class="slide">
              <div class="slide_item">
                <div class="item_pic"><img src="@/section/s3/b_pic01.webp" alt="pic">
                  <span class="font-['Noto_Sans_TC'] text-[#fff]">台大醫院</span>
                </div>

              </div>
            </SplideSlide>
            <SplideSlide class="slide">
              <div class="slide_item">
                <div class="item_pic"><img src="@/section/s3/b_pic02.webp" alt="pic">
                  <span class="font-['Noto_Sans_TC'] text-[#fff]">二二八公園</span>
                </div>
              </div>
            </SplideSlide>

            <SplideSlide class="slide">
              <div class="slide_item">
                <div class="item_pic"><img src="@/section/s3/b_pic03.webp" alt="pic">
                  <span class="font-['Noto_Sans_TC'] text-[#fff]">二二八公園</span>
                </div>
              </div>
            </SplideSlide>
            <SplideSlide class="slide">
              <div class="slide_item">
                <div class="item_pic"><img src="@/section/s3/b_pic04.webp" alt="pic">
                  <span class="font-['Noto_Sans_TC'] text-[#fff]">二二八公園</span>
                </div>
              </div>
            </SplideSlide>
            <SplideSlide class="slide">
              <div class="slide_item">
                <div class="item_pic"><img src="@/section/s3/b_pic05.webp" alt="pic">
                  <span class="font-['Noto_Sans_TC'] text-[#fff]">二二八公園</span>
                </div>
              </div>
            </SplideSlide>
          </Splide>

          <div class="_btn_">
            <div class="splide_btn prev" @click="goPrev3">
              <img src="@/section/s3/prev.svg" alt="prev">
            </div>
            <div class="splide_btn next" @click="goNext3">
              <img src="@/section/s3/next.svg" alt="next">
            </div>
          </div>

        </div>
      </div>
    </div>
    <img class="bg_decor1" src="@/section/s3/bg_decor1.webp" alt="pic">
    <img class="bg_decor2" src="@/section/s3/bg_decor2.webp" alt="pic">
  </article>
</template>

<style lang="scss" scoped>
@import '@/assets/style/function.scss';

.s3 {
  width: 100%;
  position: relative;
  box-sizing: border-box;

  .weapper {
    padding-top: size(150);
    position: relative;
    z-index: 1;

    .title {
      font-size: size(36);
      padding-bottom: size(65);
      font-weight: 500;
      text-align: center;
    }

    .content {
      display: flex;
      flex-wrap: wrap;
      width: 100%;
      max-width: size(1580);
      margin-left: auto;
      margin-right: auto;

      .item {
        display: flex;
        flex-wrap: wrap;

        .pic {
          width: 100%;

          .slide_item {
            .item_pic {
              position: relative;

              img {
                width: 100%;
              }

              span {
                position: absolute;
                bottom: size(15);
                left: size(10);
              }


            }
          }

          ._btn_ {
            margin-top: size(10);
            display: flex;
            justify-content: space-around;
            align-items: center;
            background-color: rgba(0, 0, 0, 0.44);
            width: size(72);
            height: size(22);
            border-radius: size(14);
            position: relative;

            &::before {
              content: "";
              width: size(16);
              height: 1px;
              background-color: #fff;
              transform: rotate(119.74deg);
              position: absolute;
              left: 0;
              right: 0;
              top: 0;
              bottom: 0;
              margin: auto;
            }

            .splide_btn {
              display: flex;
              justify-content: center;
              align-items: center;
              cursor: pointer;
              img {
                width: size(7);
              }
            }
          }
        }

        .text {
          width: 100%;
          display: flex;
          flex-wrap: wrap;

          h3 {
            font-size: size(20);
            font-weight: 100;
            letter-spacing: 0.87em;
            width: 100%;
            order: 1;
          }

          h4 {
            font-size: size(20);
            font-weight: 800;
            width: 100%;
            order: 2;
          }

          p {
            font-size: size(15);
            font-weight: 400;
            width: 100%;
            order: 3;
          }
        }



        &:nth-child(1),
        &:nth-child(2) {
          width: calc(50% - size(7.5));
        }

        &:nth-child(1) {
          margin-right: size(15);
          .pic{
            ._btn_ {

            }
          }
          .text {
            padding-left: size(60);

            h4 {
              order: 1;
              margin-bottom: size(10);
              padding-left: size(100);
            }

            p {
              order: 2;
              margin-bottom: size(35);
              padding-left: size(100);
            }

            h3 {
              order: 3;
            }

          }

        }

        &:nth-child(2) {
          .pic {
            order: 2;
            ._btn_ {
              margin-left: auto;
            }
          }

          .text {
            order: 1;
            padding-left: size(35);
          }
        }

      }
    }

    .content_b {
      width: 100%;
      max-width: size(1580);
      margin-left: auto;
      margin-right: auto;

      .slide_item {
        .item_pic {
          position: relative;

          img {
            width: 100%;
          }

          span {
            position: absolute;
            bottom: size(15);
            left: size(10);
          }
        }
      }
    }
  }

  .bg_decor1 {
    position: absolute;
    left: 0;
    top: size(-400);
  }

  .bg_decor2 {
    position: absolute;
    right: 0;
    top: size(700);
  }
}
</style>
