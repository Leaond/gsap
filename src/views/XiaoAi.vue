<template>
    <div class="xiao-ai">
        <header>
            <div class="head-center">
                <div class="head-left">xiao</div>
                <ul class="head-right">
                    <li>1</li>
                    <li>1</li>
                    <li>1</li>
                    <li>1</li>
                </ul>
            </div>
        </header>
        <div style="height: 50px;"></div>
        <div class="body-content">
            <video class="video" autoplay preload="auto"
                poster="//cdn.cnbj1.fds.api.mi-img.com/aife/ai-xiaoai-fe/dist/static/media/banner-video-placement.77855eef.png"
                src="//cdn.cnbj1.fds.api.mi-img.com/aife/ai-xiaoai-fe/dist/static/media/banner-video.d4e2bc16.mp4"></video>
            <div class="evolution">
                <div class="info"></div>
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
// import { ref, reactive } from 'vue';
</script>

<style scoped lang='scss'>
.xiao-ai {
    width: 100vw;
    height: 100vh;
    background: #000;
    position: relative;

    header {
        width: 100%;
        position: fixed;
        top: 0px;
        left: 0px;

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
            }

            .head-right {
                display: flex;
                align-items: center;
                justify-content: center;
            }
        }

    }

    .body-content {
        width: 100%;
        height: calc(100vh - 50px);
        background: #f5f5f7;

        .video {
            width: 100%;
            height: 800px;
        }

        .evolution {
            .info {
                height: 620px;
                display: flex;
                flex-direction: column;
                align-items: center;
                background: #f3f8ff;
            }
        }
    }

    footer {
        // width: 100%;
        background-color: #1a1a23;
    }
}</style>