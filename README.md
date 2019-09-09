# README

## Git의 용도

1. 코드 관리도구
2. 원격 저장소
3. 협업 도구
4. 

## Git 용어정리

## Git 기초

- `git init`

- `git add`

- `git commit`
  - 커밋 이름을 정하는 틀
    - 커밋을 할때는 주어는 빼자(coz 내가 커밋하는거 다 앎)
    - 동사는 시제없이 능동태로 동사원형으로 적어주자
    
  - 커밋의 식별은 Hash 값으로 하게 되는데 2^160의 고유한 번호를 부여할 수 있음.
  
     제일 큰 오픈소스인 리눅스 조차 75만개의 커밋만 가지고 있다.
     
     #### Git commit 관리하기
     
     - `git checkout [커밋번호]`
        - 커밋번호의 상태로 돌아가서 체크해볼 수 있다
        - 원래 Head는 가장 최신의 커밋한 곳을 가르키고 있는데(master)  git checkout [커밋번호]를 해주면 Head가 해당 커밋을 가르키게 된다. 

- `git log`

  - 현재까지 커밋한 내역을 보여준다
  - 빠져나올땐 q를 누름

- `git log --oneline`

  - 로그를 보여줄 때 하나의 커밋을 한줄로 보여줌

## Git 원격저장소(remote)

- `git remote add [저장소이름] [저장소주소]`
- `git remote` : 원격저장소의 리스트(이름)
- `git remote -v` : 원격저장소의 리스트(이름, 주소)





# Git Branch

- `git branch [브랜치이름]`
  - 새로운 branch를 만든다 (평행세계 만들기)
- `git branch`
  - branch 목록을 보여줌, 친절하게도 현재 branch는 색깔로 표시해준다
- `git switch [브랜치이름]`
  - branch를 이동한다, checkout과 비슷하지만 오직 branch를 왔다리 갔다리 할 때만 사용함
- `git checkout [브랜치이름 또는 커밋번호]`
  - branch를 이동하거나, 해당 커밋으로 이동한다 == Head를 바꿔 주는 것임.
- `git branch -d [브랜치이름]`
  - branch를 삭제한다
- `git checkout -b [브랜치이름]`
  - branch를 까면서 동시에 브랜치를 이동한다
- `git switch -c [브랜치이름]`
  - 위랑 똑같음 까면서 동시에 이동
- `git merge [브랜치이름]`
  - 현재 branch에서 특정 브랜치를 병합한다.
  - merge는 3가지 종류가 있음
    1. fast-forward merge
       - 분기되기 전의 브랜치에서 더이상 쌓인 커밋이 없는 상태에서 다른 커밋을 만들어 놓은 브랜치와 합치는 것 == 커밋할 브랜치가 현재 브랜치화 되는 것!
    2. auto merge (without conflict)
       - branch가 merge 될 때 두개의 내용이 합쳐지지 않을 경우에 git이 알아서 합쳐버림. 
    3. merge with conflict 
       - 서로 다른 branch에서 같은 파일을 수정했을 경우,(동일 파일이어도 내용이 연결될 수 있으면 auto merge가 일어날 수 도 있음)
       - 특히 동일 라인의 내용이 다를 경우(이경우엔 무조건 conflict가 일어납니다. 동일 파일을 수정할 떈 조심하좀)
    4. conflict 내보자

한마디로 평행세계를 만들어낸다.

visualization git을 통해 시각적으로 알아보자

url 맨 앞에 test.을 붙이면 테스트하는애들 잘하면 볼수도 있음 ㅋㅋ

git pull은 auto merge와 patch 과정을 합친것!@#!#!@#!#!@#!#