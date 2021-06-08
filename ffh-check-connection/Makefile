include $(TOPDIR)/rules.mk

PKG_NAME:=ffh-check-connection
PKG_VERSION:=1
PKG_RELEASE:=1

include $(TOPDIR)/../package/gluon.mk

define Package/$(PKG_NAME)
  TITLE:=Checks if a node can ping definable targets
  DEPENDS:=+gluon-core +libgluonutil +gluon-site +luaposix +luabitop +micrond @GLUON_MULTIDOMAIN
endef

define Package/$(PKG_NAME)/description
  Script to check if there is a connection to configurable targets
  using ICMP ping. This script is called once every minute
  by ``micrond``. It will trigger scripts which will be executed if
  e.g. the connection state changes in a definable interval.
endef

$(eval $(call BuildPackageGluon,$(PKG_NAME)))
