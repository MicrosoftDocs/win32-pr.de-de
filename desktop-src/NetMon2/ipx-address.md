---
description: Die IPX- \_ Adressstruktur stellt eine Adresse auf IPX-Protokollebene bereit.
ms.assetid: 06939ac3-3718-4441-b2c8-c73adfe3babe
title: IPX_ADDRESS Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPX_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 18645a455e780020037384a2df7173a019d71677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525868"
---
# <a name="ipx_address-structure"></a>IPX- \_ Adressstruktur

Die **IPX- \_ Adress** Struktur stellt eine Adresse auf IPX-Protokollebene bereit.

## <a name="syntax"></a>Syntax


```C++
typedef struct _IPX_ADDRESS {
  BYTE Subnet[4];
  BYTE Address[6];
} IPX_ADDRESS, *LPIPX_ADDRESS;
```



## <a name="members"></a>Member

<dl> <dt>

**Subnetz**
</dt> <dd>

Netzwerksubnetzbezeichner.

</dd> <dt>

**Adresse**
</dt> <dd>

Subnetz-NIC-Bezeichner.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




