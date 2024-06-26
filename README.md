# 나만의 일정 관리 앱 서버 만들기
### 1. Use Case Diagram
<img width="70%" alt="Use Case Diagram" src="https://github.com/20210805jiwoo/ScheduleManagementAppServer/assets/102974424/0cead6d4-97bd-4b6d-806d-2c082d5d248c">

### 2. API 명세서
[API 명세서](https://documenter.getpostman.com/view/29105336/2sA3Qv7qNM#e832717d-bbc9-4887-8a5b-7f7c881881e5)

<img width="70%" alt="API" src="https://github.com/wldnfl/ScheduleManagementAppServer/assets/102974424/4d5574ef-5a05-480b-a3cb-384343bc52d9">

### 3. ERD
[ERD](https://www.erdcloud.com/p/46RhsFCgz5ene8sM2) 

<img width="90%" alt="ERD2" src="https://github.com/wldnfl/ScheduleManagementAppServer/assets/102974424/22c048f6-6d3a-4448-bdbf-cad2066e00c1">

<hr>

### 공통 조건
1. 일정 작성, 수정, 조회 시 반환 받은 일정 정보에 `비밀번호`는 제외 되어있습니다.
2. 일정 수정, 삭제 시 선택한 일정의 `비밀번호`와 요청할 때 함께 보낸 `비밀번호`가 일치할 경우에만 가능합니다.

### 기능 1 : 일정 작성
<table>
    <thead>
        <tr>
        <td>일정</td>
        <td>할일 제목</td>
        <td>할일 내용</td>
        <td>담당자</td>
        <td>비밀번호</td>
        <td>작성일</td>
        </tr>
    </thead>
</table>

#### 조건
할일 제목, 할일 내용, 담당자, 비밀번호, 작성일을 저장할 수 있습니다.
저장된 일정 정보를 반환 받아 확인할 수 있습니다.

### 기능 2 : 선택한 일정 조회
#### 조건
선택한 일정의 정보를 조회할 수 있습니다.

### 기능 3 : 일정 목록 조회
#### 조건
등록된 일정 전체를 조회할 수 있습니다.
조회된 일정 목록은 작성일 기준 내림차순으로 정렬 되어있습니다.

### 기능 4 : 선택한 일정 수정
#### 조건
선택한 일정의 할일 제목, 할일 내용, 담당자을 수정할 수 있습니다.
서버에 일정 수정을 요청할 때 비밀번호를 함께 전달합니다.
수정된 일정의 정보를 반환 받아 확인할 수 있습니다.

### 기능 5 : 선택한 일정 삭제
#### 조건
선택한 일정을 삭제할 수 있습니다.
서버에 일정 삭제를 요청할 때 비밀번호를 함께 전달합니다.
