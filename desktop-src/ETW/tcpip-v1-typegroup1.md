---
description: Diese Klasse ist die Ereignistyp Klasse für TCP/IP-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 1cde7e37-52da-4108-90ce-7647a5653f65
title: TcpIp_V1_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_V1_TypeGroup1
- TcpIp_V1_TypeGroup1.PID
- TcpIp_V1_TypeGroup1.size
- TcpIp_V1_TypeGroup1.daddr
- TcpIp_V1_TypeGroup1.saddr
- TcpIp_V1_TypeGroup1.dport
- TcpIp_V1_TypeGroup1.sport
api_type:
- NA
api_location: ''
ms.openlocfilehash: fcd5f19eafa5308ef369a211559c6c464427b168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978233"
---
# <a name="tcpip_v1_typegroup1-class"></a>Tcpip \_ v1 \_ TypeGroup1-Klasse

Diese Klasse ist die Ereignistyp Klasse für TCP/IP-Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16}, EventTypeName{"Send", "Recv", "Connect", "Disconnect", "Retransmit", "Accept", "Reconnect"}]
class TcpIp_V1_TypeGroup1 : TcpIp_V1
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
};
```

## <a name="members"></a>Member

Die Klasse " **tcpip \_ v1 \_ TypeGroup1** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Klasse **tcpip \_ v1 \_ TypeGroup1** verfügt über diese Eigenschaften.

<dl> <dt>

daddr
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3), Erweiterung ("ipaddr")
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

Qualifizierer: wmidataid (4), Erweiterung ("ipaddr")
</dt> </dl>

Quell-IP-Adresse.

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Tcpip \_ v1**](tcpip-v1.md)
</dt> </dl>

 

 




