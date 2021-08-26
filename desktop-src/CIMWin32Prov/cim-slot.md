---
description: Die CIM \_ Slot-Klasse stellt Connectors dar, in die Pakete eingefügt werden.
ms.assetid: bcb1bdb5-fb1a-47ed-9450-dca38edca0eb
ms.tgt_platform: multiple
title: CIM_Slot-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Slot
- CIM_Slot.Caption
- CIM_Slot.ConnectorPinout
- CIM_Slot.ConnectorType
- CIM_Slot.CreationClassName
- CIM_Slot.Description
- CIM_Slot.HeightAllowed
- CIM_Slot.InstallDate
- CIM_Slot.LengthAllowed
- CIM_Slot.Manufacturer
- CIM_Slot.MaxDataWidth
- CIM_Slot.Model
- CIM_Slot.Name
- CIM_Slot.Number
- CIM_Slot.OtherIdentifyingInfo
- CIM_Slot.PartNumber
- CIM_Slot.PoweredOn
- CIM_Slot.PurposeDescription
- CIM_Slot.SerialNumber
- CIM_Slot.SKU
- CIM_Slot.SpecialPurpose
- CIM_Slot.Status
- CIM_Slot.SupportsHotPlug
- CIM_Slot.Tag
- CIM_Slot.ThermalRating
- CIM_Slot.VccMixedVoltageSupport
- CIM_Slot.Version
- CIM_Slot.VppMixedVoltageSupport
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 910fb4a3dcd5d3d95ef524d838781bad8331d33d71fc0af8ebd358ac9dd9588e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919460"
---
# <a name="cim_slot-class"></a>CIM \_ Slot-Klasse

Die **CIM \_ Slot-Klasse** stellt Connectors dar, in die Pakete eingefügt werden. Beispielsweise kann ein physisches Paket, das ein Laufwerk ist, in einen SCA-Slot eingefügt werden, oder eine Karte (eine Unterklasse von [CIM \_ PhysicalPackage](cim-physicalpackage.md)) kann in einen 16-, 32- oder 64-Bit-Erweiterungsslot auf einem Hostingboard eingefügt werden. PCI- oder PCMCIA-Slots vom Typ III sind Beispiele für Letzteres.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird aus Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[abstract, UUID("{FAF76B86-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Slot : CIM_PhysicalConnector
{
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  string   Description;
  real32   HeightAllowed;
  datetime InstallDate;
  real32   LengthAllowed;
  string   Manufacturer;
  uint16   MaxDataWidth;
  string   Model;
  string   Name;
  uint16   Number;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   PurposeDescription;
  string   SerialNumber;
  string   SKU;
  boolean  SpecialPurpose;
  string   Status;
  boolean  SupportsHotPlug;
  string   Tag;
  uint32   ThermalRating;
  uint16   VccMixedVoltageSupport[];
  string   Version;
  uint16   VppMixedVoltageSupport[];
};
```

## <a name="members"></a>Member

Die **CIM \_ Slot-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ Slot-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Kurze Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**ConnectorPinout**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Freiformzeichenfolge, die die Pinkonfiguration und Signalverwendung eines physischen Connectors beschreibt.

Diese Eigenschaft wird von [**CIM \_ PhysicalConnector**](cim-physicalconnector.md)geerbt.

</dd> <dt>

**Connectortype**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("ConnectorType"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|DMTF-Systemslot \| 004.2")
</dt> </dl>

Typ des physischen Connectors. Ein Array wird angegeben, um die Beschreibung von Kombinationen von Connectorinformationen zu ermöglichen. Beispielsweise könnte ein Arrayeintrag RS-232, ein anderer DB-25 und ein dritter den Connector als "Male" definieren.

Diese Eigenschaft wird von [**CIM \_ PhysicalConnector**](cim-physicalconnector.md)geerbt.

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

Male

</dd> <dt>

3
</dt> <dd>

Female

</dd> <dt>

4
</dt> <dd>

Geschützt

</dd> <dt>

5
</dt> <dd>

Ungeschirmt

</dd> <dt>

6
</dt> <dd>

Hohe Dichte von SCSI (A) (50 Pins)

</dd> <dt>

7
</dt> <dd>

SCSI (A) niedrige Dichte (50 Pins)

</dd> <dt>

8
</dt> <dd>

Hohe Dichte von SCSI (P) (68 Pins)

</dd> <dt>

9
</dt> <dd>

SCSI SCA-I (80 Pins)

</dd> <dt>

10
</dt> <dd>

SCSI SCA-II (80 Pins)

</dd> <dt>

11
</dt> <dd>

SCSI-Fibre Channel (DB-9, Kupfer)

</dd> <dt>

12
</dt> <dd>

SCSI-Fibre Channel (Fibre)

</dd> <dt>

13
</dt> <dd>

SCSI Fibre Channel SCA-II (40 Pins)

</dd> <dt>

14
</dt> <dd>

SCSI Fibre Channel SCA-II (20 Pins)

</dd> <dt>

15
</dt> <dd>

SCSI Fibre Channel BNC

</dd> <dt>

16
</dt> <dd>

ATA 3-1/2 Zoll (40 Pins)

</dd> <dt>

17
</dt> <dd>

ATA 2-1/2 Zoll (44 Pins)

</dd> <dt>

18
</dt> <dd>

ATA-2

</dd> <dt>

19
</dt> <dd>

ATA-3

</dd> <dt>

20
</dt> <dd>

ATA/66

</dd> <dt>

21
</dt> <dd>

DB-9

</dd> <dt>

22
</dt> <dd>

DB-15

</dd> <dt>

23
</dt> <dd>

DB-25

</dd> <dt>

24
</dt> <dd>

DB-36

</dd> <dt>

25
</dt> <dd>

RS-232C

</dd> <dt>

26
</dt> <dd>

RS-422

</dd> <dt>

27
</dt> <dd>

RS-423

</dd> <dt>

28
</dt> <dd>

RS-485

</dd> <dt>

29
</dt> <dd>

RS-449

</dd> <dt>

30
</dt> <dd>

V.35

</dd> <dt>

31
</dt> <dd>

X.21

</dd> <dt>

32
</dt> <dd>

IEEE-488

</dd> <dt>

33
</dt> <dd>

Aui

</dd> <dt>

34
</dt> <dd>

UTP-Kategorie 3

</dd> <dt>

35
</dt> <dd>

UTP-Kategorie 4

</dd> <dt>

36
</dt> <dd>

UTP-Kategorie 5

</dd> <dt>

37
</dt> <dd>

Bnc

</dd> <dt>

38
</dt> <dd>

RJ11

</dd> <dt>

39
</dt> <dd>

RJ45

</dd> <dt>

40
</dt> <dd>

Fiber MIC

</dd> <dt>

41
</dt> <dd>

Apple AUI

</dd> <dt>

42
</dt> <dd>

Apple GeoPort

</dd> <dt>

43
</dt> <dd>

PCI

</dd> <dt>

44
</dt> <dd>

ISA

</dd> <dt>

45
</dt> <dd>

Eisa

</dd> <dt>

46
</dt> <dd>

Vesa

</dd> <dt>

47
</dt> <dd>

PCMCIA

</dd> <dt>

48
</dt> <dd>

PCMCIA-Typ I

</dd> <dt>

49
</dt> <dd>

PCMCIA-Typ II

</dd> <dt>

50
</dt> <dd>

PCMCIA-Typ III

</dd> <dt>

51
</dt> <dd>

ZV-Port

</dd> <dt>

52
</dt> <dd>

Cardbus

</dd> <dt>

53
</dt> <dd>

USB

</dd> <dt>

54
</dt> <dd>

IEEE 1394

</dd> <dt>

55
</dt> <dd>

Hippi

</dd> <dt>

56
</dt> <dd>

HSSDC (6 Pins)

</dd> <dt>

57
</dt> <dd>

Gbic

</dd> <dt>

58
</dt> <dd>

DIN

</dd> <dt>

59
</dt> <dd>

Mini-DIN

</dd> <dt>

60
</dt> <dd>

Micro-DIN

</dd> <dt>

61
</dt> <dd>

PS/2

</dd> <dt>

62
</dt> <dd>

Infrarot

</dd> <dt>

63
</dt> <dd>

HP-HIL

</dd> <dt>

64
</dt> <dd>

Access.bus

</dd> <dt>

65
</dt> <dd>

NuBus

</dd> <dt>

66
</dt> <dd>

Centronics

</dd> <dt>

67
</dt> <dd>

Mini-Centronics

</dd> <dt>

68
</dt> <dd>

Mini-Centronics Typ-14

</dd> <dt>

69
</dt> <dd>

Mini-Centronics Typ-20

</dd> <dt>

70
</dt> <dd>

Mini-Centronics Typ-26

</dd> <dt>

71
</dt> <dd>

Busmaus

</dd> <dt>

72
</dt> <dd>

Adb

</dd> <dt>

73
</dt> <dd>

Agp

</dd> <dt>

74
</dt> <dd>

VME Bus

</dd> <dt>

75
</dt> <dd>

VME64

</dd> <dt>

76
</dt> <dd>

Proprietär

</dd> <dt>

77
</dt> <dd>

Proprietärer Prozessorkartenslot

</dd> <dt>

78
</dt> <dd>

Proprietärer Speicherkartenslot

</dd> <dt>

79
</dt> <dd>

Proprietärer E/A-Riser-Slot

</dd> <dt>

80
</dt> <dd>

PCI-66 MHZ

</dd> <dt>

81
</dt> <dd>

AGP2X

</dd> <dt>

82
</dt> <dd>

AGP4X

</dd> <dt>

83
</dt> <dd>

PC-98

</dd> <dt>

84
</dt> <dd>

PC-98-Hireso

</dd> <dt>

85
</dt> <dd>

PC-H98

</dd> <dt>

86
</dt> <dd>

PC-98Hinweis

</dd> <dt>

87
</dt> <dd>

PC-98Full

</dd> <dt>

88
</dt> <dd>

SSA SCSI

</dd> <dt>

89
</dt> <dd>

Kreisförmig

</dd> <dt>

90
</dt> <dd>

On Board-IDE-Connector

</dd> <dt>

91
</dt> <dd>

On Board Floppy Connector

</dd> <dt>

92
</dt> <dd>

9 Pin Dual Inline

</dd> <dt>

93
</dt> <dd>

25 Pin Dual Inline

</dd> <dt>

94
</dt> <dd>

50 Pin Dual Inline

</dd> <dt>

95
</dt> <dd>

68 Pin Dual Inline

</dd> <dt>

96
</dt> <dd>

On Board Sound Connector

</dd> <dt>

97
</dt> <dd>

Mini-Jack

</dd> <dt>

98
</dt> <dd>

PCI-X

</dd> <dt>

99
</dt> <dd>

Sbus IEEE 1396-1993 32 Bit

</dd> <dt>

100
</dt> <dd>

Sbus IEEE 1396-1993 64 Bit

</dd> <dt>

101
</dt> <dd>

MCA

</dd> <dt>

102
</dt> <dd>

Gio

</dd> <dt>

103
</dt> <dd>

XIO

</dd> <dt>

104
</dt> <dd>

HIO

</dd> <dt>

105
</dt> <dd>

N WIEGE

</dd> <dt>

106
</dt> <dd>

PMC

</dd> <dt>

107
</dt> <dd>

Mtrj

</dd> <dt>

108
</dt> <dd>

VF-45

</dd> <dt>

109
</dt> <dd>

Zukünftige E/A

</dd> <dt>

110
</dt> <dd>

SC

</dd> <dt>

111
</dt> <dd>

SG

</dd> <dt>

112
</dt> <dd>

Electrical

</dd> <dt>

113
</dt> <dd>

Optische

</dd> <dt>

114
</dt> <dd>

Menüband

</dd> <dt>

115
</dt> <dd>

Glm

</dd> <dt>

116
</dt> <dd>

1x9

</dd> <dt>

117
</dt> <dd>

Mini SG

</dd> <dt>

118
</dt> <dd>

LC

</dd> <dt>

119
</dt> <dd>

HSSC

</dd> <dt>

120
</dt> <dd>

VHDCI Shielded (68 Pins)

</dd> <dt>

121
</dt> <dd>

InfiniBand

</dd> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**\_ CIM-Schlüssel,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird. Bei Verwendung mit anderen Schlüsseleigenschaften der -Klasse ermöglicht diese Eigenschaft, dass alle Instanzen der Klasse und deren Unterklassen eindeutig identifiziert werden.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**HeightAllowed**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")
</dt> </dl>

Maximale Höhe (in Zoll) einer Adapterkarte, die in den Slot eingefügt werden kann.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Installation date")
</dt> </dl>

Datum und Uhrzeit der Installation des Objekts. Diese Eigenschaft benötigt keinen Wert, um anzugeben, dass das Objekt installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**LengthAllowed**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")
</dt> </dl>

Maximale Länge (in Zoll) einer Adapterkarte, die in den Slot eingefügt werden kann.

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Organisation, die das physische Element erzeugt hat. Weitere Informationen finden Sie unter der **Vendor-Eigenschaft** von [**CIM \_ Product**](cim-product.md).

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**MaxDataWidth**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|DMTF-Systemslot \| 004.3"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")
</dt> </dl>

Maximale Busbreite von Adapterkarten in Bits, die in den Slot eingefügt werden können.

<dt>

<span id="8"></span>

**8** (0)


</dt> <dd></dd> <dt>

<span id="16"></span>

**16** (1)


</dt> <dd></dd> <dt>

<span id="32"></span>

**32** (2)


</dt> <dd></dd> <dt>

<span id="64"></span>

**64** (3)


</dt> <dd></dd> <dt>

<span id="128"></span>

**128** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**Modell**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
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

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Bezeichnung, unter der das Objekt bekannt ist. Bei Unterklassen kann diese Eigenschaft überschrieben werden, um eine Schlüsseleigenschaft zu sein.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**Number**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Physische Slotnummer, die als Index in einer Systemslottabelle verwendet werden kann, um zu bestimmen, ob der Slot physisch belegt ist.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zusätzliche Daten, die über Assettaginformationen hinausgehen und zum Identifizieren eines physischen Elements verwendet werden können. Ein Beispiel sind Balkencodedaten, die einem Element zugeordnet sind, das ebenfalls über ein Assettag verfügt. Beachten Sie, dass diese Eigenschaft NULL und die Barcodedaten als Klassenschlüssel in der **Tag-Eigenschaft** verwendet werden, wenn nur Balkencodedaten verfügbar sind und eindeutig sind und als Elementschlüssel verwendet werden können.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**PartNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Teilenummer, die von der Organisation zugewiesen wurde, die das physische Element erstellt oder hergestellt hat.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

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

**PurposeDescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ CIM-Slot**.**SpecialPurpose**")
</dt> </dl>

Freiformzeichenfolge, die beschreibt, wie dieser Slot physisch eindeutig ist und spezielle Hardwaretypen enthalten kann. Diese Eigenschaft hat nur dann eine Bedeutung, wenn die entsprechende **boolesche SpecialPurpose-Eigenschaft** auf **TRUE festgelegt ist.**

</dd> <dt>

**Serialnumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
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

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Lagereinheitsnummer für das physische Element.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**SpecialPurpose**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ CIM-Slot**.**PurposeDescription**")
</dt> </dl>

True **gibt an,** dass der Slot physisch eindeutig ist und möglicherweise spezielle Hardwaretypen (z. B. einen Grafikprozessorslot) enthalten kann. True **gibt** an, **dass die PurposeDescription-Eigenschaft** angeben sollte, wie der Slot eindeutig oder der Zweck des Slots ist.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
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

**SupportsHotPlug**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True gibt an, dass der Slot das Hot-Plugging von Adapterkarten unterstützt.

</dd> <dt>

**Tag**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**\_ CIM-Schlüssel,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Beliebige Zeichenfolge, die das physische Element eindeutig identifiziert und als Schlüssel des Elements dient. Diese Eigenschaft kann Informationen enthalten, z. B. Assettag- oder Seriennummerndaten. Der Schlüssel für [**CIM \_ PhysicalElement**](cim-physicalelement.md) wird sehr hoch in der Objekthierarchie platziert, um die Hardware/Entität unabhängig von der physischen Platzierung in (oder in) Schränken, Adaptern usw. zu identifizieren. Beispielsweise kann eine Wechselkomponente, die im laufenden Betrieb ausgetauscht werden kann, aus dem enthaltenden Paket (Bereichspaket) entnommen und vorübergehend nicht verwendet werden. Das Objekt ist weiterhin vorhanden und kann sogar in einen anderen Bereichscontainer eingefügt werden. Der Schlüssel für ein physisches Element ist eine beliebige Zeichenfolge, die unabhängig von der Platzierung oder der standortorientierten Hierarchie definiert ist.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Thermerating**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|DMTF-Systemslot \| 004.11"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Milliwatts")
</dt> </dl>

Maximale wärmerische Dissipation des Slots in Milliwatts.

</dd> <dt>

**VccMixedVoltageSupport**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|DMTF-Systemslot \| 004.9")
</dt> </dl>

Vom Slot unterstützte VCC-Stromversorgung.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Andere** (1)


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

**3,3 V** (2)


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

**5V** (3)


</dt> <dd></dd> </dl>

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

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**VppMixedVoltageSupport**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|DMTF-Systemslot \| 004.10")
</dt> </dl>

VPP-Stromversorgung, die vom Slot unterstützt wird.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Andere** (1)


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

**3,3 V** (2)


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

**5V** (3)


</dt> <dd></dd> <dt>

<span id="12V"></span><span id="12v"></span>

**12 V** (4)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ Slot-Klasse** wird von [**CIM \_ PhysicalConnector**](cim-physicalconnector.md)abgeleitet.

WMI implementiert diese Klasse nicht. Informationen zu WMI-Klassen, die vom **\_ CIM-Slot** abgeleitet werden, finden Sie unter [Win32-Klassen.](win32-provider.md)

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden. Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ PhysicalConnector**](cim-physicalconnector.md)
</dt> </dl>

 

