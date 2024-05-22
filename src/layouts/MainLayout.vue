<template>
  <div class="screen">
    <div class="main-container" :class="$q.screen.gt.xs ? 'large' : 'small'">
      <div class="header">
        <button class="btn" v-show="$q.screen.gt.xs">
          <span class="inquiry">문의하기</span>
        </button>
        <div class="menus">
          <div
            ref="dropdown"
            @click="showMenu = !showMenu"
            class="frame"
            v-show="$q.screen.gt.xs"
          >
            <span class="recruitment">{{ selectedOption }}</span>
            <div class="navi-caret-down"></div>
          </div>
          <div class="dropdown-menu" v-if="showMenu">
            <ul>
              <li
                :class="{ selected: option === selectedOption }"
                @click="selectOption(option)"
                v-for="option in dropdownOptions"
                :key="option"
              >
                {{ option }}
              </li>
            </ul>
          </div>
          <span class="overseas-developer-service" v-show="$q.screen.gt.xs"
            >해외 개발자 활용 서비스</span
          >
        </div>
        <div class="logo" :class="$q.screen.gt.xs ? 'large' : 'small'">
          <div class="group"></div>
          <div class="vector"></div>
          <div class="vector-1"></div>
          <div class="vector-2"></div>
          <div class="vector-3"></div>
          <div class="vector-4"></div>
          <div class="vector-5"></div>
          <div class="vector-6"></div>
          <div class="vector-7"></div>
          <div class="vector-8"></div>
          <div class="vector-9"></div>
        </div>
        <img
          v-show="!$q.screen.gt.xs"
          class="burger-icon"
          src="../assets/images/Burger_Icon.svg"
          alt=""
        />
      </div>
      <div class="flex-row-ab">
        <transition name="fadein500" appear v-show="$q.screen.gt.xs">
          <button class="frame-a">
            <div class="group-b"></div>
            <span class="monthly-100k">월 100만원</span>
          </button>
        </transition>
      </div>
      <transition name="fadein500" appear v-show="!$q.screen.gt.xs">
        <button class="frame-a tooltip-small">
          <div class="group-b"></div>
          <span class="monthly-100k">월 100만원</span>
        </button>
      </transition>
      <div class="flex-row-be" :class="$q.screen.gt.xs ? 'large' : 'small'">
        <transition name="delay" appear>
          <div class="frame-c" :class="$q.screen.gt.xs ? 'large' : 'small'">
            <button
              class="frame-d"
              :class="$q.screen.gt.xs ? 'large' : 'small'"
            >
              <span
                class="full-part-time"
                :class="$q.screen.gt.xs ? 'large' : 'small'"
                >풀타임, 파트타임</span
              >
            </button>
            <!-- <div class="frame-e"><div class="polygon-f"></div></div> -->
          </div>
        </transition>
        <transition name="fadein500" appear>
          <swiper
            :modules="modules"
            :effect="'coverflow'"
            :grabCursor="true"
            :initialSlide="2"
            :spaceBetween="-168"
            :allowTouchMove="false"
            :centeredSlides="true"
            :loop="true"
            :slidesPerView="'auto'"
            :coverflowEffect="{
              rotate: 0,
              stretch: 0,
              depth: 80,
              modifier: 2.5,
              slideShadows: false,
            }"
            :navigation="{
              nextEl: '.swiper-button-next',
              prevEl: '.swiper-button-prev',
            }"
            v-show="$q.screen.gt.xs"
          >
            <swiper-slide>
              <div class="frame-10">
                <!-- Slide 1 -->
                <div class="frame-11">
                  <div class="group-12"></div>
                  <div class="frame-13">
                    <span class="abhishek-gupta" style="color: darkmagenta"
                      >Abhishek Gupta</span
                    ><span class="marketing-2y">마케팅 · 2y+</span>
                  </div>
                </div>
                <div class="frame-14">
                  <div class="frame-15">
                    <button class="frame-16">
                      <span class="marketing-content-creation"
                        >마케팅 콘텐츠 제작</span
                      ></button
                    ><button class="frame-17">
                      <span class="instagram-management">인스타그램 관리</span>
                    </button>
                  </div>
                  <div class="group-18">
                    <button class="frame-button">
                      <span class="span-twitter-management"
                        >트위터 관리</span
                      ></button
                    ><button class="frame-button-19">
                      <span class="span-blog-writing">블로그 글 작성</span>
                    </button>
                  </div>
                </div>
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="frame-10">
                <!-- Slide 2 -->
                <div class="frame-11">
                  <div class="group-12"></div>
                  <div class="frame-13">
                    <span class="abhishek-gupta" style="color: crimson"
                      >Abhishek Gupta</span
                    ><span class="marketing-2y">마케팅 · 2y+</span>
                  </div>
                </div>
                <div class="frame-14">
                  <div class="frame-15">
                    <button class="frame-16">
                      <span class="marketing-content-creation"
                        >마케팅 콘텐츠 제작</span
                      ></button
                    ><button class="frame-17">
                      <span class="instagram-management">인스타그램 관리</span>
                    </button>
                  </div>
                  <div class="group-18">
                    <button class="frame-button">
                      <span class="span-twitter-management"
                        >트위터 관리</span
                      ></button
                    ><button class="frame-button-19">
                      <span class="span-blog-writing">블로그 글 작성</span>
                    </button>
                  </div>
                </div>
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="frame-10">
                <!-- Slide 3 -->
                <div class="frame-11">
                  <div class="group-12"></div>
                  <div class="frame-13">
                    <span
                      class="abhishek-gupta"
                      style="color: rgb(41 42 60 / 89%)"
                      >Abhishek Gupta</span
                    ><span class="marketing-2y">마케팅 · 2y+</span>
                  </div>
                </div>
                <div class="frame-14">
                  <div class="frame-15">
                    <button class="frame-16">
                      <span class="marketing-content-creation"
                        >마케팅 콘텐츠 제작</span
                      ></button
                    ><button class="frame-17">
                      <span class="instagram-management">인스타그램 관리</span>
                    </button>
                  </div>
                  <div class="group-18">
                    <button class="frame-button">
                      <span class="span-twitter-management"
                        >트위터 관리</span
                      ></button
                    ><button class="frame-button-19">
                      <span class="span-blog-writing">블로그 글 작성</span>
                    </button>
                  </div>
                </div>
              </div>
            </swiper-slide>
          </swiper>
        </transition>
        <transition name="fadein500" appear>
          <swiper
            :modules="modules"
            :effect="'coverflow'"
            :grabCursor="true"
            :initialSlide="1"
            :spaceBetween="-175"
            :allowTouchMove="false"
            :centeredSlides="true"
            :loop="true"
            :slidesPerView="'auto'"
            :coverflowEffect="{
              rotate: 0,
              stretch: 0,
              depth: 300,
              modifier: 2.5,
              slideShadows: false,
            }"
            :navigation="{
              nextEl: '.nav-bt-right',
              prevEl: '.nav-bt-left',
            }"
            v-show="!$q.screen.gt.xs"
            class="swiper-small"
          >
            <swiper-slide>
              <div class="frame-10">
                <!-- Slide 1 -->
                <div class="frame-11">
                  <div class="group-12"></div>
                  <div class="frame-13">
                    <span class="abhishek-gupta" style="color: darkmagenta"
                      >Abhishek Gupta</span
                    ><span class="marketing-2y">마케팅 · 2y+</span>
                  </div>
                </div>
                <div class="frame-14">
                  <div class="frame-15">
                    <button class="frame-16">
                      <span class="marketing-content-creation"
                        >마케팅 콘텐츠 제작</span
                      ></button
                    ><button class="frame-17">
                      <span class="instagram-management">인스타그램 관리</span>
                    </button>
                  </div>
                  <div class="group-18">
                    <button class="frame-button">
                      <span class="span-twitter-management"
                        >트위터 관리</span
                      ></button
                    ><button class="frame-button-19">
                      <span class="span-blog-writing">블로그 글 작성</span>
                    </button>
                  </div>
                </div>
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="frame-10">
                <!-- Slide 1 -->
                <div class="frame-11">
                  <div class="group-12"></div>
                  <div class="frame-13">
                    <span class="abhishek-gupta" style="color: crimson"
                      >Abhishek Gupta</span
                    ><span class="marketing-2y">마케팅 · 2y+</span>
                  </div>
                </div>
                <div class="frame-14">
                  <div class="frame-15">
                    <button class="frame-16">
                      <span class="marketing-content-creation"
                        >마케팅 콘텐츠 제작</span
                      ></button
                    ><button class="frame-17">
                      <span class="instagram-management">인스타그램 관리</span>
                    </button>
                  </div>
                  <div class="group-18">
                    <button class="frame-button">
                      <span class="span-twitter-management"
                        >트위터 관리</span
                      ></button
                    ><button class="frame-button-19">
                      <span class="span-blog-writing">블로그 글 작성</span>
                    </button>
                  </div>
                </div>
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="frame-10">
                <!-- Slide 1 -->
                <div class="frame-11">
                  <div class="group-12"></div>
                  <div class="frame-13">
                    <span
                      class="abhishek-gupta"
                      style="color: rgb(41 42 60 / 89%)"
                      >Abhishek Gupta</span
                    ><span class="marketing-2y">마케팅 · 2y+</span>
                  </div>
                </div>
                <div class="frame-14">
                  <div class="frame-15">
                    <button class="frame-16">
                      <span class="marketing-content-creation"
                        >마케팅 콘텐츠 제작</span
                      ></button
                    ><button class="frame-17">
                      <span class="instagram-management">인스타그램 관리</span>
                    </button>
                  </div>
                  <div class="group-18">
                    <button class="frame-button">
                      <span class="span-twitter-management"
                        >트위터 관리</span
                      ></button
                    ><button class="frame-button-19">
                      <span class="span-blog-writing">블로그 글 작성</span>
                    </button>
                  </div>
                </div>
              </div>
            </swiper-slide>
          </swiper>
        </transition>
        <transition name="fadein500" appear>
          <div
            class="nav-bt nav-bt-left nav-caret-left"
            v-show="!$q.screen.gt.xs"
          ></div>
        </transition>
        <transition name="fadein500" appear>
          <div
            class="nav-bt nav-bt-right nav-caret-right"
            v-show="!$q.screen.gt.xs"
          ></div>
        </transition>
        <div class="checkboxes-texts" v-show="!$q.screen.gt.xs">
          <div class="checkbox-text">
            <img src="../assets/images/checkbox.png" alt="" class="checkbox" />
            <span class="text">한국어 능력</span>
          </div>
          <div class="checkbox-text">
            <img src="../assets/images/checkbox.png" alt="" class="checkbox" />
            <span class="text">업무 수행 능력</span>
          </div>
          <div class="checkbox-text">
            <img src="../assets/images/checkbox.png" alt="" class="checkbox" />
            <span class="text">겸업 여부</span>
          </div>
          <div class="checkbox-text">
            <img src="../assets/images/checkbox.png" alt="" class="checkbox" />
            <span class="text">평판 조회</span>
          </div>
        </div>
        <div class="cin-and-address">
          <div class="cin-number" v-show="!$q.screen.gt.xs">
            <div class="cin-text">사업자등록번호 CIN</div>
            <div>427-86-01187</div>
            <div>U74110DL2016PTC290812</div>
          </div>
          <div class="address-bottom" v-show="!$q.screen.gt.xs">
            <div class="address-text">주소 ADDRESS</div>
            <div>서울특별시 강남대로 479, 지하 1층 238호</div>
            <div>
              D-138, Street number 11, Jagjeet Nagar, North East Delhi, New
              Delhi,
              <br />110053 India
            </div>
          </div>
        </div>
        <transition name="title" appear>
          <span
            class="developer-needed"
            v-show="!$q.screen.gt.xs"
            :class="$q.screen.gt.xs ? 'large' : 'small'"
            >개발자가 필요하신가요?</span
          >
        </transition>
        <transition name="title" appear>
          <div
            class="foreign-talent-recruitment"
            :class="$q.screen.gt.xs ? 'large' : 'small'"
          >
            <span
              class="span-best-skill"
              :class="$q.screen.gt.xs ? 'large' : 'small'"
              >최고의 실력</span
            >
            <span class="span-with" :class="$q.screen.gt.xs ? 'large' : 'small'"
              >을 가진<br
            /></span>
            <span
              class="span-best-skill-36"
              :class="$q.screen.gt.xs ? 'large' : 'small'"
              >외국인 인재</span
            >
            <span
              class="span-looking-for"
              :class="$q.screen.gt.xs ? 'large' : 'small'"
              >를 찾고 계신가요?</span
            >
          </div>
        </transition>
        <!-- <transition name="title" appear>
          <span class="fade-in-up-500ms">FadeInUp(duration 500ms)</span>
        </transition> -->
        <!-- <transition name="title" appear>
          <span class="fade-in-up-500ms-37">FadeInUp(500ms)</span>
        </transition> -->
        <transition name="title" appear>
          <span
            class="law-hr-remote-recruitment"
            :class="$q.screen.gt.xs ? 'large' : 'small'"
            >법률 및 인사관리 부담없이<br v-show="$q.screen.gt.xs" />1주일
            이내에 원격으로 채용해보세요.</span
          >
        </transition>
        <transition name="fadein500" appear v-show="$q.screen.gt.xs">
          <div class="swiper-button-prev nav-caret-left"></div>
        </transition>
        <transition name="fadein500" appear v-show="$q.screen.gt.xs">
          <div class="swiper-button-next nav-caret-right"></div>
        </transition>
        <transition name="title" appear>
          <span class="developer-needed" v-show="$q.screen.gt.xs"
            >개발자가 필요하신가요?</span
          >
        </transition>
        <!-- <transition name="fadein500" appear>
          <span class="fade-in">fade in 3 at once(500ms)</span>
        </transition> -->
        <transition name="fadein500" appear>
          <div class="frame-39" v-show="$q.screen.gt.xs">
            <div class="frame-3a">
              <div class="line"></div>
              <span class="average-salary">평균 월 120만원</span
              ><span class="calculate-salary"
                >임금을 해당 국가를 기준으로 계산합니다.</span
              >
            </div>
            <div class="frame-3b">
              <div class="line-3c"></div>
              <span class="max-3-replacements">최대 3회 인력교체</span
              ><span class="worry-free-hiring"
                >막상 채용해보니 맞지 않아도 걱정하지 마세요.
              </span>
            </div>
            <div class="frame-3d">
              <div class="line-3e"></div>
              <span class="average-3-days">평균 3일, 최대 10일</span
              ><span class="quick-hiring"
                >급하게 사람이 필요한 경우에도 빠른 채용이 가능합니다.</span
              >
            </div>
          </div>
        </transition>
      </div>
      <transition name="fadein500" appear>
        <div class="flex-row-ea">
          <!-- <span class="slide-left"
            >fadeIn(500ms)<br /><br />Slides to the left by one every 5
            seconds</span
          > -->
          <div class="frame-3f slide-to-left slider" v-show="$q.screen.gt.xs">
            <Splide :options="options">
              <SplideSlide>
                <div class="frame-40 slide">
                  <div class="frame-41"><div class="icon-marketing"></div></div>
                  <div class="frame-42">
                    <span class="overseas-marketing">해외 마케팅</span>
                  </div>
                </div>
              </SplideSlide>
              <SplideSlide>
                <div class="frame-43 slide">
                  <div class="frame-44"><div class="icon-image"></div></div>
                  <div class="frame-45">
                    <span class="publisher">퍼블리셔</span>
                  </div>
                </div>
              </SplideSlide>
              <SplideSlide>
                <div class="frame-46 slide">
                  <div class="frame-47">
                    <div class="icon-box">
                      <div class="group-48">
                        <div class="lw-polyline">
                          <div class="group-49">
                            <div class="vector-4a"></div>
                          </div>
                        </div>
                        <div class="line-4b">
                          <div class="group-4c">
                            <div class="vector-4d"></div>
                          </div>
                        </div>
                        <div class="line-4e">
                          <div class="group-4f">
                            <div class="vector-50"></div>
                          </div>
                        </div>
                        <div class="line-51">
                          <div class="group-52">
                            <div class="vector-53"></div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                  <div class="frame-54">
                    <span class="cad-one">캐드원(제도사)</span>
                  </div>
                </div>
              </SplideSlide>
              <SplideSlide>
                <div class="frame-55 slide">
                  <div class="frame-56"><div class="icon-target"></div></div>
                  <div class="frame-57">
                    <span class="overseas-sales">해외 세일즈</span>
                  </div>
                </div>
              </SplideSlide>
              <SplideSlide>
                <div class="frame-58 slide">
                  <div class="frame-59"><div class="icon-call"></div></div>
                  <div class="frame-5a">
                    <span class="overseas-cs">해외 CS</span>
                  </div>
                </div>
              </SplideSlide>
              <!-- <SplideSlide>
                <div class="frame-5b slide">
                  <div class="frame-5c"><div class="presentation"></div></div>
                  <div class="frame-5d">
                    <span class="overseas-marketing-5e">해외 마케팅</span>
                  </div>
                </div>
              </SplideSlide> -->
            </Splide>
          </div>
        </div>
      </transition>
      <div class="flex-row-fcf" :class="$q.screen.gt.xs ? 'large' : 'small'">
        <div class="unknown"></div>
        <div class="regroup" :class="$q.screen.gt.xs ? 'large' : 'small'">
          <div class="frame-5f">
            <div class="frame-60">
              <div class="frame-61">
                <div class="icon-code">
                  <div class="vector-62"></div>
                  <div class="vector-63"></div>
                  <div class="vector-64"></div>
                </div>
              </div>
              <div class="frame-65">
                <span class="overseas-remote-hiring"
                  >해외 개발자 원격 채용</span
                >
              </div>
            </div>
            <div class="frame-66">
              <span class="shortcut">바로가기</span>
              <div class="arrow-right-square">
                <div class="arrow-right-square-67">
                  <div class="arrow-right-square-68"></div>
                </div>
              </div>
            </div>
          </div>
          <div class="frame-69">
            <div class="frame-6a">
              <div class="frame-6b">
                <div class="icon-avatar">
                  <div class="vector-6c"></div>
                  <div class="vector-6d"></div>
                </div>
              </div>
              <div class="frame-6e">
                <span class="foreigner-remote-hiring-non-dev"
                  >외국인 원격 채용 (비개발)</span
                >
              </div>
            </div>
            <div class="frame-6f">
              <span class="shortcut-70">바로가기</span>
              <div class="arrow-right-square-71">
                <div class="arrow-right-square-72">
                  <div class="arrow-right-square-73"></div>
                </div>
              </div>
            </div>
          </div>
          <div class="frame-74">
            <div class="frame-75">
              <button class="frame-button-76">
                <div class="div-icon-kor"><div class="div-kor"></div></div>
              </button>
              <div class="div-frame-77">
                <span class="span-korean-foreign-recruitment"
                  >한국어 가능 외국인 채용</span
                >
              </div>
            </div>
            <div class="div-frame-78">
              <span class="span-shortcut">바로가기</span>
              <div class="div-arrow-right-square">
                <div class="div-arrow-right-square-79">
                  <div class="div-arrow-right-square-7a"></div>
                </div>
              </div>
            </div>
          </div>
          <div class="div-frame-7b">
            <div class="div-frame-7c">
              <div class="div-frame-7d">
                <div class="div-icon-gear"><div class="div-vector"></div></div>
              </div>
              <div class="div-frame-7e">
                <span class="span-overseas-developer-services"
                  >해외 개발자 활용 서비스</span
                >
              </div>
            </div>
            <div class="div-frame-7f">
              <span class="span-shortcut-80">바로가기</span>
              <div class="div-arrow-right-square-81">
                <div class="div-arrow-right-square-82">
                  <div class="div-arrow-right-square-83"></div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <span class="span-match-top-talents"
          >우리는 국가의 장벽을 넘어 최고의 인재를 매칭해드립니다.</span
        ><span class="span-contact-number">010-0000-0000</span>
      </div>
      <span class="span-email" :class="$q.screen.gt.xs ? 'large' : 'small'"
        >aaaaa@naver.com</span
      >
      <div class="div-flex-row" :class="$q.screen.gt.xs ? 'large' : 'small'">
        <span class="span-company-name">상호명</span
        ><span class="span-ceo" v-show="$q.screen.gt.xs">대표 CEO</span
        ><span class="span-cin" v-show="$q.screen.gt.xs"
          >사업자등록번호 CIN</span
        ><span class="span-address" v-show="$q.screen.gt.xs">주소 ADDRESS</span>
      </div>
      <div class="div-flex-row-ee" :class="$q.screen.gt.xs ? 'large' : 'small'">
        <span class="span-hyperhire">하이퍼하이어</span
        ><span class="span-ceo-name" v-show="$q.screen.gt.xs">김주현</span
        ><span class="span-cin-number" v-show="$q.screen.gt.xs"
          >427-86-01187</span
        ><span v-show="$q.screen.gt.xs" class="span-company-address"
          >서울특별시 강남대로 479, 지하 1층 238호
        </span>
      </div>
      <div class="div-flex-row-84" :class="$q.screen.gt.xs ? 'large' : 'small'">
        <span class="span-hyperhire-india">Hyperhire India Private Limited</span
        ><span class="span-udlptc" v-show="$q.screen.gt.xs"
          >U74110DL2016PTC290812 </span
        ><span class="span-india-address" v-show="$q.screen.gt.xs"
          >D-138, Street number 11, Jagjeet Nagar, North East Delhi, New Delhi,
          <br />110053 India</span
        ><span class="span-juhyun-kim" v-show="$q.screen.gt.xs"
          >Juhyun Kim</span
        >
      </div>
      <span
        class="span-copyright-hyperhire"
        :class="$q.screen.gt.xs ? 'large' : 'small'"
        >ⓒ 2023 Hyperhire</span
      >
      <div
        class="div-group-85"
        :class="$q.screen.gt.xs ? 'large' : 'small'"
        style="
          background-image: url(data:image/jpeg;base64,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);
        "
      ></div>
      <div
        class="div-rectangle"
        :class="$q.screen.gt.xs ? 'large' : 'small'"
      ></div>
    </div>
  </div>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "vue-awesome-swiper";

// Import Swiper styles
import "swiper/css";
import "swiper/css/effect-coverflow";
import "swiper/css/bundle";
import "swiper/css/navigation";

import "@splidejs/vue-splide/css";

// import required modules
import SwiperClass, { EffectCoverflow, Navigation } from "swiper";

import { Splide, SplideSlide } from "@splidejs/vue-splide";

import { useQuasar } from "quasar";

import { ref, onMounted, onUpdated } from "vue";

export default {
  components: {
    Swiper,
    SwiperSlide,
    Splide,
    SplideSlide,
  },
  setup() {
    const $q = useQuasar();
    // const isgt = computed(() => {
    //   return $q.screen.gt.xs;
    // });

    onUpdated(() => {
      console.log($q.screen.gt.xs);
    });
    onMounted(() => {
      console.log($q.screen.gt.xs);
      console.log($q);
    });
    return {
      modules: [EffectCoverflow, Navigation],
    };
  },
  data() {
    return {
      options: {
        width: "100%",
        type: "loop",
        perPage: 5,
        perMove: 1,
        arrows: "false",
        pagination: "false",
        autoplay: "playing",
        interval: 5000,
        easing: "ease",
      },
      showMenu: false,
      dropdownOptions: [
        "채용",
        "해외 개발자 원격 채용",
        "외국인 원격 채용 (비개발 직군)",
        "한국어 가능 외국인 채용",
      ],
      selectedOption: "채용",
    };
  },
  created() {
    document.addEventListener("click", this.dropdown);
  },
  unmounted() {
    document.removeEventListener("click", this.dropdown);
  },
  methods: {
    dropdown(e) {
      let el = this.$refs.dropdown;
      let target = e.target;
      if (el !== target && !el.contains(target)) {
        this.showMenu = false;
      }
    },
    selectOption(option) {
      this.selectedOption = option;
      this.showMenu = false;
    },
  },
};
</script>

<style src="../css/index.css"></style>

<!-- <style>
@import "~@quasar/extras/variables.styl";
@import "~@quasar/extras/qclasses.styl";
</style> -->
