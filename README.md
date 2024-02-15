# About how to change file/folder name uppercase or reverse

## When changing a file:

1. Using `mv` is sufficient, and there is no need to modify the ignore settings.
  - 🔥issue :  use `git mv` . than `mv` (sometimes mv not working)
2. Using `git config core.ignorecase false` it remains cached file in github repo.

## When changing a folder:

1. Using mv is not applicable and will result in an error.

2. Manually changing the ignore setting to false is possible. However, it has the drawback of requiring the removal and re-upload of the cached folders and files to eliminate the previously cached files. If not done, the files that were in lowercase will remain as they are.      ` git config core.ignorecase false  `

3. Manually changing the ignore setting to true while making changes (Git interprets there are no changes, and the working tree is considered clean).



## 파일 변경할 때
1. `mv` 명령어를 사용한다. ignore을 변경하지 않아도 가능하다
` git mv old filename new filename `
  - 🔥이슈 :  `git mv` 처럼 git을 붙여야하는 것 같다. 종종 `mv` 사용했을 때 git이 인식하지 않는 경우 발견. 


## 폴더 변경할 때
1. mv는 사용 불가능 : 에러 발생
2. ignore설정 false 수동 변경 (가능)   -> 단점 : cached 폴더,파일을 제거 후 다시 올려야 이전 캐싱된 파일을 지움, 그렇지 않으면 소문자였던 파일이 그대로 남아있다.
3. ignore 설정 true 인 상태로 수동 변경 -> git이 변경사항이 없다고 판단해서 working tree가 clean하다고 뜬다.
