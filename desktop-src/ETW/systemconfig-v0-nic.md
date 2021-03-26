---
description: Diese Klasse ist die Ereignistyp Klasse für Konfigurations Ereignisse der Netzwerkschnittstellenkarte.
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
ms.openlocfilehash: 040c409564c0ad37e5208c1e91962d3f04de5fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980552"
---
# <a name="systemconfig_v0_nic-class"></a>SystemConfig \_ v0- \_ NIC-Klasse

Diese Klasse ist die Ereignistyp Klasse für Konfigurations Ereignisse der Netzwerkschnittstellenkarte.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die **System config \_ v0- \_ NIC** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **System config \_ v0- \_ NIC** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Daten**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (16)
</dt> </dl>

Datenfeld.

</dd> <dt>

**DhcpServer**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (8)
</dt> </dl>

Die IP-Adresse des DHCP-Servers (Dynamic Host Configuration Protocol). Der Wert 255.255.255.255 gibt an, dass der DHCP-Server nicht erreicht werden konnte oder gerade erreicht wird. Jedes Byte der sint32 stellt einen der vier Teile der IP-Adresse (P1. P2. P3. P4) dar. Das nieder wertige Byte enthält den Wert für P1, das nächste Byte enthält den Wert für P2 usw.

</dd> <dt>

**DnsServer1**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (12)
</dt> </dl>

Die ersten Server-IP-Adressen, die zum Abfragen von DNS-Servern verwendet werden sollen. Jedes Byte der sint32 stellt einen der vier Teile der IP-Adresse (P1. P2. P3. P4) dar. Das nieder wertige Byte enthält den Wert für P1, das nächste Byte enthält den Wert für P2 usw.

</dd> <dt>

**DnsServer2**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (13)
</dt> </dl>

Zweite Server-IP-Adressen, die zum Abfragen von DNS-Servern verwendet werden sollen. Jedes Byte der sint32 stellt einen der vier Teile der IP-Adresse (P1. P2. P3. P4) dar. Das nieder wertige Byte enthält den Wert für P1, das nächste Byte enthält den Wert für P2 usw.

</dd> <dt>

**DnsServer3**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (14)
</dt> </dl>

Dritte Server-IP-Adressen, die zum Abfragen von DNS-Servern verwendet werden sollen. Jedes Byte der sint32 stellt einen der vier Teile der IP-Adresse (P1. P2. P3. P4) dar. Das nieder wertige Byte enthält den Wert für P1, das nächste Byte enthält den Wert für P2 usw.

</dd> <dt>

**DnsServer4**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (15)
</dt> </dl>

Vierte Server-IP-Adressen, die beim Abfragen von DNS-Servern verwendet werden sollen. Jedes Byte der sint32 stellt einen der vier Teile der IP-Adresse (P1. P2. P3. P4) dar. Das nieder wertige Byte enthält den Wert für P1, das nächste Byte enthält den Wert für P2 usw.

</dd> <dt>

**Gateway**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (9)
</dt> </dl>

Die IP-Adresse des Standard Gateways, das vom Computersystem verwendet wird. Jedes Byte der sint32 stellt einen der vier Teile der IP-Adresse (P1. P2. P3. P4) dar. Das nieder wertige Byte enthält den Wert für P1, das nächste Byte enthält den Wert für P2 usw.

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (2)
</dt> </dl>

Adapter Index. Der Adapter Index kann sich ändern, wenn ein Adapter deaktiviert und dann aktiviert wird, oder unter anderen Umständen nicht als persistent eingestuft wird.

</dd> <dt>

**IpAddress**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (6)
</dt> </dl>

IP-Adressen, die der Netzwerkschnittstellenkarte zugeordnet sind. Jedes Byte der sint32 stellt einen der vier Teile der IP-Adresse (P1. P2. P3. P4) dar. Das nieder wertige Byte enthält den Wert für P1, das nächste Byte enthält den Wert für P2 usw.

</dd> <dt>

**NICNAME**
</dt> <dd> <dl> <dt>

Datentyp: **char16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (1), **Max** (256)
</dt> </dl>

Der Name der Netzwerkschnittstellenkarte.

</dd> <dt>

**Physicaladdr**
</dt> <dd> <dl> <dt>

Datentyp: **char16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (4), **Max** (8)
</dt> </dl>

Die Hardware Adresse für den Adapter.

</dd> <dt>

**Physicaladdrlen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (3)
</dt> </dl>

Länge der Hardwareadresse für den Adapter.

</dd> <dt>

**Primarywinsserver**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (10)
</dt> </dl>

Die IP-Adresse für den primären WINS-Server. Jedes Byte der sint32 stellt einen der vier Teile der IP-Adresse (P1. P2. P3. P4) dar. Das nieder wertige Byte enthält den Wert für P1, das nächste Byte enthält den Wert für P2 usw.

</dd> <dt>

**Secondarywinsserver**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (11)
</dt> </dl>

Die IP-Adresse für den sekundären WINS-Server. Jedes Byte der sint32 stellt einen der vier Teile der IP-Adresse (P1. P2. P3. P4) dar. Das nieder wertige Byte enthält den Wert für P1, das nächste Byte enthält den Wert für P2 usw.

</dd> <dt>

**Größe**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (5)
</dt> </dl>

Größe (in Bytes) der Dateneigenschaft.

</dd> <dt>

**SubnetMask**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (7)
</dt> </dl>

Die der Netzwerkschnittstellenkarte zugeordnete Subnetzmaske. Jedes Byte der sint32 stellt einen der vier Teile der IP-Adresse (P1. P2. P3. P4) dar. Das nieder wertige Byte enthält den Wert für P1, das nächste Byte enthält den Wert für P2 usw.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemConfig \_ v0**](systemconfig-v0.md)
</dt> </dl>

 

 




