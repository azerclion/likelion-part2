```zsh
# 유저이름
git config --global user.name "azerc"

# 유저 이메일
git config --global user.email zizimoos@likelion.org

# code . 명령어로 vscod 열기, shell commender 설정..
command + shift + p
# install code 검색하면 됨...설정 ok...누르면 됨

# config 파일 수정이 완료될때 까지 기다림....( vscode에 파일 그냥 닫으면 됨 ~)
git config —-global core.editor “code --wait”

# config file edit
git config --global -e

# 윈도우와 맥의 개행 처리를 동일하게
git config --global core.autocrlf input

git config --global --list

# 문제가 생겼으면.....
git config --global --replace-all core.editor "code --wait"


#
git config --global alias.hist "log --graph --all --pretty=format:'%C(yellow)[%ad]%C(reset) %C(green)[%h]%C(reset) | %C(white)%s %C(bold red){{%an}}%C(reset) %C(blue)%d%C(reset)' --date=short"

##
❯ ssh-keygen
❯ cat ~/.ssh/id_rsa.pub
ssh-rsa AAAAB3NzaC1y.....
copy and paste at github/settings/SSH and GPG keys
```

- git has 3 state (modified, staged, committed)

* git remote add origin main / origin은 별칭입니다. 다른 이름으로 사용해도 된다는 뜻입니다.
* git push origin main
* git reset build.json / reset은..어떨때 쓰는거지?

* git branch

```zsh
    git branch branchName
    git branch -l // 브랜치 종류 리스트
    git checkout dev // git Head가 main에서 dev로 이동

    git checkout -b branchName // ?
```

- git checkout
- git merge

```zsh
    git checkout main
    git merge branchName // incomming 하고 commit 해야 그래프가 합쳐짐
    git commit ... //
```

```zsh
 current // main 에 것을 선택
 incomming // dev것을 선택
 both // 모두 선택

 conflict를 해결하고 add 하고 commit 도 해줘야 함
```

- git rebase
- git rebase conflict

```zsh
// main 에서 작업하는 것임
git branch -d dev
// dev 블랜치 삭제
git checkout hotfix
// 파일 수정 & add & commit
git checkout main
// 파일 수정 & add & commit
// 분기가 두개로 갈라져 있는 상태
// hotfix로 이동
// git checkout hotfix
// git rebase main
// hotfix의 분기의 시작을 main의 최신커밋으로 hotfix의 위치가 이동(reBase)
// 이게...뭐...좀...이상헌디....이동되면, main의 변경된 최신커밋까지 자동으로 hotfix에 반영?...conflick안남?
git checkout main
git merge hotfix
// main으로 이동해서 hotfix를 merge하면...일짜로 가지 치기 없이 merge.(요게...fastmerge라는 것인데...훔.)


main이 checkout 된 상태에서
git checkout -b def
git branch -l
// dev가 checkout된 상태
git rebase main
내용을 수정하고
git add .
git commit -m "뭐라뭐라"
git rebase --continue


// github Actions
// Figma token
```
