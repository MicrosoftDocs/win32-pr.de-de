---
description: Die CIM \_ PhysicalConnector-Klasse stellt jedes physische Element dar, das zum Herstellen einer Verbindung mit anderen Elementen verwendet wird. Jedes Objekt, das Signale oder Strom zwischen zwei oder mehr physischen Elementen verbinden und übertragen kann, ist ein Nachfolger (oder Member) dieser Klasse.
ms.assetid: cc135ae8-5ae1-4028-a2e3-a81db8694d9d
ms.tgt_platform: multiple
title: CIM_PhysicalConnector-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalConnector
- CIM_PhysicalConnector.Caption
- CIM_PhysicalConnector.Description
- CIM_PhysicalConnector.InstallDate
- CIM_PhysicalConnector.Name
- CIM_PhysicalConnector.Status
- CIM_PhysicalConnector.CreationClassName
- CIM_PhysicalConnector.Manufacturer
- CIM_PhysicalConnector.Model
- CIM_PhysicalConnector.OtherIdentifyingInfo
- CIM_PhysicalConnector.PartNumber
- CIM_PhysicalConnector.PoweredOn
- CIM_PhysicalConnector.SerialNumber
- CIM_PhysicalConnector.SKU
- CIM_PhysicalConnector.Tag
- CIM_PhysicalConnector.Version
- CIM_PhysicalConnector.ConnectorPinout
- CIM_PhysicalConnector.ConnectorType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4c5e53c2c8d02abb0762a9c3cc5bc5540f175f0810ec319180eb06435948ed4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118678272"
---
# <a name="cim_physicalconnector-class"></a>CIM \_ PhysicalConnector-Klasse

Die **CIM \_ PhysicalConnector-Klasse** stellt jedes physische Element dar, das zum Herstellen einer Verbindung mit anderen Elementen verwendet wird. Jedes Objekt, das Signale oder Strom zwischen zwei oder mehr physischen Elementen verbinden und übertragen kann, ist ein Nachfolger (oder Member) dieser Klasse. Slots und D-Shell-Connectors sind beispielsweise Typen physischer Connectors.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird aus Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[abstract, UUID("{FAF76B84-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalConnector : CIM_PhysicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   Manufacturer;
  string   Model;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Tag;
  string   Version;
  string   ConnectorPinout;
  uint16   ConnectorType[];
};
```

## <a name="members"></a>Member

Die **CIM \_ PhysicalConnector-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ CIM PhysicalConnector-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Eine kurze Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**ConnectorPinout**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Freiformzeichenfolge, die die Pinkonfiguration und Signalverwendung eines physischen Connectors beschreibt.

</dd> <dt>

**Connectortype**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Typ des physischen Connectors. Ein Array wird angegeben, um die Beschreibung von Kombinationen von Connectorinformationen zu ermöglichen. Beispielsweise könnte ein Arrayeintrag RS-232, ein anderer DB-25 und ein dritter Eintrag den Connector als "male" definieren.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Andere** (1)


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

**Male** (2)


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

**Female** (3)


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

**Abgeschirmt** (4)


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

**Nicht abgeschirmt** (5)


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

**SCSI (A) High-Density (50 Pins)** (6)


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

**SCSI (A) Low-Density (50 Pins)** (7)


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

**SCSI (P) High-Density (68 Pins)** (8)


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

**SCSI SCA-I (80 Pins)** (9)


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

**SCSI SCA-II (80 Pins)** (10)


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

**SCSI-Fibre Channel (DB-9, Kupfer)** (11)


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

**SCSI-Fibre Channel (Fibre)** (12)


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

**SCSI Fibre Channel SCA-II (40 Pins)** (13)


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

**SCSI Fibre Channel SCA-II (20 Pins)** (14)


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

**SCSI Fibre Channel BNC** (15)


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

**ATA 3-1/2 Zoll (40 Pins)** (16)


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

**ATA 2-1/2 Zoll (44 Pins)** (17)


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

**ATA-2** (18)


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

**ATA-3** (19)


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

**ATA/66** (20)


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

**DB-9** (21)


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

**DB-15** (22)


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

**DB-25** (23)


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

**DB-36** (24)


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

**RS-232C** (25)


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

**RS-422** (26)


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

**RS-423** (27)


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

**RS-485** (28)


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

**RS-449** (29)


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

**V.35** (30)


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

**X.21** (31)


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

**IEEE-488** (32)


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

**AUI** (33)


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

**UTP-Kategorie 3** (34)


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

**UTP-Kategorie 4** (35)


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

**UTP-Kategorie 5** (36)


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

**BNC** (37)


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

**RJ11** (38)


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

**RJ45** (39)


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

**Fiber MIC** (40)


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

**Apple AUI** (41)


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

**Apple GeoPort** (42)


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

**PCI** (43)


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

**ISA** (44)


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

**EISA** (45)


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

**VESA** (46)


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

**PCMCIA** (47)


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

**PCMCIA-Typ I** (48)


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

**PCMCIA-Typ II** (49)


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

**PCMCIA-Typ III** (50)


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

**ZV-Port** (51)


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

**CardBus** (52)


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

**USB** (53)


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

**IEEE 1394** (54)


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

**SOLLI** (55)


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

**HSSDC (6 Pins)** (56)


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

**GBIC** (57)


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

**DIN** (58)


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

**Mini-DIN** (59)


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

**Micro-DIN** (60)


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

**PS/2** (61)


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

**Wird** (62)


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

**HP-HIL** (63)


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

**Access.bus** (64)


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

**NuBus** (65)


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

**Cenredos** (66)


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

**Mini-Schwerpunkten** (67)


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

**Mini-Centronics Type-14** (68)


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

**Mini-Centronics Type-20** (69)


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

**Mini-Centronics Type-26** (70)


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

**Busmaus** (71)


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

**ADB** (72)


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

**AGP** (73)


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

**VME-Bus** (74)


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

**VME64** (75)


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

**Proprietär** (76)


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

**Proprietärer Prozessorkartenslot** (77)


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

**Proprietärer Speicherkartenslot** (78)


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

**Proprietärer E/A-Riser-Slot** (79)


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

**PCI-66MHZ** (80)


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

**AGP2X** (81)


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

**AGP4X** (82)


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

**PC-98** (83)


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

**PC-98-Hireso** (84)


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

**PC-H98** (85)


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

**PC-98Note** (86)


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

**PC-98Full** (87)


</dt> <dd></dd> <dt>

<span id="SSA_SCSI"></span><span id="ssa_scsi"></span>

**SSA SCSI** (88)


</dt> <dd></dd> <dt>

<span id="Circular"></span><span id="circular"></span><span id="CIRCULAR"></span>

**Circular** (89)


</dt> <dd></dd> <dt>

<span id="On_Board_IDE_Connector"></span><span id="on_board_ide_connector"></span><span id="ON_BOARD_IDE_CONNECTOR"></span>

**On Board IDE Connector** (90)


</dt> <dd></dd> <dt>

<span id="On_Board_Floppy_Connector"></span><span id="on_board_floppy_connector"></span><span id="ON_BOARD_FLOPPY_CONNECTOR"></span>

**On Board Floppy Connector** (91)


</dt> <dd></dd> <dt>

<span id="9_Pin_Dual_Inline"></span><span id="9_pin_dual_inline"></span><span id="9_PIN_DUAL_INLINE"></span>

**9 Pin Dual Inline** (92)


</dt> <dd></dd> <dt>

<span id="25_Pin_Dual_Inline"></span><span id="25_pin_dual_inline"></span><span id="25_PIN_DUAL_INLINE"></span>

**25 Pin Dual Inline** (93)


</dt> <dd></dd> <dt>

<span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>

**50 Pin Dual Inline** (94)


</dt> <dd></dd> <dt>

<span id="68_Pin_Dual_Inline"></span><span id="68_pin_dual_inline"></span><span id="68_PIN_DUAL_INLINE"></span>

**68 Pin Dual Inline** (95)


</dt> <dd></dd> <dt>

<span id="On_Board_Sound_Connector"></span><span id="on_board_sound_connector"></span><span id="ON_BOARD_SOUND_CONNECTOR"></span>

**On Board Sound Connector** (96)


</dt> <dd></dd> <dt>

<span id="Mini-jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>

**Mini-Jack** (97)


</dt> <dd></dd> <dt>

<span id="PCI-X"></span><span id="pci-x"></span>

**PCI-X** (98)


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_32_bit"></span><span id="sbus_ieee_1396-1993_32_bit"></span><span id="SBUS_IEEE_1396-1993_32_BIT"></span>

**Sbus IEEE 1396-1993 32 Bit** (99)


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_64_bit"></span><span id="sbus_ieee_1396-1993_64_bit"></span><span id="SBUS_IEEE_1396-1993_64_BIT"></span>

**Sbus IEEE 1396-1993 64 Bit** (100)


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

**MCA** (101)


</dt> <dd></dd> <dt>

<span id="GIO"></span><span id="gio"></span>

**); 102 (102)**


</dt> <dd></dd> <dt>

<span id="XIO"></span><span id="xio"></span>

**XIO** (103)


</dt> <dd></dd> <dt>

<span id="HIO"></span><span id="hio"></span>

**HIO** (104)


</dt> <dd></dd> <dt>

<span id="NGIO"></span><span id="ngio"></span>

**N WIEGE** (105)


</dt> <dd></dd> <dt>

<span id="PMC"></span><span id="pmc"></span>

**PMC** (106)


</dt> <dd></dd> <dt>

<span id="MTRJ"></span><span id="mtrj"></span>

**MTRJ** (107)


</dt> <dd></dd> <dt>

<span id="VF-45"></span><span id="vf-45"></span>

**VF-45** (108)


</dt> <dd></dd> <dt>

<span id="Future_I_O"></span><span id="future_i_o"></span><span id="FUTURE_I_O"></span>

**Zukünftige E/A** (109)


</dt> <dd></dd> <dt>

<span id="SC"></span><span id="sc"></span>

**SC** (110)


</dt> <dd></dd> <dt>

<span id="SG"></span><span id="sg"></span>

**SG** (111)


</dt> <dd></dd> <dt>

<span id="Electrical"></span><span id="electrical"></span><span id="ELECTRICAL"></span>

**Electrical** (112)


</dt> <dd></dd> <dt>

<span id="Optical"></span><span id="optical"></span><span id="OPTICAL"></span>

**Optisch** (113)


</dt> <dd></dd> <dt>

<span id="Ribbon"></span><span id="ribbon"></span><span id="RIBBON"></span>

**Menüband** (114)


</dt> <dd></dd> <dt>

<span id="GLM"></span><span id="glm"></span>

**GLM** (115)


</dt> <dd></dd> <dt>

<span id="1x9"></span><span id="1X9"></span>

**1x9** (116)


</dt> <dd></dd> <dt>

<span id="Mini_SG"></span><span id="mini_sg"></span><span id="MINI_SG"></span>

**Mini SG** (117)


</dt> <dd></dd> <dt>

<span id="LC"></span><span id="lc"></span>

**LC** (118)


</dt> <dd></dd> <dt>

<span id="HSSC"></span><span id="hssc"></span>

**HSSC** (119)


</dt> <dd></dd> <dt>

<span id="VHDCI_Shielded__68_pins_"></span><span id="vhdci_shielded__68_pins_"></span><span id="VHDCI_SHIELDED__68_PINS_"></span>

**VHDCI Shielded (68 Pins)** (120)


</dt> <dd></dd> <dt>

<span id="InfiniBand"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

**InfiniBand** (121)


</dt> <dd></dd> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**\_ CIM-Taste,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird. Bei Verwendung mit anderen Schlüsseleigenschaften der -Klasse ermöglicht diese Eigenschaft, dass alle Instanzen der Klasse und deren Unterklassen eindeutig identifiziert werden.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Eine Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Installationsdatum")
</dt> </dl>

Gibt an, wann das Objekt installiert wurde. Das Fehlen eines Werts gibt nicht an, dass das Objekt nicht installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Name der Organisation, die für die Erstellung des physischen Elements verantwortlich ist. Weitere Informationen finden Sie unter der **Vendor-Eigenschaft** von [**CIM \_ Product**](cim-product.md).

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**Modell**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Name, unter dem das physische Element allgemein bekannt ist.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Bezeichnung, unter der das Objekt bekannt ist. Bei Unterklassen kann diese Eigenschaft überschrieben werden, um eine Schlüsseleigenschaft zu sein.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zusätzliche Daten, die über Assettaginformationen hinausgehen und zum Identifizieren eines physischen Elements verwendet werden können. Ein Beispiel sind Balkencodedaten, die einem Element zugeordnet sind, das ebenfalls über ein Assettag verfügt. Beachten Sie Folgendes: Wenn nur Balkencodedaten verfügbar sind und eindeutig sind und als Elementschlüssel verwendet werden können, wäre diese Eigenschaft NULL, und die Balkencodedaten würden als Klassenschlüssel in der **Tag-Eigenschaft** verwendet werden.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**PartNumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Teilenummer, die von der Organisation zugewiesen wird, die für die Produktion oder Herstellung des physischen Elements verantwortlich ist.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**PoweredOn**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True gibt an, dass das physische Element eingeschaltet ist. Andernfalls ist sie derzeit deaktiviert.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Serialnumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Vom Hersteller zugeordnete Nummer, die zum Identifizieren des physischen Elements verwendet wird.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Lagerhaltungseinheitennummer für dieses physische Element.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Zeichenfolge, die den aktuellen Status des Objekts angibt. Der Betriebsstatus und der nicht betriebsbereite Status können definiert werden. Der Betriebsstatus kann "OK", "Heruntergestuft" und "Fehler vor dem Fehler" enthalten. "Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. B. ein SMART-fähiges Festplattenlaufwerk).

Nicht betriebsbereite Status können "Error", "Starting", "Stopping" und "Service" sein. "Dienst" kann während der Datenträgerspiegelung, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen Administrativen Arbeiten angewendet werden. Nicht alle dieser Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

Folgende Werte sind gültig:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Fehler** ("Fehler")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Heruntergestuft** ("Heruntergestuft")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("Unbekannt")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Wird gestartet** ("Wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Beenden** ("Wird beendet")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Dienst** ("Dienst")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Mannslast** ("1000")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** ("Kein Kontakt")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Verlorenes Komma** ("Verlorenes Komma")


</dt> <dd></dd> </dl>

</dd> <dt>

**Tag**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**\_ CIM-Schlüssel,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identifiziert das physische Element eindeutig und dient als Schlüssel des Elements. Diese Eigenschaft kann Informationen enthalten, z. B. Assettag- oder Seriennummerndaten. Der Schlüssel für [**CIM \_ PhysicalElement**](cim-physicalelement.md) wird sehr hoch in der Objekthierarchie platziert, um die Hardware oder Entität unabhängig von der physischen Platzierung in Schränken, Adaptern usw. zu identifizieren. Beispielsweise kann eine Wechselkomponente, die im laufenden Betrieb ausgetauscht werden kann, aus dem enthaltenden Paket (Bereichspaket) entnommen und vorübergehend nicht verwendet werden. Das Objekt ist weiterhin vorhanden und kann sogar in einen anderen Bereichscontainer eingefügt werden. Der Schlüssel für ein physisches Element ist eine beliebige Zeichenfolge, die unabhängig von der Platzierung oder der standortorientierten Hierarchie definiert ist.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Gibt die Version des physischen Elements an.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ PhysicalConnector-Klasse** wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)abgeleitet.

WMI implementiert diese Klasse nicht. Informationen zu WMI-Klassen, die von **CIM \_ PhysicalConnector** abgeleitet sind, finden Sie unter [Win32-Klassen.](win32-provider.md)

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden. Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**CIM \_ PhysicalElement**](cim-physicalelement.md)
</dt> </dl>

 

