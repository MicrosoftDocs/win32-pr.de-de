---
description: Die CIM- \_ Slot-Klasse stellt Connectors dar, in die Pakete eingefügt werden.
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
ms.openlocfilehash: 73a63c8cd200096aa132d8205691669d765e54f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483830"
---
# <a name="cim_slot-class"></a>CIM- \_ Slot-Klasse

Die **CIM- \_ Slot** -Klasse stellt Connectors dar, in die Pakete eingefügt werden. Beispielsweise kann ein physisches Paket, das ein Laufwerk ist, in einen SCA-Slot eingefügt werden, oder eine Karte (eine Unterklasse von [CIM \_ physicalpackage](cim-physicalpackage.md)) kann in einen 16-, 32-oder 64-Bit-Erweiterungs Slot auf einem hostingboard eingefügt werden. PCI-oder PCMCIA-Typ-III-Slots sind Beispiele für letztere.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **CIM- \_ Slot** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ Slot** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Kurze Textbeschreibung des-Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Connectoriout**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine frei Form Zeichenfolge, die die PIN-Konfiguration und die Signal Verwendung eines physischen Verbindungs Zeichens beschreibt.

Diese Eigenschaft wird von [**CIM \_ physicalconnector**](cim-physicalconnector.md)geerbt.

</dd> <dt>

**Connector Type**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Connector Type"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Slot \| 004,2 ")
</dt> </dl>

Typ des physischen Verbindungs Typs. Ein Array wird angegeben, um die Beschreibung von Kombinationen aus Connector-Informationen zuzulassen. Beispielsweise könnte ein Array Eintrag RS-232, eine andere DB-25 und ein drittes den Connector als "männlich" definieren.

Diese Eigenschaft wird von [**CIM \_ physicalconnector**](cim-physicalconnector.md)geerbt.

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

Nicht geschirmten

</dd> <dt>

6
</dt> <dd>

SCSI (A) hohe Dichte (50 Pins)

</dd> <dt>

7
</dt> <dd>

SCSI (A) niedrige Dichte (50 Pins)

</dd> <dt>

8
</dt> <dd>

SCSI (P) High-Density (68 Pins)

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

SCSI-Fibre Channel SCA-II (40 Pins)

</dd> <dt>

14
</dt> <dd>

SCSI-Fibre Channel SCA-II (20 Pins)

</dd> <dt>

15
</dt> <dd>

SCSI-Fibre Channel BNC

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

V. 35

</dd> <dt>

31
</dt> <dd>

X. 21

</dd> <dt>

32
</dt> <dd>

IEEE-488

</dd> <dt>

33
</dt> <dd>

AUI

</dd> <dt>

34
</dt> <dd>

UTP Kategorie 3

</dd> <dt>

35
</dt> <dd>

UTP Kategorie 4

</dd> <dt>

36
</dt> <dd>

UTP Kategorie 5

</dd> <dt>

37
</dt> <dd>

BNC

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

Fiber-MIC

</dd> <dt>

41
</dt> <dd>

Apple AUI

</dd> <dt>

42
</dt> <dd>

Apple-GeoPort

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

EISA

</dd> <dt>

46
</dt> <dd>

VESA

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

CardBus

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

HIPPI

</dd> <dt>

56
</dt> <dd>

HSSDC (6 Pins)

</dd> <dt>

57
</dt> <dd>

GBIC

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

Access. Bus

</dd> <dt>

65
</dt> <dd>

NuBus

</dd> <dt>

66
</dt> <dd>

Zentronik

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

ADB

</dd> <dt>

73
</dt> <dd>

AGP

</dd> <dt>

74
</dt> <dd>

VME-Bus

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

Platzhalter für proprietäre Prozessorkarte

</dd> <dt>

78
</dt> <dd>

Eigener Speicherkarten Slot

</dd> <dt>

79
</dt> <dd>

Eigener e/a-Riser-Slot

</dd> <dt>

80
</dt> <dd>

PCI-66MHz

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

PC-98-hireso

</dd> <dt>

85
</dt> <dd>

PC-H98

</dd> <dt>

86
</dt> <dd>

PC-98note

</dd> <dt>

87
</dt> <dd>

PC-98full

</dd> <dt>

88
</dt> <dd>

SSE SCSI

</dd> <dt>

89
</dt> <dd>

Kreisförmig

</dd> <dt>

90
</dt> <dd>

On-board-IDE-Connector

</dd> <dt>

91
</dt> <dd>

Auf dem Disketten Verbinder

</dd> <dt>

92
</dt> <dd>

9 Dual Inline anheften

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

Mini Jack

</dd> <dt>

98
</dt> <dd>

PCI-X

</dd> <dt>

99
</dt> <dd>

SBus IEEE 1396-1993 32 Bit

</dd> <dt>

100
</dt> <dd>

SBus IEEE 1396-1993 64 Bit

</dd> <dt>

101
</dt> <dd>

MCA

</dd> <dt>

102
</dt> <dd>

Sant

</dd> <dt>

103
</dt> <dd>

XIO

</dd> <dt>

104
</dt> <dd>

HI

</dd> <dt>

105
</dt> <dd>

Ngio

</dd> <dt>

106
</dt> <dd>

PMC

</dd> <dt>

107
</dt> <dd>

MTRJ

</dd> <dt>

108
</dt> <dd>

VF-45

</dd> <dt>

109
</dt> <dd>

Zukünftige e/a-Vorgänge

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

Optical

</dd> <dt>

114
</dt> <dd>

Menüband

</dd> <dt>

115
</dt> <dd>

GLM

</dd> <dt>

116
</dt> <dd>

1x9

</dd> <dt>

117
</dt> <dd>

Mini-SG

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

VHDCI abgeschirmt (68 Pins)

</dd> <dt>

121
</dt> <dd>

InfiniBand

</dd> </dl>

</dd> <dt>

**"Name der Klassenname"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird. Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Die Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Erhöht**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")
</dt> </dl>

Maximale Höhe einer Adapterkarte in Zoll, die in den Slot eingefügt werden kann.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")
</dt> </dl>

Datum und Uhrzeit der Installation des-Objekts. Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Verlängert**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")
</dt> </dl>

Maximale Länge in Zoll einer Adapterkarte, die in den Slot eingefügt werden kann.

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Die Organisation, die das physische Element erzeugt hat. Weitere Informationen finden Sie unter der **Hersteller** Eigenschaft des [**CIM- \_ Produkts**](cim-product.md).

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**MaxDataWidth**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Slot \| 004,3 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bits ")
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

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Der Name, mit dem das physische Element allgemein bekannt ist.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Die Bezeichnung, nach der das-Objekt bekannt ist. Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Number**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die physische Slot-Nummer, die als Index in einer System Slot-Tabelle verwendet werden kann, um zu bestimmen, ob der Slot physisch besetzt ist.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zusätzliche Daten, über die Informationen zu Asset-Tags hinausgehen, die zum Identifizieren eines physischen Elements verwendet werden können. Ein Beispiel hierfür sind Barcode Daten, die einem Element zugeordnet sind, das ebenfalls über ein Bestands Kennzeichen verfügt. Beachten Sie Folgendes: Wenn nur Barcode Daten verfügbar sind und eindeutig sind und als Element Schlüssel verwendet werden können, ist diese Eigenschaft NULL, und die Barcode Daten werden als Klassen Schlüssel in der **Tag** -Eigenschaft verwendet.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**PartNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Die Teilenummer, die von der Organisation zugewiesen wurde, die das physische Element erstellt oder hergestellt hat.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

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

**Zweck Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Slot**.**SpecialPurpose**")
</dt> </dl>

Frei Form Zeichenfolge, die beschreibt, wie dieser Slot physisch eindeutig ist und dass er spezielle Hardwaretypen enthalten kann. Diese Eigenschaft hat nur Bedeutung, wenn die entsprechende boolesche **SpecialPurpose** -Eigenschaft auf **true** festgelegt ist.

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Vom Hersteller zugewiesene Nummer, mit der das physische Element identifiziert wird.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Die Stock Keeping Unit-Nummer für das physische Element.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Specialzweck**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Slot**.**Zweck Beschreibung**")
</dt> </dl>

**True** gibt an, dass der Slot physisch eindeutig ist und spezielle Hardwaretypen (z. b. einen Grafikprozessor Slot) enthalten kann. **True** gibt an, dass die Eigenschaft " **zieldescription** " angeben soll, wie der Slot eindeutig oder der Zweck des Slots ist.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Aktueller Status des Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

Folgende Werte sind gültig:

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

**Supportshotplug**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass der Slot das Hot-Plugging von Adapterkarten unterstützt.

</dd> <dt>

**Tag**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Eine beliebige Zeichenfolge, die das physische Element eindeutig identifiziert und als Schlüssel des Elements fungiert. Diese Eigenschaft kann Informationen enthalten, z. b. Daten zu Bestands Kennzeichen oder Seriennummer. Der Schlüssel für [**CIM \_ PhysicalElement**](cim-physicalelement.md) wird in der Objekthierarchie sehr hoch platziert, um die Hardware/Entität unabhängig von der physischen Platzierung in (oder in) Schränken, Adaptern usw. unabhängig voneinander zu identifizieren. Beispielsweise kann eine Wechsel Komponente, für die ein ausgetauschte Vorgang ausgeführt werden kann, aus dem enthaltenden (Bereichs bezogenen) Paket entnommen und vorübergehend nicht verwendet werden. Das Objekt bleibt weiterhin vorhanden und kann sogar in einen anderen Bereichs Container eingefügt werden. Der Schlüssel für ein physisches Element ist eine beliebige Zeichenfolge, die unabhängig von der Platzierung oder der Speicherort orientierten Hierarchie definiert wird.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Theritäts Bewertung**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Slot \| 004,11 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Milliwatt ")
</dt> </dl>

Maximale thermische Unterschiede des Slots in Milliwatt.

</dd> <dt>

**Vccmixedvoltagesupport**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Slot \| 004,9 ")
</dt> </dl>

VCC-Spannung wird vom Slot unterstützt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

**3.3 v** (2)


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

**5V** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Version des physischen Elements.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Vppmixedvoltagesupport**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Slot \| 004,10 ")
</dt> </dl>

VPP-Spannung wird vom Slot unterstützt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

**3.3 v** (2)


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

**5V** (3)


</dt> <dd></dd> <dt>

<span id="12V"></span><span id="12v"></span>

**12V** (4)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **CIM- \_ Slot** -Klasse wird von [**CIM \_ physicalconnector**](cim-physicalconnector.md)abgeleitet.

Diese Klasse wird von WMI nicht implementiert. Informationen zu WMI-Klassen, die vom **CIM- \_ Slot** abgeleitet sind, finden Sie unter [Win32](win32-provider.md)

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

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

[**CIM \_ physicalconnector**](cim-physicalconnector.md)
</dt> </dl>

 

