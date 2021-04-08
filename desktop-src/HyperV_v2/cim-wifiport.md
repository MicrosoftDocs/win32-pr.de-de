---
description: Stellt ein Drahtlos Netzwerk Kommunikationsgerät dar, das der IEEE 802,11-Reihe von Spezifikationen entspricht.
ms.assetid: c4e3345f-5c7d-4d1d-9a94-64112d7334ff
title: CIM_WiFiPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_WiFiPort
- CIM_WiFiPort.Speed
- CIM_WiFiPort.MaxSpeed
- CIM_WiFiPort.PortType
- CIM_WiFiPort.PermanentAddress
- CIM_WiFiPort.NetworkAddresses
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 098bd0a3795f3e8e0531be5286a65b79d9f6ee0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865779"
---
# <a name="cim_wifiport-class"></a>CIM- \_ wifport-Klasse

Stellt ein Drahtlos Netzwerk Kommunikationsgerät dar, das der IEEE 802,11-Reihe von Spezifikationen entspricht.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_WiFiPort : CIM_NetworkPort
{
  uint64 Speed;
  uint64 MaxSpeed;
  uint16 PortType;
  string PermanentAddress;
  string NetworkAddresses[];
};
```

## <a name="members"></a>Member

Die **CIM- \_ wifport** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ wifport** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**MAXSPEED**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("MAXSPEED")
</dt> </dl>

Die maximal unterstützte Bandbreite in Bits pro Sekunde basierend auf dem Betriebsmodus, der in der **portType** -Eigenschaft angegeben ist. **MAXSPEED** ist beispielsweise "11 Millionen", wenn " **portType** " "71" (802.11 b) enthält.

</dd> <dt>

**"Networkaddresses"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Netzwerkadressen")
</dt> </dl>

Ein Array, das die IEEE 802 EUI-48 Mac-Adressen enthält. Die Mac-Adresse ist als zwölf hexadezimal Ziffern formatiert, wobei jedes Paar einen der sechs Oktette der Mac-Adresse in kanonischer bitreihenfolge darstellt.

</dd> <dt>

**Permanent Address**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Permanent Address")
</dt> </dl>

Die IEEE 802 EUI-48 Mac-Adresse des Ports. Die Mac-Adresse ist als zwölf hexadezimal Ziffern formatiert, wobei jedes Paar einen der sechs Oktette der Mac-Adresse in kanonischer bitreihenfolge darstellt.

</dd> <dt>

**PortType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")
</dt> </dl>

Der 802,11-Betriebsmodus, der auf dem Port aktiviert ist.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="802.11a"></span><span id="802.11A"></span>

**802.11 a** (70)


</dt> <dd></dd> <dt>

<span id="802.11b"></span><span id="802.11B"></span>

**802.11 b** (71)


</dt> <dd></dd> <dt>

<span id="802.11g"></span><span id="802.11G"></span>

**802.11 g** (72)


</dt> <dd></dd> <dt>

<span id="802.11n"></span><span id="802.11N"></span>

**802.11 n** (73)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Anbieter reserviert** (16000..)


</dt> <dd></dd> </dl>

</dd> <dt>

**Geschwindigkeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Geschwindigkeit")
</dt> </dl>

Die Datenrate, mit der die aktuelle ppdu-Protokolldaten Einheit (in Bits pro Sekunde) empfangen wurde. Dieser Wert wird in den ersten 4 Bits des plcp-Headers in jedem plcp-Frame codiert.

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

[**CIM- \_ Netzwerkport**](cim-networkport.md)
</dt> </dl>

 

