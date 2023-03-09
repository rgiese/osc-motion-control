set(TARGET osc-stepper-controller)

add_executable(${TARGET}
        main.c
        )

# Configuration
pico_set_program_url(${TARGET} "https://grumpycorp.com")
        
# Dependencies
target_link_libraries(${TARGET} 
        pico_stdlib
        pico_cyw43_arch_none
        )

# Output
pico_add_uf2_output(${TARGET})
