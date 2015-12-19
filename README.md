# [license](https://github.com/nishanths/license)

Create licenses for your open-source projects from the command-line. *Hello, productivity!*


* Works without network access (except for first-run)
* Automatically stays up-to-date with the licenses in GitHub's API
* Makes it easy to customize the name, year, and output filename when needed


[![wercker status](https://app.wercker.com/status/1407b8c71c720358bf15eeb5815f99bd/s "wercker status")](https://app.wercker.com/project/bykey/1407b8c71c720358bf15eeb5815f99bd)
[![GitHub license](https://img.shields.io/github/license/nishanths/license.svg)](https://github.com/nishanths/license/blob/master/LICENSE)

# Demo

<img src="https://zippy.gfycat.com/JoyfulBlandGermanshorthairedpointer.gif" width="650px"/>

# Install

To install license, run:

````
$ go get github.com/nishanths/license
````

Alternatively, grab a binary for your platform [at this page]().

# Usage

### Generating a license

To generate a license, simply run `license` followed by the license name. The following command, for example, generates the MIT license:

````bash
$ license mit
````

### Creating a license file

Use the `-o` option to save the license to a file. The following command creates the file `LICENSE.txt` with the contents of the ISC license:

````
$ license -o LICENSE.txt isc
```` 

More options and commands are described below.

# Options

### Customize name and year on the license

By default, `license` uses the current year for the year on the generated license. For the name, `license` follows the following algorithm:

* First, it looks at provided command-line arguments
* If command-line args are absent, it looks at the environment variable `LICENSE_FULL_NAME`
* Finally, it uses the name from git config and mercurial config.

You can specify the name and year to use on the license, like so:

````
$ license --name Alice --year 2013 mit
````


### List available licenses

View the list of locally avaialable licenses by running:

````
$ license ls
````

The remote counterpart is:

````
$ license ls-remote
````

[Currently available list of licenses](https://github.com/nishanths/license/wiki/List-of-current-licenses)

### Help

Help text is available by running `license --help`. [View help command output](https://github.com/nishanths/license/wiki/Help-output)

# Contributing

Pull requests for new features, bug fixes, and suggestions are welcome!

# License

Licensed under the [MIT License](https://github.com/nishanths/license/blob/master/LICENSE).

(Yep, the license file was generated by output from this program.)

