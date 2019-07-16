define KernelPackage/crypto-chacha20poly1305
  TITLE:=CryptoAPI ChaCha20-Poly1305 AEAD support
  DEPENDS:=+kmod-crypto-aead @!LINUX_3_18 @!LINUX_4_1
  KCONFIG:= \
	CONFIG_CRYPTO_CHACHA20POLY1305 \
	CONFIG_CRYPTO_CHACHA20 \
	CONFIG_CRYPTO_POLY1305
  FILES:= \
	$(LINUX_DIR)/crypto/chacha20_generic.ko \
	$(LINUX_DIR)/crypto/poly1305_generic.ko \
	$(LINUX_DIR)/crypto/chacha20poly1305.ko
  AUTOLOAD:=$(call AutoLoad,09,chacha20_generic poly1305_generic chacha20poly1305)
  $(call AddDepends/crypto)
endef

$(eval $(call KernelPackage,crypto-chacha20poly1305))
