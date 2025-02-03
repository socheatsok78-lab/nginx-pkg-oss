# ngx_http_proxy_connect_module

include $(dir $(abspath $(lastword $(MAKEFILE_LIST))))/version
HTTP_PROXY_CONNECT_MODULE_URL := $(GITHUB)/chobits/ngx_http_proxy_connect_module/archive/v$(HTTP_PROXY_CONNECT_MODULE_VERSION).tar.gz

PKGS += ngx_http_proxy_connect_module

$(TARBALLS)/ngx_http_proxy_connect_module-$(HTTP_PROXY_CONNECT_MODULE_VERSION).tar.gz:
	$(call download_pkg,$(HTTP_PROXY_CONNECT_MODULE_URL),ngx_http_proxy_connect_module)

.sum-ngx_http_proxy_connect_module: ngx_http_proxy_connect_module-$(HTTP_PROXY_CONNECT_MODULE_VERSION).tar.gz

ngx_http_proxy_connect_module: ngx_http_proxy_connect_module-$(HTTP_PROXY_CONNECT_MODULE_VERSION).tar.gz .sum-ngx_http_proxy_connect_module
	$(UNPACK)
	$(APPLY) $(CONTRIB)/tarballs/ngx_http_proxy_connect_module-$(HTTP_PROXY_CONNECT_MODULE_VERSION)/patches/proxy_connect_rewrite_102101.patch
	$(MOVE)

.ngx_http_proxy_connect_module: ngx_http_proxy_connect_module
	touch $@
