###############################################################################
# Makefile for project 
###############################################################################

## General options
PROJECT = 
MCU = 80C31
COMPILER = "ASEM-51 (Proteus)"
TARGET = Debug
SHELL = C:\WINDOWS\system32\cmd.exe

## Tools general options

## Processing Tools
ASM=asem.exe
DDX=ASEMDDX.EXE
#  D:/2020计组课设/80C31/Debug/Debug.HEX: TOOL=ASM
#  Post: $(DDX) $(DDXFLAGS) Debug.lst
#     D:/2020计组课设/ASM/1126TEST.asm

# Build tree:
all:	Debug

Debug:	Debug.HEX

Debug.HEX:	../../ASM/1126TEST.asm 
	$(ASM) "..\..\ASM\1126TEST.asm" "Debug.HEX" Debug.lst $(ASMFLAGS)  /INCLUDES:"..\..\..\Proteus 8 Professional\Tools\ASEM51"
	$(DDX) $(DDXFLAGS) Debug.lst

# tidy - delete all temporary files which are not involved in the target generation
tidy:
	rm -rf Debug.lst

# cleanup - delete all generated files
clean:	tidy
	rm -rf Debug.HEX
	rm -rf Debug.SDI
