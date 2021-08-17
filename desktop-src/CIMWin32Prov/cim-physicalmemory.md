---
description: Die CIM PhysicalMemory-Klasse stellt Speichergeräte auf niedriger Ebene dar, z. B. \_ SIMMS, DIMMs, unformatte Speicherchips und so weiter.
ms.assetid: a25c5f00-cd85-42e6-9b26-8e9380b3c73b
ms.tgt_platform: multiple
title: CIM_PhysicalMemory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalMemory
- CIM_PhysicalMemory.BankLabel
- CIM_PhysicalMemory.Capacity
- CIM_PhysicalMemory.Caption
- CIM_PhysicalMemory.CreationClassName
- CIM_PhysicalMemory.DataWidth
- CIM_PhysicalMemory.Description
- CIM_PhysicalMemory.FormFactor
- CIM_PhysicalMemory.HotSwappable
- CIM_PhysicalMemory.InstallDate
- CIM_PhysicalMemory.InterleavePosition
- CIM_PhysicalMemory.Manufacturer
- CIM_PhysicalMemory.MemoryType
- CIM_PhysicalMemory.Model
- CIM_PhysicalMemory.Name
- CIM_PhysicalMemory.OtherIdentifyingInfo
- CIM_PhysicalMemory.PartNumber
- CIM_PhysicalMemory.PositionInRow
- CIM_PhysicalMemory.PoweredOn
- CIM_PhysicalMemory.Removable
- CIM_PhysicalMemory.Replaceable
- CIM_PhysicalMemory.SerialNumber
- CIM_PhysicalMemory.SKU
- CIM_PhysicalMemory.Speed
- CIM_PhysicalMemory.Status
- CIM_PhysicalMemory.Tag
- CIM_PhysicalMemory.TotalWidth
- CIM_PhysicalMemory.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b85a4e80588b98625f166f76c09aff9d52b114adcee4507eb7b81957746d88e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080484"
---
# <a name="cim_physicalmemory-class"></a>CIM \_ PhysicalMemory-Klasse

Die **CIM \_ PhysicalMemory-Klasse** stellt Speichergeräte auf niedriger Ebene dar, z. B. SIMMS, DIMMs, unformatte Speicherchips und so weiter.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[abstract, UUID("{FAF76B7B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalMemory : CIM_Chip
{
  string   BankLabel;
  uint64   Capacity;
  string   Caption;
  string   CreationClassName;
  uint16   DataWidth;
  string   Description;
  uint16   FormFactor;
  boolean  HotSwappable;
  datetime InstallDate;
  uint32   InterleavePosition;
  string   Manufacturer;
  uint16   MemoryType;
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
  uint32   Speed;
  string   Status;
  string   Tag;
  uint16   TotalWidth;
  string   Version;
};
```

## <a name="members"></a>Member

Die **CIM \_ PhysicalMemory-Klasse** verfügt über diese Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ PhysicalMemory-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**BankLabel**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|DMTF-Speichergerät \| 002.4")
</dt> </dl>

Bezeichnete Bank, in der sich der Arbeitsspeicher befindet. Beispiel: "Bank 0" oder "Bank A".

</dd> <dt>

**Capacity**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|DMTF-Speichergerät \| 002.5"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")
</dt> </dl>

Gesamtkapazität des physischen Arbeitsspeichers in Bytes.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Kurze Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**\_ CIM-Schlüssel,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird. Bei Verwendung mit anderen Schlüsseleigenschaften der -Klasse ermöglicht diese Eigenschaft, dass alle Instanzen der Klasse und deren Unterklassen eindeutig identifiziert werden.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**DataWidth**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|DMTF-Speichergerät \| 002.8"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")
</dt> </dl>

Datenbreite des physischen Speichers in Bits. Eine Datenbreite von 0 (null) und eine Gesamtbreite von 8 gibt an, dass der Arbeitsspeicher ausschließlich zur Bereitstellung von Fehlerkorrekturbits verwendet wird.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**FormFactor**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("FormFactor"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|DMTF-Speichergerät \| 002.6")
</dt> </dl>

Implementierungsformfaktor für den Chip. Beispielsweise können Werte wie SIMM, TSOP oder PGA angegeben werden.

Diese Eigenschaft wird vom [**\_ CIM-Chip geerbt.**](cim-chip.md)

<dt>

0
</dt> <dd>

Unbekannt

</dd> <dt>

1
</dt> <dd>

Sonstiges

</dd> <dt>

2
</dt> <dd>

Sip

</dd> <dt>

3
</dt> <dd>

DIP

</dd> <dt>

4
</dt> <dd>

ZIP

</dd> <dt>

5
</dt> <dd>

SOJ

</dd> <dt>

6
</dt> <dd>

Proprietär

</dd> <dt>

7
</dt> <dd>

Simm

</dd> <dt>

8
</dt> <dd>

Dimm

</dd> <dt>

9
</dt> <dd>

Tsop

</dd> <dt>

10
</dt> <dd>

Pga

</dd> <dt>

11
</dt> <dd>

Rimm

</dd> <dt>

12
</dt> <dd>

Sodimm

</dd> <dt>

13
</dt> <dd>

SRIMM

</dd> <dt>

14
</dt> <dd>

Smd

</dd> <dt>

15
</dt> <dd>

SSMP

</dd> <dt>

16
</dt> <dd>

Qfp

</dd> <dt>

17
</dt> <dd>

Tqfp

</dd> <dt>

18
</dt> <dd>

SOIC

</dd> <dt>

19
</dt> <dd>

Lcc

</dd> <dt>

20
</dt> <dd>

Plcc

</dd> <dt>

21
</dt> <dd>

Bga

</dd> <dt>

22
</dt> <dd>

FPBGA

</dd> <dt>

23
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

True **gibt an,** dass das Paket im heißen Tausch verwendet werden kann. Ein physisches Paket kann im Hot-Swap-Format ausgetauscht werden, wenn das Element durch ein physisch anderes (aber äquivalentes) ersetzt werden kann, während das enthaltende Paket aktiviert ist. Beispielsweise kann eine Lüfterkomponente so entworfen werden, dass sie hot-swaped ist. Alle Komponenten, die im Hot-Swap-System ausgetauscht werden können, sind grundsätzlich austauschbar und austauschbar.

Diese Eigenschaft wird von [**CIM \_ PhysicalComponent geerbt.**](cim-physicalcomponent.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Installationsdatum")
</dt> </dl>

Datum und Uhrzeit der Installation des Objekts. Diese Eigenschaft benötigt keinen Wert, um anzugeben, dass das Objekt installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**InterleavePosition**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device Mapped Addresses \| 001.7")
</dt> </dl>

Position des physischen Speichers in einer Verwebung. Der Wert 0 gibt an, dass nicht verwebt ist, 1 die erste Position, 2 die zweite Position und so weiter. Bei einem 2:1-Interleave gibt der Wert 1 beispielsweise an, dass sich der Arbeitsspeicher an der gleichmäßigen Position befindet.

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

**MemoryType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|DMTF-Speichergerät \| 002.9")
</dt> </dl>

Typ des physischen Speichers.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

**DRAM** (2)


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

**Synchrones DRAM** (3)


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

**Cache-DRAM** (4)


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

**EDO** (5)


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

**EDRAM** (6)


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

**VRAM** (7)


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

**SRAM** (8)


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

**RAM** (9)


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

**ROM** (10)


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

**Flash** (11)


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

**EEPROM** (12)


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

**FEPROM** (13)


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

**EPROM** (14)


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

**CDRAM** (15)


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

**3DRAM** (16)


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

**SDRAM** (17)


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

**SGRAM** (18)


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

**RDRAM** (19)


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

**DDR** (20)


</dt> <dd></dd> <dt>

<span id="DDR2"></span><span id="ddr2"></span>

**DDR2** (21)


</dt> <dd></dd> <dt>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>

**DDR2 FB-DIM** (22)


</dt> <dd></dd> </dl>

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

Zusätzliche Daten, die über Assettaginformationen hinausgehen und zum Identifizieren eines physischen Elements verwendet werden können. Ein Beispiel sind Balkencodedaten, die einem Element zugeordnet sind, das ebenfalls über ein Assettag verfügt. Beachten Sie, dass diese Eigenschaft NULL und die Barcodedaten als Klassenschlüssel in der **Tag-Eigenschaft** verwendet werden, wenn nur Balkencodedaten verfügbar sind und eindeutig sind und als Elementschlüssel verwendet werden können. Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**PartNumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Teilenummer, die von der Organisation zugewiesen wurde, die das physische Element erstellt oder hergestellt hat.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**PositionInRow**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device Mapped Addresses \| 001.6")
</dt> </dl>

Position des physischen Speichers in einer Zeile. Wenn beispielsweise zwei 8-Bit-Speichergeräte eine 16-Bit-Zeile bilden, gibt der Wert 2 an, dass der Arbeitsspeicher das zweite Gerät ist. Der Wert 0 ist ein ungültiger Wert für diese Eigenschaft.

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

True **gibt** an, dass dieses Element so konzipiert ist, dass es in den physischen Container aufgenommen und aus ihm herausgenommen wird, in dem es sich normalerweise befindet, ohne die Funktion der Gesamtpaketierung zu beeinträchtigen. Ein Paket gilt auch dann als wechselbar, wenn die Stromversorgung ausgeschaltet sein muss, um das Entfernen durchzuführen. Wenn die Stromversorgung ein- und das Paket entfernt werden kann, ist das Element wechselbar und kann mit dem Heißen getauscht werden. Beispielsweise ist ein nicht erweiterbarer Prozessorchip wechselbar.

Diese Eigenschaft wird von [**CIM \_ PhysicalComponent geerbt.**](cim-physicalcomponent.md)

</dd> <dt>

**Austauschbare**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True **gibt** an, dass das Element durch ein physisch anderes ersetzt werden kann. Einige Computersysteme ermöglichen z. B. das Upgrade des Hauptprozessorchips auf eine der höheren Taktwerte. In diesem Fall wird der Prozessor als ersetzbar bezeichnet. Alle Wechselkomponenten sind grundsätzlich austauschbar.

Diese Eigenschaft wird von [**CIM \_ PhysicalComponent geerbt.**](cim-physicalcomponent.md)

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

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Lagereinheitsnummer für das physische Element.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**Geschwindigkeit**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nanosekunden")
</dt> </dl>

Geschwindigkeit des physischen Speichers in Nanosekunden.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Aktueller Status des Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

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

**Wird** gestartet ("Wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Wird beendet** ("Wird beendet")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Dienst** ("Dienst")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Striche** ("Strich")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** ("Kein Kontakt")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Lost Comm** ("Lost Comm")


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

Eine beliebige Zeichenfolge, die das physische Element eindeutig identifiziert und als Schlüssel des Elements dient. Diese Eigenschaft kann Informationen enthalten, z. B. Assettag- oder Seriennummerdaten. Der Schlüssel für [**CIM \_ PhysicalElement**](cim-physicalelement.md) wird in der Objekthierarchie sehr hoch platziert, um die Hardware oder Entität unabhängig von der physischen Platzierung in (oder auf) Schränken, Adaptern und so weiter zu identifizieren. Beispielsweise kann eine Wechselkomponente, die im Hot-Swap-Tausch verwendet werden kann, aus dem enthaltenden Paket (Bereichspaket) übernommen und vorübergehend nicht verwendet werden. Das Objekt ist weiterhin vorhanden und kann sogar in einen anderen Bereichscontainer eingefügt werden. Der Schlüssel für ein physisches Element ist eine beliebige Zeichenfolge, die unabhängig von der Platzierung oder standortorientierten Hierarchie definiert wird.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**TotalWidth**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|DMTF-Speichergerät \| 002.7"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")
</dt> </dl>

Gesamtbreite des physischen Speichers in Bits, einschließlich Prüf- oder Fehlerkorrekturbits. Wenn keine Fehlerkorrekturbits angegeben sind, sollte der Wert in dieser Eigenschaft mit dem wert übereinstimmen, der für die **DataWidth-Eigenschaft angegeben** ist.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Version des physischen Elements.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ PhysicalMemory-Klasse** wird von [**CIM Chip \_ abgeleitet.**](cim-chip.md)

WMI implementiert diese Klasse nicht. Informationen zu WMI-Klassen, die **von CIM \_ PhysicalMemory abgeleitet sind,** finden Sie unter [Win32-Klassen](win32-provider.md).

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden. Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.

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

[**\_CIM-Chip**](cim-chip.md)
</dt> </dl>

 

