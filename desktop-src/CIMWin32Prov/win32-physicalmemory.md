---
description: Stellt ein physisches Speichergerät dar, das sich auf einem Computersystem befindet und dem Betriebssystem zur Verfügung steht.
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
ms.openlocfilehash: e026c3c3d0a29bbbd10ed2b5565708f0bcb0900c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483958"
---
# <a name="win32_physicalmemory-class"></a>Win32 \_ PhysicalMemory-Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für den **Win32 \_ PhysicalMemory** stellt ein physisches Speichergerät dar, das sich auf einem Computersystem befindet und dem Betriebssystem zur Verfügung steht.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **Win32 \_ PhysicalMemory** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ PhysicalMemory** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Attribute**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 17- \| Attribute")
</dt> </dl>

SMBIOS-Type 17: Attribute. Stellt den Rang dar.

Dieser Wert stammt aus dem **Attributmember** der **Speichergeräte** Struktur in den SMBIOS-Informationen.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows Server 2016 und Windows 10 nicht unterstützt.

</dd> <dt>

**Banklabel**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Speichergerät \| 002,4 ")
</dt> </dl>

Physisch Bezeichnung Bank, auf der sich der Speicher befindet.

Beispiele: "Bank 0", "Bank A"

Dieser Wert stammt aus dem **Bank Locator** -Member der **Speichergeräte** Struktur in den SMBIOS-Informationen.

Diese Eigenschaft wird von [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)geerbt.

</dd> <dt>

**Capacity**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Speichergerät \| 002,5 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (Bytes)
</dt> </dl>

Gesamtkapazität des physischen Speichers – (in Bytes).

Dieser Wert stammt aus der **Speichergeräte** Struktur in den SMBIOS-Versionsinformationen. Für SMBIOS-Versionen 2,1 bis 2,6 ergibt sich der Wert aus dem **size** -Member. Für SMBIOS, Version 2.7 und höher, wird der Wert aus dem **erweiterten Größen** Element abgeleitet.

Diese Eigenschaft wird von [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)geerbt.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Kurze Beschreibung des Objekts – eine einzeilige Zeichenfolge.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Konfigurations Geschwindigkeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 17 \| konfigurierte Speicher Taktgeschwindigkeit")
</dt> </dl>

Die konfigurierte Taktfrequenz des Speichergeräts in Megahertz (MHz) oder 0 (null), wenn die Geschwindigkeit unbekannt ist.

Dieser Wert stammt aus dem **konfigurierten speicherclock-Geschwindigkeits** Element der **Speichergeräte** Struktur in den SMBIOS-Informationen.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows Server 2016 und Windows 10 nicht unterstützt.

</dd> <dt>

**Konfiguriert**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 17 \| konfigurierte Spannung")
</dt> </dl>

Konfigurierte Spannung für dieses Gerät (in Millivolt) oder 0 (null), wenn die Spannung unbekannt ist.

Dieser Wert stammt aus dem **konfigurierten Spannungs** Element der **Speichergeräte** Struktur in den SMBIOS-Informationen.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows Server 2016 und Windows 10 nicht unterstützt.

</dd> <dt>

**"Name der Klassenname"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird. Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**DataWidth**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Speichergerät \| 002,8 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Bits ")
</dt> </dl>

Daten Breite des physischen Speichers – in Bits. Eine Daten Breite von 0 (null) und eine Gesamtbreite von 8 (acht) gibt an, dass der Arbeitsspeicher ausschließlich zur Bereitstellung von Fehlerkorrektur Bits verwendet wird.

Dieser Wert stammt aus dem **datenwidth** -Member der **Speichergeräte** Struktur in den SMBIOS-Informationen.

Diese Eigenschaft wird von [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Die Beschreibung eines Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**DeviceLocator**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 17 \| Device Locator")
</dt> </dl>

Die Bezeichnung des Sockets oder der Verbindungs Platine, die den Arbeitsspeicher enthält.

Beispiel: "SIMM 3"

Dieser Wert stammt aus dem **geräterlocatormember** der **Speichergeräte** Struktur in den SMBIOS-Informationen.

</dd> <dt>

**Formfaktor**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Speichergerät \| 002,6 ")
</dt> </dl>

Der Implementierungs Formfaktor für den Chip.

Dieser Wert stammt aus dem **Form Faktor** -Member der **Speichergeräte** Struktur in den SMBIOS-Informationen.

Diese Eigenschaft wird vom [**CIM- \_ Chip**](cim-chip.md)geerbt.

<dt>



  (0)


</dt> <dd>

Unbekannt

</dd> <dt>



 (1)


</dt> <dd>

Sonstiges

</dd> <dt>



 (2)


</dt> <dd>

Fen

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

Soj

</dd> <dt>



  (6)


</dt> <dd>

Proprietär

</dd> <dt>



 (7)


</dt> <dd>

SIMM

</dd> <dt>



 (8)


</dt> <dd>

DIMM

</dd> <dt>



 (9)


</dt> <dd>

Wahrheits Satz

</dd> <dt>



 (10)


</dt> <dd>

Besetzten

</dd> <dt>



 (11)


</dt> <dd>

RIMM

</dd> <dt>



 (12)


</dt> <dd>

SODIMM

</dd> <dt>



 (13)


</dt> <dd>

Srimm

</dd> <dt>



 (14)


</dt> <dd>

Tenden

</dd> <dt>



 (15)


</dt> <dd>

SSMP

</dd> <dt>



 (16)


</dt> <dd>

QFP

</dd> <dt>



 (17)


</dt> <dd>

TQFP

</dd> <dt>



 (18)


</dt> <dd>

SOIC

</dd> <dt>



 (19)


</dt> <dd>

LCC

</dd> <dt>



 (20)


</dt> <dd>

PLCC

</dd> <dt>



 (21)


</dt> <dd>

BGA

</dd> <dt>



 (22)


</dt> <dd>

Fpbga

</dd> <dt>



 (23)


</dt> <dd>

LGA

</dd> </dl>

</dd> <dt>

**"Anappable"**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass diese physische Medien Komponente durch eine physisch andere, aber entsprechende ersetzt werden kann, während das enthaltende Paket die Stromversorgung hat. Beispielsweise kann eine Lüfter-Komponente so entworfen werden, dass Sie im laufenden Betrieb ausgetauscht wird. Alle Komponenten, bei denen es sich um eine ausgetauschte Komponente handelt, sind von Natur aus austauschbar und austauschbar.

Diese Eigenschaft wird von [**CIM \_ physicalcomponent**](cim-physicalcomponent.md)geerbt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")
</dt> </dl>

Datum und Uhrzeit der Installation des-Objekts. Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**InterleaveDataDepth**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 20 \| verschachtelte Datentiefe")
</dt> </dl>

Ganze 16-Bit-Ganzzahl ohne Vorzeichen: maximale Anzahl aufeinander folgender Daten Zeilen, auf die in einer einzelnen überlappenden Übertragung vom Arbeitsspeicher Gerät zugegriffen wird. Wenn der Wert 0 (null) ist, wird der Arbeitsspeicher nicht überlappt.

</dd> <dt>

**Interleaveposition**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". Zugeordnete DMTF- \| Speichergeräte Adressen \| 001,7 ")
</dt> </dl>

Die Position des physischen Speichers in einem Interleave. Beispielsweise gibt der Wert "1" in einem 2:1-Interleave an, dass sich der Speicher an der "geraden" Position befindet.

Diese Eigenschaft wird von [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)geerbt.

<dt>

0
</dt> <dd>

Nicht Interleaved

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

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Der Name der Organisation, die für die Erstellung des physischen Elements verantwortlich ist.

Dieser Wert stammt vom **Hersteller** Mitglied der **Speichergeräte** Struktur in den SMBIOS-Informationen.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Maxspannung**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 17 \| Maximale Spannung")
</dt> </dl>

Die maximale Betriebsspannung für dieses Gerät (in Millivolt) oder 0 (null), wenn die Spannung unbekannt ist.

Dieser Wert stammt aus dem **Maximum-Spannungs** Element der **Speichergeräte** Struktur in den SMBIOS-Informationen.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows Server 2016 und Windows 10 nicht unterstützt.

</dd> <dt>

**MemoryType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Speichergerät \| 002,9 ")
</dt> </dl>

Typ des physischen Speichers. Dies ist ein CIM-Wert, der dem SMBIOS-Wert zugeordnet ist. Die Eigenschaft **smbiosmemorytype** enthält den unformatierten SMBIOS-Arbeitsspeichertyp.

Dieser Wert stammt aus dem **Speichertyp** Element der **Speichergeräte** Struktur in den SMBIOS-Informationen.

Diese Eigenschaft wird von [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)geerbt.

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

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>**Synchroner DRAM** (3)


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Cache-DRAM** (4)


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span id="EDO"></span><span id="edo"></span>**Edo** (5)


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

<span id="ROM"></span><span id="rom"></span>**Rom** (10)


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>**Flash** (11)


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span id="EEPROM"></span><span id="eeprom"></span>**EEPROM** (12)


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span id="FEPROM"></span><span id="feprom"></span>**Feprom** (13)


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span id="EPROM"></span><span id="eprom"></span>**EPROM** (14)


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span id="CDRAM"></span><span id="cdram"></span>**CDRAM** (15)


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span id="3DRAM"></span><span id="3dram"></span>**3dram** (16)


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

DDR2 – ist möglicherweise nicht verfügbar.

</dd> <dt>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>**DDR2 FB-DIMM** (22)


</dt> <dd>

DDR2 – FB-DIMM ist möglicherweise nicht verfügbar.

</dd> <dt>

24
</dt> <dd>

"DDR3 –" ist möglicherweise nicht verfügbar.

</dd> <dt>

25
</dt> <dd>

FBD2

</dt> <dd></dd> <dt>

<span id="DDR4"></span><span id="DDR4"></span>**DDR4** (26)

</dd> </dl>

</dd> <dt>

**Minspannung**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 20 \| minimale Spannung")
</dt> </dl>

Die minimale Betriebsspannung für dieses Gerät (in Millivolt) oder 0 (null), wenn die Spannung unbekannt ist.

Dieser Wert stammt aus dem **minimalen Spannungs** Element der **Speichergeräte** Struktur in den SMBIOS-Informationen.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows Server 2016 und Windows 10 nicht unterstützt.

</dd> <dt>

**Modell**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Der Name für das physische Element.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Die Bezeichnung für das-Objekt. Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zusätzliche Daten, über die Informationen zu Asset-Tags hinausgehen, die zum Identifizieren eines physischen Elements verwendet werden können. Ein Beispiel hierfür sind Barcode-Daten, die einem Element zugeordnet sind, das auch über ein Bestands Kennzeichen verfügt. Wenn nur Barcode Daten verfügbar und eindeutig sind oder als Element Schlüssel verwendet werden können, ist diese Eigenschaft **null** , und die Barcode Daten werden als Klassen Schlüssel in der Tag-Eigenschaft verwendet.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**PartNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Teilenummer, die von der Organisation zugewiesen wurde, die für das Erstellen oder die Herstellung des physischen Elements verantwortlich ist

Dieser Wert stammt aus dem **Teil Nummern** Element der **Speichergeräte** Struktur in den SMBIOS-Informationen.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Positioninrow**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". Zugeordnete DMTF- \| Speichergeräte Adressen \| 001,6 ")
</dt> </dl>

Die Position des physischen Speichers in einer Zeile. Wenn z. b. 2 8-Bit-Speichergeräte zum bilden einer 16-Bit-Zeile benötigt werden, bedeutet der Wert 2 (zwei), dass dieser Speicher das zweite Gerät ist – 0 (null) ist ein ungültiger Wert für diese Eigenschaft.

Diese Eigenschaft wird von [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)geerbt.

</dd> <dt>

**Poweredon**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass das physische Element eingeschaltet ist.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Ab**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass eine physische Komponente Wechsel Datenträger ist (wenn Sie so konzipiert ist, dass Sie in den physischen Container übernommen wird, in dem Sie normalerweise gefunden wird, ohne dass die Funktion der gesamten Paket Erstellung beeinträchtigt wird). Eine Komponente kann weiterhin Wechsel Datenträger durchgeführt werden, wenn die Stromversorgung deaktiviert werden muss. Wenn Power "on" sein kann und die Komponente entfernt wurde, ist das Element austauschbar und kann im laufenden Betrieb ausgetauscht werden. Beispielsweise kann ein aktualisierbarer Prozessor Chip entfernt werden.

Diese Eigenschaft wird von [**CIM \_ physicalcomponent**](cim-physicalcomponent.md)geerbt.

</dd> <dt>

**Replaceable**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass diese physische Medien Komponente durch eine physisch andere ersetzt werden kann. Beispielsweise ist für einige Computersysteme das Upgrade des Hauptprozessor-Chips auf eine höhere Bewertungsstufe möglich. In diesem Fall wird der Prozessor als ersetzbar bezeichnet. Alle wechselkomponenten sind von Natur aus ersetzbar.

Diese Eigenschaft wird von [**CIM \_ physicalcomponent**](cim-physicalcomponent.md)geerbt.

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Vom Hersteller zugewiesene Nummer, um das physische Element zu identifizieren.

Dieser Wert stammt aus dem **Seriennummern** Element der **Speichergeräte** Struktur in den SMBIOS-Informationen.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Die Stock Keeping Unit-Nummer für das physische Element.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Smbiosmemorytype**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 17- \| \_ Arbeitsspeichertyp")
</dt> </dl>

Der unformatierte SMBIOS-Arbeitsspeichertyp. Der Wert der **MemoryType** -Eigenschaft ist ein CIM-Wert, der dem SMBIOS-Wert zugeordnet ist.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows Server 2016 und Windows 10 nicht unterstützt.

</dd> <dt>

**Geschwindigkeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("nanoseconds")
</dt> </dl>

Geschwindigkeit des physischen Speichers – in Nanosekunden.

Dieser Wert stammt aus dem **Geschwindigkeits** Mitglied der **Speichergeräte** Struktur in den SMBIOS-Informationen.

Diese Eigenschaft wird von [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)geerbt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden. Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen). Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service". Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

Mögliche Werte sind.

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Fehler** ("Fehler")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

Herunter **gestuft ("** heruntergestuft")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("unbekannt")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred-** Fehler ("pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

Wird **gestartet** ("wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

Wird **beendet ("wird angehalten** ")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Dienst** ("Dienst")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Betont** ("gestresst")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Nicht wiederherstellen** ("nicht wiederherstellen")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** ("kein Kontakt")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Verlorene** Kommunikations ("verlorene Kommunikations-")


</dt> <dd></dd> </dl>

</dd> <dt>

**Tag**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Eindeutiger Bezeichner für das physische Speichergerät, das durch eine Instanz von **Win32 \_ PhysicalMemory** repräsentiert wird. Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

Beispiel: "physischer Speicher 1"

</dd> <dt>

**TotalWidth**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Speichergerät \| 002,7 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Bits ")
</dt> </dl>

Gesamtbreite des physischen Speichers (in Bits), einschließlich der Check-oder Error-Korrektur Bits. Wenn keine Fehlerkorrektur Bits vorhanden sind, sollte der Wert in dieser Eigenschaft mit den Angaben für die **DataWidth** -Eigenschaft identisch sein.

Dieser Wert stammt aus dem **Total Width** -Element der **Speichergeräte** Struktur in den SMBIOS-Informationen.

Diese Eigenschaft wird von [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)geerbt.

</dd> <dt>

**TypeDetail**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 17 \| Type Details")
</dt> </dl>

Typ des dargestellten physischen Speichers.

Dieser Wert stammt vom **typdetailmember** der **Speichergeräte** Struktur in den SMBIOS-Informationen.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserviert** (1)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (4)


</dt> <dd></dd> <dt>

<span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>

<span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>**Schnell Auslagerung(** 8)


</dt> <dd></dd> <dt>

<span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>

<span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>**Statische Spalte** (16)


</dt> <dd></dd> <dt>

<span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>

<span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>**Pseudo statisch** (32)


</dt> <dd></dd> <dt>

<span id="RAMBUS"></span><span id="rambus"></span>

<span id="RAMBUS"></span><span id="rambus"></span>**Rambus** (64)


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>**Synchron** (128)


</dt> <dd></dd> <dt>

<span id="CMOS"></span><span id="cmos"></span>

<span id="CMOS"></span><span id="cmos"></span>**CMOS** (256)


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span id="EDO"></span><span id="edo"></span>**Edo** (512)


</dt> <dd></dd> <dt>

<span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>

<span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>**Fenster DRAM** (1024)


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

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Version des physischen Elements.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32 \_ PhysicalMemory** -Klasse wird von [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)abgeleitet.

## <a name="examples"></a>Beispiele

Das PowerShell [-Beispiel Get-ComputerInfo-Query Computer Info from Local/Remote Computers-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) in der TechNet Gallery verwendet eine Reihe von Aufrufen von Hardware und Software, einschließlich **Win32 \_ PhysicalMemory**, um Informationen über ein lokales oder Remote System anzuzeigen.

Das PowerShell-Beispiel für [Server Berichte](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) in der TechNet Gallery verwendet eine Reihe von Aufrufen von Hardware und Software, einschließlich **Win32 \_ PhysicalMemory**, um Server Informationen zu erfassen und in Word-Dokumenten zu veröffentlichen.

Das folgende PowerShell-Beispielcode ruft Informationen zum physischen Speicher des lokalen Computers ab.


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
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ PhysicalMemory**](cim-physicalmemory.md)
</dt> <dt>

[Computer System-Hardware Klassen](computer-system-hardware-classes.md)
</dt> </dl>

 

 
