---
title: IPX_NEXT_HOP_ADDRESS -Struktur (Rtm.h)
description: Die IPX \_ NEXT \_ HOP \_ ADDRESS-Struktur enthält die Adresse für den Next-Hop-Router für eine IPX-Route.
ms.assetid: 079e3284-6238-4bcf-a17f-68ff86775f18
keywords:
- IPX_NEXT_HOP_ADDRESS-Struktur
- PIPX_NEXT_HOP_ADDRESS Strukturzeiger RAS
topic_type:
- apiref
api_name:
- IPX_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8abbb67f916960d015b26337734ffcff6f8e6551ab664bd4f4cc0d7511630a7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790758"
---
# <a name="ipx_next_hop_address-structure"></a>IPX \_ NEXT \_ HOP \_ ADDRESS-Struktur

\[Diese API wurde durch die [RoutingTabellen-Manager-API Version 2](about-routing-table-manager-version-2.md) ersetzt und ist über Windows Server 2003 hinaus nicht mehr verfügbar. Anwendungen sollten die Routingtabellen-Manager-API Version 2 verwenden.\]

Die **IPX \_ NEXT HOP \_ \_ ADDRESS-Struktur** enthält die Adresse für den Next-Hop-Router für eine IPX-Route.

## <a name="syntax"></a>Syntax


```C++
typedef struct _IPX_NEXT_HOP_ADDRESS {
  BYTE NHA_Mac[6];
} IPX_NEXT_HOP_ADDRESS, *PIPX_NEXT_HOP_ADDRESS;
```



## <a name="members"></a>Member

<dl> <dt>

**NHA \_ Mac**
</dt> <dd>

Gibt die MAC-Adresse des Routers des nächsten Hops an.

</dd> </dl>

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

[**\_RTM-IPX-ROUTE \_**](rtm-ipx-route.md)
</dt> </dl>

 

 





