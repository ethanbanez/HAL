# TODO: find compile time definitions that enable LL driver

# USE_FULL_LL_DRIVER
add_library(stm32hal STATIC)
target_include_directories(stm32hal PUBLIC Inc)
target_link_libraries(stm32hal
PRIVATE
armcmsis
stm32cmsis_headers
)
target_sources(stm32hal 
PRIVATE 
Src/stm32h7xx_ll_utils.c
)