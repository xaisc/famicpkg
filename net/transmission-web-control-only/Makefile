include $(TOPDIR)/rules.mk

PKG_NAME:=transmission-web-control-only
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/ronggang/transmission-web-control
PKG_SOURCE_DATE:=2020-09-13
PKG_SOURCE_VERSION:=c26a0761e3a8fe3cff2480735ec363dc253c5105
PKG_MIRROR_HASH:=c078750537e16cd2dd1f6d01f81d1cba5b2e3a9736839970c607402473adfca0

PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE
PKG_MAINTAINER:=Richard Yu <yurichard3839@gmail.com>

include $(INCLUDE_DIR)/package.mk

define Package/transmission-web-control-only
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=BitTorrent
  DEPENDS:=
  CONFLICTS:=transmission-web,transmission-web-control
  TITLE:=Transmission Web Control Only (for Transmission Docker)
  URL:=https://github.com/ronggang/transmission-web-control
  PKGARCH:=all
endef

define Package/transmission-web-control-only/description
 Transmission Web Control is a custom Web UI for Transmission.
endef

define Build/Compile
endef

define Package/transmission-web-control-only/install
	$(INSTALL_DIR) $(1)/usr/share/transmission/web
	$(CP) $(PKG_BUILD_DIR)/src/* $(1)/usr/share/transmission/web
endef

$(eval $(call BuildPackage,transmission-web-control-only))
