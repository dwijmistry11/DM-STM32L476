################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
001_Hello_world.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
001_Hello_world.list \

OBJCOPY_BIN += \
001_Hello_world.bin \


# All Target
all: 001_Hello_world.elf secondary-outputs

# Tool invocations
001_Hello_world.elf: $(OBJS) $(USER_OBJS) /Users/bliss/Documents/Projects/DM-STM32L476/Workplace/001_Hello\ World/001_Hello_world/STM32L476RGTX_FLASH.ld
	arm-none-eabi-gcc -o "001_Hello_world.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"/Users/bliss/Documents/Projects/DM-STM32L476/Workplace/001_Hello World/001_Hello_world/STM32L476RGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="001_Hello_world.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

001_Hello_world.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "001_Hello_world.list"
	@echo 'Finished building: $@'
	@echo ' '

001_Hello_world.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "001_Hello_world.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
