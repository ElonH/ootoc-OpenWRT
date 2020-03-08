####
 #  File: /Makefile
 #  Project: libtar
 #  File Created: Saturday, 7th March 2020 6:57:51 pm
 #  Author: ElonH[EH](elonhhuang@gmail.com)
 #  License: GNU General Public License v3.0 or later(http://www.gnu.org/licenses/gpl-3.0-standalone.html)
 #  Copyright (C) 2020 [ElonH]
####

include $(TOPDIR)/rules.mk

PKG_NAME:=libtar
PKG_VERSION:=1.2.20
PKG_RELEASE:=2

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/ElonH/libtar.git
PKG_MIRROR_HASH:=8f045682622874870665f2cba1e47ae69640ed0c20cee0faeb108023f1d1bd96
PKG_SOURCE_VERSION:=f5b0048c740ad0a165187be02683db5dee607cf1
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz

PKG_LICENSE:=GPLv3
PKG_LICENSE_FILES:=LICENSE
PKG_MAINTAINER:=ElonH <elonhhuang@gmail.com>

PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)

PKG_INSTALL:=1
PKG_FIXUP:=autoreconf
PKG_USE_MIPS16:=0
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

# CONFIGURE_ARGS+= -std=c99

define Package/libtar
	SECTION:=lib
	CATEGORY:=Libraries
	URL:=https://github.com/ElonH/libtar
	TITLE:=libtar - C library for manipulating tar files
	DEPENDS:=+zlib
endef

define Package/libtar/description
libtar is a library for manipulating tar files from within C programs.
Here are some of its features:

  * Handles both POSIX tar file format and the GNU extensions.
  * API provides functions for easy use, such as tar_extract_all().
  * Also provides functions for more granular use, such as 
    tar_append_regfile().

endef

define Package/libtar/install
	# $(INSTALL_DIR) $(1)/usr/lib
endef


$(eval $(call BuildPackage,libtar))
