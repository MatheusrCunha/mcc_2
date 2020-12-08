################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
pisca_LED_STM32F103T4.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
pisca_LED_STM32F103T4.list \

OBJCOPY_HEX += \
pisca_LED_STM32F103T4.hex \

OBJCOPY_BIN += \
pisca_LED_STM32F103T4.bin \


# All Target
all: pisca_LED_STM32F103T4.elf secondary-outputs

# Tool invocations
pisca_LED_STM32F103T4.elf: $(OBJS) $(USER_OBJS) /Users/Carcara/Desktop/Programas_uCII/pisca_LED_STM32F103T4/STM32F103T4UX_FLASH.ld
	arm-none-eabi-gcc -o "pisca_LED_STM32F103T4.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"/Users/Carcara/Desktop/Programas_uCII/pisca_LED_STM32F103T4/STM32F103T4UX_FLASH.ld" --specs=nosys.specs -Wl,-Map="pisca_LED_STM32F103T4.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

pisca_LED_STM32F103T4.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "pisca_LED_STM32F103T4.list"
	@echo 'Finished building: $@'
	@echo ' '

pisca_LED_STM32F103T4.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "pisca_LED_STM32F103T4.hex"
	@echo 'Finished building: $@'
	@echo ' '

pisca_LED_STM32F103T4.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "pisca_LED_STM32F103T4.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
