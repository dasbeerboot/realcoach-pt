<template>
    <div class="container">
        <embed
            v-if="isMobile"
            class="embed-container" 
            src="https://realptcoach.waveon.io/"
            title="RealCoach PT"
            frameborder="0"
        />
        <div v-else class="is-desktop">
            현재 사전예약 페이지는 모바일에서만 지원됩니다. <br/>
            해당 URL을 모바일 브라우저에서 열어주세요. <br/>
            빠른시일내에 더 좋은 모습으로 찾아뵙겠습니다 🙏
        </div>
    </div>
  </template>
  <script lang="ts" setup>
  import { useMediaQuery } from '@vueuse/core'
  
  const isMobile = useMediaQuery('(max-width: 450px)')
  </script>

  <style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;500;700&display=swap');
  .container {
    font-family: 'Noto Sans KR', sans-serif;
  }
  .embed-container {
     width: 100vw;
     height: 7350px;
     max-height: max-content;
     display: flex;
     flex-direction: column;
     justify-content: center;
     align-items: center;
  }
  
  .is-desktop {
     width: 100vw;
     height: 100vh;
     display: flex;
     justify-content: center;
     align-items: center;
     background-color: #255FBB;
     color: #f5f5f5;
  }
  </style>