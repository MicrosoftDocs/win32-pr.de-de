---
description: Eine logische Darstellung eines Netzwerkports auf einem Netzwerkgerät.
ms.assetid: afcfc93d-174e-43b5-a16f-28937b4bf81a
title: CIM_NetworkPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkPort
- CIM_NetworkPort.Speed
- CIM_NetworkPort.OtherNetworkPortType
- CIM_NetworkPort.PortNumber
- CIM_NetworkPort.LinkTechnology
- CIM_NetworkPort.OtherLinkTechnology
- CIM_NetworkPort.PermanentAddress
- CIM_NetworkPort.NetworkAddresses
- CIM_NetworkPort.FullDuplex
- CIM_NetworkPort.AutoSense
- CIM_NetworkPort.SupportedMaximumTransmissionUnit
- CIM_NetworkPort.ActiveMaximumTransmissionUnit
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: aa69b2728f3d0cdb97bcc972ef6b72ab5bd0df3202df60e92f87e161ea9a1702
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694710"
---
# <a name="cim_networkport-class"></a>CIM \_ NetworkPort-Klasse

Eine logische Darstellung eines Netzwerkports auf einem Netzwerkgerät.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_NetworkPort : CIM_LogicalPort
{
  uint64  Speed;
  string  OtherNetworkPortType;
  uint16  PortNumber;
  uint16  LinkTechnology;
  string  OtherLinkTechnology;
  string  PermanentAddress;
  string  NetworkAddresses[];
  boolean FullDuplex;
  boolean AutoSense;
  uint64  SupportedMaximumTransmissionUnit;
  uint64  ActiveMaximumTransmissionUnit;
};
```

## <a name="members"></a>Member

Die **CIM \_ NetworkPort-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ NetworkPort-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ActiveMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("Byte")
</dt> </dl>

Die aktive oder ausgehandelte maximale Übertragungseinheit (MAXIMUM TRANSMISSION Unit, MTU), die vom Port unterstützt wird.

</dd> <dt>

**Autosense**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**TRUE,** wenn der Port automatisch die Geschwindigkeit oder ein anderes Kommunikationsmerkmal des angefügten Netzwerkmediums bestimmen kann; andernfalls **FALSE.**

</dd> <dt>

**FullDuplex**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**TRUE,** wenn der Port im Vollduplexmodus ausgeführt wird. andernfalls **FALSE.**

</dd> <dt>

**LinkTechnology**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ NetworkPort**.**OtherLinkTechnology**")
</dt> </dl>

Die vom Port verwendete Linktechnologie. Bei Festlegung auf "1" (other) enthält die **OtherLinkTechnology-Eigenschaft** eine Beschreibung des Linktyps.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Andere** (1)


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (2)


</dt> <dd></dd> <dt>

<span id="IB"></span><span id="ib"></span>

**IB** (3)


</dt> <dd></dd> <dt>

<span id="FC"></span><span id="fc"></span>

**FC** (4)


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

**FDDI** (5)


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

**ATM** (6)


</dt> <dd></dd> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

**Tokenring** (7)


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

**Frame Relay** (8)


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

**Wird** (9)


</dt> <dd></dd> <dt>

<span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>

**BlueTooth** (10)


</dt> <dd></dd> <dt>

<span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>

**Wlan** (11)


</dt> <dd></dd> </dl>

</dd> <dt>

**NetworkAddresses**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|DMTF-Netzwerkadapter 802 Port \| 001.3")
</dt> </dl>

Ein Array, das die Netzwerkadressen für den Port enthält.

</dd> <dt>

**OtherLinkTechnology**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ NetworkPort**.**LinkTechnology**")
</dt> </dl>

Die Linktechnologie, wenn **LinkTechnology** auf "1" (sonstige) festgelegt ist.

</dd> <dt>

**OtherNetworkPortType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM \_ NetworkPort**.**OtherPortType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalPort**](cim-logicalport.md).**PortType**")
</dt> </dl>

> [!Note]  
> Veraltete Beschreibung: Der Modultyp des Ports, wenn die **PortType-Eigenschaft** 1 (andere) enthält.

 

Diese Eigenschaft ist veraltet. Stattdessen wird die **PortType-Eigenschaft** in der [**CIM \_ LogicalPort-Klasse**](cim-logicalport.md) empfohlen.

</dd> <dt>

**PermanentAddress**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|DMTF-Netzwerkadapter 802 Port \| 001.2")
</dt> </dl>

Die Netzwerkadresse, die in einen Port hartcodiert ist. Die hartcodierte Adresse kann mithilfe eines Firmwareupgrades oder einer Softwarekonfiguration geändert werden. Wenn diese Änderung vorgenommen wird, sollte diese Eigenschaft gleichzeitig aktualisiert werden. **PermanentAddress** sollte leer gelassen werden, wenn die Adresse nicht vorhanden ist.

</dd> <dt>

**Portnumber**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Portnummer des Netzwerkports. Netzwerkports sind häufig relativ zu einem logischen Modul oder einem Netzwerkelement nummeriert.

</dd> <dt>

**Geschwindigkeit**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Geschwindigkeit"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| MIB-II.ifSpeed", "MIF. \|DMTF-Netzwerkadapter 802 Port \| 001.5"), **PUnit** ("bit/second")
</dt> </dl>

Die aktuelle Bandbreite des Ports in Bits pro Sekunde. Für Ports, die sich in der Bandbreite unterscheiden, oder für Ports, für die keine genaue Schätzung vorgenommen werden kann, sollte diese Eigenschaft die nominale Bandbreite enthalten.

</dd> <dt>

**SupportedMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("Byte")
</dt> </dl>

Die maximale Übertragungseinheit (MTU), die vom Port unterstützt wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ LogicalPort**](cim-logicalport.md)
</dt> </dl>

 

