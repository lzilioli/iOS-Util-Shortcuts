# README

By using the SC Pshr ⬆️ (Shortcut Pusher), shortcut developers can easily share, distribute, and collaborate on Apple Shortcuts and their dependencies through a single Git repository, making the process more efficient and convenient. Then, using the SC Pllr ⬇️ (Shortcut Puller) shortcut, users can install all shortcuts within a published repository with the git url on their clipboard and a single run of the shortcut.

The iOS Util Shortcuts Git repository addresses the following pain points:

*Shortcut developers:* When developing and distributing complex shortcuts, the developer sometimes must require the user to download multiple shortcuts: the main shortcut, and various helper shortcuts that the main shortcut relies on. The process for sharing and distributing updates is cumbersome. Don't even mention versioning ahortcuts or collaborating on the, with other developers. This repository solves that.

This pain is illustrated well in the [instructions for the MacStories Automation April contest](https://www.macstories.net/stories/enter-your-shortcuts-in-the-2023-automation-april-shortcuts-contest/):

> Although you are limited to submitting two shortcuts, your shortcuts can rely on calling other shortcuts that you use to provide blocks of functionality within the shortcut you submit. So, if your main shortcut relies on the Run Shortcut action, please link those subsidiary shortcuts in the description of your shortcut, so the judges can install them and properly test your shortcut.

## Introduction

Welcome to the iOS Util Shortcuts Git repository! This project offers an innovative way to share and distribute Apple Shortcuts and their dependencies through a single Git repository, eliminating the need to manually download multiple shortcuts and making updates more convenient. The main components of this system include the **SC Pshr ⬆️ (Shortcut Pusher)** and **SC Pllr ⬇️ (Shortcut Puller)** shortcuts. 

Please note that SC Psher ⬆ is only required if you are a Shortcut developer looking to publish shortcuts to your own git repository using this method.

## Getting Started

1. Install the **SC Pllr ⬇️** shortcut from the repository by clicking [this link](https://github.com/lzilioli/iOS-Util-Shortcuts/blob/main/SC%20Pllr%20%E2%AC%87%EF%B8%8F.shortcut?raw=true).
2. By default, the shortcut will run and install the shortcuts within this repository.

>Note: The SC Pshr ⬆️ and SC Pllr ⬇️ actions require [Working Copy](https://workingcopy.app/) to be installed on your iOS device.

## Apple Shortcuts in this Repository

1. **SC Pllr ⬇️**: This shortcut prompts for a Git repository URL, and installs all of the shortcuts. When run with a URL you’ve already cloned, it will install the latest version of all shortcuts if necessary.
2. **SC Pshr ⬆️**: Accepts a dictionary as an input, requiring two keys: “shortcuts” (a list of shortcuts to be published) and “repo” (a URL for the repository being published). This shortcut saves the latest version of the shortcuts to the repository and includes a “src” folder containing the shortcut in XML and JSON representation for easier PR review. if you publish a repository with this shortcut, please include "sc-pllr-info.json" in a .gitignore file
3. **Call SC Pshr**: Illustrates how to use the SC Pshr ⬆️ shortcut. In fact, it demonstrates how to use it for the iOS Util Shortcuts repo itself. If you are a shortcut developer and you wish to publish your own shortcut repository, you can duplicate this shortcut and adapt the “Filter Shortcuts” action to find the shortcuts you wish to publish.
4. **Find Shortcut**: A small utility that looks for a shortcut and searches for it in the Shortcuts app.

## Troubleshooting

If you encounter any errors related to untrusted shortcuts or private sharing, please follow these steps:

1. Open the Settings app on your iOS device.
2. Scroll down and tap on “Shortcuts”.
3. Enable “Allow Untrusted Shortcuts” (Private Sharing on iOS 16 or later)
4. Try to install the **SC Pllr ⬇️** shortcut again.
 
# Shoutouts

This repo uses a technique for extracting shortcuts as json and xml for storing them in the repository that was shared by [Fredrico on Macstories](https://club.macstories.net/posts/parsing-shortcuts-as-xml-or-json-and-extracting-comments-from-them).
