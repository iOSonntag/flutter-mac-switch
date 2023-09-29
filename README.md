# flutter-app
A base project for flutter app development. 
- `10x` your development 
- `20x` decrease
your time spent on bugs 
- `30x` your project setup speed and
- `40x` your skills in detecting `10x` bullshit 

## Notes
- initially only platform `macos` enabled - enabling more platforms is explained [here](#adding-another-platform)
- made for [VSCode](https://code.visualstudio.com/) - adding support for other
  editors such as [Android
  Studio](https://developer.android.com/studio) should be just one Google search
 away - see
  [this
  link](https://letmegooglethat.com/?q=add+android+studio+support+to+existing+flutter+project)

## Features
- [Less important files & folders hidden by default](#hidden-files--folders)
- [Meaningful commit messages](#meaningful-commit-messages)
- [(*coming soon*) - Automatic versioning & `CHANGELOG.md` generation](#coming-soon---automatic-versioning--changelogmd-generation)
## Features Breakdown
### Hidden Files & Folders  
Less important files & folders are hidden using `"files.exclude"` from projects
  `.vscode/settings.json` workspace settings.
  - keeps project clean and avoids cluttering
  - feel free to change it to your needs

<br/> 

### Meaningful Commit Messages
Uses [Husky](https://typicode.github.io/husky/) to enforce a specific commit message
format. Docs on the format are defined in the repository's
[READ_FORMATS.md](READ_FORMATS.md#commit-message-format) file.
  - using npm package: `commitlint`
  - ensures consistent format across all commits
  - required for [semantic-release](https://npmjs.com/package/semantic-release)
  package to do its magic 

<br/> 

### (*coming soon*) - Automatic Versioning & `CHANGELOG.md` Generation
 Uses
  [semantic-release](https://npmjs.com/package/semantic-release) to
  automatically create new versions of the project based on the commit messages.
  It parses all commits since the last version tag and determines the next
  version number based on the severity of the commits.  
  Also generates a `CHANGELOG.md` file based on the commit messages.
  - no worries about versioning
  - automatic `CHANGELOG.md` generation
  - automatic `git tag` creation
  - works because of [meaningful commit messages](#meaningful-commit-messages)


### Preinstalled packages
  - [http](https://pub.dev/packages/http)
  - [google_fonts](https://pub.dev/packages/google_fonts)
  - [provider](https://pub.dev/packages/provider)
  - [uuid](https://pub.dev/packages/uuid)
  - [build_runner](https://pub.dev/packages/build_runner)
  - [path_provider](https://pub.dev/packages/path_provider)
  - [shared_preferences](https://pub.dev/packages/shared_preferences)
  - [flutter_launcher_icons](https://pub.dev/packages/flutter_launcher_icons)
  - [flutter_native_splash](https://pub.dev/packages/flutter_native_splash)
  - [flutter_svg](https://pub.dev/packages/flutter_svg)
  - [get_it](https://pub.dev/packages/get_it)  

- (*more coming soon*)


## Setup
1. Clone the repository
2. Run `npm run i` in the root directory of the project
### Adding Another Platform
You can add more
platforms by running  
```bash
# adds web & ios support to the project
flutter create --platforms=web,ios . 

# Available Platforms: 
# [macos, ios, android, linux, windows, web]
```

in the root directory of the project. Do not worry about your prior code
changes, they are left untouched - the project will not be replaced. 



## TODO
- [ ] add semantic-release feature