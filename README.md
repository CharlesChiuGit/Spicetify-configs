# Spicetify configs

Watch full set up at [spicetify-cli](https://github.com/khanhas/spicetify-cli) & [spicetify themes](https://github.com/morpheusthewhite/spicetify-themes/tree/master).

### Install Spicetify

1. Run the script.

```powershell
Add-Type -AssemblyName PresentationFramework

Invoke-WebRequest -UseBasicParsing "https://raw.githubusercontent.com/khanhas/spicetify-cli/master/install.ps1" | Invoke-Expression

spicetify

spicetify backup apply enable-devtool

[System.Windows.MessageBox]::Show('Please drag the themes into the themes folder located at | C:\Users\YourUserName\.spicetify\Themes |')

spicetify config inject_css 1 replace_colors 1 overwrite_assets 1

spicetify apply

pause
```

2. Log-in to spotify.

### Add Spicetify theme

1. Clone this repository.

```git
git clone https://github.com/morpheusthewhite/spicetify-themes.git
```

2. Copy the files into the [Spicetify Themes folder](https://github.com/khanhas/spicetify-cli/wiki/Customization#themes). Run:

&emsp;&emsp;**Windows**

```powershell
cd spicetify-themes
cp * "$(spicetify -c | Split-Path)\Themes\" -Recurse
```

3. Choose which theme to apply just by running:

&emsp;&emsp;&emsp;3-1 Paste the **.js file** to **User\ .spicetify\Extensions**

&emsp;&emsp;&emsp;3-2 Then run:

```powershell
spicetify restore
spicetify config extensions dribbblish.js
spicetify config current_theme Dribbblish
spicetify config color_scheme nord-dark
spicetify apply
```

### Re-apply theme

```powershell
spicetify apply
```

### Change theme

1. Make sure what theme u used right now.

```powershell
spicetify config extensions
```

2. Remove the extensions

```powershell
spicetify config extensions dribbblish.js-
```

3. Apply new theme.

### Remove Spicetify

1. Restore normal spotify

```powershell
spicetify restore
```

2. Delete the **User\ .spicetify** folder and **User\spicetify-cli** folder.
