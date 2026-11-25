# QM OS by Rust Unlicense

## Cây thư mục


  
```
crates/
├──qm-image
│   │   Cargo.toml
│   │   
│   ├──docs
│   │   │   0.md
│   │   │   1.md
│   │   │   3-demo.md
│   │   │   lib.md
│   │   │   
│   │   └──tests
│   │           bundle_and_container.md
│   │           
│   ├──src
│   │       bundle.rs
│   │       container.rs
│   │       error.rs
│   │       lib.rs
│   │       writer.rs
│   │       
│   └──tests
│           bundle_and_container.rs
│           
├──qm-kernel
│   │   Cargo.toml
│   │   link.ld
│   │   README.md
│   │   
│   ├──docs
│   │   │   0-custom-container.md
│   │   │   1-main.md
│   │   │   2-panic.md
│   │   │   3-log.md
│   │   │   link_linker.md
│   │   │   pha_0.md
│   │   │   pha_0_1.md
│   │   │   server.md
│   │   │   
│   │   ├──arch
│   │   ├──boot
│   │   │   │   0-common.md
│   │   │   │   0.md
│   │   │   │   1-mod.md
│   │   │   │   2-entry.md
│   │   │   │   3-sbi.md
│   │   │   │   4-uart.md
│   │   │   │   dtb.md
│   │   │   │   initframefs.md
│   │   │   │   
│   │   │   ├──common
│   │   │   │       boot_info.md
│   │   │   │       container.md
│   │   │   │       mod.md
│   │   │   │       
│   │   │   ├──riscv64
│   │   │   │       0.md
│   │   │   │       dtb.md
│   │   │   │       entry.md
│   │   │   │       mod.md
│   │   │   │       sbi.md
│   │   │   │       uart.md
│   │   │   │       
│   │   │   └──x86_64
│   │   │           entry.md
│   │   │           mod.md
│   │   │           stage_0.md
│   │   │           
│   │   ├──loader
│   │   │       container.md
│   │   │       mod.md
│   │   │       
│   │   ├──log
│   │   │       mod.md
│   │   │       
│   │   ├──memory
│   │   │       mod.md
│   │   │       
│   │   ├──scheduler
│   │   │       mod.md
│   │   │       
│   │   └──sync
│   │           mod.md
│   │           spinlock.md
│   │           
│   ├──src
│   │   │   boot_stage.rs
│   │   │   log-.rs
│   │   │   main.rs
│   │   │   panic.rs
│   │   │   
│   │   ├──arch
│   │   │   │   mod.rs
│   │   │   │   
│   │   │   ├──riscv64
│   │   │   │   │   csr.rs
│   │   │   │   │   mod.rs
│   │   │   │   │   trap.rs
│   │   │   │   │   
│   │   │   │   └──paging
│   │   │   │           mapper.rs
│   │   │   │           pte.rs
│   │   │   │           runtime.rs
│   │   │   │           scheme.rs
│   │   │   │           table.rs
│   │   │   │           
│   │   │   └──x86_64
│   │   │           sys_regs.rs
│   │   │           
│   │   ├──boot
│   │   │   │   mod.rs
│   │   │   │   
│   │   │   ├──aarch64
│   │   │   ├──common
│   │   │   │       boot_info.rs
│   │   │   │       container.rs
│   │   │   │       mod.rs
│   │   │   │       
│   │   │   ├──riscv64
│   │   │   │       dtb.rs
│   │   │   │       entry.rs
│   │   │   │       sbi.rs
│   │   │   │       uart.rs
│   │   │   │       
│   │   │   └──x86_64
│   │   │           entry.rs
│   │   │           mod.rs
│   │   │           paging.rs
│   │   │           pat.rs
│   │   │           pcid.rs
│   │   │           stage_0.rs
│   │   │           w_x.rs
│   │   │           
│   │   ├──loader
│   │   │       mod.rs
│   │   │       
│   │   ├──log
│   │   │   │   mod.rs
│   │   │   │   
│   │   │   └──x86_64
│   │   │           io_com1.rs
│   │   │           
│   │   ├──memory
│   │   │       frame.rs
│   │   │       mod.rs
│   │   │       
│   │   ├──scheduler
│   │   │       mod.rs
│   │   │       
│   │   ├──sync
│   │   │       mod.rs
│   │   │       spinlock.rs
│   │   │       
│   │   └──syscall
│   │           mod.rs
│   │           
│   └──tests
│       └──boot
│           ├──riscv64
│           │       sv39_math.rs
│           │       
│           └──x86_64
│                   stage_0_0_paging_math.rs
│                   stage_0_1_page_table_builder.rs
│                   stage_0_2_boot_memory_layout.rs
│                   stage_0_3_boot_mapping_plan.rs
│                   stage_0_4_apply_plan_to_tables.rs
│                   
├──qm-shell
│   │   Cargo.toml
│   │   
│   └──src
│           lib.rs
│           main.rs
│           window_manager.rs
│           
├──qm-sys
│   │   Cargo.toml
│   │   
│   ├──docs
│   │       0-sys.md
│   │       1-types.md
│   │       10-container.md
│   │       10-vdso.md
│   │       11-syscall.md
│   │       2-rights.md
│   │       3-handle.md
│   │       4-error.md
│   │       5-signals.md
│   │       6-memobj.md
│   │       7-channel.md
│   │       8-process.md
│   │       9-bootinfo.md
│   │       
│   ├──src
│   │   │   bootinfo.rs
│   │   │   channel.rs
│   │   │   error.rs
│   │   │   handle.rs
│   │   │   lib.rs
│   │   │   memobj.rs
│   │   │   process.rs
│   │   │   rights.rs
│   │   │   signals.rs
│   │   │   syscall.rs
│   │   │   types.rs
│   │   │   
│   │   └──container
│   │           bootstrap.rs
│   │           header.rs
│   │           mod.rs
│   │           segment.rs
│   │           
│   └──tests
│           integration_tests.rs
│           
├──qm-ui
│   │   Cargo.toml
│   │   
│   └──src
│           lib.rs
│           
├──qm-web
│   │   Cargo.toml
│   │   index.html
│   │   README.md
│   │   Trunk.toml
│   │   
│   ├──icons
│   │       quangmy-192x192.png
│   │       quangmy-512x512.png
│   │       
│   ├──src
│   │       main.rs
│   │       
│   └──static
│           qm-web-compositor.js
│           qm-web-init-worker.js
│           qm-web-kernel-worker.js
│           
├──qm-web-kernel
│   │   Cargo.toml
│   │   index.html
│   │   Trunk.toml
│   │   
│   └──src
│           main.rs
│           wasm_bridge.rs
│           
├──qm-web-sys
│   │   Cargo.toml
│   │   
│   └──src
│           compositor.rs
│           lib.rs
│           sab.rs
│           
├──qm-xtask
│   │   Cargo.toml
│   │   
│   ├──docs
│   │       0.md
│   │       main.md
│   │       run.md
│   │       
│   └──src
│       │   bundle.rs
│       │   main.rs
│       │   
│       └──arch
│               mod.rs
│               riscv64.rs
│               x86_64.rs
│               
└──qm-zerox
    │   Cargo.toml
    │   
    └──src
            lib.rs
            lib2.rs
            
```

## License
[Unlicense](LICENSE).
