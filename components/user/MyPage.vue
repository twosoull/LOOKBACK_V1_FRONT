<template>
    <!-- 프로필 카드 -->
    <div class="mypage-profile-with">
      <div class="profile-top-row">
        <!-- 왼쪽: 프로필 이미지 + 텍스트 -->
        <div class="profile-left">
          <div class="profile-photo">
            <!-- 실제 프로필 이미지로 교체 -->
            <img src="./images/userProfile.jpeg" alt="사용자 이미지">
          </div>
          <div class="profile-text">
            <div class="profile-name">이영훈</div>
            <div class="profile-stats">26세 | 남자 | 185cm | 80kg</div>
          </div>
        </div>
        <!-- 오른쪽: 수정하기 버튼 -->
        <div class="profile-bottom">
          <div>
            <button class="edit-btn2">
              <div>
                수정하기
              </div>
              <div>
                <img src="./icons/chevron-right.svg" alt="">
              </div>
            </button>
          </div>
        </div>
      </div>
    </div>

    <!-- 연결된 트레이너 -->

    <div class="trainer-title">연결된 트레이너</div>
    <div class="mypage-profile-card">
      <div class="card-top-row">
        <div class="card-left">
          <div class="profile-photo">
            <!-- 실제 프로필 이미지로 교체 -->
            <img src="./images/userProfile.jpeg" alt="사용자 이미지">
          </div>
          <div class="profile-text">
            <div class="profile-name">이영훈</div>
          </div>
        </div>
        <div class="">
          <button class="back-btn"><img src="./icons/chevron-right.svg" alt=""></button>
        </div>
      </div>
    </div>

    <!-- 약관 및 정책 / 계정 -->
    <div class="mypage-menu">
      <!-- 약관 및 정책 -->
      <div class="menu-group">
        <div class="menu-title">약관 및 정책</div>
        <div class="menu-item">개인정보처리방침</div>
        <div class="menu-item">이용약관</div>
      </div>

      <!-- 계정 -->
      <div class="menu-group">
        <div class="menu-title">계정</div>
        <div class="menu-item" @click="logout">로그아웃</div>
        <div class="menu-item">탈퇴</div>
      </div>
    </div>
</template>

<script setup lang="ts">
import {useRouter} from "#vue-router";
const router = useRouter();

const logout = () => {
  localStorage.clear();
  router.push('/auth/kakao/login');
}

</script>

<style scoped>

</style>