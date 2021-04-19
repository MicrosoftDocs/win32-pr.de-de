---
title: IP_NEXT_HOP_ADDRESS Struktur (RTM. h)
description: Die IP \_ \_ -Adressstruktur "Nächster Hop" \_ enthält die Adresse für den Router für den nächsten Hop für eine IP-Route.
ms.assetid: a97b3995-dfaa-4e53-be86-3ad46b8be691
keywords:
- IP_NEXT_HOP_ADDRESS Struktur-RAS
- PIP_NEXT_HOP_ADDRESS Struktur-RAS
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
ms.openlocfilehash: 1818a49e7977dbb4dfa31ebac1dae7651adb8d45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346321"
---
# <a name="ip_next_hop_address-structure"></a>IP \_ - \_ Adressstruktur des nächsten Hops \_

\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]

Die **IP-Adressstruktur " \_ Nächster \_ Hop \_** " enthält die Adresse für den Router für den nächsten Hop für eine IP-Route.

## <a name="syntax"></a>Syntax


```C++
typedef struct _IP_NEXT_HOP_ADDRESS {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NEXT_HOP_ADDRESS, *PIP_NEXT_HOP_ADDRESS;
```



## <a name="members"></a>Member

<dl> <dt>

**N \_ netnumber**
</dt> <dd>

Gibt die IP-Netzwerkadresse an, die als IP-Adresse in Computer-Byte-Reihenfolge ausgedrückt wird.

</dd> <dt>

**N \_ Netzmaske**
</dt> <dd>

Gibt die Netzwerk Maske an. Wenden Sie diese Maske auf die IP-Adresse an, um die Netzwerkadresse zu extrahieren. Die Netzwerk Maske befindet sich in der Computer-Byte-Reihenfolge.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **IP \_ - \_ \_ Adresse für den nächsten Hop** ist eine typedef der [**IP- \_ Netzwerk**](ip-network.md) Struktur. Die typedef befindet sich in "RTM. h".

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

[**IP- \_ Netzwerk**](ip-network.md)
</dt> <dt>

[**RTM \_ -IP- \_ Route**](rtm-ip-route.md)
</dt> </dl>

 

 





