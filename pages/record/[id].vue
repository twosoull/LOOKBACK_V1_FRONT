<template>
  <!-- 전체 컨테이너 -->
  <div class="container">
    <!-- 일반회원 -->
    <header class="default-header" style="display: none;">
      <div class="default-div">
        <div class="default-title">운동기록</div>
      </div>
    </header>
    <!-- 트레이너일 떄 -->
    <header class="default-header" >
      <div class="default-div">
        <div>
          <div class="back-btn-box-text">
            <button class="back-btn"><img src="@/assets/icons/chevron-left.svg" alt=""></button>
            <div class="default-back-title">이영훈</div>
          </div>
        </div>
        <div class="default-header-item">
          <div><img src="@/assets/icons/ellypsis.svg" alt=""></div>
        </div>
      </div>
    </header>
    <!-- 카테고리 메뉴 -->
    <nav class="category-nav">
      <button class="category-btn active">운동기록</button>
      <button class="category-btn">프로필</button>
    </nav>

    <div class="search-filters default-nav border-none">
      <div class="filter-buttons scrollable">
        <button class="filter-btn active">전체(52)</button>
        <button class="filter-btn">PT</button>
        <button class="filter-btn">개인</button>
      </div>
      <!-- 1번: 셀렉트 버튼 -->
      <div class="custom-select">
        <button class="select-btn">
          <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path class="control-icon" d="M14.1667 5L14.1667 15" stroke="black" stroke-linecap="round"/>
            <path class="control-icon" d="M10 5L10 15" stroke="black" stroke-linecap="round"/>
            <path class="control-icon" d="M5.83333 5L5.83333 15" stroke="black" stroke-linecap="round"/>
            <path class="control-icon" d="M4.16666 6.66667H7.5" stroke="black" stroke-linecap="round"/>
            <path class="control-icon" d="M8.33334 13.3333H11.6667" stroke="black" stroke-linecap="round"/>
            <path class="control-icon" d="M12.5 10H15.8333" stroke="black" stroke-linecap="round"/>
          </svg>
          <span>필터</span>
        </button>
      </div>
    </div>
    <div class="profile-container" style="display: none;">
      <div class="profile-image">
        <img src="@/assets/images/userProfile.jpeg" alt="사용자 이미지">
      </div>
      <div class="profile-info">
        <div class="profile-row">
          <span class="profile-label gray-text">이름</span>
          <span class="profile-value">이영훈</span>
        </div>
        <div class="profile-row">
          <span class="profile-label gray-text">생년월일</span>
          <span class="profile-value">1992.06.27(23세)</span>
        </div>
        <div class="profile-row">
          <span class="profile-label gray-text">성별</span>
          <span class="profile-value">남자</span>
        </div>
        <div class="profile-row">
          <span class="profile-label gray-text">전화번호</span>
          <span class="profile-value">010-2725-7349</span>
        </div>
        <div class="profile-row">
          <span class="profile-label gray-text">이메일</span>
          <span class="profile-value">koon270692@gmail.com</span>
        </div>
        <div class="profile-row">
          <span class="profile-label gray-text">키</span>
          <span class="profile-value">200cm</span>
        </div>
        <div class="profile-row">
          <span class="profile-label gray-text">몸무게</span>
          <span class="profile-value">80kg</span>
        </div>

      </div>
    </div>



    <div class="record-container">
      <!-- 기록이 없을 경우 표시될 문구 -->

      <div style="display: none;" class="no-records-message">등록하신 회원이 없습니다.</div>

      <div class="record-item-container" data-id="record-1">
        <!-- 기록 정보 -->
        <a>
          <div class="record-item">
            <div class="record-info">
              <div class="record-image">
                <div class="circle personal">개인</div>
              </div>
              <div class="record-text">
                <div class="record-title">1월 10일 (금)</div>
                <div class="record-descript">
                  <div>근력, 스트레칭, 유산소</div>
                  <div class="gray-text">&nbsp;| 전신, 등, 가슴, 어깨, 하체, 복부</div>
                </div>
              </div>
            </div>
          </div>
        </a>
        <a>
          <div class="record-item">
            <div class="record-info">
              <div class="record-image">
                <div class="circle personal">PT</div>
              </div>
              <div class="record-text">
                <div class="record-title">1월 10일 (금)</div>
                <div class="record-descript">
                  <div>근력, 스트레칭, 유산소</div>
                  <div class="gray-text">&nbsp;| 전신, 등, 가슴, 어깨, 하체, 복부</div>
                </div>
              </div>
            </div>
          </div>
        </a>

        <!-- 기록 정보 -->
      </div>
    </div>
    <!-- 정렬 모달 -->
    <div id="sortModal" class="record-sort-modal hidden">
      <ul class="sort-options">
        <li class="sort-option" data-value="recommend">가나다순</li>
        <li class="sort-option" data-value="newest">최근 수업순</li>
      </ul>
    </div>
    <!-- 하단 고정 푸터 -->
    <footer class="fixed-footer" style="display: none;">
      <div class="footer-item active" data-target="회원관리">운동기록</div>
      <div class="footer-item" data-target="마이페이지">마이페이지</div>
    </footer>
  </div>
  <button class="add-btn"><img src="@/assets/icons/add (floating button).svg" alt=""></button>
</template>

<script setup lang="ts">

import {useRecordStore} from "~/store/record";
let recordStore = useRecordStore();

onMounted(async () => {
  
})
</script>

<style scoped>

</style>