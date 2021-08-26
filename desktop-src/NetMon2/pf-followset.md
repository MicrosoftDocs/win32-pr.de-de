---
description: Die PF \_ FOLLOWSET-Struktur definiert die Protokolle, die einem Protokoll voran- oder folgen können.
ms.assetid: ef444af9-edae-4547-9548-8a682c279f08
title: PF_FOLLOWSET -Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: d404e602e78452a38343a6e62fce8c5b16941270eaa2825de8339f583c064a8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036830"
---
# <a name="pf_followset-structure"></a>PF \_ FOLLOWSET-Struktur

Die **PF \_ FOLLOWSET-Struktur** definiert die Protokolle, die einem Protokoll voran- oder folgen können.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PF_FOLLOWSET {
  DWORD          nEntries;
  PF_FOLLOWENTRY Entry[];
} PF_FOLLOWSET, *PPF_FOLLOWSET;
```



## <a name="members"></a>Member

<dl> <dt>

**nEntries**
</dt> <dd>

Anzahl der Protokolle in der Liste.

</dd> <dt>

**Eingabe**
</dt> <dd>

Array von [PF \_ FOLLOWENTRY-Strukturen,](pf-followentry.md) die jedes Protokoll beschreiben.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [PF \_ PARSERINFO-Struktur](pf-parserinfo.md) verwendet die **PF \_ FOLLOWSET-Struktur,** um die Protokolle auflisten, die dem vom Parser erkannten Protokoll voran- oder folgen können.

Netzwerkmonitor verwendet die Informationen in der **PF \_ FOLLOWSET-Struktur,** um die folgenden Sätze bestimmter Parser zu aktualisieren. Die **PF \_ FOLLOWSET-Struktur** muss mithilfe von **HeapAlloc zugeordnet werden.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[PF \_ FOLLOWENTRY](pf-followentry.md)
</dt> <dt>

[PF \_ PARSERINFO](pf-parserinfo.md)
</dt> </dl>

 

 




