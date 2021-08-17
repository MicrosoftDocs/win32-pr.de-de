---
description: Diese Klasse ist die Ereignistypklasse für IPv6-TCP/IP-Sendeereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 231ef62f-e3a5-497d-b10a-79449dc73c71
title: TcpIp_SendIPV6-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_SendIPV6
- TcpIp_SendIPV6.PID
- TcpIp_SendIPV6.size
- TcpIp_SendIPV6.daddr
- TcpIp_SendIPV6.saddr
- TcpIp_SendIPV6.dport
- TcpIp_SendIPV6.sport
- TcpIp_SendIPV6.startime
- TcpIp_SendIPV6.endtime
- TcpIp_SendIPV6.seqnum
- TcpIp_SendIPV6.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1f9314688bce48f48274131a2b1dd605d8a555e3e31c205a67a07d2895e55c2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069630"
---
# <a name="tcpip_sendipv6-class"></a>TcpIp \_ SendIPV6-Klasse

Diese Klasse ist die Ereignistypklasse für IPv6-TCP/IP-Sendeereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{26}, EventTypeName{"SendIPV6"}]
class TcpIp_SendIPV6 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 startime;
  uint32 endtime;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a>Member

Die **TcpIp \_ SendIPV6-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **TcpIp \_ SendIPV6-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

connid
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(10), Zeiger
</dt> </dl>

Ein eindeutiger Verbindungsbezeichner zum Korrelieren von Ereignissen, die zur gleichen Verbindung gehören.

</dd> <dt>

daddr
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3), Extension("IPAddrV6")
</dt> </dl>

Ziel-IP-Adresse.

</dd> <dt>

dport
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(5), Extension("Port")
</dt> </dl>

Zielportnummer.

</dd> <dt>

**Endtime**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(8)
</dt> </dl>

Sendeanforderungszeit beenden.

</dd> <dt>

PID
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1)
</dt> </dl>

Bezeichner des Prozesses, der der Anforderung zugeordnet ist.

</dd> <dt>

saddr
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4), Extension("IPAddrV6")
</dt> </dl>

Quell-IP-Adresse.

</dd> <dt>

seqnum
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(9)
</dt> </dl>

Sequenznummer.

</dd> <dt>

Größe
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2)
</dt> </dl>

Größe des Pakets.

</dd> <dt>

Sport
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(6), Extension("Port")
</dt> </dl>

Quellportnummer.

</dd> <dt>

**startime**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(7)
</dt> </dl>

Sendeanforderungszeit starten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Tcpip**](tcpip.md)
</dt> </dl>

 

 




