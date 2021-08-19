---
description: Die ANDEXP-Struktur enthält ein Array von Muster übereinstimmungen, die zum Auswerten von Framedaten verwendet werden.
ms.assetid: e5f4c030-eb2b-4cc9-9032-9ad4701b6503
title: ANDEXP-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ANDEXP
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7ee2ac65e10e0dc9be46ab103fe21abcc78dc403302b298f3eb2fc83000802cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117982952"
---
# <a name="andexp-structure"></a>ANDEXP-Struktur

Die **ANDEXP-Struktur** enthält ein Array von Muster übereinstimmungen, die zum Auswerten von Framedaten verwendet werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _ANDEXP {
  DWORD        nPatternMatches;
  PATTERNMATCH PatternMatch[MAX_PATTERNS];
} ANDEXP, *LPANDEXP;
```



## <a name="members"></a>Member

<dl> <dt>

**nPatternMatches**
</dt> <dd>

Anzahl der Muster übereinstimmungen.

</dd> <dt>

**PatternMatch**
</dt> <dd>

Array von Muster match-Elementen. Beachten Sie, dass jede **ANDEXP-Struktur** bis zu vier Muster-Match-Elemente enthalten kann. Weitere Informationen zu diesem Member finden Sie unter [Erfassungsfilter.](capture-filters.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Muster im **PatternMatch** \[ MAX \_ \] PATTERNS-Array werden als Peers in logischen OR-Anweisungen im Format verknüpft.

(Muster 1 \| \| Muster 2 \| \| Muster 3).

Weitere Informationen zum Implementieren dieser Struktur finden Sie unter [Erfassungsfilter.](capture-filters.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[PATTERNMATCH](patternmatch.md)
</dt> </dl>

 

 




