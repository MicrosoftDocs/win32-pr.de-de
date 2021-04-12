---
title: IPX_NEXT_HOP_ADDRESS Struktur (RTM. h)
description: Die IPX \_ \_ -Adressstruktur "Nächster Hop" \_ enthält die Adresse für den Router für den nächsten Hop für eine IPX-Route.
ms.assetid: 079e3284-6238-4bcf-a17f-68ff86775f18
keywords:
- IPX_NEXT_HOP_ADDRESS Struktur-RAS
- PIPX_NEXT_HOP_ADDRESS-Struktur Zeiger RAS
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
ms.openlocfilehash: 99c3eb135f1d87050cd190fe47d0088fd1ab86f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475057"
---
# <a name="ipx_next_hop_address-structure"></a>IPX \_ - \_ Adressstruktur "Nächster Hop" \_

\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]

Die **IPX \_ - \_ \_ Adressstruktur "Nächster Hop** " enthält die Adresse für den Router für den nächsten Hop für eine IPX-Route.

## <a name="syntax"></a>Syntax


```C++
typedef struct _IPX_NEXT_HOP_ADDRESS {
  BYTE NHA_Mac[6];
} IPX_NEXT_HOP_ADDRESS, *PIPX_NEXT_HOP_ADDRESS;
```



## <a name="members"></a>Member

<dl> <dt>

**Nha- \_ Mac**
</dt> <dd>

Gibt die Mac-Adresse des Routers des nächsten Hops an.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                   |
| Header<br/>                   | <dl> <dt>RTM. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Referenz für Routing Tabellen-Manager Version 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Routing Tabellen-Manager, Version 1, Strukturen](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**RTM- \_ IPX- \_ Route**](rtm-ipx-route.md)
</dt> </dl>

 

 





