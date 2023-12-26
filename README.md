INSTALLER
=========

Installer is a simple script that creates a `install.sh` file
that automatically downloads and extracts a package.

## Help

installer

    Usage: installer [PARAMS...]
    
    This commands read the "InstallFile" file and creates a "install.sh"
    file that automatically downloads and extracts the package.
    
    The "InstallFile" file is a bourne shell script. It contains the
    urls to download in TARFILES variable.
    
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    #H: Help message.
    TARFILES="
        https://.../PACKAGE--$(uname -s)-$(uname -m).tar.gz
        ...
    "
    GETURLS() {
        : Alternative URL calculation.
    }
    POSTINSTALL() {
        : Executed after installation.
    }
    CHECKUSER() {
        : Executed before installation to check permissions. It is
        : skipped if the user specified a DESTDIR.
    }
    DESTDIR=<dir>       # The directory onto which to extract the tars.
    LICENSE_REGEX=REGEX # LICENSE file regex in tars to ask for acceptance.
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

## Collaborating

For making bug reports, feature requests and donations visit
one of the following links:

1. [gemini://harkadev.com/oss/](gemini://harkadev.com/oss/)
2. [https://harkadev.com/oss/](https://harkadev.com/oss/)
