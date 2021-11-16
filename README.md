# eyedrops's resume

[![build pdf](https://github.com/eyedropsP/resume/actions/workflows/build-pdf.yml/badge.svg)](https://github.com/eyedropsP/resume/actions/workflows/build-pdf.yml)
[![create issue](https://github.com/eyedropsP/resume/actions/workflows/create-issue.yml/badge.svg)](https://github.com/eyedropsP/resume/actions/workflows/create-issue.yml)
[![lint text](https://github.com/eyedropsP/resume/actions/workflows/lint-text.yml/badge.svg)](https://github.com/eyedropsP/resume/actions/workflows/lint-text.yml)
[![release date](https://img.shields.io/github/release-date/eyedropsP/resume?color=blue&logo=github)](https://github.com/eyedropsP/resume/releases)

[ English | [日本語](https://github.com/eyedropsP/resume/blob/master/README.ja.md) ]

## Data

- [GitHub Pages](https://eyedropsp.github.io/resume)
- [PDF](https://github.com/eyedropsP.github.com/eyedropsP/resume/releases)
- [File](https://github.com/eyedropsP/resume/blob/master/docs/README.md)

## Features

### 💅 Lint text

Automatic proofreading with [textlint](https://github.com/textlint/textlint).

```
$ yarn lint --fix
```
It is also automatically executed when pre-commit by [husky](https://github.com/typicode/husky).  
proofreading rules are set with `.textlintrc`.



### 📝 Convert MD to PDF

You can generate PDF with [md-to-pdf](https://www.npmjs.com/package/md-to-pdf).


```
$ yarn build:pdf
```

The output PDF can be styled as you like with CSS. Edit the `pdf-configs/style.css`.  

### 🛠 Create release

When you push with a `v**` tag, GitHub Actions will run the build, generate the PDF, create a Release, and register the PDF to Assets.

```
$ git commit -m "add job"
$ git tag v1.0
$ git push origin --tags
```

### 📆 Remind update

Automatically generate issues every three months with GitHub Actions Schedules triggers to prompt you to update your resume.

To change the duration or stop the job, edit `.github/workflows/create-issue.yml`.  
To change the issue contents, edit `.github/ISSUE_TEMPLATE.md`.
