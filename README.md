# Poke-dex Project
1. styled-component 사용
2. React Router 사용
3. Poke API 호출 -> Fetch API 보다 Axios 라이브러리 사용
  - 최신 브라우저 위주의 호환성
  - XSRF 보안 기능 미흡
  - Request Cancel 불가
4. useEffect 내부에 API호출(비동기 통신을 위해)
5. infinite scroll(무한스크롤) 구현 => useInfiniteScroll() 사용
6. Intersection Observer 구현 
  - 아직 화면에 보여지지 않은 부분도 데이터를 가져옴
  - 불필요하게 많은 API호출
  - 실제로 화면에 표시되고 있는 데이터만 불러오게 변경
7. 전역 상태관리 (Redux)
  - Flux 패턴 기반 데이터 흐름 제어
  - Middleware를 이용한 Data Fetching
  - 데이터 흐름을 일관적으로 관리
  - Dispatcher === Reducer
  - Action이 발생되었을 때 Reducer로 향하는 흐름을 중간에 관찰하거나, 가로채고 다른 작업을 할 수 있으며, 이후에 Reducer로 액션을 발생 시킬 수도 있음
8. createAsyncThunk 