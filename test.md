# Getting Started

git pushgit

token test

SSH 삭제

자동 등록

credential 정보 삭제하기
git config --global --unset credential.helper

git 로그인 정보 저장/조회/삭제

1. Credential 정보 저장
   credential.helper의 store 옵션을 주게 되면 해당 git directory에서는 반영구적으로 인증 절차가 생략 됩니다.

- store 설정 정보를 해당 git directory의 .git 폴더 밑에 config파일에 저장(계정/git repository 단위)
- 인증 정보는 ~/.git-credentials에 저장
- 모든 프로젝트에 Credential 정보를 적용하기 위해 --global 옵션을 줄 수 있습니다

$git config crednetial.helper store
$git config --global crednetial.helper store

2. 설정 정보 조회
   아래 명령어를 통해 현재 설정된 git 정보를 확인 가능

$git config --list

3. 설정 삭제
   아래 명령어를 통해 현재 설정된 git 정보를 삭제 가능하며 global 설정된 경우 동일하게 --global 옵션을 줘서 삭제

- 같은 설정을 2번 입력 하게 되면 "credential.helper has multiple values"와 같이 충돌 에러가 발생하는데
  => 이럴 경우 .git/config 파일이나 ~./.git-credentials 파일 내의 [Credential] 항목 라인을 삭제하여 해결할 수 있다.

$git config --unset credential.helper
$git config --global --unset credential.helper

test4
