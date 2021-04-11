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
ms.openlocfilehash: 9e3ac64b55e17d0526527ebbaca168c3f7b289f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217815"
---
# <a name="cim_networkport-class"></a>CIM- \_ networkport-Klasse

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

Die **CIM- \_ networkport** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ networkport** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Activemaximumtransmissionunit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **Punit** ("Byte")
</dt> </dl>

Die aktive oder ausgehandelte maximale Übertragungseinheit (Maximum Transmission Unit, MTU), die vom Port unterstützt wird.

</dd> <dt>

**AutoSense**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**true** , wenn der Port die Geschwindigkeit oder andere Kommunikationsmerkmale der angeschlossenen Netzwerk Medien automatisch bestimmen kann. andernfalls **false**.

</dd> <dt>

**Vollduplex**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**true** , wenn der Port im Vollduplex Modus betrieben wird. andernfalls **false**.

</dd> <dt>

**Linktechnology**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ networkport**".**Otherlinktechnology**")
</dt> </dl>

Die vom Port verwendete Link Technologie. Wenn der Wert auf "1" festgelegt ist, enthält die **otherlinktechnology** -Eigenschaft eine Beschreibung des linktyps.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


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

**F-di** (5)


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

**ATM** (6)


</dt> <dd></dd> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

**TokenRing** (7)


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

**Frame Relay** (8)


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

**Infrarot** (9)


</dt> <dd></dd> <dt>

<span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>

**Bluetooth** (10)


</dt> <dd></dd> <dt>

<span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>

**Drahtlos LAN** (11)


</dt> <dd></dd> </dl>

</dd> <dt>

**"Networkaddresses"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Netzwerk Adapter 802-Port \| 001,3 ")
</dt> </dl>

Ein Array, das die Netzwerkadressen für den Port enthält.

</dd> <dt>

**Otherlinktechnology**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ networkport**".**Linktechnology**")
</dt> </dl>

Die Link Technologie, wenn **linktechnology** auf "1" festgelegt ist, (andere).

</dd> <dt>

**Othernetworkporttype**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM \_ networkport**.**Otherporttype**"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ logicalport**](cim-logicalport.md)".**PortType**")
</dt> </dl>

> [!Note]  
> Deprecated Description: der Modultyp des Ports, wenn die **portType** -Eigenschaft 1 (Sonstiges) enthält.

 

Diese Eigenschaft ist veraltet. Stattdessen empfehlen wir die **portType** -Eigenschaft in der [**CIM \_ logicalport**](cim-logicalport.md) -Klasse.

</dd> <dt>

**Permanent Address**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Netzwerk Adapter 802-Port \| 001,2 ")
</dt> </dl>

Die Netzwerkadresse, die in einem Port hart codiert ist. Die hart codierte Adresse kann mithilfe eines Firmwareupdates oder einer Softwarekonfiguration geändert werden. Wenn diese Änderung vorgenommen wird, sollte diese Eigenschaft gleichzeitig aktualisiert werden. " **Permanentaddress** " sollte leer gelassen werden, wenn die Adresse nicht vorhanden ist.

</dd> <dt>

**PortNumber**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Portnummer des Netzwerkports. Netzwerkports sind häufig in Bezug auf ein logisches Modul oder ein Netzwerkelement nummeriert.

</dd> <dt>

**Geschwindigkeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Geschwindigkeit"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| MIB-II. IfSpeed "," MIF. DMTF- \| Netzwerk Adapter 802 Port \| 001,5 "), **Punit** (" Bit/Sekunde ")
</dt> </dl>

Die aktuelle Bandbreite des Ports in Bits pro Sekunde. Für Ports, die die Bandbreite variieren, oder für diejenigen, bei denen keine genaue Schätzung vorgenommen werden kann, sollte diese Eigenschaft die nominale Bandbreite enthalten.

</dd> <dt>

**Supportedmaximumtransmissionunit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **Punit** ("Byte")
</dt> </dl>

Die vom Port unterstützte maximale Übertragungseinheit (MTU).

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

[**CIM \_ logicalport**](cim-logicalport.md)
</dt> </dl>

 

