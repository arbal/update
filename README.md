# Update command scripts

This project has Unix update scripts for many tools,
systems, package managers, language modules, et. al.

 * `update`: run all the udpate scripts.
 * `update-apm`: update Atom Package Manager - for the GitHub Atom editor.
 * `update-apt`: update apt-get - for Debian, Ubuntu, etc.
 * `update-brew`: update Homebrew packages - for macOS.
 * `update-brewfile`: update brew packages for macOS by using a Brewfile
 * `update-brew-cask`: update Homebrew Cask packages - for macOS apps.
 * `update-cabal`: update Haskell Cabal pacakages.
 * `update-cargo`: update Rust cargo package manager.
 * `update-carthage`: udpate Xcode Carthage pacakges - for macOS.
 * `update-gem`: update Ruby gems.
 * `update-gemfile`: update gem packages for Ruby by using a Gemfile.
 * `update-mas`: update mas packages by using the Mac App Store.
 * `update-motion`: update Ruby Motion - needs a valid paid license.
 * `update-npm`: update Node Package Manager.
 * `update-macos`: update the macOS Mac operating system - large downloads.
 * `update-pip`: update Python PIP.
 * `update-pod`: update Cocoapods for macOS
 * `update-podfile`: update Cocoapods packages for macOS by using a Podfile
 * `update-repos`: update Git repositories - customize this for your system.
 * `update-rust`: update Rust programming language tooling.
 * `update-swift`: update macOS Swift language - this merely prints advice.
 * `update-ubuntu-release`: update Ubuntu release - for major Linux system upgrades.

## Examples

Examples of the commands that these update scripts use:

    apm upgrade
    apt-get update && apt-get upgrade
    brew update && brew upgrade
    cabal update
    cargo install-update -a
    carthage update
    gem update
    softwareupdate --install --all
    mas upgrade
    motion update
    npm update
    upgrade_oh_my_zsh
    rustup update stable
    do-release-upgrade
    yum update

## To run daily

To run the update command daily, you can use the `crontab` command.

To see if you have an existing `crontab` file, you can list it by running this:

    crontab -l > ~/.crontab

Edit the `~/.crontab` file.

Add a line that runs the `nice` command and use the full path to the `update` command:

    @daily /usr/bin/nice /foo/bar/update

Then install the file:

    crontab ~/.crontab


## Configuration files

This tool will also use any of these configuration files:

    ~/.config/Brewfile/Brewfile
    ~/.config/Gemfile/Gemfile
    ~/.config/Podfile/Podfile

The config directory uses the `XDG_CONFIG_HOME` environment variable, which is a POSIX standard environment variable. The default is `$HOME/.config`.


## Tracking

  * Package: UpdateCommand
  * Version: 4.3.0
  * Created: 2005-07-05
  * Updated: 2017-03-02
  * License: GPL
  * Contact: Joel Parker Henderson (joel@joelparkerhenderson.com)
