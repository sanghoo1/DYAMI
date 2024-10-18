
## 어려웠던 점

### 백그라운드 이미지와  호버시 백그라운드 컬러추가

백그라운드이미지가 부모로 와야하고 그 안에 div overlay를 추가해서 background: rgb(0,0,0) 을 넣어야한다.
그리고 높이값 설정해줘야함 height:100%;
background-color 안됨
background 중첩에서 컬러랑 이미지 중첩 안됨

### youtube 적용할 때
.youtube-wrapper{
  
  width: 100%;
  
  
}
.youtube-wrapper .youtube{
  width: 100%;
  aspect-ratio: 16/9;
  object-fit: cover;
  
  

}
iframe을 감싸는 곳에 위드값 100%(?)

iframe에 위드값 100%와 에스펙트 16/9로 세로값주고
오브젝트 핏으로 영상 꽉채우기

### html에 이미지넣기 vs 백그라운드 이미지로 처리하기

width,height 값을 어디에 어떻게 줘야하는 지 헷갈림
차이가 뭔지 정확히 인지못하겠음

### display:none;엔 transition 안먹힘

### 반응형웹 제작시 모바일 버전의 패딩과 폰트사이즈는 rem으로 주기

### object-fit과 object-position

비디오,이미지의 비율 조절

### aspect-ratio

이미지,비디오의 가로,세로값의 비율정의

### background의 축약형

background: url() no-repeat (attachment) 50% (50%) / cover (100px)

백그라운드: 이미지 반복없음 뷰포트비율 위치 / 크기

### figure

 <figure>
   <img src="./images/img-07.jpg">
   <figcaption>
      <h3>Analysis</h3>
      <p>이 이제 가을 하나에 내린 까닭이요, 듯합니다</p>
   </figcaption>
 </figure>

### 페이지 구성시 감싸는 태그가 필요한지 판단하기

같이 이동하는,구성되는 텍스트들 감싸는 div 필요함

### iframe 
<iframe src="https://www.youtube.com/embed/wcIf3huwFhc?si=UtNTXOmoy2u1FHx3controls=0&mute=1&autoplay=1"
title="YouTube video player" frameborder="0"
allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen class="youtube"></iframe>

### 카카오맵 스크립트

#### 헤더 스크립트
<script src="https://dapi.kakao.com/v2/maps/sdk.js?appkey=e2de939460f43392c76dc857847a14cc"></script>

#### 바디스크립트

<script>
		const mapContainer = document.getElementById('kakaoMap'), // 지도를 표시할 div 
		    mapOption = {
		        center: new kakao.maps.LatLng(37.2680712, 127.0002517), // 지도의 중심좌표
		        level: 3, // 지도의 확대 레벨
		        mapTypeId : kakao.maps.MapTypeId.ROADMAP // 지도종류
		    }; 

		// 지도를 생성한다 
		const map = new kakao.maps.Map(mapContainer, mapOption); 

		// 지도에 마커를 생성하고 표시한다
		const marker = new kakao.maps.Marker({
		    position: new kakao.maps.LatLng(37.2680712, 127.0002517), // 마커의 좌표
		    map: map // 마커를 표시할 지도 객체
		});

	</script>