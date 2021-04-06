---
title: IP_NETWORK Struktur (RTM. h)
description: Die IP- \_ Netzwerkstruktur beschreibt eine IP-Netzwerkadresse.
ms.assetid: 5dcc733f-c86f-407e-8727-64f3ae71dd48
keywords:
- IP_NETWORK Struktur-RAS
- PIP_NETWORK-Struktur Zeiger RAS
topic_type:
- apiref
api_name:
- IP_NETWORK
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2541c493b1b2e3805e3705c71e890c6a6aaa98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742480"
---
# <a name="ip_network-structure"></a>IP- \_ Netzwerkstruktur

\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]

Die **IP- \_ Netzwerk** Struktur beschreibt eine IP-Netzwerkadresse.

## <a name="syntax"></a>Syntax


```C++
typedef struct _IP_NETWORK {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NETWORK, *PIP_NETWORK;
```



## <a name="members"></a>Member

<dl> <dt>

**N \_ netnumber**
</dt> <dd>

Gibt die IP-Netzwerk Nummer an, die als IP-Adresse in Computer-Byte-Reihenfolge ausgedrückt wird.

</dd> <dt>

**N \_ Netzmaske**
</dt> <dd>

Gibt die Netzwerk Maske an. Wenden Sie diese Maske auf die IP-Adresse an, um die Netzwerkadresse zu extrahieren. Die Netzwerk Maske befindet sich in der Computer-Byte-Reihenfolge.

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

[**RTM \_ -IP- \_ Route**](rtm-ip-route.md)
</dt> </dl>

 

 





