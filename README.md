This repository contains a comprehensive how-to guide on configuring your iTerm2 terminal like mine. Let's be honest, the default Mac OS Terminal application is pretty boring, and if you use it, you'll appear to be an unimaginative, dull developer. However, you don't have to be boring. If you want trick other developers into thinking that you're cool, do like I did and download iTerm2 with some cool plugins and themes!

## Demo
<p align="center">
  <img src="https://raw.githubusercontent.com/elijahsawyers/iTerm2-Configuration/master/Demo.gif" />
</p>

## Tutorial
### Install iTerm2 (if you haven't already)
Install [iTerm2](https://www.iterm2.com/) through their website. Download the application, unzip it, and move it into your *~/Applications* folder.

If you have [Homebrew](https://brew.sh/), which you definitely should if you're a Mac user, install iTerm2 with the following command:

```sh
brew cask install iterm2
```

### Install Oh My Zsh
[Oh My Zsh](https://ohmyz.sh/) is a frameword for managing your zsh configuration, and it allows you to use a bunch of cool plugins and themes!

To install Oh My Zsh, use the following curl command:

```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

After installing, it will ask you if you want to change your default shell to zsh, select yes.

### Install Powerline fonts
To install [Powerline](https://github.com/powerline/fonts) fonts, simply clone their GitHub repository and run the install script.

```sh
git clone https://github.com/powerline/fonts.git --depth=1
cd fonts
./install.sh
```

After installing Powerline fonts, set your font in iTerm2 by going to ```Preferences... -> Profiles -> Text``` and changing the font to *Regular 12pt Meslo LG S DZ for Powerline*.

### Change the zsh theme to agnoster
To do this, you'll need to edit your *~/.zshrc* file. Open up your text editor of choice (if you're a programming wizard, you use vim) and set ```ZSH_THEME="agnoster"```. There should already be a *ZSH_THEME* environment variable in the file, so you'll just have to change the value to be *"agnoster"*.

To see the change, you'll either have to source the  *~/.zshrc* file or close your current iTerm2 window and open a new one.

### Set the default user
I, personally, do not like having *username@computer* displayed next to my current working directory, so I removed it. To do this, in the *~/.zshrc* file, add a line with: ```DEFAULT_USER=$USER```

Again, to see the change, you'll either have to source the  *~/.zshrc* file or close your current iTerm2 window and open a new one.

### Change the color theme to Dracula
In my opinion, [Dracula](https://draculatheme.com/) is the best color theme out there for anything programming-related. I not only use it in iTerm2, but I also use it as my theme in [VS Code](https://code.visualstudio.com/).

To get Dracula, download the [Dracula.itermcolors](https://github.com/dracula/iterm/blob/fb852408c1320069a416d734eca876e82ac4cc43/Dracula.itermcolors) file. After doing so, in iTerm2, go to ```Preferences... -> Profiles -> Colors``` and select ```Color Presets... -> Import```. Navigate to the *Dracula.itermcolors* file and select it. After importing the Dracula theme, select ```Color Presets... -> Dracula```.

You should now have the Dracula theme in iTerm2!

### Change the theme to minimal and set the default window title
To get rid of the color mismatch between the iTerm2 window and the title bar, go to ```Preferences... -> Appearance -> General -> Theme``` and select *Minimal*. While here, if you'd like to remove the window number in the title bar (i.e. the ⌥⌘1), go to ```Preferences... -> Appearance -> Windows``` and uncheck *Show window number in title bar*.

To change the default window title, go to ```Preferences... -> Profiles -> Window```, check *Custom window title*, and type whatever you'd like. I chose to simply type *Shell*, but it's honesty up to you.

## That's all folks
That's it! You should now have an iTerm2 shell that looks exactly like mine! Gone are the days of having a boring terminal on Mac OS!
