---
description: Die Abstraktion eines Ports oder Verbindungs Punkts eines Geräts.
ms.assetid: ee725c64-587b-4e5f-9b1c-7a58902b0631
title: CIM_LogicalPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalPort
- CIM_LogicalPort.Speed
- CIM_LogicalPort.MaxSpeed
- CIM_LogicalPort.RequestedSpeed
- CIM_LogicalPort.UsageRestriction
- CIM_LogicalPort.PortType
- CIM_LogicalPort.OtherPortType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: eeed69e9669048377340cb0ca21e7a2e89f4baff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958685"
---
# <a name="cim_logicalport-class"></a>CIM \_ logicalport-Klasse

Die Abstraktion eines Ports oder Verbindungs Punkts eines Geräts.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_LogicalPort : CIM_LogicalDevice
{
  uint64 Speed;
  uint64 MaxSpeed;
  uint64 RequestedSpeed;
  uint16 UsageRestriction;
  uint16 PortType;
  string OtherPortType;
};
```

## <a name="members"></a>Member

Die **CIM \_ logicalport** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ logicalport** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**MAXSPEED**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde"), **Punit** ("Bit/Sekunde")
</dt> </dl>

Die maximale Bandbreite des Ports (in Bits pro Sekunde).

</dd> <dt>

**Otherporttype**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ logicalport**".**PortType**")
</dt> </dl>

Beschreibt den Modultyp, wenn " **portType** " auf " **other** " ("1") festgelegt ist.

</dd> <dt>

**PortType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ networkport**](cim-networkport.md)".**Othernetworkporttype**")
</dt> </dl>

Der Porttyp.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Nicht zutreffend** (2)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (3.. 15999)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Anbieter reserviert** (16000.65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**RequestedSpeed**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ logicalport**".**Geschwindigkeit**"), **Punit** (" Bit/Sekunde ")
</dt> </dl>

Die angeforderte Bandbreite des Ports (in Bits pro Sekunde). Die tatsächliche Bandbreite wird in der Eigenschaft **Geschwindigkeit** gemeldet.

</dd> <dt>

**Geschwindigkeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde"), **Punit** ("Bit/Sekunde")
</dt> </dl>

Die Bandbreite des Ports (in Bits pro Sekunde).

</dd> <dt>

**Einsatz Einschränkung**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Port auf einen Front-End-oder Back-End-Port beschränkt ist.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>

**Nur Front-End** (2)


</dt> <dd></dd> <dt>

<span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>

**Nur Back-End** (3)


</dt> <dd></dd> <dt>

<span id="Not_restricted"></span><span id="not_restricted"></span><span id="NOT_RESTRICTED"></span>

**Nicht eingeschränkt** (4)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

