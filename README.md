# RisuAI Chat Reader

RisuAI 채팅 로그를 다시 읽기 위한 뷰어. 새 대화는 못 함.

**라이브 데모**: https://mitchellmoon.github.io/risu-reader/

## 기능

- charx 봇 파일 직접 파싱 (JPEG + zip polyglot)
- risum 추가 에셋 팩 디코딩 (자체 rPack 포맷)
- 채팅 JSON 렌더링 (이미지 태그 → 실제 일러스트 매칭)
- 메시지 내 검색
- 모바일/PC 반응형
- 모든 데이터는 브라우저 IndexedDB에만 저장 (서버 전송 없음)

## 사용법

1. 왼쪽 `+` 버튼으로 charx 파일 업로드
2. 봇 선택 후 `+ 채팅 추가` 로 채팅 JSON 업로드
3. 다양한 에셋 (모듈 적용은 안됨) 보고 싶으면 하단 `+ 추가`로 risum 업로드

## 다운로드해서 로컬로 쓰기

[Releases 페이지](../../releases)에서 HTML 파일 받아 더블클릭으로 열어도 동일하게 동작합니다.

## 기술 스택

- Vanilla JS (의존성: JSZip)
- IndexedDB (영구 저장)
- 단일 HTML 파일 (배포 단순)

## 알려진 한계

- 풀 risum (수백 MB)은 첫 로드에 시간 걸림. 한 번 풀고 나면 IndexedDB 캐시
- 모바일에서 큰 파일 업로드는 느림
