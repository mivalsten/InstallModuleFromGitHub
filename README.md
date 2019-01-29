Install a PowerShell Module from GitHub
-

Not all PowerShell Modules are published to the PowerShellGallery but are hosted on GitHub.

[Read the blog post](https://dfinke.github.io/2016/Quickly-Install-PowerShell-Modules-from-GitHub/)

## In Action
![image](https://github.com/dfinke/InstallModuleFromGitHub/blob/master/media/InstallFromGitHub.gif?raw=true)

## Manual installation

Download zip/tar or `git clone` repo to your disk. Open powershell admin console, navigate to installation directory. Launch `InstallModule.ps1`. Module is installed to `C:\Program Files\WindowsPowerShell\Modules`

## Usage
Import module:
`Import-Module Install-ModuleFromGitHub`

To install module from [username]/[reponame], branch master:
`Install-ModuleFromGitHub -GitHubRepo [username]/[reponame]`

To chose different branch
`Install-ModuleFromGitHub -GitHubRepo [username]/[reponame] -branch testing`

Use `-destinationPath` to select different installation path.

Use `-SSOToken` to authenticate in private repositories. Default is anonymous authentication with access to public repositories.

Use `-moduleName` to change module name. Default is repository name.

