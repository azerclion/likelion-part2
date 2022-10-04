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
