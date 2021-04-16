---
description: Stellt die Attribute der grundlegenden Eingabe-/Ausgabedienste (BIOS) des Computer Systems dar, die auf einem Computer installiert sind.
ms.assetid: e4a5aaf0-0432-4517-97b7-ac05ffd10b5b
ms.tgt_platform: multiple
title: Win32_BIOS-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BIOS
- Win32_BIOS.BiosCharacteristics
- Win32_BIOS.BIOSVersion
- Win32_BIOS.BuildNumber
- Win32_BIOS.Caption
- Win32_BIOS.CodeSet
- Win32_BIOS.CurrentLanguage
- Win32_BIOS.Description
- Win32_BIOS.EmbeddedControllerMajorVersion
- Win32_BIOS.EmbeddedControllerMinorVersion
- Win32_BIOS.IdentificationCode
- Win32_BIOS.InstallableLanguages
- Win32_BIOS.InstallDate
- Win32_BIOS.LanguageEdition
- Win32_BIOS.ListOfLanguages
- Win32_BIOS.Manufacturer
- Win32_BIOS.Name
- Win32_BIOS.OtherTargetOS
- Win32_BIOS.PrimaryBIOS
- Win32_BIOS.ReleaseDate
- Win32_BIOS.SerialNumber
- Win32_BIOS.SMBIOSBIOSVersion
- Win32_BIOS.SMBIOSMajorVersion
- Win32_BIOS.SMBIOSMinorVersion
- Win32_BIOS.SMBIOSPresent
- Win32_BIOS.SoftwareElementID
- Win32_BIOS.SoftwareElementState
- Win32_BIOS.Status
- Win32_BIOS.SystemBiosMajorVersion
- Win32_BIOS.SystemBiosMinorVersion
- Win32_BIOS.TargetOperatingSystem
- Win32_BIOS.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 53c1e953c9c1348a133cf4755ab04f6024c42034
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524112"
---
# <a name="win32_bios-class"></a><span data-ttu-id="1c0a2-103">Win32- \_ BIOS-Klasse</span><span class="sxs-lookup"><span data-stu-id="1c0a2-103">Win32\_BIOS class</span></span>

<span data-ttu-id="1c0a2-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) des **Win32- \_ BIOS** stellt die Attribute der grundlegenden Eingabe-/Ausgabedienste (BIOS) des Computer Systems dar, die auf einem Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-104">The **Win32\_BIOS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the attributes of the computer system's basic input/output services (BIOS) that are installed on a computer.</span></span>

<span data-ttu-id="1c0a2-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1c0a2-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c0a2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c0a2-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_BIOS : CIM_BIOSElement
{
  uint16   BiosCharacteristics[];
  string   BIOSVersion[];
  string   BuildNumber;
  string   Caption;
  string   CodeSet;
  string   CurrentLanguage;
  string   Description;
  uint8    EmbeddedControllerMajorVersion;
  uint8    EmbeddedControllerMinorVersion;
  string   IdentificationCode;
  uint16   InstallableLanguages;
  datetime InstallDate;
  string   LanguageEdition;
  String   ListOfLanguages[];
  string   Manufacturer;
  string   Name;
  string   OtherTargetOS;
  boolean  PrimaryBIOS;
  datetime ReleaseDate;
  string   SerialNumber;
  string   SMBIOSBIOSVersion;
  uint16   SMBIOSMajorVersion;
  uint16   SMBIOSMinorVersion;
  boolean  SMBIOSPresent;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  string   Status;
  uint8    SystemBiosMajorVersion;
  uint8    SystemBiosMinorVersion;
  uint16   TargetOperatingSystem;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="1c0a2-108">Member</span><span class="sxs-lookup"><span data-stu-id="1c0a2-108">Members</span></span>

<span data-ttu-id="1c0a2-109">Die **Win32- \_ BIOS** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1c0a2-109">The **Win32\_BIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="1c0a2-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1c0a2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1c0a2-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1c0a2-111">Properties</span></span>

<span data-ttu-id="1c0a2-112">Die **Win32- \_ BIOS** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-112">The **Win32\_BIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c0a2-113">**BiosCharacteristics**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-113">**BiosCharacteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-114">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="1c0a2-114">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-116">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 0 \| BIOS-Merkmale")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|BIOS Characteristics")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-117">Array von BIOS-Merkmalen, das vom System gemäß der Systemverwaltungs-BIOS-Referenz Spezifikation unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-117">Array of BIOS characteristics supported by the system as defined by the System Management BIOS Reference Specification.</span></span>

<span data-ttu-id="1c0a2-118">Dieser Wert stammt aus dem **BIOS-Eigenschaften** Element der **BIOS-Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-118">This value comes from the **BIOS Characteristics** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1c0a2-119">Mögliche Werte sind.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-119">The possible values are.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="1c0a2-120"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserviert** (0)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-120"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="1c0a2-121"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserviert** (1)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-121"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c0a2-122"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-122"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="BIOS_Characteristics_Not_Supported"></span><span id="bios_characteristics_not_supported"></span><span id="BIOS_CHARACTERISTICS_NOT_SUPPORTED"></span>

<span data-ttu-id="1c0a2-123"><span id="BIOS_Characteristics_Not_Supported"></span><span id="bios_characteristics_not_supported"></span><span id="BIOS_CHARACTERISTICS_NOT_SUPPORTED"></span>**BIOS-Eigenschaften werden nicht unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-123"><span id="BIOS_Characteristics_Not_Supported"></span><span id="bios_characteristics_not_supported"></span><span id="BIOS_CHARACTERISTICS_NOT_SUPPORTED"></span>**BIOS Characteristics Not Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_is_supported"></span><span id="isa_is_supported"></span><span id="ISA_IS_SUPPORTED"></span>

<span data-ttu-id="1c0a2-124"><span id="ISA_is_supported"></span><span id="isa_is_supported"></span><span id="ISA_IS_SUPPORTED"></span>**ISA wird unterstützt** (4)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-124"><span id="ISA_is_supported"></span><span id="isa_is_supported"></span><span id="ISA_IS_SUPPORTED"></span>**ISA is supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA_is_supported"></span><span id="mca_is_supported"></span><span id="MCA_IS_SUPPORTED"></span>

<span data-ttu-id="1c0a2-125"><span id="MCA_is_supported"></span><span id="mca_is_supported"></span><span id="MCA_IS_SUPPORTED"></span>**MCA wird unterstützt** (5)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-125"><span id="MCA_is_supported"></span><span id="mca_is_supported"></span><span id="MCA_IS_SUPPORTED"></span>**MCA is supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA_is_supported"></span><span id="eisa_is_supported"></span><span id="EISA_IS_SUPPORTED"></span>

<span data-ttu-id="1c0a2-126"><span id="EISA_is_supported"></span><span id="eisa_is_supported"></span><span id="EISA_IS_SUPPORTED"></span>**EISA wird unterstützt** (6)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-126"><span id="EISA_is_supported"></span><span id="eisa_is_supported"></span><span id="EISA_IS_SUPPORTED"></span>**EISA is supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_is_supported"></span><span id="pci_is_supported"></span><span id="PCI_IS_SUPPORTED"></span>

<span data-ttu-id="1c0a2-127"><span id="PCI_is_supported"></span><span id="pci_is_supported"></span><span id="PCI_IS_SUPPORTED"></span>**PCI wird unterstützt** (7)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-127"><span id="PCI_is_supported"></span><span id="pci_is_supported"></span><span id="PCI_IS_SUPPORTED"></span>**PCI is supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PC_Card__PCMCIA__is_supported"></span><span id="pc_card__pcmcia__is_supported"></span><span id="PC_CARD__PCMCIA__IS_SUPPORTED"></span>

<span data-ttu-id="1c0a2-128"><span id="PC_Card__PCMCIA__is_supported"></span><span id="pc_card__pcmcia__is_supported"></span><span id="PC_CARD__PCMCIA__IS_SUPPORTED"></span>**PC-Karte (PCMCIA) wird unterstützt** (8)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-128"><span id="PC_Card__PCMCIA__is_supported"></span><span id="pc_card__pcmcia__is_supported"></span><span id="PC_CARD__PCMCIA__IS_SUPPORTED"></span>**PC Card (PCMCIA) is supported** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Plug_and_Play_is_supported"></span><span id="plug_and_play_is_supported"></span><span id="PLUG_AND_PLAY_IS_SUPPORTED"></span>

<span data-ttu-id="1c0a2-129"><span id="Plug_and_Play_is_supported"></span><span id="plug_and_play_is_supported"></span><span id="PLUG_AND_PLAY_IS_SUPPORTED"></span>**Plug & Play wird unterstützt** (9)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-129"><span id="Plug_and_Play_is_supported"></span><span id="plug_and_play_is_supported"></span><span id="PLUG_AND_PLAY_IS_SUPPORTED"></span>**Plug and Play is supported** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="APM_is_supported"></span><span id="apm_is_supported"></span><span id="APM_IS_SUPPORTED"></span>

<span data-ttu-id="1c0a2-130"><span id="APM_is_supported"></span><span id="apm_is_supported"></span><span id="APM_IS_SUPPORTED"></span>**APM wird unterstützt** (10)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-130"><span id="APM_is_supported"></span><span id="apm_is_supported"></span><span id="APM_IS_SUPPORTED"></span>**APM is supported** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="BIOS_is_Upgradeable__Flash_"></span><span id="bios_is_upgradeable__flash_"></span><span id="BIOS_IS_UPGRADEABLE__FLASH_"></span>

<span data-ttu-id="1c0a2-131"><span id="BIOS_is_Upgradeable__Flash_"></span><span id="bios_is_upgradeable__flash_"></span><span id="BIOS_IS_UPGRADEABLE__FLASH_"></span>**BIOS ist aktualisierbar (Flash)** (11)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-131"><span id="BIOS_is_Upgradeable__Flash_"></span><span id="bios_is_upgradeable__flash_"></span><span id="BIOS_IS_UPGRADEABLE__FLASH_"></span>**BIOS is Upgradeable (Flash)** (11)</span></span>


</dt> <dd>

<span data-ttu-id="1c0a2-132">BIOS ist aktualisierbar (Flash)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-132">BIOS is Upgradable (Flash)</span></span>

</dd> <dt>

<span id="BIOS_shadowing_is_allowed"></span><span id="bios_shadowing_is_allowed"></span><span id="BIOS_SHADOWING_IS_ALLOWED"></span>

<span data-ttu-id="1c0a2-133"><span id="BIOS_shadowing_is_allowed"></span><span id="bios_shadowing_is_allowed"></span><span id="BIOS_SHADOWING_IS_ALLOWED"></span>**BIOS-shadowingist zulässig** (12)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-133"><span id="BIOS_shadowing_is_allowed"></span><span id="bios_shadowing_is_allowed"></span><span id="BIOS_SHADOWING_IS_ALLOWED"></span>**BIOS shadowing is allowed** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="VL-VESA_is_supported"></span><span id="vl-vesa_is_supported"></span><span id="VL-VESA_IS_SUPPORTED"></span>

<span data-ttu-id="1c0a2-134"><span id="VL-VESA_is_supported"></span><span id="vl-vesa_is_supported"></span><span id="VL-VESA_IS_SUPPORTED"></span>**VL-VESA wird unterstützt** (13)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-134"><span id="VL-VESA_is_supported"></span><span id="vl-vesa_is_supported"></span><span id="VL-VESA_IS_SUPPORTED"></span>**VL-VESA is supported** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCD_support_is_available"></span><span id="escd_support_is_available"></span><span id="ESCD_SUPPORT_IS_AVAILABLE"></span>

<span data-ttu-id="1c0a2-135"><span id="ESCD_support_is_available"></span><span id="escd_support_is_available"></span><span id="ESCD_SUPPORT_IS_AVAILABLE"></span>**ESCD-Unterstützung ist verfügbar** (14)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-135"><span id="ESCD_support_is_available"></span><span id="escd_support_is_available"></span><span id="ESCD_SUPPORT_IS_AVAILABLE"></span>**ESCD support is available** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_from_CD_is_supported"></span><span id="boot_from_cd_is_supported"></span><span id="BOOT_FROM_CD_IS_SUPPORTED"></span>

<span data-ttu-id="1c0a2-136"><span id="Boot_from_CD_is_supported"></span><span id="boot_from_cd_is_supported"></span><span id="BOOT_FROM_CD_IS_SUPPORTED"></span>**Starten von CD wird unterstützt** (15)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-136"><span id="Boot_from_CD_is_supported"></span><span id="boot_from_cd_is_supported"></span><span id="BOOT_FROM_CD_IS_SUPPORTED"></span>**Boot from CD is supported** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Selectable_Boot_is_supported"></span><span id="selectable_boot_is_supported"></span><span id="SELECTABLE_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="1c0a2-137"><span id="Selectable_Boot_is_supported"></span><span id="selectable_boot_is_supported"></span><span id="SELECTABLE_BOOT_IS_SUPPORTED"></span>**Auswählbarer Start wird unterstützt** (16)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-137"><span id="Selectable_Boot_is_supported"></span><span id="selectable_boot_is_supported"></span><span id="SELECTABLE_BOOT_IS_SUPPORTED"></span>**Selectable Boot is supported** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="BIOS_ROM_is_socketed"></span><span id="bios_rom_is_socketed"></span><span id="BIOS_ROM_IS_SOCKETED"></span>

<span data-ttu-id="1c0a2-138"><span id="BIOS_ROM_is_socketed"></span><span id="bios_rom_is_socketed"></span><span id="BIOS_ROM_IS_SOCKETED"></span>**BIOS-ROM wird** in ein-/Auss-(17)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-138"><span id="BIOS_ROM_is_socketed"></span><span id="bios_rom_is_socketed"></span><span id="BIOS_ROM_IS_SOCKETED"></span>**BIOS ROM is socketed** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_From_PC_Card__PCMCIA__is_supported"></span><span id="boot_from_pc_card__pcmcia__is_supported"></span><span id="BOOT_FROM_PC_CARD__PCMCIA__IS_SUPPORTED"></span>

<span data-ttu-id="1c0a2-139"><span id="Boot_From_PC_Card__PCMCIA__is_supported"></span><span id="boot_from_pc_card__pcmcia__is_supported"></span><span id="BOOT_FROM_PC_CARD__PCMCIA__IS_SUPPORTED"></span>**Der Start von der PC-Karte (PCMCIA) wird unterstützt** (18).</span><span class="sxs-lookup"><span data-stu-id="1c0a2-139"><span id="Boot_From_PC_Card__PCMCIA__is_supported"></span><span id="boot_from_pc_card__pcmcia__is_supported"></span><span id="BOOT_FROM_PC_CARD__PCMCIA__IS_SUPPORTED"></span>**Boot From PC Card (PCMCIA) is supported** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="EDD__Enhanced_Disk_Drive__Specification_is_supported"></span><span id="edd__enhanced_disk_drive__specification_is_supported"></span><span id="EDD__ENHANCED_DISK_DRIVE__SPECIFICATION_IS_SUPPORTED"></span>

<span data-ttu-id="1c0a2-140"><span id="EDD__Enhanced_Disk_Drive__Specification_is_supported"></span><span id="edd__enhanced_disk_drive__specification_is_supported"></span><span id="EDD__ENHANCED_DISK_DRIVE__SPECIFICATION_IS_SUPPORTED"></span>**EDD (Enhanced Disk Drive)-Spezifikation wird unterstützt** (19)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-140"><span id="EDD__Enhanced_Disk_Drive__Specification_is_supported"></span><span id="edd__enhanced_disk_drive__specification_is_supported"></span><span id="EDD__ENHANCED_DISK_DRIVE__SPECIFICATION_IS_SUPPORTED"></span>**EDD (Enhanced Disk Drive) Specification is supported** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_13h_-_Japanese_Floppy_for_NEC_9800_1.2mb__3.5____1k_Bytes_Sector__360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_nec_9800_1.2mb__3.5____1k_bytes_sector__360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_NEC_9800_1.2MB__3.5____1K_BYTES_SECTOR__360_RPM__IS_SUPPORTED"></span>

<span data-ttu-id="1c0a2-141"><span id="Int_13h_-_Japanese_Floppy_for_NEC_9800_1.2mb__3.5____1k_Bytes_Sector__360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_nec_9800_1.2mb__3.5____1k_bytes_sector__360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_NEC_9800_1.2MB__3.5____1K_BYTES_SECTOR__360_RPM__IS_SUPPORTED"></span>**Int 13h-japanische Diskette für NEC 9800 1.2 MB (3,5 \\ ", 1.000 Bytes/Sektor, 360 rpm) wird unterstützt** (20)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-141"><span id="Int_13h_-_Japanese_Floppy_for_NEC_9800_1.2mb__3.5____1k_Bytes_Sector__360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_nec_9800_1.2mb__3.5____1k_bytes_sector__360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_NEC_9800_1.2MB__3.5____1K_BYTES_SECTOR__360_RPM__IS_SUPPORTED"></span>**Int 13h - Japanese Floppy for NEC 9800 1.2mb (3.5\\", 1k Bytes/Sector, 360 RPM) is supported** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1c0a2-142">Int 13h-japanische Diskette für NEC 9800 1.2 MB (3,5, 1.000 Bytes/Sektor, 360 rpm) wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-142">Int 13h - Japanese Floppy for NEC 9800 1.2mb (3.5, 1k Bytes/Sector, 360 RPM) is supported</span></span>

</dd> <dt>

<span id="Int_13h_-_Japanese_Floppy_for_Toshiba_1.2mb__3.5____360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_toshiba_1.2mb__3.5____360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_TOSHIBA_1.2MB__3.5____360_RPM__IS_SUPPORTED"></span>

<span data-ttu-id="1c0a2-143"><span id="Int_13h_-_Japanese_Floppy_for_Toshiba_1.2mb__3.5____360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_toshiba_1.2mb__3.5____360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_TOSHIBA_1.2MB__3.5____360_RPM__IS_SUPPORTED"></span>**Int 13h-japanische Diskette für Toshiba 1.2 MB (3,5 \\ ", 360 rpm) wird unterstützt** (21)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-143"><span id="Int_13h_-_Japanese_Floppy_for_Toshiba_1.2mb__3.5____360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_toshiba_1.2mb__3.5____360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_TOSHIBA_1.2MB__3.5____360_RPM__IS_SUPPORTED"></span>**Int 13h - Japanese Floppy for Toshiba 1.2mb (3.5\\", 360 RPM) is supported** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1c0a2-144">Int 13h-japanische Diskette für Toshiba 1,2 MB (3,5, 360 rpm) wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-144">Int 13h - Japanese Floppy for Toshiba 1.2mb (3.5, 360 RPM) is supported</span></span>

</dd> <dt>

<span id="Int_13h_-_5.25_____360_KB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25_____360_kb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25_____360_KB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="1c0a2-145"><span id="Int_13h_-_5.25_____360_KB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25_____360_kb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25_____360_KB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h-5,25 \\ "/360 KB Disketten Dienste werden unterstützt** (22)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-145"><span id="Int_13h_-_5.25_____360_KB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25_____360_kb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25_____360_KB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h - 5.25\\" / 360 KB Floppy Services are supported** (22)</span></span>


</dt> <dd>

<span data-ttu-id="1c0a2-146">Int 13h-5,25/360 KB-Disketten Dienste werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-146">Int 13h - 5.25 / 360 KB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_13h_-_5.25____1.2MB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25____1.2mb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25____1.2MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="1c0a2-147"><span id="Int_13h_-_5.25____1.2MB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25____1.2mb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25____1.2MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h-5,25 \\ "/1.2MB Disketten Dienste werden unterstützt** (23)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-147"><span id="Int_13h_-_5.25____1.2MB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25____1.2mb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25____1.2MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h - 5.25\\" /1.2MB Floppy Services are supported** (23)</span></span>


</dt> <dd>

<span data-ttu-id="1c0a2-148">Int 13h-5,25/1.2MB Disketten Dienste werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-148">Int 13h - 5.25 /1.2MB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_13h_-_3.5_____720_KB_Floppy_Services_are__supported"></span><span id="int_13h_-_3.5_____720_kb_floppy_services_are__supported"></span><span id="INT_13H_-_3.5_____720_KB_FLOPPY_SERVICES_ARE__SUPPORTED"></span>

<span data-ttu-id="1c0a2-149"><span id="Int_13h_-_3.5_____720_KB_Floppy_Services_are__supported"></span><span id="int_13h_-_3.5_____720_kb_floppy_services_are__supported"></span><span id="INT_13H_-_3.5_____720_KB_FLOPPY_SERVICES_ARE__SUPPORTED"></span>**Int 13h-3,5 \\ "/720 KB Disketten Dienste werden unterstützt** (24)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-149"><span id="Int_13h_-_3.5_____720_KB_Floppy_Services_are__supported"></span><span id="int_13h_-_3.5_____720_kb_floppy_services_are__supported"></span><span id="INT_13H_-_3.5_____720_KB_FLOPPY_SERVICES_ARE__SUPPORTED"></span>**Int 13h - 3.5\\" / 720 KB Floppy Services are supported** (24)</span></span>


</dt> <dd>

<span data-ttu-id="1c0a2-150">Int 13h-3,5/720 KB-Disketten Dienste werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-150">Int 13h - 3.5 / 720 KB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_13h_-_3.5_____2.88_MB_Floppy_Services_are_supported"></span><span id="int_13h_-_3.5_____2.88_mb_floppy_services_are_supported"></span><span id="INT_13H_-_3.5_____2.88_MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="1c0a2-151"><span id="Int_13h_-_3.5_____2.88_MB_Floppy_Services_are_supported"></span><span id="int_13h_-_3.5_____2.88_mb_floppy_services_are_supported"></span><span id="INT_13H_-_3.5_____2.88_MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h-3,5 \\ "/2,88 MB Disketten Dienste werden unterstützt** (25)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-151"><span id="Int_13h_-_3.5_____2.88_MB_Floppy_Services_are_supported"></span><span id="int_13h_-_3.5_____2.88_mb_floppy_services_are_supported"></span><span id="INT_13H_-_3.5_____2.88_MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h - 3.5\\" / 2.88 MB Floppy Services are supported** (25)</span></span>


</dt> <dd>

<span data-ttu-id="1c0a2-152">Int 13h-3,5/2,88 MB Disketten Dienste werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-152">Int 13h - 3.5 / 2.88 MB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_5h__Print_Screen_Service_is_supported"></span><span id="int_5h__print_screen_service_is_supported"></span><span id="INT_5H__PRINT_SCREEN_SERVICE_IS_SUPPORTED"></span>

<span data-ttu-id="1c0a2-153"><span id="Int_5h__Print_Screen_Service_is_supported"></span><span id="int_5h__print_screen_service_is_supported"></span><span id="INT_5H__PRINT_SCREEN_SERVICE_IS_SUPPORTED"></span>**Int 5h, druckbildschirm Dienst wird unterstützt** (26)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-153"><span id="Int_5h__Print_Screen_Service_is_supported"></span><span id="int_5h__print_screen_service_is_supported"></span><span id="INT_5H__PRINT_SCREEN_SERVICE_IS_SUPPORTED"></span>**Int 5h, Print Screen Service is supported** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_9h__8042_Keyboard_services_are_supported"></span><span id="int_9h__8042_keyboard_services_are_supported"></span><span id="INT_9H__8042_KEYBOARD_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="1c0a2-154"><span id="Int_9h__8042_Keyboard_services_are_supported"></span><span id="int_9h__8042_keyboard_services_are_supported"></span><span id="INT_9H__8042_KEYBOARD_SERVICES_ARE_SUPPORTED"></span>**Int 9H, 8042 Tastatur Dienste werden unterstützt** (27)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-154"><span id="Int_9h__8042_Keyboard_services_are_supported"></span><span id="int_9h__8042_keyboard_services_are_supported"></span><span id="INT_9H__8042_KEYBOARD_SERVICES_ARE_SUPPORTED"></span>**Int 9h, 8042 Keyboard services are supported** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_14h__Serial_Services_are_supported"></span><span id="int_14h__serial_services_are_supported"></span><span id="INT_14H__SERIAL_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="1c0a2-155"><span id="Int_14h__Serial_Services_are_supported"></span><span id="int_14h__serial_services_are_supported"></span><span id="INT_14H__SERIAL_SERVICES_ARE_SUPPORTED"></span>**Int 14h, serielle Dienste werden unterstützt** (28)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-155"><span id="Int_14h__Serial_Services_are_supported"></span><span id="int_14h__serial_services_are_supported"></span><span id="INT_14H__SERIAL_SERVICES_ARE_SUPPORTED"></span>**Int 14h, Serial Services are supported** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_17h__printer_services_are_supported"></span><span id="int_17h__printer_services_are_supported"></span><span id="INT_17H__PRINTER_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="1c0a2-156"><span id="Int_17h__printer_services_are_supported"></span><span id="int_17h__printer_services_are_supported"></span><span id="INT_17H__PRINTER_SERVICES_ARE_SUPPORTED"></span>**Int 17h, Druckerdienste werden unterstützt** (29)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-156"><span id="Int_17h__printer_services_are_supported"></span><span id="int_17h__printer_services_are_supported"></span><span id="INT_17H__PRINTER_SERVICES_ARE_SUPPORTED"></span>**Int 17h, printer services are supported** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_10h__CGA_Mono_Video_Services_are_supported"></span><span id="int_10h__cga_mono_video_services_are_supported"></span><span id="INT_10H__CGA_MONO_VIDEO_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="1c0a2-157"><span id="Int_10h__CGA_Mono_Video_Services_are_supported"></span><span id="int_10h__cga_mono_video_services_are_supported"></span><span id="INT_10H__CGA_MONO_VIDEO_SERVICES_ARE_SUPPORTED"></span>**Int 10h, CGA/Mono-Video Dienste werden unterstützt** (30)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-157"><span id="Int_10h__CGA_Mono_Video_Services_are_supported"></span><span id="int_10h__cga_mono_video_services_are_supported"></span><span id="INT_10H__CGA_MONO_VIDEO_SERVICES_ARE_SUPPORTED"></span>**Int 10h, CGA/Mono Video Services are supported** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC_PC-98"></span><span id="nec_pc-98"></span>

<span data-ttu-id="1c0a2-158"><span id="NEC_PC-98"></span><span id="nec_pc-98"></span>**NEC-PC-98** (31)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-158"><span id="NEC_PC-98"></span><span id="nec_pc-98"></span>**NEC PC-98** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ACPI_supported"></span><span id="acpi_supported"></span><span id="ACPI_SUPPORTED"></span>

<span data-ttu-id="1c0a2-159"><span id="ACPI_supported"></span><span id="acpi_supported"></span><span id="ACPI_SUPPORTED"></span>**ACPI unterstützt** (32)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-159"><span id="ACPI_supported"></span><span id="acpi_supported"></span><span id="ACPI_SUPPORTED"></span>**ACPI supported** (32)</span></span>


</dt> <dd>

<span data-ttu-id="1c0a2-160">ACPI wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-160">ACPI is supported</span></span>

</dd> <dt>

<span id="USB_Legacy_is_supported"></span><span id="usb_legacy_is_supported"></span><span id="USB_LEGACY_IS_SUPPORTED"></span>

<span data-ttu-id="1c0a2-161"><span id="USB_Legacy_is_supported"></span><span id="usb_legacy_is_supported"></span><span id="USB_LEGACY_IS_SUPPORTED"></span>**USB-Legacy wird unterstützt** (33)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-161"><span id="USB_Legacy_is_supported"></span><span id="usb_legacy_is_supported"></span><span id="USB_LEGACY_IS_SUPPORTED"></span>**USB Legacy is supported** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP_is_supported"></span><span id="agp_is_supported"></span><span id="AGP_IS_SUPPORTED"></span>

<span data-ttu-id="1c0a2-162"><span id="AGP_is_supported"></span><span id="agp_is_supported"></span><span id="AGP_IS_SUPPORTED"></span>**AGP wird unterstützt** (34)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-162"><span id="AGP_is_supported"></span><span id="agp_is_supported"></span><span id="AGP_IS_SUPPORTED"></span>**AGP is supported** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="I2O_boot_is_supported"></span><span id="i2o_boot_is_supported"></span><span id="I2O_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="1c0a2-163"><span id="I2O_boot_is_supported"></span><span id="i2o_boot_is_supported"></span><span id="I2O_BOOT_IS_SUPPORTED"></span>**I2O Boot wird unterstützt** (35)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-163"><span id="I2O_boot_is_supported"></span><span id="i2o_boot_is_supported"></span><span id="I2O_BOOT_IS_SUPPORTED"></span>**I2O boot is supported** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="LS-120_boot_is_supported"></span><span id="ls-120_boot_is_supported"></span><span id="LS-120_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="1c0a2-164"><span id="LS-120_boot_is_supported"></span><span id="ls-120_boot_is_supported"></span><span id="LS-120_BOOT_IS_SUPPORTED"></span>**LS-120-Start wird unterstützt** (36)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-164"><span id="LS-120_boot_is_supported"></span><span id="ls-120_boot_is_supported"></span><span id="LS-120_BOOT_IS_SUPPORTED"></span>**LS-120 boot is supported** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="ATAPI_ZIP_Drive_boot_is_supported"></span><span id="atapi_zip_drive_boot_is_supported"></span><span id="ATAPI_ZIP_DRIVE_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="1c0a2-165"><span id="ATAPI_ZIP_Drive_boot_is_supported"></span><span id="atapi_zip_drive_boot_is_supported"></span><span id="ATAPI_ZIP_DRIVE_BOOT_IS_SUPPORTED"></span>Der **ATAPI-ZIP-Laufwerk Start wird unterstützt** (37).</span><span class="sxs-lookup"><span data-stu-id="1c0a2-165"><span id="ATAPI_ZIP_Drive_boot_is_supported"></span><span id="atapi_zip_drive_boot_is_supported"></span><span id="ATAPI_ZIP_DRIVE_BOOT_IS_SUPPORTED"></span>**ATAPI ZIP Drive boot is supported** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="1394_boot_is_supported"></span><span id="1394_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="1c0a2-166"><span id="1394_boot_is_supported"></span><span id="1394_BOOT_IS_SUPPORTED"></span>**1394 Start wird unterstützt** (38)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-166"><span id="1394_boot_is_supported"></span><span id="1394_BOOT_IS_SUPPORTED"></span>**1394 boot is supported** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Smart_Battery_supported"></span><span id="smart_battery_supported"></span><span id="SMART_BATTERY_SUPPORTED"></span>

<span data-ttu-id="1c0a2-167"><span id="Smart_Battery_supported"></span><span id="smart_battery_supported"></span><span id="SMART_BATTERY_SUPPORTED"></span>**Smart Akku unterstützt** (39)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-167"><span id="Smart_Battery_supported"></span><span id="smart_battery_supported"></span><span id="SMART_BATTERY_SUPPORTED"></span>**Smart Battery supported** (39)</span></span>


</dt> <dd>

<span data-ttu-id="1c0a2-168">Smart Akku wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-168">Smart Battery is supported</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-169">40 47</span><span class="sxs-lookup"><span data-stu-id="1c0a2-169">40 47</span></span>
</dt> <dd>

<span data-ttu-id="1c0a2-170">Für BIOS-Hersteller reserviert</span><span class="sxs-lookup"><span data-stu-id="1c0a2-170">Reserved for BIOS vendor</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-171">48 63</span><span class="sxs-lookup"><span data-stu-id="1c0a2-171">48 63</span></span>
</dt> <dd>

<span data-ttu-id="1c0a2-172">Für Systemhersteller reserviert</span><span class="sxs-lookup"><span data-stu-id="1c0a2-172">Reserved for system vendor</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1c0a2-173">**Biosversion**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-173">**BIOSVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-174">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="1c0a2-174">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-176">Array der gesamten System-BIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-176">Array of the complete system BIOS information.</span></span> <span data-ttu-id="1c0a2-177">In vielen Computern können mehrere Versions Zeichenfolgen vorhanden sein, die in der Registrierung gespeichert sind und die System-BIOS-Informationen darstellen.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-177">In many computers there can be several version strings that are stored in the registry and represent the system BIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-178">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-178">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-181">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Informationen zur DMTF- \| Software Komponente \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-181">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-182">Interner Bezeichner für diese Kompilierung dieses Software Elements.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-182">Internal identifier for this compilation of this software element.</span></span>

<span data-ttu-id="1c0a2-183">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-183">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-184">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-187">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-187">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-188">Kurze Beschreibung des Objekts eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-188">Short description of the object a one-line string.</span></span>

<span data-ttu-id="1c0a2-189">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-190">**Codesatz**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-190">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-191">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-193">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-193">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-194">Der von diesem Softwareelement verwendete Codesatz.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-194">Code set used by this software element.</span></span>

<span data-ttu-id="1c0a2-195">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-195">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-196">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-196">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-197">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-199">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 13 \| aktuelle Sprache")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 13\|Current Language")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-200">Der Name der aktuellen BIOS-Sprache.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-200">Name of the current BIOS language.</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-201">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-201">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-202">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-204">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-204">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-205">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-205">Description of the object.</span></span>

<span data-ttu-id="1c0a2-206">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-206">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-207">**Embeddedcontrollermajorversion**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-207">**EmbeddedControllerMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-208">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-208">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-210">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 0 \| Embedded Controller Firmware Major Release")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-210">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|Embedded Controller Firmware Major Release")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-211">Die Hauptversion der eingebetteten Controller Firmware.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-211">The major release of the embedded controller firmware.</span></span>

<span data-ttu-id="1c0a2-212">Dieser Wert stammt aus dem **eingebetteten Controller** -firmwaremember der **BIOS-Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-212">This value comes from the **Embedded Controller Firmware Major Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1c0a2-213">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 10 und Windows Server 2016 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-213">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-214">**Embeddedcontrollerminorversion**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-214">**EmbeddedControllerMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-215">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-215">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-216">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-217">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 0 \| Embedded Controller-Firmware neben Version")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-217">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|Embedded Controller Firmware Minor Release")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-218">Die neben Version der eingebetteten Controller Firmware.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-218">The minor release of the embedded controller firmware.</span></span>

<span data-ttu-id="1c0a2-219">Dieser Wert stammt aus dem **Embedded Controller** -Element für die Firmware-neben Version der **BIOS-Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-219">This value comes from the **Embedded Controller Firmware Minor Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1c0a2-220">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 10 und Windows Server 2016 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-220">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-221">**Identificationcode**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-221">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-222">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-223">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-224">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Informationen zur DMTF- \| Software Komponente \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-224">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-225">Der Bezeichner des Herstellers für dieses Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-225">Manufacturer's identifier for this software element.</span></span> <span data-ttu-id="1c0a2-226">Häufig handelt es sich hierbei um eine Stock Keeping Unit (SKU) oder eine Teilenummer.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-226">Often this will be a stock keeping unit (SKU) or a part number.</span></span>

<span data-ttu-id="1c0a2-227">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-227">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-228">**Installablelanguages**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-228">**InstallableLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-229">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-230">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-231">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 13 \| installierbare Sprachen")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-231">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 13\|Installable Languages")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-232">Anzahl der Sprachen, die für die Installation auf diesem System verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-232">Number of languages available for installation on this system.</span></span> <span data-ttu-id="1c0a2-233">Die Sprache bestimmt möglicherweise Eigenschaften, z. b. die Notwendigkeit von Unicode und bidirektionalem Text.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-233">Language may determine properties such as the need for Unicode and bidirectional text.</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-234">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-234">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-235">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-235">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-236">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-237">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-237">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-238">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-238">Date and time the object was installed.</span></span> <span data-ttu-id="1c0a2-239">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-239">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="1c0a2-240">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-240">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-241">**Languageedition**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-241">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-242">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-243">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-244">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Informationen zur DMTF- \| Software Komponente \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-244">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-245">Language Edition dieses Software Elements.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-245">Language edition of this software element.</span></span> <span data-ttu-id="1c0a2-246">Die in ISO 639 definierten Sprachcodes sollten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-246">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="1c0a2-247">Wenn das Softwareelement eine mehrsprachige oder internationale Version eines Produkts darstellt, sollte die Zeichenfolge "mehrsprachig" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-247">Where the software element represents a multilingual or international version of a product, the string "multilingual" should be used.</span></span>

<span data-ttu-id="1c0a2-248">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-248">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-249">**ListOf-Sprachen**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-249">**ListOfLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-250">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="1c0a2-250">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-251">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-252">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 13 \| Language Strings")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-252">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 13\|Language Strings")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-253">Ein Array von Namen von verfügbaren BIOS-installierbaren Sprachen.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-253">Array of names of available BIOS-installable languages.</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-254">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-254">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-255">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-256">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-257">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System-BIOS \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-257">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-258">Hersteller dieses Software Elements.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-258">Manufacturer of this software element.</span></span>

<span data-ttu-id="1c0a2-259">Dieser Wert stammt vom **Vendor** -Member der **BIOS-Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-259">This value comes from the **Vendor** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1c0a2-260">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-260">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-261">**Name**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-261">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-262">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-264">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-264">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-265">Der Name, der zum Identifizieren dieses Software Elements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-265">Name used to identify this software element.</span></span>

<span data-ttu-id="1c0a2-266">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-266">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-267">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-267">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-268">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-269">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-270">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-270">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-271">Zeichnet den Hersteller und den Betriebs Systemtyp für ein Softwareelement auf, wenn die **TargetOperatingSystem** -Eigenschaft den Wert 1 (sonstige) aufweist.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-271">Records the manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 (Other).</span></span> <span data-ttu-id="1c0a2-272">Wenn **TargetOperatingSystem** den Wert 1 hat, müssen **OtherTargetOS** einen nicht-NULL-Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-272">When **TargetOperatingSystem** has a value of 1, **OtherTargetOS** must have a nonnull value.</span></span> <span data-ttu-id="1c0a2-273">Für alle anderen Werte von **TargetOperatingSystem** ist **OtherTargetOS** **null**.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-273">For all other values of **TargetOperatingSystem**, **OtherTargetOS** is **NULL**.</span></span>

<span data-ttu-id="1c0a2-274">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-274">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-275">**Primarybios**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-275">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-276">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1c0a2-276">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-277">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-278">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System-BIOS \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-278">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-279">**True** gibt an, dass dies das primäre BIOS des Computer Systems ist.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-279">If **TRUE**, this is the primary BIOS of the computer system.</span></span>

<span data-ttu-id="1c0a2-280">Diese Eigenschaft wird von [**CIM \_ bioselements**](cim-bioselement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-280">This property is inherited from [**CIM\_BIOSElement**](cim-bioselement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-281">**ReleaseDate**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-281">**ReleaseDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-282">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-282">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-283">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-284">Das Veröffentlichungsdatum des Windows-BIOS im UTC-Format (koordinierte Weltzeit) von YYYYMMDDHHMMSS. mmmmmm (+-) OOO.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-284">Release date of the Windows BIOS in the Coordinated Universal Time (UTC) format of YYYYMMDDHHMMSS.MMMMMM(+-)OOO.</span></span>

<span data-ttu-id="1c0a2-285">Dieser Wert stammt aus dem **BIOS-ReleaseDate** -Member der **BIOS-Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-285">This value comes from the **BIOS Release Date** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-286">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-286">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-287">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-288">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-289">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-289">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-290">Zugewiesene Seriennummer des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-290">Assigned serial number of the software element.</span></span>

<span data-ttu-id="1c0a2-291">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-291">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-292">**SMBIOSBIOSVersion**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-292">**SMBIOSBIOSVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-293">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-294">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-295">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 0 \| BIOS Version")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-295">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|BIOS Version")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-296">Von SMBIOS gemeldete BIOS-Version.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-296">BIOS version as reported by SMBIOS.</span></span>

<span data-ttu-id="1c0a2-297">Dieser Wert stammt aus dem **BIOS** -Versionsmember der **BIOS-Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-297">This value comes from the **BIOS Version** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-298">**SMBIOSMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-298">**SMBIOSMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-299">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-300">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-301">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| csmbios \| GetVersion")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-301">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|CSMBios\|GetVersion")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-302">Wichtige SMBIOS-Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-302">Major SMBIOS version number.</span></span> <span data-ttu-id="1c0a2-303">Diese Eigenschaft ist **null** , wenn SMBIOS nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-303">This property is **NULL** if SMBIOS is not found.</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-304">**SMBIOSMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-304">**SMBIOSMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-305">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-306">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-307">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| csmbios \| GetVersion")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-307">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|CSMBios\|GetVersion")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-308">Kleinere SMBIOS-Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-308">Minor SMBIOS version number.</span></span> <span data-ttu-id="1c0a2-309">Diese Eigenschaft ist **null** , wenn SMBIOS nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-309">This property is **NULL** if SMBIOS is not found.</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-310">**Smbiospree gesendet**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-310">**SMBIOSPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-311">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1c0a2-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-312">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-313">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| csmbios \| Init")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-313">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|CSMBios\|Init")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-314">**True** gibt an, dass das SMBIOS auf diesem Computersystem verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-314">If **true**, the SMBIOS is available on this computer system.</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-315">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-315">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-316">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-317">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-318">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-318">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-319">Bezeichner für dieses Softwareelement; soll in Verbindung mit anderen Schlüsseln verwendet werden, um eine eindeutige Darstellung dieser Instanz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-319">Identifier for this software element; designed to be used in conjunction with other keys to create a unique representation of this instance.</span></span>

<span data-ttu-id="1c0a2-320">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-320">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-321">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-321">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-322">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-322">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-324">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-324">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-325">Status eines Software Elements.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-325">State of a software element.</span></span>

<span data-ttu-id="1c0a2-326">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-326">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="1c0a2-327">Mögliche Werte sind.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-327">The possible values are.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="1c0a2-328">**Bereitstellbar** (0)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-328">**Deployable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="1c0a2-329">**Installier Bar** (1)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-329">**Installable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="1c0a2-330">**Ausführbare Datei** (2)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-330">**Executable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="1c0a2-331">Wird **ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-331">**Running** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1c0a2-332">**Status**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-332">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-333">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-334">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-335">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-335">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-336">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-336">Current status of the object.</span></span> <span data-ttu-id="1c0a2-337">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-337">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="1c0a2-338">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="1c0a2-338">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="1c0a2-339">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="1c0a2-339">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1c0a2-340">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-340">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1c0a2-341">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-341">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1c0a2-342">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1c0a2-343">Mögliche Werte sind.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-343">The possible values are.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1c0a2-344">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-344">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1c0a2-345">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-345">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1c0a2-346">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-346">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c0a2-347">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-347">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1c0a2-348">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-348">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1c0a2-349">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-349">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1c0a2-350">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-350">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1c0a2-351">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-351">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1c0a2-352">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-352">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1c0a2-353">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-353">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1c0a2-354">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-354">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1c0a2-355">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-355">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1c0a2-356">**Systembiosmajorversion**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-356">**SystemBiosMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-357">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-357">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-358">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-359">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 0 \| System-BIOS-Hauptversion")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-359">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|System BIOS Major Release")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-360">Die Hauptversion des System-BIOS.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-360">The major release of the System BIOS.</span></span>

<span data-ttu-id="1c0a2-361">Dieser Wert stammt aus dem **System-BIOS-hauptreleasemember** der **BIOS-Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-361">This value comes from the **System BIOS Major Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1c0a2-362">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 10 und Windows Server 2016 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-362">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-363">**Systembiosminorversion**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-363">**SystemBiosMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-364">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-364">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-365">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-366">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 0 \| System-BIOS-neben Version")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-366">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|System BIOS Minor Release")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-367">Die neben Version des System-BIOS.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-367">The minor release of the System BIOS.</span></span>

<span data-ttu-id="1c0a2-368">Dieser Wert stammt aus dem **System-BIOS-neben** Versions Mitglied der **BIOS-Informations** Struktur in den SMBIOS-Informationen.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-368">This value comes from the **System BIOS Minor Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1c0a2-369">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 10 und Windows Server 2016 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-369">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="1c0a2-370">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-370">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-371">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-371">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-372">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-373">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Software Komponenten Informationen \| 002,5 "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md)".**OSType**")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-373">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-374">Ziel Betriebssystem des besitzenden Software Elements.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-374">Target operating system of the owning software element.</span></span>

<span data-ttu-id="1c0a2-375">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-375">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="1c0a2-376">Mögliche Werte sind.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-376">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c0a2-377">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-377">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1c0a2-378">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-378">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="1c0a2-379">**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-379">**MACOS** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="1c0a2-380">**Attunix** (3)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-380">**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="1c0a2-381">**Dgux** (4)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-381">**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="1c0a2-382">**Decnt** (5)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-382">**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="1c0a2-383">**Digital UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-383">**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="1c0a2-384">**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-384">**OpenVMS** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="1c0a2-385">**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-385">**HPUX** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="1c0a2-386">**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-386">**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="1c0a2-387">**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-387">**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="1c0a2-388">**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-388">**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="1c0a2-389">**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-389">**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="1c0a2-390">**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-390">**JavaVM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="1c0a2-391">**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-391">**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="1c0a2-392">**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-392">**WIN3x** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="1c0a2-393">**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-393">**WIN95** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="1c0a2-394">**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-394">**WIN98** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="1c0a2-395">**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-395">**WINNT** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="1c0a2-396">**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-396">**WINCE** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="1c0a2-397">**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-397">**NCR3000** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="1c0a2-398">**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-398">**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="1c0a2-399">**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-399">**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="1c0a2-400">**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-400">**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="1c0a2-401">**Abhängige UNIX** -(24)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-401">**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="1c0a2-402">**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-402">**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="1c0a2-403">**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-403">**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="1c0a2-404">**Sequenent** (27)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-404">**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="1c0a2-405">**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-405">**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="1c0a2-406">**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-406">**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="1c0a2-407">**Sonnen Betriebssystem** (30)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-407">**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="1c0a2-408">**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-408">**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="1c0a2-409">**Aseries** (32)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-409">**ASERIES** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="1c0a2-410">**Tandemnsk** (33)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-410">**TandemNSK** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="1c0a2-411">**Tandemnt** (34)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-411">**TandemNT** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="1c0a2-412">**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-412">**BS2000** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="1c0a2-413">**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-413">**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="1c0a2-414">**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-414">**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="1c0a2-415">**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-415">**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="1c0a2-416">**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-416">**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="1c0a2-417">**Interaktives UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-417">**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="1c0a2-418">**Bsdunix** (41)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-418">**BSDUNIX** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="1c0a2-419">**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-419">**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="1c0a2-420">**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-420">**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="1c0a2-421">**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-421">**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="1c0a2-422">**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-422">**OS9** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="1c0a2-423">**Mach-Kernel** (46)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-423">**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="1c0a2-424">**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-424">**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="1c0a2-425">**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-425">**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="1c0a2-426">**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-426">**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="1c0a2-427">**Ixworks** (50)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-427">**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="1c0a2-428">**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-428">**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="1c0a2-429">**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-429">**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="1c0a2-430">**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-430">**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="1c0a2-431">**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-431">**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="1c0a2-432">**NeXTStep** (55)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-432">**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="1c0a2-433">**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-433">**PalmPilot** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="1c0a2-434">**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-434">**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="1c0a2-435">**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-435">**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="1c0a2-436">**Dediziert** (59)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-436">**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="1c0a2-437">**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-437">**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="1c0a2-438">**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-438">**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1c0a2-439">**Version**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-439">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0a2-440">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-441">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c0a2-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c0a2-442">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Version"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Hardware \\ \\ Description \\ \\ System \| systembiosversion")</span><span class="sxs-lookup"><span data-stu-id="1c0a2-442">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HARDWARE\\\\Description\\\\System\|SystemBiosVersion")</span></span>
</dt> </dl>

<span data-ttu-id="1c0a2-443">Die BIOS-Version.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-443">Version of the BIOS.</span></span> <span data-ttu-id="1c0a2-444">Diese Zeichenfolge wird vom BIOS-Hersteller erstellt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-444">This string is created by the BIOS manufacturer.</span></span>

<span data-ttu-id="1c0a2-445">Diese Eigenschaft wird von [**CIM \_ Softwareelement**](cim-softwareelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-445">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c0a2-446">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c0a2-446">Remarks</span></span>

<span data-ttu-id="1c0a2-447">Die **Win32- \_ BIOS** -Klasse wird von [**CIM \_ bioselements**](cim-bioselement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-447">The **Win32\_BIOS** class is derived from [**CIM\_BIOSElement**](cim-bioselement.md).</span></span>

<span data-ttu-id="1c0a2-448">Die Eigenschaften in der **Win32- \_ BIOS** -Klasse können sich für ein bestimmtes Computersystem mit demselben BIOS ändern, beispielsweise durch das Starten über einen Legacy-BIOS-Modus im Vergleich zum Starten über den UEFI-BIOS-Modus.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-448">The properties in the **Win32\_BIOS** class may change for a specific computer system with the same BIOS, for example booting through a legacy BIOS mode vs. booting through UEFI BIOS mode.</span></span> <span data-ttu-id="1c0a2-449">Die von den SMBIOS-Strukturen abgerufenen Eigenschaften sollten jedoch unverändert bleiben.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-449">However the properties retrieved from the SMBIOS structures should remain the same.</span></span>

## <a name="examples"></a><span data-ttu-id="1c0a2-450">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c0a2-450">Examples</span></span>

<span data-ttu-id="1c0a2-451">Das PowerShell-Beispiel " [Get-ComputerInfo-Query Computer Info from Local/Remote Computers-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) " in der TechNet Gallery verwendet eine Reihe von Aufrufen von Hardware und Software, einschließlich **Win32- \_ BIOS**, um Informationen über ein lokales oder Remote System anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-451">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_BIOS**, to display information about a local or remote system.</span></span>

<span data-ttu-id="1c0a2-452">Das Beispiel zum [Generieren von Systeminformationen as XML Hierarchy](https://Gallery.TechNet.Microsoft.Com/Generate-system-information-3f40629f) VBScript in der TechNet Gallery verwendet eine Reihe von Aufrufen von Hardware und Software, einschließlich **Win32- \_ BIOS**, um eine XML-Darstellung eines Systems mithilfe einer manuellen XML-Ausgabe zu generieren.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-452">The [Generate system information as XML hierarchy](https://Gallery.TechNet.Microsoft.Com/Generate-system-information-3f40629f) VBScript sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_BIOS**, to generate an XML representation of a system using a manual XML output.</span></span>

<span data-ttu-id="1c0a2-453">Im folgenden PowerShell-Codebeispiel wird das **Win32- \_ BIOS** verwendet, um Eigenschaften des BIOS zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="1c0a2-453">The following PowerShell code sample uses **Win32\_BIOS** to return characteristics of the BIOS</span></span>


```PowerShell
# wmi-win32_bios.ps1
# Demonstrates use of Win32_Bios WMI class
# Thomas Lee - tfl@psp.co.uk



# Helper function to return characterics of the BIOS
function get-WmiBiosCharacteristics {
param ([uint16] $char)

# parse and return values

If ($char -le 39) {

switch ($char) {
0   {"00-Reserved"}
1   {"01-Reserved"}
2   {"02-Unknown"}
3   {"03-BIOS Characteristics Not Supported"}
4   {"04-ISA is supported"}
5   {"05-MCA is supported"}
6   {"06-EISA is supported"}
7   {"07-PCI is supported"}
8   {"08-PC Card (PCMCIA) is supported"}
9   {"09-Plug and Play is supported"}
10  {"10-APM is supported"}
11  {"11-BIOS is Upgradable (Flash)"}
12  {"12-BIOS shadowing is allowed"}
13  {"13-VL-VESA is supported"}
14  {"14-ESCD support is available"}
15  {"15-Boot from CD is supported"}
16  {"16-Selectable Boot is supported"}
17  {"17-BIOS ROM is socketed"}
18  {"18-Boot From PC Card (PCMCIA) is supported"}
19  {"19-EDD (Enhanced Disk Drive) Specification is supported"}
20  {"20-Int 13h - Japanese Floppy for NEC 9800 1.2mb (3.5, 1k Bytes/Sector, 360 RPM) is supported"}
21  {"21-Int 13h - Japanese Floppy for Toshiba 1.2mb (3.5, 360 RPM) is supported"}
22  {"22-Int 13h - 5.25 / 360 KB Floppy Services are supported"}
23  {"23-Int 13h - 5.25 /1.2MB Floppy Services are supported"}
24  {"24-Int 13h - 3.5 / 720 KB Floppy Services are supported"}
25  {"25-Int 13h - 3.5 / 2.88 MB Floppy Services are supported"}
26  {"26-Int 5h, Print Screen Service is supported"}
27  {"27-Int 9h, 8042 Keyboard services are supported"}
28  {"28-Int 14h, Serial Services are supported"}
29  {"29-Int 17h, printer services are supported"}
30  {"30-Int 10h, CGA/Mono Video Services are supported"}
31  {"31-NEC PC-98"}
32  {"32-ACPI supported"}
33  {"33-USB Legacy is supported"}
34  {"34-AGP is supported"}
35  {"35-I2O boot is supported"}
36  {"36-LS-120 boot is supported"}
37  {"37-ATAPI ZIP Drive boot is supported"}
38  {"38-1394 boot is supported"}
39  {"39-Smart Battery supported"}
}
Return
}

If ($char -ge 40 -and $char -le 45) {
          "{0}-Reserved for BIOS vendor" -f $char
return
}

If ($char -ge 48 -and $char -le 63) {
           "{0}-Reserved for system vendor" -f $char
return
}
"{0}-Unknown Value " -f $char
}

# Get BIOS information from WMI
$bios = Get-WMIObject Win32_Bios

# Display BIOS Details
"Win32_Bios WMI Information"
"Bios Characteristics"
foreach ($ch in $bios.BiosCharacteristics) {
"                      :  {0}" -f  (Get-WmiBiosCharacteristics($ch))
} 
"Bios Version          :  {0}" -f $bios.BiosVersion
"Codeset               :  {0}" -f $bios.Codeset
"CurrentLanguage       :  {0}" -f $bios.CurrentLanguage
"Description           :  {0}" -f $bios.Description
"IdentificatonCode     :  {0}" -f $bios.IdentificatonCode
"InstallableLanguages  :  {0}" -f $bios.InstallableLanguages
"InstallDate           :  {0}" -f $bios.InstallDate 
"LanguageEdition       :  {0}" -f $bios.LanguageEdition
"ListOfLanguages       :  {0}" -f $bios.ListOfLanguages
"Manufacturer          :  {0}" -f $bios.Manufacturer
"OtherTargetOS         :  {0}" -f $bios.OtherTargetOS
"PrimaryBIOS           :  {0}" -f $bios.PrimaryBIOS
"ReleaseDate           :  {0}" -f $bios.ReleaseDate
"SerialNumber          :  {0}" -f $bios.SerialNumber
"SMBIOSBIOSVersion     :  {0}" -f $bios.SMBIOSBIOSVersion
"SMBIOSMajorVersion    :  {0}" -f $bios.SMBIOSMajorVersion
"SMBIOSMinorVersion    :  {0}" -f $bios.SMBIOSMinorVersion
"SoftwareElementID     :  {0}" -f $bios.SoftwareElementID 
"SoftwareElementState  :  {0}" -f $bios.SoftwareElementState
"TargetOperatingSystem :  {0}" -f $bios.TargetOperatingSystem
"Version               :  {0}" -f $bios.Version 
```



<span data-ttu-id="1c0a2-454">Im vorherigen Codebeispiel werden die folgenden Informationen zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="1c0a2-454">The previous code sample returns the following information:</span></span>

``` syntax
Win32_Bios WMI Information
Bios Characteristics
                      :  04-ISA is supported
                      :  07-PCI is supported
                      :  08-PC Card (PCMCIA) is supported
                      :  09-Plug and Play is supported
                      :  11-BIOS is Upgradable (Flash)
                      :  12-BIOS shadowing is allowed
                      :  15-Boot from CD is supported
                      :  16-Selectable Boot is supported
                      :  24-Int 13h - 3.5 / 720 KB Floppy Services are supported
                      :  26-Int 5h, Print Screen Service is supported
                      :  27-Int 9h, 8042 Keyboard services are supported
                      :  28-Int 14h, Serial Services are supported
                      :  29-Int 17h, printer services are supported
                      :  30-Int 10h, CGA/Mono Video Services are supported
                      :  32-ACPI supported
                      :  33-USB Legacy is supported
                      :  34-AGP is supported
                      :  39-Smart Battery supported
                      :  40-Reserved for BIOS vendor
                      :  41-Reserved for BIOS vendor
                      :  42-Reserved for BIOS vendor
                      :  58-Reserved for system vendor
                      :  74-Unknown Value
Bios Version          :  DELL   - 27d60a0d
Codeset               :
CurrentLanguage       :  en|US|iso8859-1
Description           :  Phoenix ROM BIOS PLUS Version 1.10 A04
IdentificatonCode     :
InstallableLanguages  :  1
InstallDate           :
LanguageEdition       :
ListOfLanguages       :  en|US|iso8859-1
Manufacturer          :  Dell Inc.
OtherTargetOS         :
PrimaryBIOS           :  True
ReleaseDate           :  20061013000000.000000+000
SerialNumber          :  DDC2H2J
SMBIOSBIOSVersion     :  A04
SMBIOSMajorVersion    :  2
SMBIOSMinorVersion    :  4
SoftwareElementID     :  Phoenix ROM BIOS PLUS Version 1.10 A04
SoftwareElementState  :  3
TargetOperatingSystem :  0
Version               :  DELL   - 27d60a0d
```

## <a name="requirements"></a><span data-ttu-id="1c0a2-455">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c0a2-455">Requirements</span></span>



| <span data-ttu-id="1c0a2-456">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c0a2-456">Requirement</span></span> | <span data-ttu-id="1c0a2-457">Wert</span><span class="sxs-lookup"><span data-stu-id="1c0a2-457">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c0a2-458">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-458">Minimum supported client</span></span><br/> | <span data-ttu-id="1c0a2-459">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c0a2-459">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1c0a2-460">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1c0a2-460">Minimum supported server</span></span><br/> | <span data-ttu-id="1c0a2-461">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c0a2-461">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1c0a2-462">Namespace</span><span class="sxs-lookup"><span data-stu-id="1c0a2-462">Namespace</span></span><br/>                | <span data-ttu-id="1c0a2-463">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1c0a2-463">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1c0a2-464">MOF</span><span class="sxs-lookup"><span data-stu-id="1c0a2-464">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c0a2-465"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a2-465"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c0a2-466">DLL</span><span class="sxs-lookup"><span data-stu-id="1c0a2-466">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c0a2-467"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c0a2-467"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c0a2-468">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c0a2-468">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c0a2-469">**CIM- \_ bioselare**</span><span class="sxs-lookup"><span data-stu-id="1c0a2-469">**CIM\_BIOSElement**</span></span>](cim-bioselement.md)
</dt> <dt>

[<span data-ttu-id="1c0a2-470">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="1c0a2-470">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

