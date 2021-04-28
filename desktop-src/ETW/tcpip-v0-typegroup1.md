---
description: 'TcpIp_V0_TypeGroup1-Klasse: Diese Klasse ist die Ereignistypklasse für TCP/IP-Ereignisse. Die folgende Syntax wird aus MOF-Code vereinfacht.'
ms.assetid: 007f0744-8b74-4c57-85bc-f6bdb20bffa7
title: TcpIp_V0_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_V0_TypeGroup1
- TcpIp_V0_TypeGroup1.daddr
- TcpIp_V0_TypeGroup1.saddr
- TcpIp_V0_TypeGroup1.dport
- TcpIp_V0_TypeGroup1.sport
- TcpIp_V0_TypeGroup1.size
- TcpIp_V0_TypeGroup1.PID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 96df2214aff9b5be6f10a1f08f6e6ea2e015c6b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105788"
---
# <a name="tcpip_v0_typegroup1-class"></a>TcpIp \_ V0 \_ TypeGroup1-Klasse

Diese Klasse ist die Ereignistypklasse für TCP/IP-Ereignisse.

Die folgende Syntax wird aus MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"Send", "Recv", "Connect", "Disconnect", "Retransmit", "Accept"}]
class TcpIp_V0_TypeGroup1 : TcpIp_V0
{
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 size;
  uint32 PID;
};
```

## <a name="members"></a>Member

Die **TcpIp \_ V0 \_ TypeGroup1-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **TcpIp \_ V0 \_ TypeGroup1-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

daddr
</dt> <dd> <dl> <dt>

Datentyp: **object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Extension("IPAddr")
</dt> </dl>

Ziel-IP-Adresse.

</dd> <dt>

dport
</dt> <dd> <dl> <dt>

Datentyp: **object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3), Extension("Port")
</dt> </dl>

Zielportnummer.

</dd> <dt>

PID
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(6)
</dt> </dl>

Bezeichner des Prozesses, der der Anforderung zugeordnet ist.

</dd> <dt>

saddr
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2), Extension("IPAddr")
</dt> </dl>

Quell-IP-Adresse.

</dd> <dt>

Größe
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(5)
</dt> </dl>

Größe des Pakets.

</dd> <dt>

Sport
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4), Extension("Port")
</dt> </dl>

Quellportnummer.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TcpIp \_ V0**](tcpip-v0.md)
</dt> </dl>

 

 




