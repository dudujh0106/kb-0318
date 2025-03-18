# IT 기초용어집

## 프로젝트 소개
IT 기초 용어집

## 구현 페이지
1. index.html
2. 하드웨어
3. 컴퓨터공학
4. 프로그래밍
5. 웹 개발

# 구조
```
- index.html
   - **각자 개발한 페이지로 이동하는 링크** 
   - 각자 하나의 페이지 개발
   - pages/ (예시)
        - hardware.html - 팀원 1
        - cs.html - 팀원 2
        - programming.html - 팀원 3
        - web.html 팀원 4
   - css/
   - js/
      - 공통코드
```
# 과제
1. 주제 정하기
    - 기능 정의
    - -> 이슈로 만들기
2. 각자 역할 분담 -> 이슈에 담당자를 할당
3. 각자 페이지를 개발 : 강사가 전달하는 요구사항에 맞춰서 커밋
    - main branch 를 base로 하는 feature branch 따서 작업(local)
    - 1인당 커밋은 최소 3개 (PR 3개 올려 주셔야해요)
      - 파일 추가 하는 커밋
      - 파일 변경(mv) 혹은 삭제(rm)하는 커밋
      - html 요소 하나 추가할 때 마다 한개의 커밋 만들어보고, rebase -i 로 합쳐보기
    - 다른 사람의 PR이 main으로 머지되면, 현재 작업중인 feature branch를 origin/main 기준으로 rebase 한 뒤, 작업 재개
      - 작업하던 내용은 git stash 명령어로 잠시 스택에 넣어둘 수 있음. rebase 완료 후에는 stash에 있는 변경사항 꺼내서 작업 다시 하시면 됩니다~!
    - 예시
```
git stash # 현재 작업중인 내용 잠시 stash
git fetch
git checkout main
git pull (혹은 git merge, git rebase)
git checkout 원래-작업하던-브랜치
git stash pop
```
  - 작업이 완료되면 마지막 커밋은 index.html 인덱스 페이지에 내가 개발한 페이지로 이동하는 링크 (이건 추가 커밋이라 5개에 포함 안됩니다 ^_^)
    - 마지막 커밋의 커밋 메시지에 이슈 번호 넣어주세요
4. 개발이 완료된 로컬 브랜치는, 원격으로 push -> Pull Request 팀원들 전부
5. 코드리뷰 진행
    - 코드리뷰 반영 커밋
6. 충돌이 발생하면 해결 -> 머지
