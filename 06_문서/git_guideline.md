# 최초에 실행

- git bash 설치
  (https://xangmin.tistory.com/102)
- 프로젝트 할 폴더 생성
- 생성된 폴더에 들어가 마우스 오른쪽 버튼클릭 후 git bash 실행
- 해당 폴더에 git을 시작, 초기화하겠다고 선언: `git init`
- 작업 내용 올릴 git 저장소 내용 가져오기:
  `https://github.com/leeAnalyst/KOSPI-Prj.git`
- 매번 주소 입력하기 쉽지 않으므로 등록
  - https://github.com/leeAnalyst/KOSPI-Prj.git라는 주소를 origin이라고 이제 칭하도록 등록:
    `git remote add origin https://github.com/leeAnalyst/KOSPI-Prj.git`

# 작업 내역 올리기

- 작업 전 다른 사람의 코드가 올라가 있을수있으므로 fetch(다운로드) 해서 내 코드와 합치기:
  `git fetch origin && git rebase origin/master`

- 작업해서 폴더에 올리기
- 작업한 내용 추가: `git add .`
- 작업하는 동안 다른 사람의 코드가 올라가 있을 수 있으므로 fetch 해서 합치기:
  `git fetch origin && git rebase origin/master`
- 추가한 내용 커밋하기

  - 무슨 내용을 작업했는지 메시지 넣어주기
    `type: 구현한 내용 넣기`

    | type     | 설명                          |
    | -------- | ----------------------------- |
    | feat     | 작업내용업로드                |
    | docs     | 문서작업업로드                |
    | fix      | 잘못된 부분, 에러수정         |
    | refactor | 기존 코드를 개선한 경우       |
    | comment  | 주석을 삭제하거나 추가한 경우 |
    | chore    | 개발환경이 변경한 경우        |
    | rename   | 파일 및 폴더명을 수정한 경우  |
    | remove   | 파일을 삭제하는 경우          |
    | test     | 테스트가 필요한경우           |

    ex) 커밋 메시지 예시

    ```
    git commit -m 'docs: README.md를 작성'
    git commit -m 'remove: python1.py 파일 삭제'
    git fix -m 'fix: syntax관련 에러를 수정함'
    ```

- 추가하고 커밋한 내역 orgin (git)에 올리기
  `git push origin master`
