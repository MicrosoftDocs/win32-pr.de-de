---
description: Diese Klasse ist die Ereignistypklasse für Netzwerkschnittstellenkarten-Konfigurationsereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 66b2c116-810e-489d-ad5e-f9c09902005b
title: SystemConfig_NIC-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_NIC
- SystemConfig_NIC.PhysicalAddr
- SystemConfig_NIC.PhysicalAddrLen
- SystemConfig_NIC.Ipv4Index
- SystemConfig_NIC.Ipv6Index
- SystemConfig_NIC.NICDescription
- SystemConfig_NIC.IpAddresses
- SystemConfig_NIC.DnsServerAddresses
api_type:
- NA
api_location: ''
ms.openlocfilehash: 822e8404137eee9731bbfcee9f5d9f4495609078c4251b53269371dd4904cea7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393816"
---
# <a name="systemconfig_nic-class"></a>\_SystemConfig-NIC-Klasse

Diese Klasse ist die Ereignistypklasse für Netzwerkschnittstellenkarten-Konfigurationsereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_NIC : SystemConfig
{
  uint64 PhysicalAddr;
  uint32 PhysicalAddrLen;
  uint32 Ipv4Index;
  uint32 Ipv6Index;
  string NICDescription;
  string IpAddresses;
  string DnsServerAddresses;
};
```

## <a name="members"></a>Member

Die **\_ SystemConfig-NIC-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ SystemConfig-NIC-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

DnsServerAddresses
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(7), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

IP-Adressen, die beim Abfragen von DNS-Servern verwendet werden sollen. Die Liste der Adressen ist durch Kommas getrennt.

</dd> <dt>

Ipaddresses
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(6), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

IP-Adressen, die der Netzwerkschnittstellenkarte zugeordnet sind. Die Liste der Adressen ist durch Kommas getrennt.

</dd> <dt>

Ipv4Index
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3)
</dt> </dl>

Adapterindex für IPv4-NIC. Der Adapterindex kann sich ändern, wenn ein Adapter deaktiviert und dann aktiviert wird, oder unter anderen Umständen und sollte nicht als persistent betrachtet werden.

</dd> <dt>

Ipv6Index
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4)
</dt> </dl>

Adapterindex für IPv6-NIC. Der Adapterindex kann sich ändern, wenn ein Adapter deaktiviert und dann aktiviert wird, oder unter anderen Umständen und sollte nicht als persistent betrachtet werden.

</dd> <dt>

NICDescription
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(5), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Beschreibung des Adapters.

</dd> <dt>

PhysicalAddr
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Format("x")
</dt> </dl>

Hardwareadresse für den Adapter.

</dd> <dt>

PhysicalAddrLen
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2)
</dt> </dl>

Länge der Hardwareadresse für den Adapter.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




