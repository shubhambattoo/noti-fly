<h1 align="center">Welcome to noti-fly 👋</h1>
<p>
  <img src="https://img.shields.io/badge/version-1.0.0-blue.svg?cacheSeconds=2592000" />
  <a href="https://github.com/shubhambattoo/noti-fly#readme">
    <img alt="Documentation" src="https://img.shields.io/badge/documentation-yes-brightgreen.svg" target="_blank" />
  </a>
  <a href="https://github.com/shubhambattoo/noti-fly/graphs/commit-activity">
    <img alt="Maintenance" src="https://img.shields.io/badge/Maintained%3F-yes-green.svg" target="_blank" />
  </a>
  <a href="https://github.com/shubhambattoo/noti-fly/blob/master/LICENSE">
    <img alt="License: ISC" src="https://img.shields.io/badge/License-MIT-yellow.svg" target="_blank" />
  </a>
  <a href="https://www.webcomponents.org/element/noti-fly-component">
    <img alt="Web Components" src="https://img.shields.io/badge/webcomponents.org-published-blue.svg">
  </a>
</p>

> Simple Notification Web Component

### 🏠 [Homepage](https://github.com/shubhambattoo/noti-fly#readme)

### Demo

[Demo Page](https://noti-fly.surge.sh)

## Install

```sh
npm install noti-fly-component
```

## Usage

Install the package or Download the library from `dist/noti-fly.js`

In your HTML file include `vue.js` <br>
Include the downloaded library and you are good to go

```sh
<script src="https://unpkg.com/vue"></script>
<script src="your/path/dist/noti-fly.js"></script>

<noti-fly showalert=true fixed=true heading="Woah!" msg="I am stuck here"></noti-fly>
```

### Required Inputs

<li> showalert : type boolean or String with value "true" or "false", needs to be passed to show or hide the component </li>

<li> type : type string, acceptable values = "success", "danger", "info", "warning", advisable to pass, or else takes "success" </li>

### Optional Inputs

<li> fixed : type boolean or String with value "true" or "false", if passed as true, makes it fixed at the bottom centered.  </li>

```sh
<noti-fly type="danger"></noti-fly>
```

<li> heading : type string, if passed is the top value in the component or else is "Success" by default </li>

<li> msg : type string, if passed is the bottom/meta value in the component </li>

```sh
<noti-fly showalert=true type="info" heading="Info" msg="This is some Info"></noti-fly>
```

## Author

👤 **Shubham Battoo**

- Github: [@shubhambattoo](https://github.com/shubhambattoo)

## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](https://github.com/shubhambattoo/noti-fly/issues).

## Show your support

Give a ⭐️ if this project helped you!

## 📝 License

Copyright © 2019 [shubhambattoo](https://github.com/shubhambattoo).<br />
This project is [MIT](https://github.com/shubhambattoo/noti-fly/blob/master/LICENSE) licensed.

---

_This README was generated with ❤️ by [readme-md-generator](https://github.com/kefranabg/readme-md-generator)_
