---
description: Enthält eine Gruppe von ANDEXP-Arrays, die als Peers ausgewertet werden.
ms.assetid: 14fa568c-9535-4415-923d-7e93ba4d2e80
title: EXPRESSION-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPRESSION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4efa1f79477e3dcc13bedfddb2cdca7fd660f5430b7d7f2b87dbd9d4b4425098
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366838"
---
# <a name="expression-structure"></a>EXPRESSION-Struktur

Die **EXPRESSION-Struktur** enthält eine Gruppe von **ANDEXP-Arrays,** die als Peers in logischen AND-Ausdrücken ausgewertet werden, die das Format haben.

(ANDEXP 1 && ANDEXP 2 && ANDEXP 3).

## <a name="syntax"></a>Syntax


```C++
typedef struct _EXPRESSION {
  DWORD  nAndExps;
  ANDEXP AndExp[MAX_PATTERNS];
} EXPRESSION, *LPEXPRESSION;
```



## <a name="members"></a>Member

<dl> <dt>

**nAndExps**
</dt> <dd>

Anzahl von **ANDEXP-Mustern.**

</dd> <dt>

**AndExp**
</dt> <dd>

Array von **ANDEXP-Mustern.** Der Erfassungsfilter ordnet alle Zeilen dieses Arrays als logische AND-Anweisungen an. Beachten Sie, dass jede EXPRESSION-Struktur maximal vier **ANDEXP-Muster enthalten** kann.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Weitere Informationen zum Implementieren dieser Struktur als Teil eines Erfassungsfilters finden Sie unter [Erfassungsfilter.](capture-filters.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ANDEXP](andexp.md)
</dt> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




