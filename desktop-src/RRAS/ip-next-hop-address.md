---
title: IP_NEXT_HOP_ADDRESS -Struktur (Rtm.h)
description: Die IP \_ NEXT \_ HOP \_ ADDRESS-Struktur enthält die Adresse für den Next-Hop-Router für eine IP-Route.
ms.assetid: a97b3995-dfaa-4e53-be86-3ad46b8be691
keywords:
- IP_NEXT_HOP_ADDRESS Ras-Struktur
- PIP_NEXT_HOP_ADDRESS-Struktur
topic_type:
- apiref
api_name:
- IP_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94f79b850c7d5f48e5f409e5380ad7345288187b8939b752b4f282b2274a99cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790964"
---
# <a name="ip_next_hop_address-structure"></a>IP \_ NEXT \_ HOP \_ ADDRESS-Struktur

\[Diese API wurde durch die [RoutingTabellen-Manager-API Version 2](about-routing-table-manager-version-2.md) ersetzt und ist über Windows Server 2003 hinaus nicht mehr verfügbar. Anwendungen sollten die Routingtabellen-Manager-API Version 2 verwenden.\]

Die **IP NEXT HOP \_ \_ \_ ADDRESS-Struktur** enthält die Adresse für den Next-Hop-Router für eine IP-Route.

## <a name="syntax"></a>Syntax


```C++
typedef struct _IP_NEXT_HOP_ADDRESS {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NEXT_HOP_ADDRESS, *PIP_NEXT_HOP_ADDRESS;
```



## <a name="members"></a>Member

<dl> <dt>

**N \_ NetNumber**
</dt> <dd>

Gibt die IP-Netzwerkadresse an, die als IP-Adresse in Machine Byte-Reihenfolge ausgedrückt wird.

</dd> <dt>

**N \_ NetMask**
</dt> <dd>

Gibt die Netzwerkmaske an. Wenden Sie diese Maske auf die IP-Adresse an, um die Netzwerkadresse zu extrahieren. Die Netzwerkmaske befindet sich in machine-byte-Reihenfolge.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **IP NEXT HOP \_ \_ \_ ADDRESS-Struktur** ist eine Typdefinition der [**\_ IP-Netzwerkstruktur.**](ip-network.md) Die typedef befindet sich in Rtm.h.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                   |
| Header<br/>                   | <dl> <dt>Rtm.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Routing Table Manager Version 1 Reference](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Routingtabellen-Manager- Version 1-Strukturen](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_IP-NETZWERK**](ip-network.md)
</dt> <dt>

[**\_RTM-IP-ROUTE \_**](rtm-ip-route.md)
</dt> </dl>

 

 





