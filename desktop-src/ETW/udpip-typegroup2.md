---
description: Diese Klasse ist die Ereignistyp Klasse für UDP/IP-IPv6-Sende-und-Empfangs Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 059041f6-bf34-4bf8-8e1a-2dfbc6c30edc
title: UdpIp_TypeGroup2-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_TypeGroup2
- UdpIp_TypeGroup2.PID
- UdpIp_TypeGroup2.size
- UdpIp_TypeGroup2.daddr
- UdpIp_TypeGroup2.saddr
- UdpIp_TypeGroup2.dport
- UdpIp_TypeGroup2.sport
- UdpIp_TypeGroup2.seqnum
- UdpIp_TypeGroup2.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 88d9cb4935d005f3c25f1fb6c3c421328fb285bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978865"
---
# <a name="udpip_typegroup2-class"></a>Udpip \_ TypeGroup2-Klasse

Diese Klasse ist die Ereignistyp Klasse für UDP/IP-IPv6-Sende-und-Empfangs Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{26, 27}, EventTypeName{"SendIPV6", "RecvIPV6"}]
class UdpIp_TypeGroup2 : UdpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a>Member

Die **udpip- \_ TypeGroup2** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **udpip- \_ TypeGroup2** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

nicht konform
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (8), Zeiger
</dt> </dl>

Ein eindeutiger Verbindungs Bezeichner zum Korrelieren von Ereignissen, die zur gleichen Verbindung gehören.

</dd> <dt>

daddr
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3), Extension ("IPAddrV6")
</dt> </dl>

Ziel-IP-Adresse.

</dd> <dt>

dport
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (5), Erweiterung ("Port")
</dt> </dl>

Die Ziel Portnummer.

</dd> <dt>

PID
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1)
</dt> </dl>

Der Bezeichner des Prozesses, der der Anforderung zugeordnet ist.

</dd> <dt>

saddr
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (4), Extension ("IPAddrV6")
</dt> </dl>

Quell-IP-Adresse.

</dd> <dt>

SEQNUM
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (7)
</dt> </dl>

Sequenznummer.

</dd> <dt>

size
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2)
</dt> </dl>

Größe des Pakets.

</dd> <dt>

Reit
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (6), Erweiterung ("Port")
</dt> </dl>

Quell Portnummer.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Udpip**](udpip.md)
</dt> </dl>

 

 




