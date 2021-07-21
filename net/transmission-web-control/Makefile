include $(TOPDIR)/rules.mk

PKG_NAME:=transmission-web-control
PKG_RELEASE:=1.6.1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/ronggang/transmission-web-control
PKG_SOURCE_DATE:=2021-05-09
PKG_SOURCE_VERSION:=f28505e81737ba42d5fd8508824eaeb799e3c3d8
PKG_MIRROR_HASH:=d361ff37411cf08530f18351086b9fcc37b298ea5470fd5a2bee067da65b4158

PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE
PKG_MAINTAINER:=Richard Yu <yurichard3839@gmail.com>

include $(INCLUDE_DIR)/package.mk

define Package/transmission-web-control
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=BitTorrent
  DEPENDS:=+transmission-daemon-openssl
  CONFLICTS:=transmission-web
  TITLE:=Transmission Web Control
  URL:=https://github.com/ronggang/transmission-web-control
  PKGARCH:=all
endef

define Package/transmission-web-control/description
 Transmission Web Control is a custom Web UI for Transmission.
endef

define Build/Compile
endef

define Package/transmission-web-control/install
	$(INSTALL_DIR) $(1)/usr/share/transmission/web
	$(CP) $(PKG_BUILD_DIR)/src/* $(1)/usr/share/transmission/web
	$(CP) $(PKG_BUILD_DIR)/src/index.html $(1)/usr/share/transmission/web/index.original.html
endef

$(eval $(call BuildPackage,transmission-web-control))
