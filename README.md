# C16-multicart
4MB multicart for C16/PLUS4 computer. Supports single-load PRG-files and cartridge images that are selectable via simple menu.

Cart is based to 2 x 27C160 EPROMs running on 8 bit mode and using memory areas for c1lo and c1hi. EPROM memory space is furthermore split to 128 32kB banks. Reset signal returns to bank 0 and manual bank switching can be done by writing bank number to memory address $fda0.

generate_c16_multicart.py script generates EPROM binaries that can be used with cartridge. Script uses files and directories as input parameter and generates eprom binaries from suitable files (single-load prgs and cart-binaries) also adds simple menu.  

E.g.
python generate_c16_multicart.py files/

will generate files cart_lo.bin and cart_hi.bin. Those files can then be burn to 27C160 EPROMs.
