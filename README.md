## About how to change file/folder name uppercase or reverse

# When changing a file:

Using mv is sufficient, and there is no need to modify the ignore settings.

# When changing a folder:

1. Using mv is not applicable and will result in an error.

2. Manually changing the ignore setting to false is possible. However, it has the drawback of requiring the removal and re-upload of the cached folders and files to eliminate the previously cached files. If not done, the files that were in lowercase will remain as they are.

3. Manually changing the ignore setting to true while making changes (Git interprets there are no changes, and the working tree is considered clean).
