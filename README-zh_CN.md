<p align="center">
  <img width="200" src="https://raw.githubusercontent.com/canisminor1990/lobe-commit/master/docs/logo.webp">
</p>
<h1 align="center">Lobe Commit</h1>

<div align="center">
  Lobe Commit 是一款使用 ChatGPT 生成基于 Gitmoji 的 CLI 提交工具
<br/>

<!-- SHIELD GROUP -->

[![release][release-shield]][release-url] [![releaseDate][release-date-shield]][release-date-url] [![ciTest][ci-test-shield]][ci-test-url] [![ciRelease][ci-release-shield]][ci-release-url] <br/> [![contributors][contributors-shield]][contributors-url] [![forks][forks-shield]][forks-url] [![stargazers][stargazers-shield]][stargazers-url] [![issues][issues-shield]][issues-url]

</div>

![](https://raw.githubusercontent.com/canisminor1990/lobe-commit/master/docs/preview.webp)

[English](./README.md) | 简体中文

<br/>

## ✨ 特性

- [x] 🤯 支持使用 ChatGPT 根据 git diffs 自动生成提交信息
- [x] 🛠️ 流畅的提交信息编辑流程
- [x] 😜 支持添加 Gitmoji
- [x] 📝 支持 Conventional Commits 规范
- [x] ⚡️ 支持拉取 issues 列表并便捷绑定
- [ ] 🚧 支持多语言提交信息
- [ ] 🚧 支持自定义 Prompt

<br/>

## 📦 安装

要安装 Lobe Commit，请运行以下命令：

```bash
npm install -g @lobehub/commit-cli
```

<br/>

## 🤯 使用

使用 `lobe-commit` 命令为暂生成提交信息信息：

```shell
$ git add <files...>
$ lobe-commit
```

> 👉 提示：如果认为 `lobe-commit` 太长了，可以使用`lobe`别名

#### AI 模式

在 AI 模式下，可以使用 ChatGPT 生成完整的提交信息

![](https://raw.githubusercontent.com/canisminor1990/lobe-commit/master/docs/preview-ai.webp)

> 👉 提示：如果有特殊的网络要求，可以在设置中添加 OpenAI 的转发地址

#### 编辑器模式

在编辑器模式下，可以通过简单的流程生成 `<type>(<optional scope>): <subject> [<issues>]` 格式的提交信息

> 👉 提示：如果项目是 GitHub Repo，则将自动获取该仓库的 issues，可以使用 <kbd>空格</kbd> 选择多个问题将其链接到提交信息中

![](https://raw.githubusercontent.com/canisminor1990/lobe-commit/master/docs/preview-editor.webp)

<br/>

### Git hook

可以通过 `prepare-commit-msg`钩子将 Lobe Commit 与 Git 集成, 允许像往常一样使用 Git 并在提交之前编辑提交信息

#### 安装

要在项目中安装 hook，请运行以下命令：

```shell
$ lobe-coomit --init   # 或使用短标志 -i
```

#### 卸载

要从项目中卸载 hook，请运行以下命令：

```shell
$ lobe-coomit --remove   # 或使用短标志 -r
```

<br/>

### 配置

要配置 Lobe Commit，请运行以下命令：

```shell
$ lobe-coomit --config   # 或使用短标志 -o
```

- 要使用 AI 自动生成，需要在设置中填写 [OpenAI 令牌](<(https://platform.openai.com/account/api-keys)>)
- 要自动拉取私人仓库 issues，需要在设置中填写具有 repo 权限的 [GitHub 令牌](https://github.com/settings/tokens)

<br/>

### 选项

Lobe Commit 支持以下选项：

```shell
--commit  -c       使用提示交互式提交
--config  -o       设置lobe-commit首选项
--help    -h       打印基本选项
--init    -i       将lobe-commit初始化为提交钩子
--remove  -r       删除先前初始化的提交钩子
--list    -l       列出所有可用的提交类型
--version -v       打印lobe-commit安装版本
```

<br/>

## ⌨️ 本地开发

可以使用 Gitpod 进行在线开发：

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/canisminor1990/lobe-commit)

或者，可以克隆存储库并运行以下命令进行本地开发：

```bash
$ git clone https://github.com/canisminor1990/lobe-commit.git
$ cd lobe-commit
$ npm install
$ npm start
```

<br/>

## 🤝 参与贡献

<!-- CONTRIBUTION GROUP -->

> 📊 总计：<kbd>**3**</kbd>

<a href="https://github.com/canisminor1990" title="canisminor1990">
  <img src="https://avatars.githubusercontent.com/u/17870709?v=4" width="50" />
</a>
<a href="https://github.com/apps/dependabot" title="dependabot[bot]">
  <img src="https://avatars.githubusercontent.com/in/29110?v=4" width="50" />
</a>
<a href="https://github.com/actions-user" title="actions-user">
  <img src="https://avatars.githubusercontent.com/u/65916846?v=4" width="50" />
</a>

<!-- CONTRIBUTION END -->

<br/>
<br/>

## 🔗 链接

- gitmoji-cli: https://github.com/carloscuesta/gitmoji-cli
- ai-commit: https://github.com/insulineru/ai-commit

<!-- SHIELD LINK GROUP -->

<!-- release -->

[release-shield]: https://img.shields.io/npm/v/@lobehub/commit-cli?label=%F0%9F%A4%AF%20NPM
[release-url]: https://www.npmjs.com/package/@lobehub/commit-cli

<!-- releaseDate -->

[release-date-shield]: https://img.shields.io/github/release-date/canisminor1990/lobe-commit?style=flat
[release-date-url]: https://github.com/canisminor1990/lobe-commit/releases

<!-- ciTest -->

[ci-test-shield]: https://github.com/canisminor1990/lobe-commit/workflows/Test%20CI/badge.svg
[ci-test-url]: https://github.com/canisminor1990/lobe-commit/actions/workflows/test.yml

<!-- ciRelease -->

[ci-release-shield]: https://github.com/canisminor1990/lobe-commit/workflows/Build%20and%20Release/badge.svg
[ci-release-url]: https://github.com/canisminor1990/lobe-commit/actions/workflows/release.yml

<!-- contributors -->

[contributors-shield]: https://img.shields.io/github/contributors/canisminor1990/lobe-commit.svg?style=flat
[contributors-url]: https://github.com/canisminor1990/lobe-commit/graphs/contributors

<!-- forks -->

[forks-shield]: https://img.shields.io/github/forks/canisminor1990/lobe-commit.svg?style=flat
[forks-url]: https://github.com/canisminor1990/lobe-commit/network/members

<!-- stargazers -->

[stargazers-shield]: https://img.shields.io/github/stars/canisminor1990/lobe-commit.svg?style=flat
[stargazers-url]: https://github.com/canisminor1990/lobe-commit/stargazers

<!-- issues -->

[issues-shield]: https://img.shields.io/github/issues/canisminor1990/lobe-commit.svg?style=flat
[issues-url]: https://img.shields.io/github/issues/canisminor1990/lobe-commit.svg?style=flat