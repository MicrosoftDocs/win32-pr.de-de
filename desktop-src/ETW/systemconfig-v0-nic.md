---
description: Diese Klasse ist die Ereignistypklasse für Netzwerkschnittstellenkarten-Konfigurationsereignisse.
ms.assetid: 1cae611b-fb6a-4416-8fd4-0c882e8aa5e6
title: SystemConfig_V0_NIC-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_NIC
- SystemConfig_V0_NIC.NICName
- SystemConfig_V0_NIC.Index
- SystemConfig_V0_NIC.PhysicalAddrLen
- SystemConfig_V0_NIC.PhysicalAddr
- SystemConfig_V0_NIC.Size
- SystemConfig_V0_NIC.IpAddress
- SystemConfig_V0_NIC.SubnetMask
- SystemConfig_V0_NIC.DhcpServer
- SystemConfig_V0_NIC.Gateway
- SystemConfig_V0_NIC.PrimaryWinsServer
- SystemConfig_V0_NIC.SecondaryWinsServer
- SystemConfig_V0_NIC.DnsServer1
- SystemConfig_V0_NIC.DnsServer2
- SystemConfig_V0_NIC.DnsServer3
- SystemConfig_V0_NIC.DnsServer4
- SystemConfig_V0_NIC.Data
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6abe9356ce222d8f461509ec9cfa25ab0a49b8583022ee5e1d832cf29a226dcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746470"
---
# <a name="systemconfig_v0_nic-class"></a>SystemConfig \_ \_ V0-NIC-Klasse

Diese Klasse ist die Ereignistypklasse für Netzwerkschnittstellenkarten-Konfigurationsereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_V0_NIC : SystemConfig_V0
{
  char16 NICName[];
  uint32 Index;
  uint32 PhysicalAddrLen;
  char16 PhysicalAddr;
  uint32 Size;
  sint32 IpAddress;
  sint32 SubnetMask;
  sint32 DhcpServer;
  sint32 Gateway;
  sint32 PrimaryWinsServer;
  sint32 SecondaryWinsServer;
  sint32 DnsServer1;
  sint32 DnsServer2;
  sint32 DnsServer3;
  sint32 DnsServer4;
  uint32 Data;
};
```

## <a name="members"></a>Member

Die **SystemConfig \_ \_ V0-NIC-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SystemConfig \_ \_ V0-NIC-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Daten**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (16)
</dt> </dl>

Datenfeld.

</dd> <dt>

**DhcpServer**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (8)
</dt> </dl>

IP-Adresse des DHCP-Servers (Dynamic Host Configuration Protocol). Der Wert 255.255.255.255 gibt an, dass der DHCP-Server nicht erreicht werden konnte oder gerade erreicht wird. Jedes Byte von sint32 stellt einen der vier Teile der IP-Adresse dar (p1.p2.p3.p4). Das niedrige Byte enthält den Wert für p1, das nächste Byte enthält den Wert für p2 und so weiter.

</dd> <dt>

**DnsServer1**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (12)
</dt> </dl>

Die ersten Server-IP-Adressen, die beim Abfragen von DNS-Servern verwendet werden sollen. Jedes Byte von sint32 stellt einen der vier Teile der IP-Adresse dar (p1.p2.p3.p4). Das niedrige Byte enthält den Wert für p1, das nächste Byte enthält den Wert für p2 und so weiter.

</dd> <dt>

**DnsServer2**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (13)
</dt> </dl>

Zweite Ip-Adressen des Servers, die bei Abfragen von DNS-Servern verwendet werden sollen. Jedes Byte von sint32 stellt einen der vier Teile der IP-Adresse dar (p1.p2.p3.p4). Das niedrige Byte enthält den Wert für p1, das nächste Byte enthält den Wert für p2 und so weiter.

</dd> <dt>

**DnsServer3**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (14)
</dt> </dl>

IP-Adressen des dritten Servers, die beim Abfragen von DNS-Servern verwendet werden sollen. Jedes Byte von sint32 stellt einen der vier Teile der IP-Adresse dar (p1.p2.p3.p4). Das niedrige Byte enthält den Wert für p1, das nächste Byte enthält den Wert für p2 und so weiter.

</dd> <dt>

**DnsServer4**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (15)
</dt> </dl>

Vierte Server-IP-Adressen, die beim Abfragen von DNS-Servern verwendet werden sollen. Jedes Byte von sint32 stellt einen der vier Teile der IP-Adresse dar (p1.p2.p3.p4). Das niedrige Byte enthält den Wert für p1, das nächste Byte enthält den Wert für p2 und so weiter.

</dd> <dt>

**Gateway**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (9)
</dt> </dl>

IP-Adresse des Standardgateways, das vom Computersystem verwendet wird. Jedes Byte von sint32 stellt einen der vier Teile der IP-Adresse dar (p1.p2.p3.p4). Das niedrige Byte enthält den Wert für p1, das nächste Byte enthält den Wert für p2 und so weiter.

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (2)
</dt> </dl>

Adapterindex. Der Adapterindex kann sich ändern, wenn ein Adapter deaktiviert und dann aktiviert wird, oder unter anderen Umständen, und sollte nicht als persistent betrachtet werden.

</dd> <dt>

**IpAddress**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (6)
</dt> </dl>

IP-Adressen, die der Netzwerkschnittstellenkarte zugeordnet sind. Jedes Byte von sint32 stellt einen der vier Teile der IP-Adresse dar (p1.p2.p3.p4). Das niedrige Byte enthält den Wert für p1, das nächste Byte enthält den Wert für p2 und so weiter.

</dd> <dt>

**NICName**
</dt> <dd> <dl> <dt>

Datentyp: **char16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (1), **Max** (256)
</dt> </dl>

Name der Netzwerkschnittstellenkarte.

</dd> <dt>

**PhysicalAddr**
</dt> <dd> <dl> <dt>

Datentyp: **char16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (4), **Max** (8)
</dt> </dl>

Hardwareadresse für den Adapter.

</dd> <dt>

**PhysicalAddrLen**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (3)
</dt> </dl>

Länge der Hardwareadresse für den Adapter.

</dd> <dt>

**PrimaryWinsServer**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (10)
</dt> </dl>

IP-Adresse für den primären WINS-Server. Jedes Byte von sint32 stellt einen der vier Teile der IP-Adresse dar (p1.p2.p3.p4). Das niedrige Byte enthält den Wert für p1, das nächste Byte enthält den Wert für p2 und so weiter.

</dd> <dt>

**SecondaryWinsServer**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (11)
</dt> </dl>

IP-Adresse für den sekundären WINS-Server. Jedes Byte von sint32 stellt einen der vier Teile der IP-Adresse dar (p1.p2.p3.p4). Das niedrige Byte enthält den Wert für p1, das nächste Byte enthält den Wert für p2 und so weiter.

</dd> <dt>

**Größe**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (5)
</dt> </dl>

Größe der Data-Eigenschaft in Bytes.

</dd> <dt>

**SubnetMask**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (7)
</dt> </dl>

Subnetzmaske, die der Netzwerkschnittstellenkarte zugeordnet ist. Jedes Byte von sint32 stellt einen der vier Teile der IP-Adresse dar (p1.p2.p3.p4). Das niedrige Byte enthält den Wert für p1, das nächste Byte enthält den Wert für p2 und so weiter.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




