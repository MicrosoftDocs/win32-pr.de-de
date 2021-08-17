---
description: 'TcpIp_V1_TypeGroup1-Klasse: Diese Klasse ist die Ereignistypklasse für TCP/IP-Ereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.'
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
ms.openlocfilehash: 2b16f125eac6bf22904e93aef9084f00bbf6ca55be85c762de54c286631b584e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069550"
---
# <a name="tcpip_v1_typegroup1-class"></a>TcpIp \_ V1 \_ TypeGroup1-Klasse

Diese Klasse ist die Ereignistypklasse für TCP/IP-Ereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

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

Die **TcpIp \_ V1 \_ TypeGroup1-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **TcpIp \_ V1 \_ TypeGroup1-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

daddr
</dt> <dd> <dl> <dt>

Datentyp: **object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3), Extension("IPAddr")
</dt> </dl>

Ziel-IP-Adresse.

</dd> <dt>

dport
</dt> <dd> <dl> <dt>

Datentyp: **object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(5), Extension("Port")
</dt> </dl>

Zielportnummer.

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

Datentyp: **object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4), Extension("IPAddr")
</dt> </dl>

Quell-IP-Adresse.

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

Datentyp: **object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(6), Extension("Port")
</dt> </dl>

Quellportnummer.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TcpIp \_ V1**](tcpip-v1.md)
</dt> </dl>

 

 




