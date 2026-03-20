# eBPF Solana

Adds support to Ghidra to decompile Anza sBPF files. It supports Ghidra 12.0.4.

# Installation

- Download Release version of extension and install it in Ghidra `File → Install Extensions...`
- Use gradle to build extension: `GHIDRA_INSTALL_DIR=${GHIDRA_HOME} gradle` and use Ghidra to install it: `File → Install Extensions...`

# Known Issues
- Rebasing after a program has been imported might lead to messed up relocations.
  Everything should work as expected when specifying base address in import options.
- Functions with more than 5 parameters are not correctly decompiled. See data/languages/eBPFSol.cspec.

# Useful links

* [Main source for how solana eBPF works](https://github.com/solana-labs/rbpf).
  Contains a disassembler, implements relocations, etc.
* [General Ghidra processor module resource](https://swarm.ptsecurity.com/creating-a-ghidra-processor-module-in-sleigh-using-v8-bytecode-as-an-example/).
  Covers implementing a processor module for V8 bytecode with lots of background
  info.

