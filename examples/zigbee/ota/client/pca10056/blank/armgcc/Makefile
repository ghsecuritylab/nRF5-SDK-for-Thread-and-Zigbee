PROJECT_NAME     := zigbee_ota_client_pca10056
TARGETS          := nrf52840_xxaa
OUTPUT_DIRECTORY := _build

SDK_ROOT := ../../../../../../..
PROJ_DIR := ../../..

$(OUTPUT_DIRECTORY)/nrf52840_xxaa.out: \
  LINKER_SCRIPT  := zigbee_ota_client_gcc_nrf52.ld

# Source files common to all targets
SRC_FILES += \
  $(SDK_ROOT)/modules/nrfx/mdk/gcc_startup_nrf52840.S \
  $(SDK_ROOT)/components/libraries/log/src/nrf_log_backend_rtt.c \
  $(SDK_ROOT)/components/libraries/log/src/nrf_log_backend_serial.c \
  $(SDK_ROOT)/components/libraries/log/src/nrf_log_backend_uart.c \
  $(SDK_ROOT)/components/libraries/log/src/nrf_log_default_backends.c \
  $(SDK_ROOT)/components/libraries/log/src/nrf_log_frontend.c \
  $(SDK_ROOT)/components/libraries/log/src/nrf_log_str_formatter.c \
  $(SDK_ROOT)/components/boards/boards.c \
  $(SDK_ROOT)/modules/nrfx/mdk/system_nrf52840.c \
  $(SDK_ROOT)/external/zboss/zb_error/zb_error_to_string.c \
  $(SDK_ROOT)/external/zboss/osif/zb_nrf52840_common.c \
  $(SDK_ROOT)/external/zboss/osif/zb_nrf52840_nrf_logger.c \
  $(SDK_ROOT)/external/zboss/osif/zb_nrf52840_nvram.c \
  $(SDK_ROOT)/external/zboss/osif/zb_nrf52840_ota.c \
  $(SDK_ROOT)/external/zboss/osif/zb_nrf52840_sdk_config_deps.c \
  $(SDK_ROOT)/external/zboss/osif/zb_nrf52840_timer.c \
  $(SDK_ROOT)/components/libraries/crypto/backend/cc310_bl/cc310_bl_backend_ecc.c \
  $(SDK_ROOT)/components/libraries/crypto/backend/cc310_bl/cc310_bl_backend_ecdsa.c \
  $(SDK_ROOT)/components/libraries/crypto/backend/cc310_bl/cc310_bl_backend_hash.c \
  $(SDK_ROOT)/components/libraries/crypto/backend/cc310_bl/cc310_bl_backend_init.c \
  $(SDK_ROOT)/components/libraries/crypto/backend/cc310_bl/cc310_bl_backend_shared.c \
  $(SDK_ROOT)/components/libraries/util/app_error.c \
  $(SDK_ROOT)/components/libraries/util/app_error_handler_gcc.c \
  $(SDK_ROOT)/components/libraries/util/app_error_weak.c \
  $(SDK_ROOT)/components/libraries/scheduler/app_scheduler.c \
  $(SDK_ROOT)/components/libraries/timer/app_timer.c \
  $(SDK_ROOT)/components/libraries/util/app_util_platform.c \
  $(SDK_ROOT)/components/libraries/assert/assert.c \
  $(SDK_ROOT)/components/libraries/crc32/crc32.c \
  $(SDK_ROOT)/components/libraries/mem_manager/mem_manager.c \
  $(SDK_ROOT)/components/libraries/util/nrf_assert.c \
  $(SDK_ROOT)/components/libraries/atomic/nrf_atomic.c \
  $(SDK_ROOT)/components/libraries/balloc/nrf_balloc.c \
  $(SDK_ROOT)/external/fprintf/nrf_fprintf.c \
  $(SDK_ROOT)/external/fprintf/nrf_fprintf_format.c \
  $(SDK_ROOT)/components/libraries/fstorage/nrf_fstorage.c \
  $(SDK_ROOT)/components/libraries/fstorage/nrf_fstorage_nvmc.c \
  $(SDK_ROOT)/components/libraries/memobj/nrf_memobj.c \
  $(SDK_ROOT)/components/libraries/pwr_mgmt/nrf_pwr_mgmt.c \
  $(SDK_ROOT)/components/libraries/queue/nrf_queue.c \
  $(SDK_ROOT)/components/libraries/ringbuf/nrf_ringbuf.c \
  $(SDK_ROOT)/components/libraries/experimental_section_vars/nrf_section_iter.c \
  $(SDK_ROOT)/components/libraries/strerror/nrf_strerror.c \
  $(SDK_ROOT)/components/libraries/sha256/sha256.c \
  $(SDK_ROOT)/integration/nrfx/legacy/nrf_drv_clock.c \
  $(SDK_ROOT)/integration/nrfx/legacy/nrf_drv_rng.c \
  $(SDK_ROOT)/integration/nrfx/legacy/nrf_drv_uart.c \
  $(SDK_ROOT)/modules/nrfx/hal/nrf_ecb.c \
  $(SDK_ROOT)/components/drivers_nrf/nrf_soc_nosd/nrf_nvic.c \
  $(SDK_ROOT)/modules/nrfx/hal/nrf_nvmc.c \
  $(SDK_ROOT)/components/drivers_nrf/nrf_soc_nosd/nrf_soc.c \
  $(SDK_ROOT)/modules/nrfx/soc/nrfx_atomic.c \
  $(SDK_ROOT)/modules/nrfx/drivers/src/nrfx_clock.c \
  $(SDK_ROOT)/modules/nrfx/drivers/src/prs/nrfx_prs.c \
  $(SDK_ROOT)/modules/nrfx/drivers/src/nrfx_rng.c \
  $(SDK_ROOT)/modules/nrfx/drivers/src/nrfx_systick.c \
  $(SDK_ROOT)/modules/nrfx/drivers/src/nrfx_timer.c \
  $(SDK_ROOT)/modules/nrfx/drivers/src/nrfx_uart.c \
  $(SDK_ROOT)/modules/nrfx/drivers/src/nrfx_uarte.c \
  $(SDK_ROOT)/components/libraries/crypto/nrf_crypto_ecc.c \
  $(SDK_ROOT)/components/libraries/crypto/nrf_crypto_ecdsa.c \
  $(SDK_ROOT)/components/libraries/crypto/nrf_crypto_hash.c \
  $(SDK_ROOT)/components/libraries/crypto/nrf_crypto_init.c \
  $(SDK_ROOT)/components/libraries/crypto/nrf_crypto_shared.c \
  $(PROJ_DIR)/../../../dfu/dfu_public_key.c \
  $(PROJ_DIR)/main.c \
  $(SDK_ROOT)/external/segger_rtt/SEGGER_RTT.c \
  $(SDK_ROOT)/external/segger_rtt/SEGGER_RTT_Syscalls_GCC.c \
  $(SDK_ROOT)/external/segger_rtt/SEGGER_RTT_printf.c \
  $(SDK_ROOT)/components/iot/background_dfu/background_dfu_block.c \
  $(SDK_ROOT)/components/iot/background_dfu/background_dfu_operation.c \
  $(SDK_ROOT)/components/iot/background_dfu/background_dfu_state.c \
  $(SDK_ROOT)/external/nano-pb/pb_common.c \
  $(SDK_ROOT)/external/nano-pb/pb_decode.c \
  $(SDK_ROOT)/components/libraries/bootloader/dfu/dfu-cc.pb.c \
  $(SDK_ROOT)/components/libraries/bootloader/dfu/nrf_dfu.c \
  $(SDK_ROOT)/components/libraries/bootloader/dfu/nrf_dfu_flash.c \
  $(SDK_ROOT)/components/libraries/bootloader/dfu/nrf_dfu_handling_error.c \
  $(SDK_ROOT)/components/libraries/bootloader/dfu/nrf_dfu_mbr.c \
  $(SDK_ROOT)/components/libraries/bootloader/dfu/nrf_dfu_req_handler.c \
  $(SDK_ROOT)/components/libraries/bootloader/dfu/nrf_dfu_settings.c \
  $(SDK_ROOT)/components/libraries/bootloader/dfu/nrf_dfu_transport.c \
  $(SDK_ROOT)/components/libraries/bootloader/dfu/nrf_dfu_utils.c \
  $(SDK_ROOT)/components/libraries/bootloader/dfu/nrf_dfu_validation.c \
  $(SDK_ROOT)/components/libraries/bootloader/dfu/nrf_dfu_ver_validation.c \
  $(SDK_ROOT)/components/zigbee/ota/zigbee_dfu_transport.c \
  $(SDK_ROOT)/components/zigbee/common/zigbee_helpers.c \
  $(SDK_ROOT)/components/zigbee/common/zigbee_logger_eprxzcl.c \
  $(SDK_ROOT)/components/libraries/crypto/backend/oberon/oberon_backend_chacha_poly_aead.c \
  $(SDK_ROOT)/components/libraries/crypto/backend/oberon/oberon_backend_ecc.c \
  $(SDK_ROOT)/components/libraries/crypto/backend/oberon/oberon_backend_ecdh.c \
  $(SDK_ROOT)/components/libraries/crypto/backend/oberon/oberon_backend_ecdsa.c \
  $(SDK_ROOT)/components/libraries/crypto/backend/oberon/oberon_backend_eddsa.c \
  $(SDK_ROOT)/components/libraries/crypto/backend/oberon/oberon_backend_hash.c \
  $(SDK_ROOT)/components/libraries/crypto/backend/oberon/oberon_backend_hmac.c \

# Include folders common to all targets
INC_FOLDERS += \
  $(SDK_ROOT)/components/softdevice/mbr/nrf52840/headers \
  $(SDK_ROOT)/components/libraries/crypto/backend/cc310 \
  $(SDK_ROOT)/components/libraries/crypto/backend/cifra \
  $(SDK_ROOT)/external/fprintf \
  $(PROJ_DIR) \
  $(SDK_ROOT)/components/iot/background_dfu \
  $(SDK_ROOT)/components/libraries/experimental_section_vars \
  $(SDK_ROOT)/external/zboss/osif \
  $(SDK_ROOT)/external/nrf_cc310/include \
  $(SDK_ROOT)/components/libraries/atomic \
  ../config \
  $(SDK_ROOT)/external/nRF-IEEE-802.15.4-radio-driver/src \
  $(SDK_ROOT)/external/zboss/include/ha \
  $(SDK_ROOT)/components/libraries/delay \
  $(SDK_ROOT)/external/nRF-IEEE-802.15.4-radio-driver/src/rsch \
  $(SDK_ROOT)/external/nrf_oberon/include \
  $(SDK_ROOT)/external/nRF-IEEE-802.15.4-radio-driver/src/mac_features \
  $(SDK_ROOT)/components/iot/background_dfu/transport \
  $(SDK_ROOT)/external/nRF-IEEE-802.15.4-radio-driver/src/mac_features/ack_generator \
  $(SDK_ROOT)/components/libraries/crypto \
  $(SDK_ROOT)/components/toolchain/cmsis/include \
  $(SDK_ROOT)/components/libraries/balloc \
  $(SDK_ROOT)/components/libraries/mem_manager \
  $(SDK_ROOT)/components/libraries/log \
  $(SDK_ROOT)/external/nrf_oberon \
  $(SDK_ROOT)/components/libraries/memobj \
  $(SDK_ROOT)/components/libraries/stack_info \
  $(SDK_ROOT)/components/libraries/crypto/backend/optiga \
  $(SDK_ROOT)/components/libraries/crypto/backend/nrf_sw \
  $(SDK_ROOT)/components/libraries/scheduler \
  $(SDK_ROOT)/components/libraries/strerror \
  $(SDK_ROOT)/integration/nrfx \
  $(SDK_ROOT)/components/zigbee/ota \
  $(SDK_ROOT)/modules/nrfx/drivers/include \
  $(SDK_ROOT)/components/zigbee/common \
  $(SDK_ROOT)/components/libraries/crypto/backend/cc310_bl \
  $(SDK_ROOT)/external/zboss/include/zcl \
  $(SDK_ROOT)/components/libraries/bootloader/dfu \
  $(SDK_ROOT)/external/zboss/include \
  $(SDK_ROOT)/components/libraries/ringbuf \
  $(SDK_ROOT)/external/nano-pb \
  $(SDK_ROOT)/modules/nrfx \
  $(SDK_ROOT)/components/drivers_nrf/nrf_soc_nosd \
  $(SDK_ROOT)/components/libraries/log/src \
  $(SDK_ROOT)/external/segger_rtt \
  $(SDK_ROOT)/external/zboss/include/osif \
  $(SDK_ROOT)/external/zboss/zb_error \
  $(SDK_ROOT)/modules/nrfx/hal \
  $(SDK_ROOT)/components/libraries/mutex \
  $(SDK_ROOT)/components/libraries/crypto/backend/micro_ecc \
  $(SDK_ROOT)/components/libraries/crypto/backend/mbedtls \
  $(SDK_ROOT)/components/libraries/queue \
  $(SDK_ROOT)/components/libraries/pwr_mgmt \
  $(SDK_ROOT)/components/libraries/crypto/backend/nrf_hw \
  $(SDK_ROOT)/external/nrf_cc310_bl/include \
  $(SDK_ROOT)/integration/nrfx/legacy \
  $(SDK_ROOT)/modules/nrfx/mdk \
  $(SDK_ROOT)/components/libraries/crc32 \
  $(SDK_ROOT)/components/libraries/fstorage \
  $(SDK_ROOT)/components/boards \
  $(SDK_ROOT)/components/libraries/timer \
  $(SDK_ROOT)/external/nRF-IEEE-802.15.4-radio-driver/src/fem \
  $(SDK_ROOT)/components/libraries/util \
  $(SDK_ROOT)/components/libraries/sha256 \
  $(SDK_ROOT)/components/libraries/crypto/backend/oberon \
  $(SDK_ROOT)/components/libraries/bootloader \

# Libraries common to all targets
LIB_FILES += \
  $(SDK_ROOT)/external/zboss/lib/gcc/libzboss.a \
  $(SDK_ROOT)/external/zboss/lib/gcc/nrf_radio_driver.a \
  $(SDK_ROOT)/external/nrf_oberon/lib/cortex-m4/hard-float/liboberon_2.0.7.a \
  $(SDK_ROOT)/external/nrf_cc310_bl/lib/cortex-m4/hard-float/libnrf_cc310_bl_0.9.12.a \

# Optimization flags
OPT = -Os -ggdb3
# Uncomment the line below to enable link time optimization
#OPT += -flto

# C flags common to all targets
CFLAGS += $(OPT)
CFLAGS += -DBOARD_PCA10056
CFLAGS += -DBOOTLOADER_START_ADDR=BOOTLOADER_ADDRESS
CFLAGS += -DCONFIG_GPIO_AS_PINRESET
CFLAGS += -DENABLE_FEM
CFLAGS += -DFLOAT_ABI_HARD
CFLAGS += -DMBR_PRESENT
CFLAGS += -DNRF52840_XXAA
CFLAGS += -DNRF_DFU_SETTINGS_VERSION=2
CFLAGS += -DSWI_DISABLE0
CFLAGS += -DZB_TRACE_LEVEL=0
CFLAGS += -DZB_TRACE_MASK=0
CFLAGS += -mcpu=cortex-m4
CFLAGS += -mthumb -mabi=aapcs
CFLAGS += -Wall -Werror
CFLAGS += -mfloat-abi=hard -mfpu=fpv4-sp-d16
# keep every function in a separate section, this allows linker to discard unused ones
CFLAGS += -ffunction-sections -fdata-sections -fno-strict-aliasing
CFLAGS += -fno-builtin -fshort-enums -Wno-packed-bitfield-compat

# C++ flags common to all targets
CXXFLAGS += $(OPT)
# Assembler flags common to all targets
ASMFLAGS += -ggdb3
ASMFLAGS += -mcpu=cortex-m4
ASMFLAGS += -mthumb -mabi=aapcs
ASMFLAGS += -mfloat-abi=hard -mfpu=fpv4-sp-d16
ASMFLAGS += -DBOARD_PCA10056
ASMFLAGS += -DCONFIG_GPIO_AS_PINRESET
ASMFLAGS += -DENABLE_FEM
ASMFLAGS += -DFLOAT_ABI_HARD
ASMFLAGS += -DMBR_PRESENT
ASMFLAGS += -DNRF52840_XXAA
ASMFLAGS += -DNRF_DFU_SETTINGS_VERSION=2
ASMFLAGS += -DSWI_DISABLE0
ASMFLAGS += -DZB_TRACE_LEVEL=0
ASMFLAGS += -DZB_TRACE_MASK=0

# Linker flags
LDFLAGS += $(OPT)
LDFLAGS += -mthumb -mabi=aapcs -L$(SDK_ROOT)/modules/nrfx/mdk -T$(LINKER_SCRIPT)
LDFLAGS += -mcpu=cortex-m4
LDFLAGS += -mfloat-abi=hard -mfpu=fpv4-sp-d16
# let linker dump unused sections
LDFLAGS += -Wl,--gc-sections
# use newlib in nano version
LDFLAGS += --specs=nano.specs

nrf52840_xxaa: CFLAGS += -D__HEAP_SIZE=8192
nrf52840_xxaa: CFLAGS += -D__STACK_SIZE=8192
nrf52840_xxaa: ASMFLAGS += -D__HEAP_SIZE=8192
nrf52840_xxaa: ASMFLAGS += -D__STACK_SIZE=8192

# Add standard libraries at the very end of the linker input, after all objects
# that may need symbols provided by these libraries.
LIB_FILES += -lc -lnosys -lm -lstdc++


.PHONY: default help

# Default target - first one defined
default: nrf52840_xxaa

# Print all targets that can be built
help:
	@echo following targets are available:
	@echo		nrf52840_xxaa
	@echo		sdk_config - starting external tool for editing sdk_config.h
	@echo		flash      - flashing binary

TEMPLATE_PATH := $(SDK_ROOT)/components/toolchain/gcc


include $(TEMPLATE_PATH)/Makefile.common

$(foreach target, $(TARGETS), $(call define_target, $(target)))

.PHONY: flash erase

# Flash the program
flash: default
	@echo Flashing: $(OUTPUT_DIRECTORY)/nrf52840_xxaa.hex
	nrfjprog -f nrf52 --program $(OUTPUT_DIRECTORY)/nrf52840_xxaa.hex --sectorerase
	nrfjprog -f nrf52 --reset

erase:
	nrfjprog -f nrf52 --eraseall

SDK_CONFIG_FILE := ../config/sdk_config.h
CMSIS_CONFIG_TOOL := $(SDK_ROOT)/external_tools/cmsisconfig/CMSIS_Configuration_Wizard.jar
sdk_config:
	java -jar $(CMSIS_CONFIG_TOOL) $(SDK_CONFIG_FILE)
