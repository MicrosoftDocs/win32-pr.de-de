---
description: Enthält eine Gruppe von als Peers bewerteten andexp-Arrays.
ms.assetid: 14fa568c-9535-4415-923d-7e93ba4d2e80
title: Ausdrucks Struktur (Netmon. h)
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
ms.openlocfilehash: b6565c294c0d8e0a7a277769404cb8b1b206380e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346074"
---
# <a name="expression-structure"></a>Ausdrucks Struktur

Die **Ausdrucks** Struktur enthält eine Gruppe von **andexp** -Arrays, die als Peers in logischen Ausdrücken und Ausdrücken ausgewertet werden, die das Format aufweisen.

(Andexp 1 && andexp 2 && andexp 3).

## <a name="syntax"></a>Syntax


```C++
typedef struct _EXPRESSION {
  DWORD  nAndExps;
  ANDEXP AndExp[MAX_PATTERNS];
} EXPRESSION, *LPEXPRESSION;
```



## <a name="members"></a>Member

<dl> <dt>

**nandexps**
</dt> <dd>

Anzahl von **andexp** -Mustern.

</dd> <dt>

**Andexp**
</dt> <dd>

Array von **andexp** -Mustern. Der Erfassungs Filter ordnet alle Zeilen dieses Arrays als logische and-Anweisungen an. Beachten Sie, dass jede Ausdrucks Struktur maximal vier **andexp** -Muster enthalten kann.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zum Implementieren dieser Struktur als Teil eines Erfassungs Filters finden Sie unter [Capture Filters (Erfassen von Filtern](capture-filters.md)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Andexp](andexp.md)
</dt> <dt>

[Capturefilter](capturefilter.md)
</dt> </dl>

 

 




