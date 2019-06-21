<h1 align="center">CombineExamples</h1>

<h3 align="center">WIP</h3>

<div align="center">
👷 🧱 🧰 🛠️
</div>
<div align="center">
<strong>Getting started with Combine</strong>
</div>
<div align="center">
 A collection of simple examples using Apple Combine reactive framework
</div>

<br />

<div align="center">
<!-- Last commit -->
<img src="https://img.shields.io/github/last-commit/tailec/CombineExamples.svg" alt="last commit"/>
<!-- Open issues -->
<img src="https://img.shields.io/github/issues-raw/tailec/CombineExamples.svg" alt="open issues" />
<!-- Swift version -->
<img src="https://img.shields.io/badge/swift%20version-5.1-brightgreen.svg" alt="swift version">
<!-- Platform -->
<img src="https://img.shields.io/badge/platform-ios-lightgrey.svg" alt="platform" />
<!-- License -->
<img src="https://img.shields.io/badge/licence%20-MIT%20-blue.svg" alt="license" />
</div>


<div align="center">
<sub>Built with ❤︎ by
Pawel Krawiec
</sub>
</div>
<br />
<br />


## Examples


<img align="left" src="https://github.com/tailec/CombineExamples/blob/master/Resources/LoginGif.gif" />
<p><a href="https://github.com/tailec/CombineExamples/tree/master/CombineExamples/Login"><h1 align="left">LOGIN SCREEN</h1></a></p>
<h4>Simple user login validation</h4>

```swift
let credentials = Publishers
    .CombineLatest($username, $password)
    .share()

credentials
    .map { uname, pass in
        uname.count >= 4 && pass.count >= 4
    }
    .prepend(false) // initial state
    .assign(to: \.isEnabled, on: loginButton)
    .cancelled(by: cancellableBag)
```

<br></br><br></br>


<img align="left" src="https://github.com/tailec/CombineExamples/blob/master/Resources/TimerGif.gif" />
<p><a href="https://github.com/tailec/CombineExamples/tree/master/CombineExamples/Timer"><h1 align="left">TIMER</h1></a></p>
<h4>Simplified stopwatch</h4>
<br></br><br></br><br></br><br></br><br></br><br></br>


<img align="left" src="https://github.com/tailec/CombineExamples/blob/master/Resources/SearchGif.gif" />
<p><a href="https://github.com/tailec/CombineExamples/tree/master/CombineExamples/Search"><h1 align="left">SEARCH</h1></a></p>
<h4>Browsing GitHub repositories</h4>
<br></br><br></br><br></br><br></br><br></br><br></br>


<img align="left" src="https://github.com/tailec/CombineExamples/blob/master/Resources/UsernameGif.gif" />
<p><a href="https://github.com/tailec/CombineExamples/tree/master/CombineExamples/Username"><h1 align="left">AVAILABILITY</h1></a></p>
<h4>Check if your repository name is already taken</h4>
<br></br><br></br><br></br><br></br><br></br><br></br>


<h3>Stay tuned. More examples coming.</h3>


## Licence
MIT.

The Apple logo and the Combine framework are property of Apple Inc.
