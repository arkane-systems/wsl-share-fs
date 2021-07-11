#
# Debian Makefile.
#

# Installation locations.

DESTDIR=debian/wsl-share-fs

BINDIR = $(DESTDIR)/usr/bin
SVCDIR = $(DESTDIR)/lib/systemd/system

#
# Default target: package.
#

package:
        # Packaging for Debian.
        debuild

package-inner:
        # Innermost iteration; invoked by debuild.

        # Binaries.
        install -Dm 0755 -o root share-distro-fs -t "$(BINDIR)"

        # Unit files.
        install -Dm 0644 -o root wsl-share-fs.service -t "$(SVCDIR)"

clean:
        debuild -- clean
