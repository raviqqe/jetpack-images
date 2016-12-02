PARENT_IMAGE = 3ofcoins.net/freebsd-base
PKG_INSTALL = nsd

zone_file = raviqqe.com.zone
conf_file = nsd.conf

build:
	for file in ${conf_file} ${zone_file}; \
	do \
		install -v -m 0600 $$file /usr/local/etc/nsd/$$file; \
	done
	sysrc nsd_enable=YES

.include <${.jetpack.image.mk:U${${JETPACK:Ujetpack} config path.share:L:sh}/jetpack.image.mk}>
