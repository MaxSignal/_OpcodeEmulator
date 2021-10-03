OpcodeEmulator by Meowthra

Intel Haswell Pentium / Celeron Series Or older processor expansion instruction set Emulation

https://www.insanelymac.com/forum/topic/329704-opcode-emulator-opemu-plug-in-project/

requires Lilu plugin

#
Updated sources to new Lilu requirements.
#
To Compile
#
- Lilu

`git clone https://github.com/acidanthera/Lilu`
`cd Lilu && git clone https://github.com/acidanthera/MacKernelSDK`
`xcodebuild -project ./Lilu.xcodeproj -configuration Debug clean build ARCHS=x86_64 ONLY_ACTIVE_ARCH=YES`
#
- OpcodeEmulator

`git clone https://github.com/LAbyOne/Opcode-Emu`
`cp -r $HOME/Lilu/build/Debug/Lilu.kext $HOME/Opcode-Emu`
`cp -Rf $HOME/Lilu/MacKernelSDK` $HOME/Opcode-Emu
`xcodebuild -project ./OpcodeEmulator/OpcodeEmulator.xcodeproj -configuration Release clean build ARCHS=x86_64 ONLY_ACTIVE_ARCH=YES`
#
