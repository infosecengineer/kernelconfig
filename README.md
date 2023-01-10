# kernelconfig

kernel config used to add NFT and Wireguard support to the solid-fog pro ubuntu image

Configs were created with 'make menuconfig' on standard linux kernel then used with the
solid-fog runme.sh script to merge configs

around Line 316 the new configs were added:

format is:
script defconfig cn913x_additions.config <additional-configs-separated-by-space>

eg:

./scripts/kconfig/merge_config.sh arch/arm64/configs/defconfig $ROOTDIR/configs/linux/cn913x_additions.config $ROOTDIR/configs/linux/nft_tables.config $ROOTDIR/configs/linux/more_config.config $ROOTDIR/configs/linux/newest_config-v2.config
