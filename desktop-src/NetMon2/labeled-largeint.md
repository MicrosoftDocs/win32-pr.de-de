---
description: Die LABELED \_ LARGEINT-Struktur definiert eine Bezeichnung, die angezeigt wird, wenn ein bestimmter LARGEINT-Eigenschaftswert erkannt wird.
ms.assetid: ca565be0-96bb-4265-9422-793db0723563
title: LABELED_LARGEINT-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_LARGEINT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: fab2942a2a5188527c57663af0c6000aa2cb628eaa2499eef054854df9187784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778770"
---
# <a name="labeled_largeint-structure"></a>BEZEICHNETE \_ LARGEINT-Struktur

Die **LABELED \_ LARGEINT-Struktur** definiert eine Bezeichnung, die angezeigt wird, wenn ein bestimmter LARGEINT-Eigenschaftswert erkannt wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _LABELED_LARGEINT {
  LARGE_INTEGER Value;
  LPSTR         Label;
} LABELED_LARGEINT, *LPLABELED_LARGEINT;
```



## <a name="members"></a>Member

<dl> <dt>

**Wert**
</dt> <dd>

LARGEINT-Wert der Eigenschaft, die Sie erkennen möchten.

</dd> <dt>

**Label**
</dt> <dd>

Textbeschreibung oder Bezeichnung, die angezeigt wird, wenn der im **Wertmember** angegebene LARGEINT-Wert erkannt wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der **lpLabeledLargeIntTable-Member** der [SET-Struktur](set.md) zeigt auf ein Array von **SET-Strukturen,** die ein oder mehrere **Label-Member** der LARGEINT-Wertpaare definieren. Die Paare werden verwendet, wenn Sie anstelle eines bestimmten LARGEINT-Werts, der sich in einem Protokollpaket befindet, eine Bezeichnung anzeigen möchten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 




