include $(TOPDIR)/rules.mk

PKG_NAME:=gluon-mesh-batman-adv
PKG_VERSION:=3

PKG_BUILD_DIR := $(BUILD_DIR)/$(PKG_NAME)

include $(GLUONDIR)/include/package.mk

define Package/gluon-mesh-batman-adv
  SECTION:=gluon
  CATEGORY:=Gluon
  TITLE:=Support for batman-adv meshing
  DEPENDS:=+gluon-core +kmod-batman-adv-legacy +firewall +kmod-ipt-nathelper
endef

define Package/gluon-mesh-batman-adv/description
	Gluon community wifi mesh firmware framework: batman-adv support
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/gluon-mesh-batman-adv/install
	$(CP) ./files/* $(1)/
endef

define Package/gluon-mesh-batman-adv/postinst
#!/bin/sh
$(call GluonCheckSite,check_site.lua)
endef


$(eval $(call BuildPackage,gluon-mesh-batman-adv))
