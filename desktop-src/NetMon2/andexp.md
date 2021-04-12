---
description: Die Struktur "andexp" enthält ein Array von Muster Übereinstimmungen, mit denen Frame-Daten ausgewertet werden.
ms.assetid: e5f4c030-eb2b-4cc9-9032-9ad4701b6503
title: Andexp-Struktur (Netmon. h)
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
ms.openlocfilehash: 1d27d5bdd51a45b31f518271053f44b45917cdeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346838"
---
# <a name="andexp-structure"></a>Andexp-Struktur

Die Struktur " **andexp** " enthält ein Array von Muster Übereinstimmungen, mit denen Frame-Daten ausgewertet werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _ANDEXP {
  DWORD        nPatternMatches;
  PATTERNMATCH PatternMatch[MAX_PATTERNS];
} ANDEXP, *LPANDEXP;
```



## <a name="members"></a>Member

<dl> <dt>

**npatternmatches**
</dt> <dd>

Anzahl der Muster Übereinstimmungen.

</dd> <dt>

**Patternmatch**
</dt> <dd>

Array von Muster Übereinstimmungs Elementen. Beachten Sie, dass jede **andexp** -Struktur bis zu vier Muster Übereinstimmungs Elemente enthalten kann. Weitere Informationen zu diesem Member finden Sie unter [Erfassungs Filter](capture-filters.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Muster im Muster Array " **patternmatch** \[ Max \_ Patterns" \] werden als Peers in logischen OR-Anweisungen im Format verknüpft.

(Muster 1 \| \| Muster 2 \| \| Muster 3).

Weitere Informationen zum Implementieren dieser Struktur finden Sie unter [Erfassungs Filter](capture-filters.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Patternmatch](patternmatch.md)
</dt> </dl>

 

 




