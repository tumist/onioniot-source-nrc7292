#
# Copyright (C) 2009-2011 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=cli_app
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/newracom/nrc7292_sw_pkg
PKG_SOURCE_DATE:=2022-07-28
PKG_SOURCE_VERSION:=d3d44d9fda248d9d7673ea2bc346d115749c71f8
PKG_MIRROR_HASH:=0600c8d47656273349f050ce7cb250f6aaa6983b643f02f87b2bdd09a796b47b
#PKG_INSTALL:=0

include $(INCLUDE_DIR)/package.mk

define Package/cli_app
  SECTION:=net
  CATEGORY:=Network
  URL:=https://github.com/newracom/
  TITLE:=CLI app for nrc7292 driver
endef

define Package/cli_app/description
  Description
endef

MAKE_PATH:=package/host/src/cli_app

define Package/cli_app/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/package/host/src/cli_app/cli_app $(1)/usr/bin/
endef


$(eval $(call BuildPackage,cli_app))
