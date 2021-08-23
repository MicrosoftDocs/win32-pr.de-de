---
description: Die PF FOLLOWENTRY-Struktur definiert ein Protokoll, Netzwerkmonitor dem folgenden Satz eines Parsers \_ hinzufügt.
ms.assetid: 931ae70f-8c5e-4b7a-aae6-64a33dac3b23
title: PF_FOLLOWENTRY -Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 8fd7452a4db6318df0d4c23ea405d2cd4afcf6575c7abac34749a66bc88c2084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063730"
---
# <a name="pf_followentry-structure"></a>PF \_ FOLLOWENTRY-Struktur

Die **PF \_ FOLLOWENTRY-Struktur** definiert ein Protokoll, Netzwerkmonitor dem folgenden Satz eines Parsers hinzufügt.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PF_FOLLOWENTRY {
  char szProtocol[MAX_PROTOCOL_NAME_LEN];
} PF_FOLLOWENTRY, *PPF_FOLLOWENTRY;
```



## <a name="members"></a>Member

<dl> <dt>

**szProtocol**
</dt> <dd>

Der Name des Protokolls.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [PF \_ FOLLOWSET-Struktur](pf-followset.md) verwendet ein Array von **PF \_ FOLLOWENTRY-Strukturen.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[PF \_ FOLLOWSET](pf-followset.md)
</dt> </dl>

 

 




