# name of your application
APPLICATION = cpp11_condition_variable
include ../Makefile.tests_common

# ROM is overflowing for these boards when using
# gcc-arm-none-eabi-4.9.3.2015q2-1trusty1 from ppa:terry.guo/gcc-arm-embedded
# (Travis is using this PPA currently, 2015-06-23)
# Debian jessie libstdc++-arm-none-eabi-newlib-4.8.3-9+4 works fine, though.
# Remove this line if Travis is upgraded to a different toolchain which does
# not pull in all C++ locale code whenever exceptions are used.
BOARD_INSUFFICIENT_MEMORY := nucleo-f334 spark-core stm32f0discovery

# Comment this out to disable code in RIOT that does safety checking
# which is not needed in a production environment but helps in the
# development process:
CFLAGS += -DDEVELHELP

# If you want to add some extra flags when compile c++ files, add these flags
# to CXXEXFLAGS variable
CXXEXFLAGS += -std=c++11

USEMODULE += cpp11-compat
USEMODULE += xtimer
USEMODULE += timex

include $(RIOTBASE)/Makefile.include
