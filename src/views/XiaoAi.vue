<template>
    <div class="xiao-ai">
        <header>
            <div class="head-center">
                <div class="head-left">
                    <img src="//cdn.cnbj1.fds.api.mi-img.com/aife/ai-xiaoai-fe/dist/static/media/logoblank.f3920032.png"
                        alt="">
                </div>
                <ul class="head-right">
                    <li>获得小爱</li>
                    <li>只能家居</li>
                    <li>探索技能</li>
                    <li>小爱论坛</li>
                    <li>开放平台</li>
                    <li>关于我们</li>
                </ul>
            </div>
        </header>
        <div style="height: 50px;"></div>
        <div class="body-content">
            <div class="banner-video">
                <div class="video-container">
                    <video class="video" autoplay preload="auto"
                        poster="//cdn.cnbj1.fds.api.mi-img.com/aife/ai-xiaoai-fe/dist/static/media/banner-video-placement.77855eef.png"
                        src="//cdn.cnbj1.fds.api.mi-img.com/aife/ai-xiaoai-fe/dist/static/media/banner-video.d4e2bc16.mp4"></video>
                    <!-- <div class="text-container">
                    <div class="text-title">小爱同学</div>
                    <div class="text-subtitle">这一次，不止语音</div>
                </div> -->
                </div>
            </div>
            <div class="evolution">
                <div class="info">
                    <div class="main-title">
                        <span>智能进化 全新升级</span>
                        <div></div>
                    </div>
                    <div class="main-types">
                        <div class="xiaoai-type need-animation">
                            <img src="https://cdn.cnbj1.fds.api.mi-img.com/aife/xiaoai-open-platform/xiaoai6/common/icon-xajy.png"
                                alt="">
                            <div class="need-animation">
                                <div class="type-title">小爱建议</div>
                                <div class="type-subtitle">省心省力不忘事儿</div>
                            </div>
                        </div>
                        <div class="xiaoai-type need-animation">
                            <img src="https://cdn.cnbj1.fds.api.mi-img.com/aife/xiaoai-open-platform/xiaoai6/common/icon-xayy.png"
                                alt="">
                            <div class="need-animation">
                                <div class="type-title">小爱语音</div>
                                <div class="type-subtitle">一句话搞定各种事</div>
                            </div>
                        </div>
                        <div class="xiaoai-type need-animation">
                            <img src="https://cdn.cnbj1.fds.api.mi-img.com/aife/xiaoai-open-platform/xiaoai6/common/icon-xasj.png"
                                alt="">
                            <div class="need-animation">
                                <div class="type-title">小爱视觉</div>
                                <div class="type-subtitle">扫码识物识文档</div>
                            </div>
                        </div>
                        <div class="xiaoai-type need-animation">
                            <img src="https://cdn.cnbj1.fds.api.mi-img.com/aife/xiaoai-open-platform/xiaoai6/common/icon-xafy.png"
                                alt="">
                            <div class="need-animation">
                                <div class="type-title">小爱翻译</div>
                                <div class="type-subtitle">多语言智能翻译</div>
                            </div>
                        </div>
                        <div class="xiaoai-type need-animation">
                            <img src="https://cdn.cnbj1.fds.api.mi-img.com/aife/xiaoai-open-platform/xiaoai6/common/icon-xath.png"
                                alt="">
                            <div class="need-animation">
                                <div class="type-title">小爱通话</div>
                                <div class="type-subtitle">智能防骚扰防漏接</div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="video-container">
                    <div class="video-player">
                        <video class="video" preload="auto" loop
                            poster="https://cdn.cnbj1.fds.api.mi-img.com/aife/xiaoai-open-platform/xiaoai6/evolution/evolution-video-placement.png"
                            src="https://cdn.cnbj1.fds.api.mi-img.com/aife/xiaoai-open-platform/xiaoai6/evolution/h5-evolution-video.mp4"></video>
                    </div>
                </div>
            </div>
        </div>
        <footer>
            <!-- xiaoai -->
        </footer>
    </div>
</template>

<script setup lang="ts">
import { nextTick } from 'vue';
import gsap from 'gsap';
import { ScrollTrigger } from 'gsap/all';
gsap.registerPlugin(ScrollTrigger)
let tl = gsap.timeline()
nextTick(() => {
    tl.to('.xiaoai-type', {
        y: -20,
        opacity:1,
        delay:0.2,
        duration:0.8,
        ease: "power1.out",
        scrollTrigger: {
            trigger: '.xiaoai-type',
            scrub:true,
            // start:"top top",
        },
        stagger:0.1,
    })
})

</script>

<style scoped lang='scss'>
.xiao-ai {
    // width: 100vw;
    height: 100vh;
    background: #000;
    position: relative;

    header {
        width: 100%;
        position: fixed;
        top: 0px;
        left: 0px;
        z-index: 99;
        background: #ffffff;

        .head-center {
            width: 1100px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin: 0 auto;

            .head-left {
                display: flex;
                align-items: center;
                justify-content: center;

                img {
                    width: 96px;
                    height: 21px;
                }
            }

            .head-right {
                display: flex;
                align-items: center;
                justify-content: center;
                list-style: none;
                width: 560px;

                li {
                    float: left;
                    font-size: 13px;
                    color: #666666;
                    margin-left: 33px;
                    cursor: pointer;

                    &:hover {
                        color: #0099ff;
                    }
                }
            }
        }

    }

    .body-content {
        width: 100%;
        height: calc(100vh - 50px);
        background: #f5f5f7;

        .banner-video {
            height: calc(100vh - 50px);
            display: flex;
            justify-content: center;
            overflow: hidden;
            position: relative;
            //background: linear-gradient(180deg, #F1F4F7 0%, #E2E6ED 51%, #D4DAE3 100%);
            background: #E7EDFA;
            background-size: cover;

            .video-container {
                height: 100%;
                width: 100%;
                position: relative;

                .video {
                    object-fit: cover;
                    height: 100%;
                    width: 100%;
                }

                .text-container {
                    position: absolute;
                    left: 50%;
                    bottom: 15.5%;
                    text-align: center;
                    opacity: 1;
                    transform: translate3d(-50%, 45%, 0);
                    transition: transform 1.3s ease, opacity 1.3s linear;

                    &.visible {
                        transform: translate3d(-50%, 0, 0);
                        opacity: 1;
                    }

                    .text-title {
                        -webkit-background-clip: text;
                        color: transparent;
                        display: inline-block;
                        background-image: linear-gradient(85deg, #0BD5F9 -3.25%, #099CF7 28.53%, #1C87ED 53.62%, #6793F1 80.38%, #BC57FB 103.79%);
                        height: 7.2vh;
                        font-size: 7.2vh;
                        margin-bottom: 1.8vh;
                    }

                    .text-subtitle {
                        font-size: 6.8vh;
                    }
                }
            }
        }

        .evolution {
            .info {
                height: 620px;
                display: flex;
                flex-direction: column;
                align-items: center;
                background: #f3f8ff;
            }

            .video-container {
                display: flex;
                justify-content: center;
                overflow: hidden;
                position: relative;
                align-items: center;

                .video-player {
                    width: 100%;

                    .video {
                        width: 100%;
                    }
                }

                img {
                    height: 100%;
                    display: block;
                }
            }

            .main-title {
                margin-top: 120px;
                margin-bottom: 110px;
                position: relative;
                color: #000;
                overflow: hidden;

                &>span {
                    line-height: 1;
                    font-size: 80px;
                    font-weight: 570;
                }

                &-bg {
                    --transition-y: 0;
                    pointer-events: none;
                    height: 410%;
                    width: 100%;
                    position: absolute;
                    mix-blend-mode: lighten;
                    top: 0;
                    left: 0;
                    transform: translate3d(0, calc(-41.745433541040796%), 0);
                    background: url(//cdn.cnbj1.fds.api.mi-img.com/aife/ai-xiaoai-fe/dist/static/media/evolution-img-text-bg.4562380f.jpg) no-repeat;
                    background-size: 100% 100%;
                    z-index: 0;
                }
            }

            .main-types {
                display: grid;
                grid-template-columns: repeat(5, 1fr);
                grid-gap: 48px;


                .xiaoai-type {
                    text-align: center;
                    padding: 0 30px;

                    .text-animation {
                        transition: unset;
                    }

                    img {
                        width: 100px;
                        margin-bottom: 30px;
                    }
                }

                .xiaoai-type.need-animation {
                    transition-duration: 0.8s;
                    transition-timing-function: ease-out;
                    transition-delay: 0.1s;
                    transform: translate3d(0, 50px, 0);
                    opacity: 0;
                }


                .type-title {
                    font-size: 26px;
                    margin-bottom: 12px;
                    line-height: 1;
                    font-weight: 430;
                    color: #000;
                }

                .type-subtitle {
                    font-size: 16px;
                    line-height: 1;
                    font-weight: 305;
                    color: #000;
                }
            }
        }
    }

    footer {
        // width: 100%;
        background-color: #1a1a23;
    }
}
</style>