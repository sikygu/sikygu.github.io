# Siqi Gu — Personal Academic Homepage

A single-page static site (plain HTML/CSS/JS, no build step) for sikygu.github.io.

## Structure

```
index.html        Page content (About / News / Education / Publications / Research / Honors / Contact)
css/style.css      All styling
js/script.js       Mobile nav toggle + footer year
assets/profile.jpg Profile photo (cropped from your UK trip photo)
assets/Siqi_Gu_CV.pdf   CV, linked from the "CV (PDF)" button in the header
```

## 发布到 GitHub Pages（steps to publish）

1. 在 GitHub 上新建一个仓库，名字必须是 `sikygu.github.io`（用户名.github.io），设为 Public。
2. 在这个文件夹里执行：

   ```bash
   git init
   git add .
   git commit -m "Initial personal homepage"
   git branch -M main
   git remote add origin https://github.com/sikygu/sikygu.github.io.git
   git push -u origin main
   ```

3. 推送后几分钟内，网站会自动出现在 `https://sikygu.github.io/`。
   （`用户名.github.io` 这种仓库名，GitHub 会自动开启 Pages，一般不用再去 Settings 里手动配置；
   如果几分钟后还打不开，去仓库的 Settings → Pages 检查一下 Source 是否选的是 `main` 分支 / `root` 目录。）

## 以后怎么改内容

- 改文字：直接编辑 `index.html` 里对应的段落/列表。
- 加一条新论文或新闻：复制 `<li>...</li>` 里的一整条，改文字即可，格式会自动跟着走。
- 换照片：替换 `assets/profile.jpg`（建议正方形、至少 900×900）。
- 换CV：替换 `assets/Siqi_Gu_CV.pdf`，文件名保持一致就不用改链接；如果改了文件名，同步修改 `index.html` 里 `CV (PDF)` 那个链接。
- 改完之后本地想预览，在这个文件夹里运行 `python3 -m http.server 8000`，然后浏览器打开 `http://localhost:8000`。
- 改完想更新网站：`git add . && git commit -m "update" && git push`，推送后几分钟内线上会自动更新。

## 小提醒

- 现在页面上的 GitHub 链接指向 `github.com/sikygu`，Google Scholar 和邮箱链接来自你的CV，如果以后换了邮箱/账号记得同步改。
- 页面里"求职"相关的表述很克制（只在 About 里提了一句"open to postdoctoral research opportunities"），如果想加更醒目的横幅或去掉，直接改 `index.html` 里 `#about` 那一段就行。
