---
description: Stellt ein physisches Speichergerät dar, das sich auf einem Computersystem befindet und für das Betriebssystem verfügbar ist.
ms.assetid: 34baca53-ab85-4e06-9853-71b904ede4ab
ms.tgt_platform: multiple
title: Win32_PhysicalMemory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemory
- Win32_PhysicalMemory.Attributes
- Win32_PhysicalMemory.BankLabel
- Win32_PhysicalMemory.Capacity
- Win32_PhysicalMemory.Caption
- Win32_PhysicalMemory.ConfiguredClockSpeed
- Win32_PhysicalMemory.ConfiguredVoltage
- Win32_PhysicalMemory.CreationClassName
- Win32_PhysicalMemory.DataWidth
- Win32_PhysicalMemory.Description
- Win32_PhysicalMemory.DeviceLocator
- Win32_PhysicalMemory.FormFactor
- Win32_PhysicalMemory.HotSwappable
- Win32_PhysicalMemory.InstallDate
- Win32_PhysicalMemory.InterleaveDataDepth
- Win32_PhysicalMemory.InterleavePosition
- Win32_PhysicalMemory.Manufacturer
- Win32_PhysicalMemory.MaxVoltage
- Win32_PhysicalMemory.MemoryType
- Win32_PhysicalMemory.MinVoltage
- Win32_PhysicalMemory.Model
- Win32_PhysicalMemory.Name
- Win32_PhysicalMemory.OtherIdentifyingInfo
- Win32_PhysicalMemory.PartNumber
- Win32_PhysicalMemory.PositionInRow
- Win32_PhysicalMemory.PoweredOn
- Win32_PhysicalMemory.Removable
- Win32_PhysicalMemory.Replaceable
- Win32_PhysicalMemory.SerialNumber
- Win32_PhysicalMemory.SKU
- Win32_PhysicalMemory.SMBIOSMemoryType
- Win32_PhysicalMemory.Speed
- Win32_PhysicalMemory.Status
- Win32_PhysicalMemory.Tag
- Win32_PhysicalMemory.TotalWidth
- Win32_PhysicalMemory.TypeDetail
- Win32_PhysicalMemory.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5559de847cf15b60e3af27f8b092605b8ca8c3bfd874d27ebab7a0edda454d14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972210"
---
# <a name="win32_physicalmemory-class"></a>Win32 \_ PhysicalMemory-Klasse

Die **WMI-Klasse \_ Win32 PhysicalMemory** stellt ein physisches Speichergerät dar, das sich auf einem Computersystem befindet und für das Betriebssystem verfügbar ist. [](../wmisdk/retrieving-a-class.md)

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B93-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PhysicalMemory : CIM_PhysicalMemory
{
  uint32   Attributes;
  string   BankLabel;
  uint64   Capacity;
  string   Caption;
  uint32   ConfiguredClockSpeed;
  uint32   ConfiguredVoltage;
  string   CreationClassName;
  uint16   DataWidth;
  string   Description;
  string   DeviceLocator;
  uint16   FormFactor;
  boolean  HotSwappable;
  datetime InstallDate;
  uint16   InterleaveDataDepth;
  uint32   InterleavePosition;
  string   Manufacturer;
  uint32   MaxVoltage;
  uint16   MemoryType;
  uint32   MinVoltage;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  uint32   PositionInRow;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  uint32   SMBIOSMemoryType;
  uint32   Speed;
  string   Status;
  string   Tag;
  uint16   TotalWidth;
  uint16   TypeDetail;
  string   Version;
};
```

## <a name="members"></a>Member

Die **Win32 \_ PhysicalMemory-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ PhysicalMemory-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Attribute**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 17 \| Attributes")
</dt> </dl>

SMBIOS: Geben Sie 17 – Attribute ein. Stellt den RANK dar.

Dieser Wert stammt aus dem **Attributes-Member** der **Memory Device-Struktur** in den SMBIOS-Informationen.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008** und Windows Vista: Diese Eigenschaft wird nicht unterstützt, bevor Windows Server 2016 und Windows 10.

</dd> <dt>

**BankLabel**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|DMTF-Speichergerät \| 002.4")
</dt> </dl>

Physisch bezeichnete Bank, in der sich der Arbeitsspeicher befindet.

Beispiele: "Bank 0", "Bank A"

Dieser Wert stammt aus dem **Bank Locator-Member** der **Memory Device-Struktur** in den SMBIOS-Informationen.

Diese Eigenschaft wird von [**CIM \_ PhysicalMemory geerbt.**](cim-physicalmemory.md)

</dd> <dt>

**Capacity**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|DMTF-Speichergerät \| 002.5"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bytes")
</dt> </dl>

Gesamtkapazität des physischen Speichers – in Bytes.

Dieser Wert stammt aus der **Speichergerätestruktur** in den SMBIOS-Versionsinformationen. Für die SMBIOS-Versionen 2.1 bis 2.6 stammt der Wert vom **Size-Member.** Für SMBIOS Version 2.7 und mehr stammt der Wert vom **Member "Erweiterte** Größe".

Diese Eigenschaft wird von [**CIM \_ PhysicalMemory geerbt.**](cim-physicalmemory.md)

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](../wmisdk/creating-a-wmi-script.md)

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Kurze Beschreibung des -Objekts– eine einzeilenbasierte Zeichenfolge.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**ConfiguredClockSpeed**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 17 \| Configured Memory Clock Speed")
</dt> </dl>

Die konfigurierte Taktgeschwindigkeit des Speichergeräts in Megahertz (MHz) oder 0, wenn die Geschwindigkeit unbekannt ist.

Dieser Wert stammt aus dem **Configured Memory Clock Speed-Member** der **Memory Device-Struktur** in den SMBIOS-Informationen.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008** und Windows Vista: Diese Eigenschaft wird nicht unterstützt, bevor Windows Server 2016 und Windows 10.

</dd> <dt>

**ConfiguredVoltage**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 17 \| Configured voltage")
</dt> </dl>

Konfigurierte Spannung für dieses Gerät in Millisekunden oder 0, wenn die Spannung unbekannt ist.

Dieser Wert stammt aus dem **konfigurierten Spannungs-Member** der **Memory Device-Struktur** in den SMBIOS-Informationen.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008** und Windows Vista: Diese Eigenschaft wird nicht unterstützt, bevor Windows Server 2016 und Windows 10.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**\_ CIM-Schlüssel,**](../wmisdk/standard-wmi-qualifiers.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Name der ersten konkreten Klasse, die in der Vererbungskette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird. Bei Verwendung mit den anderen Schlüsseleigenschaften der -Klasse ermöglicht die -Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**DataWidth**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|DMTF-Speichergerät \| 002.8"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bits")
</dt> </dl>

Datenbreite des physischen Speichers in Bits. Eine Datenbreite von 0 (null) und eine Gesamtbreite von 8 (acht) gibt an, dass der Arbeitsspeicher ausschließlich zur Bereitstellung von Fehlerkorrekturbits verwendet wird.

Dieser Wert stammt aus dem **Datenbreiten-Member** der **Speichergerätestruktur** in den SMBIOS-Informationen.

Diese Eigenschaft wird von [**CIM \_ PhysicalMemory geerbt.**](cim-physicalmemory.md)

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Beschreibung eines Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**DeviceLocator**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 17 \| Device Locator")
</dt> </dl>

Bezeichnung des Sockets oder der Leitungsplatine, die den Arbeitsspeicher enthält.

Beispiel: "SIMM 3"

Dieser Wert stammt aus dem **Device Locator-Member** der **Memory Device-Struktur** in den SMBIOS-Informationen.

</dd> <dt>

**FormFactor**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|DMTF-Speichergerät \| 002.6")
</dt> </dl>

Implementierungsformfaktor für den Chip.

Dieser Wert stammt aus dem **Form Factor-Element** der **Memory Device-Struktur** in den SMBIOS-Informationen.

Diese Eigenschaft wird vom [**\_ CIM-Chip geerbt.**](cim-chip.md)

<dt>



  (0)


</dt> <dd>

Unbekannt

</dd> <dt>



 (1)


</dt> <dd>

Andere

</dd> <dt>



 (2)


</dt> <dd>

Sip

</dd> <dt>



 (3)


</dt> <dd>

DIP

</dd> <dt>



 (4)


</dt> <dd>

ZIP

</dd> <dt>



 (5)


</dt> <dd>

SOJ

</dd> <dt>



  (6)


</dt> <dd>

Proprietär

</dd> <dt>



 (7)


</dt> <dd>

Simm

</dd> <dt>



 (8)


</dt> <dd>

Dimm

</dd> <dt>



 (9)


</dt> <dd>

Tsop

</dd> <dt>



 (10)


</dt> <dd>

Pga

</dd> <dt>



 (11)


</dt> <dd>

Rimm

</dd> <dt>



 (12)


</dt> <dd>

Sodimm

</dd> <dt>



 (13)


</dt> <dd>

SRIMM

</dd> <dt>



 (14)


</dt> <dd>

Smd

</dd> <dt>



 (15)


</dt> <dd>

SSMP

</dd> <dt>



 (16)


</dt> <dd>

Qfp

</dd> <dt>



 (17)


</dt> <dd>

Tqfp

</dd> <dt>



 (18)


</dt> <dd>

SOIC

</dd> <dt>



 (19)


</dt> <dd>

Lcc

</dd> <dt>



 (20)


</dt> <dd>

Plcc

</dd> <dt>



 (21)


</dt> <dd>

Bga

</dd> <dt>



 (22)


</dt> <dd>

FPBGA

</dd> <dt>



 (23)


</dt> <dd>

LGA

</dd> </dl>

</dd> <dt>

**HotSwappable**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True **gibt an,** dass diese physische Medienkomponente durch eine physisch unterschiedliche, aber äquivalente Komponente ersetzt werden kann, während auf das enthaltende Paket die Energie angewendet wird. Beispielsweise kann eine Lüfterkomponente so entworfen werden, dass sie hot-swaped ist. Alle Komponenten, die im Hot-Swap-System ausgetauscht werden können, sind grundsätzlich austauschbar und austauschbar.

Diese Eigenschaft wird von [**CIM \_ PhysicalComponent geerbt.**](cim-physicalcomponent.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Installation date")
</dt> </dl>

Datum und Uhrzeit der Installation des Objekts. Diese Eigenschaft benötigt keinen Wert, um anzugeben, dass das Objekt installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**InterleaveDataDepth**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 20 \| Interleaved Data Depth")
</dt> </dl>

16-Bit-Ganzzahl ohne Vorzeichen maximale Anzahl aufeinanderfolgender Datenzeilen, auf die in einer einzelnen überlappten Übertragung vom Speichergerät zugegriffen wird. Wenn der Wert 0 (null) ist, ist der Arbeitsspeicher nicht übereinander.

</dd> <dt>

**InterleavePosition**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Memory Device Mapped Addresses \| 001.7")
</dt> </dl>

Position des physischen Speichers in einer Verwebung. Bei einem 2:1-Interleave gibt der Wert "1" beispielsweise an, dass sich der Arbeitsspeicher an der "gleichmäßigen" Position befindet.

Diese Eigenschaft wird von [**CIM \_ PhysicalMemory geerbt.**](cim-physicalmemory.md)

<dt>

0
</dt> <dd>

Nicht interleaved

</dd> <dt>

1
</dt> <dd>

Erste Position

</dd> <dt>

2
</dt> <dd>

Zweite Position

</dd> </dl>

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Name der Organisation, die für die Erstellung des physischen Elements verantwortlich ist.

Dieser Wert stammt aus dem **Manufacturer-Member** der **Memory Device-Struktur** in den SMBIOS-Informationen.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**MaxVoltage**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 17 \| Maximum voltage")
</dt> </dl>

Die maximale Betriebsspannung für dieses Gerät in Millisekunden oder 0, wenn die Spannung unbekannt ist.

Dieser Wert stammt aus dem **Maximum-Spannungs-Member** der **Memory Device-Struktur** in den SMBIOS-Informationen.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird nicht unterstützt, bevor Windows Server 2016 und Windows 10.

</dd> <dt>

**MemoryType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|DMTF-Speichergerät \| 002.9")
</dt> </dl>

Typ des physischen Speichers. Dies ist ein CIM-Wert, der dem SMBIOS-Wert zugeordnet ist. Die **SMBIOSMemoryType-Eigenschaft** enthält den unformatten SMBIOS-Speichertyp.

Dieser Wert stammt aus dem **Memory Type-Member** der **Memory Device-Struktur** in den SMBIOS-Informationen.

Diese Eigenschaft wird von [**CIM \_ PhysicalMemory geerbt.**](cim-physicalmemory.md)

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span id="DRAM"></span><span id="dram"></span>**DRAM** (2)


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>**Synchrones DRAM** (3)


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Cache-DRAM** (4)


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span id="EDO"></span><span id="edo"></span>**EDO** (5)


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span id="EDRAM"></span><span id="edram"></span>**EDRAM** (6)


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span id="VRAM"></span><span id="vram"></span>**VRAM** (7)


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span id="SRAM"></span><span id="sram"></span>**SRAM** (8)


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span id="RAM"></span><span id="ram"></span>**RAM** (9)


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span id="ROM"></span><span id="rom"></span>**ROM** (10)


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>**Flash** (11)


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span id="EEPROM"></span><span id="eeprom"></span>**EEPROM** (12)


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span id="FEPROM"></span><span id="feprom"></span>**FEPROM** (13)


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span id="EPROM"></span><span id="eprom"></span>**EPROM** (14)


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span id="CDRAM"></span><span id="cdram"></span>**CDRAM** (15)


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span id="3DRAM"></span><span id="3dram"></span>**3DRAM** (16)


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span id="SDRAM"></span><span id="sdram"></span>**SDRAM** (17)


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span id="SGRAM"></span><span id="sgram"></span>**SGRAM** (18)


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span id="RDRAM"></span><span id="rdram"></span>**RDRAM** (19)


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span id="DDR"></span><span id="ddr"></span>**DDR** (20)


</dt> <dd></dd> <dt>

<span id="DDR2"></span><span id="ddr2"></span>

<span id="DDR2"></span><span id="ddr2"></span>**DDR2** (21)


</dt> <dd>

DDR2– Ist möglicherweise nicht verfügbar.

</dd> <dt>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>**DDR2 FB-DIM** (22)


</dt> <dd>

DDR2 – FB-DIM, möglicherweise nicht verfügbar.

</dd> <dt>

24
</dt> <dd>

DDR3– Ist möglicherweise nicht verfügbar.

</dd> <dt>

25
</dt> <dd>

FBD2

</dt> <dd></dd> <dt>

<span id="DDR4"></span><span id="DDR4"></span>**DDR4** (26)

</dd> </dl>

</dd> <dt>

**MinVoltage**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 20 \| Minimum voltage")
</dt> </dl>

Die Mindestbetriebsspannung für dieses Gerät in Millisekunden oder 0, wenn die Spannung unbekannt ist.

Dieser Wert stammt aus dem **Minimum-Spannungs-Member** der **Memory Device-Struktur** in den SMBIOS-Informationen.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird nicht unterstützt, bevor Windows Server 2016 und Windows 10.

</dd> <dt>

**Modell**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Name für das physische Element.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Bezeichnung für das -Objekt. Bei Unterklassen kann die Eigenschaft überschrieben werden, um eine Schlüsseleigenschaft zu sein.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zusätzliche Daten, die über Assettaginformationen hinausgehen und zum Identifizieren eines physischen Elements verwendet werden können. Ein Beispiel sind Balkencodedaten, die einem Element zugeordnet sind, das auch über ein Assettag verfügt. Wenn nur Balkencodedaten verfügbar sind und eindeutig sind oder als Elementschlüssel verwendet werden können, ist diese Eigenschaft **NULL,** und die Barcodedaten werden als Klassenschlüssel in der Tageigenschaft verwendet.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**PartNumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Teilenummer, die von der Organisation zugewiesen wird, die für die Produktion oder Herstellung des physischen Elements zuständig ist.

Dieser Wert stammt aus dem **Part Number-Member** der **Memory Device-Struktur** in den SMBIOS-Informationen.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**PositionInRow**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Memory Device Mapped Addresses \| 001.6")
</dt> </dl>

Position des physischen Speichers in einer Zeile. Wenn beispielsweise zwei 8-Bit-Speichergeräte eine 16-Bit-Zeile bilden, bedeutet der Wert 2 (zwei), dass dieser Speicher das zweite Gerät ist– 0 (null) ist ein ungültiger Wert für diese Eigenschaft.

Diese Eigenschaft wird von [**CIM \_ PhysicalMemory geerbt.**](cim-physicalmemory.md)

</dd> <dt>

**PoweredOn**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True **gibt an,** dass das physische Element eingeschaltet wird.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**Abnehmbare**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True **gibt** an, dass eine physische Komponente wechselbar ist (wenn sie so konzipiert ist, dass sie in den physischen Container, in dem sie sich normalerweise befindet, ein- und aus dem Container entfernt wird, ohne die Funktion der Gesamtpaketierung zu beeinträchtigen). Eine Komponente kann weiterhin wechselbar sein, wenn die Stromversorgung "aus" sein muss, um das Entfernen durchzuführen. Wenn die Stromversorgung "ein" sein kann und die Komponente entfernt werden kann, ist das Element wechselbar und kann mit hot ausgetauscht werden. Beispielsweise ist ein erweiterbarer Prozessorchip wechselbar.

Diese Eigenschaft wird von [**CIM \_ PhysicalComponent geerbt.**](cim-physicalcomponent.md)

</dd> <dt>

**Austauschbare**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True **gibt an,** dass diese physische Medienkomponente durch eine physisch andere ersetzt werden kann. Einige Computersysteme ermöglichen z. B. das Upgrade des Hauptprozessorchips auf eine der höheren Taktwerte. In diesem Fall wird der Prozessor als ersetzbar bezeichnet. Alle Wechselkomponenten sind grundsätzlich austauschbar.

Diese Eigenschaft wird von [**CIM \_ PhysicalComponent geerbt.**](cim-physicalcomponent.md)

</dd> <dt>

**Serialnumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Vom Hersteller zugeordnete Zahl, um das physische Element zu identifizieren.

Dieser Wert stammt aus dem **Serial Number-Member** der **Memory Device-Struktur** in den SMBIOS-Informationen.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Lagerhaltungseinheitennummer für das physische Element.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**SMBIOSMemoryType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS-Typ \| 17 \| \_ Arbeitsspeichertyp")
</dt> </dl>

Der SMBIOS-Rohdatenspeichertyp. Der Wert der **MemoryType-Eigenschaft** ist ein CIM-Wert, der dem SMBIOS-Wert zugeordnet ist.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows Server 2016 und Windows 10 nicht unterstützt.

</dd> <dt>

**Geschwindigkeit**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Nanosekunden")
</dt> </dl>

Geschwindigkeit des physischen Speichers – in Nanosekunden.

Dieser Wert stammt aus dem **Speed-Member** der **Speichergerätestruktur** in den SMBIOS-Informationen.

Diese Eigenschaft wird von [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)geerbt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene Betriebs- und Nichtoperationsstatus definiert werden. Betriebsstatus: "OK", "Heruntergestuft" und "Pred Fail" (ein Element, z. B. ein SMART-fähiges Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, sagt aber einen Fehler in naher Zukunft vorher). Nichtoperationale Status: "Error", "Starting", "Stopping" und "Service". Letzteres, "Dienst", kann während des Spiegelungsresilverings eines Datenträgers, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen Verwaltungsaufgaben angewendet werden. Nicht alle dieser Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

Die möglichen Werte sind.

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

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Eindeutiger Bezeichner für das physische Speichergerät, das durch eine Instanz von **Win32 \_ PhysicalMemory** dargestellt wird. Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

Beispiel: "Physischer Speicher 1"

</dd> <dt>

**TotalWidth**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|DMTF-Speichergerät \| 002.7"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bits")
</dt> </dl>

Gesamtbreite des physischen Speichers in Bits, einschließlich Überprüfungs- oder Fehlerkorrekturbits. Wenn keine Fehlerkorrekturbits vorhanden sind, sollte der Wert in dieser Eigenschaft mit dem für die **DataWidth-Eigenschaft** angegebenen Wert übereinstimmen.

Dieser Wert stammt aus dem **Element Gesamtbreite** der **Speichergerätestruktur** in den SMBIOS-Informationen.

Diese Eigenschaft wird von [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)geerbt.

</dd> <dt>

**TypeDetail**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 17 \| Type Detail")
</dt> </dl>

Typ des dargestellten physischen Arbeitsspeichers.

Dieser Wert stammt aus dem **Typdetailmember** der **Speichergerätestruktur** in den SMBIOS-Informationen.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserviert** (1)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (4)


</dt> <dd></dd> <dt>

<span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>

<span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>**Fast-paged** (8)


</dt> <dd></dd> <dt>

<span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>

<span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>**Statische Spalte** (16)


</dt> <dd></dd> <dt>

<span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>

<span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>**Pseudo statisch** (32)


</dt> <dd></dd> <dt>

<span id="RAMBUS"></span><span id="rambus"></span>

<span id="RAMBUS"></span><span id="rambus"></span>**RAMBUS** (64)


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>**Synchron** (128)


</dt> <dd></dd> <dt>

<span id="CMOS"></span><span id="cmos"></span>

<span id="CMOS"></span><span id="cmos"></span>**SENSORS** (256)


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span id="EDO"></span><span id="edo"></span>**EDO** (512)


</dt> <dd></dd> <dt>

<span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>

<span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>**Fenster-DRAM** (1024)


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Cache-DRAM** (2048)


</dt> <dd></dd> <dt>

<span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>

<span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>**Nicht flüchtig** (4096)


</dt> <dd>

Nicht volatil

</dd> </dl>

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Version des physischen Elements.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ PhysicalMemory-Klasse** wird von [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)abgeleitet.

## <a name="examples"></a>Beispiele

Das [PowerShell-Beispiel Get-ComputerInfo – Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) im TechNet Gallery verwendet eine Reihe von Aufrufen von Hardware und Software, einschließlich **Win32 \_ PhysicalMemory,** um Informationen zu einem lokalen oder Remotesystem anzuzeigen.

Das PowerShell-Beispiel für [Serverbericht](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) im TechNet-Katalog verwendet eine Reihe von Aufrufen von Hardware und Software, einschließlich **Win32 \_ PhysicalMemory,** um Serverinformationen zu sammeln und im Word-Dokument zu veröffentlichen.

Im folgenden PowerShell-Codebeispiel werden Informationen zum physischen Arbeitsspeicher des lokalen Computers abgerufen.


```PowerShell
function get-WmiMemoryFormFactor {
param ([uint16] $char)

If ($char -ge 0 -and  $char  -le 22) {

switch ($char) {
0     {"00-Unknown"}
1     {"01-Other"}
2     {"02-SiP"}
3     {"03-DIP"}
4     {"04-ZIP"}
5     {"05-SOJ"}
6     {"06-Proprietary"}
7     {"07-SIMM"}
8     {"08-DIMM"}
9     {"09-TSOPO"}
10     {"10-PGA"}
11     {"11-RIM"}
12     {"12-SODIMM"}
13     {"13-SRIMM"}
14     {"14-SMD"}
15     {"15-SSMP"}
16     {"16-QFP"}
17     {"17-TQFP"}
18     {"18-SOIC"}
19     {"19-LCC"}
20     {"20-PLCC"}
21     {"21-FPGA"}
22     {"22-LGA"}
}
}

else {"{0} - undefined value" -f $char
}

Return
}

# Helper function to return memory Interleave  Position

function get-WmiInterleavePosition {
param ([uint32] $char)

If ($char -ge 0 -and  $char -le 2) {

switch ($char) {
0     {"00-Non-Interleaved"}
1     {"01-First Position"}
2     {"02-Second Position"}
}
}

else {"{0} - undefined value" -f $char
}

Return
}


# Helper function to return Memory Tupe
function get-WmiMemoryType {
param ([uint16] $char)

If ($char -ge 0 -and  $char  -le 20) {

switch ($char) {
0     {"00-Unknown"}
1     {"01-Other"}
2     {"02-DRAM"}
3     {"03-Synchronous DRAM"}
4     {"04-Cache DRAM"}
5     {"05-EDO"}
6     {"06-EDRAM"}
7     {"07-VRAM"}
8     {"08-SRAM"}
9     {"09-ROM"}
10     {"10-ROM"}
11     {"11-FLASH"}
12     {"12-EEPROM"}
13     {"13-FEPROM"}
14     {"14-EPROM"}
15     {"15-CDRAM"}
16     {"16-3DRAM"}
17     {"17-SDRAM"}
18     {"18-SGRAM"}
19     {"19-RDRAM"}
20     {"20-DDR"}
}

}

else {"{0} - undefined value" -f $char
}

Return
}


# Get the object
$memory = Get-WMIObject Win32_PhysicalMemory

#  Format and Print
"System has {0} memory sticks:" -f $memory.count

Foreach ($stick in $memory) {

# Do some conversions
$cap=$stick.capacity/1mb
$ff=get-WmiMemoryFormFactor($stick.FormFactor)
$ilp=get-WmiInterleavePosition($stick.InterleavePosition)
$mt=get-WMIMemoryType($stick.MemoryType)

# print details of each stick
"BankLabel            {0}"  -f $stick.banklabel
"Capacity (MB)        {0}"  -f $cap
"Caption              {0}"  -f $stick.Caption
"CreationClassName    {0}"  -f $stick.creationclassname
"DataWidth            {0}"  -f $stick.DataWidth
"Description          {0}"  -f $stick.Description
"DeviceLocator        {0}"  -f $stick.DeviceLocator
"FormFactor           {0}"  -f $ff
"HotSwappable         {0}"  -f $stick.HotSwappable
"InstallDate          {0}"  -f $stick.InstallDate
"InterleaveDataDepth  {0}"  -f $stick.InterleaveDataDepth
"InterleavePosition   {0}"  -f $ilp
"Manufacturer         {0}"  -f $stick.Manufacturer
"MemoryType           {0}"  -f $mt
"Model                {0}"  -f $stick.Model
"Name                 {0}"  -f $stick.Name
"OtherIdentifyingInfo {0}"  -f $stick.OtherIdentifyingInfo
"PartNumber           {0}"  -f $stick.PartNumber
"PositionInRow        {0}"  -f $stick.PositionInRow
"PoweredOn            {0}"  -f $stick.PoweredOn
"Removable            {0}"  -f $stick.Removable
"Replaceable          {0}"  -f $stick.Replaceable
"SerialNumber         {0}"  -f $stick.SerialNumber
"SKU                  {0}"  -f $stick.SKU 
"Speed                {0}"  -f $stick.Speed 
"Status               {0}"  -f $stick.Status
"Tag                  {0}"  -f $stick.Tag
"TotalWidth           {0}"  -f $stick.TotalWidth 
"TypeDetail           {0}"  -f $stick.TypeDetail
"Version              {0}"  -f $stick.Version
""
}
"-----"
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ PhysicalMemory**](cim-physicalmemory.md)
</dt> <dt>

[Hardwareklassen des Computersystems](computer-system-hardware-classes.md)
</dt> </dl>

 

 
