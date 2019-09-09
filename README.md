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
    - 커밋을 할때는 주어는 빼자(내가 커밋하는거 다 앎)
    - 동사는 시제없이 능동태로 동사원형으로 적어주자
    
  - 커밋의 식별은 Hash 값으로 하게 되는데 2^160의 고유한 번호를 부여할 수 있음.
  
     제일 큰 오픈소스인 리눅스 조차 75만개의 커밋만 가지고 있다.
     
     #### Git commit 관리하기
     
     - `git checkout [커밋번호]`
        - 커밋번호의 상태로 돌아가서 체크해볼 수 있다
        - 원래 Head는 가장 최신의 커밋한 곳을 가르키고 있는데(master)  git checkout [커밋번호]를 해주면 Head가 해당 커밋을 가르키게 된다. 

- `git log`

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
  - branch를 이동한다
- `git checkout [브랜치이름 또는 커밋번호]`
  - branch를 이동하거나, 해당 커밋으로 이동한다 == Head를 바꿔 주는 것임.
- `git branch -d [브랜치이름]`
  - branch를 삭제한다
- `git checkout -b [브랜치이름]`
  - branch를 까면서 동시에 브랜치를 이동한다
- `git switch -c [브랜치이름]
  - 위랑 똑같음 까면서 동시에 이동

한마디로 평행세계를 만들어낸다.

