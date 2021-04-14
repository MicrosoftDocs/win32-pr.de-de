---
description: Beschreibt mögliche Computerarchitekturen.
ms.assetid: 1E5E4F98-925B-424D-9B3D-BC6716FBF990
title: Bilddatei-Computer Konstanten (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c8c43767ce0d86edf2285241772ea060573efc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526984"
---
# <a name="image-file-machine-constants"></a>Bilddatei-Computer Konstanten

Beschreibt mögliche Computerarchitekturen. Wird in [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a), [**IsWow64GuestMachineSupported**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64guestmachinesupported) und [**IsWow64Process2**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process2)verwendet.

<dl> <dt>

<span id="IMAGE_FILE_MACHINE_UNKNOWN"></span><span id="image_file_machine_unknown"></span>**Bild \_ Datei \_ Computer \_ unbekannt**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Unbekannt


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_TARGET_HOST"></span><span id="image_file_machine_target_host"></span>**\_Bilddatei \_ - \_ \_ Zielhost**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Interagiert mit dem Host und nicht mit einem WOW64-Gast

> [!Note]  
> Diese Konstante ist ab Windows 10, Version 1607 und Windows Server 2016 verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_I386"></span><span id="image_file_machine_i386"></span>**Bild \_ Datei \_ Computer \_ i386**
</dt> <dd> <dl> <dt>

0x014c
</dt> <dt>



Intel 386


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R3000"></span><span id="image_file_machine_r3000"></span>**Image \_ Datei \_ Computer \_ R3000**
</dt> <dd> <dl> <dt>

0x0162
</dt> <dt>



MIPS Little--in, 0x160 Big---in


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R4000"></span><span id="image_file_machine_r4000"></span>**Image \_ Datei \_ Computer \_ R4000**
</dt> <dd> <dl> <dt>

0x0166
</dt> <dt>



MIPS Little-d


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R10000"></span><span id="image_file_machine_r10000"></span>**Image \_ Datei \_ Computer \_ R10000**
</dt> <dd> <dl> <dt>

0x0168
</dt> <dt>



MIPS Little-d


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_WCEMIPSV2"></span><span id="image_file_machine_wcemipsv2"></span>**Image \_ Datei \_ Computer \_ WCEMIPSV2**
</dt> <dd> <dl> <dt>

0x0169
</dt> <dt>



MIPS Little-in WCE v2


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ALPHA"></span><span id="image_file_machine_alpha"></span>**Bild \_ Datei \_ Computer \_ Alpha**
</dt> <dd> <dl> <dt>

0x0184
</dt> <dt>



Alpha \_ AXP


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3"></span><span id="image_file_machine_sh3"></span>**Image \_ Datei \_ Computer \_ SH3**
</dt> <dd> <dl> <dt>

0x01a2
</dt> <dt>



SH3 Little-d


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3DSP"></span><span id="image_file_machine_sh3dsp"></span>**Image \_ Datei \_ Computer \_ SH3DSP**
</dt> <dd> <dl> <dt>

0x01a3
</dt> <dt>



SH3DSP


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3E"></span><span id="image_file_machine_sh3e"></span>**Image \_ Datei \_ Computer \_ SH3E**
</dt> <dd> <dl> <dt>

0x01a4
</dt> <dt>



SH3E Little-d


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH4"></span><span id="image_file_machine_sh4"></span>**Image \_ Datei \_ Computer \_ SH4**
</dt> <dd> <dl> <dt>

0x01a6
</dt> <dt>



SH4 Little-d


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH5"></span><span id="image_file_machine_sh5"></span>**Image \_ Datei \_ Computer \_ SH5**
</dt> <dd> <dl> <dt>

0x01a8
</dt> <dt>



SH5


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARM"></span><span id="image_file_machine_arm"></span>**Bild \_ Datei \_ Computer- \_ Arm**
</dt> <dd> <dl> <dt>

0x01c0
</dt> <dt>



Arm-Little-Endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_THUMB"></span><span id="image_file_machine_thumb"></span>**Ziehpunkt für Bild \_ Datei \_ Computer \_**
</dt> <dd> <dl> <dt>

0x01c2
</dt> <dt>



Arm Thumb/Thumb-2 Little-Endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARMNT"></span><span id="image_file_machine_armnt"></span>**Bilddatei- \_ \_ Computer \_ armnt**
</dt> <dd> <dl> <dt>

0x01c4
</dt> <dt>



Arm-Thumb-2-Little-Endian

> [!Note]  
> Diese Konstante ist ab Windows 7 und Windows Server 2008 R2 verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AM33"></span><span id="image_file_machine_am33"></span>**Image \_ Datei \_ Computer \_ AM33**
</dt> <dd> <dl> <dt>

0x01d3
</dt> <dt>



TAM33BD


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_POWERPC"></span><span id="image_file_machine_powerpc"></span>**Bild \_ Datei \_ Computer \_ powerpc**
</dt> <dd> <dl> <dt>

0x01f 0
</dt> <dt>



IBM PowerPC-Little-Endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_POWERPCFP"></span><span id="image_file_machine_powerpcfp"></span>**Image \_ Datei \_ Computer- \_ powerpcfp**
</dt> <dd> <dl> <dt>

0x01f 1
</dt> <dt>



Powerpcfp


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_IA64"></span><span id="image_file_machine_ia64"></span>**Bild \_ Datei \_ Computer \_ ia64**
</dt> <dd> <dl> <dt>

0x0200
</dt> <dt>



Intel 64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPS16"></span><span id="image_file_machine_mips16"></span>**Image \_ Datei \_ Computer \_ MIPS16**
</dt> <dd> <dl> <dt>

0x0266
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ALPHA64"></span><span id="image_file_machine_alpha64"></span>**Image \_ Datei \_ Computer \_ ALPHA64**
</dt> <dd> <dl> <dt>

0x0284
</dt> <dt>



ALPHA64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPSFPU"></span><span id="image_file_machine_mipsfpu"></span>**Bild \_ Datei \_ Computer \_ mipsfpu**
</dt> <dd> <dl> <dt>

0x0366
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPSFPU16"></span><span id="image_file_machine_mipsfpu16"></span>**Image \_ Datei \_ Computer \_ MIPSFPU16**
</dt> <dd> <dl> <dt>

0x0466
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AXP64"></span><span id="image_file_machine_axp64"></span>**Image \_ Datei \_ Computer \_ AXP64**
</dt> <dd> <dl> <dt>

0x0284
</dt> <dt>



AXP64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_TRICORE"></span><span id="image_file_machine_tricore"></span>**der Abbild \_ Datei- \_ Computer- \_ zentrale**
</dt> <dd> <dl> <dt>

0x0520
</dt> <dt>



Infineon


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_CEF"></span><span id="image_file_machine_cef"></span>**Image \_ Datei \_ Computer \_ CEF**
</dt> <dd> <dl> <dt>

0x0cef
</dt> <dt>



CEF


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_EBC"></span><span id="image_file_machine_ebc"></span>**Image \_ Datei \_ Computer \_ EBC**
</dt> <dd> <dl> <dt>

0x0ebc
</dt> <dt>



EFI-Bytecode


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AMD64"></span><span id="image_file_machine_amd64"></span>**Bild \_ Datei \_ Computer \_ amd64**
</dt> <dd> <dl> <dt>

0x8664
</dt> <dt>



Amd64 (K8)


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_M32R"></span><span id="image_file_machine_m32r"></span>**Image \_ Datei \_ Computer \_ M32R**
</dt> <dd> <dl> <dt>

0x9041
</dt> <dt>



M32R Little-d


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARM64"></span><span id="image_file_machine_arm64"></span>**Image \_ Datei \_ Computer \_ ARM64**
</dt> <dd> <dl> <dt>

0xaa64
</dt> <dt>



ARM64 Little-Endian

> [!Note]  
> Diese Konstante ist ab Windows 8.1 und Windows Server 2012 R2 verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_CEE"></span><span id="image_file_machine_cee"></span>**Bild \_ Datei \_ Computer- \_ CEE**
</dt> <dd> <dl> <dt>

0xc0ee
</dt> <dt>



CEE


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WinNT. h</dt> </dl> |



 

 




