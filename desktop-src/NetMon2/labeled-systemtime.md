---
description: Die LABELED \_ SYSTEMTIME-Struktur definiert eine Bezeichnung, die angezeigt wird, wenn ein bestimmter SYSTEMTIME-Eigenschaftswert erkannt wird.
ms.assetid: 307b490a-af8e-4f2a-a45a-33a84fcb4d5c
title: LABELED_SYSTEMTIME-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_SYSTEMTIME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 94ce2a2e0b86c24ea6c16627fd0b866e18aaf48f3c1f0b318a601809e1ee03dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742710"
---
# <a name="labeled_systemtime-structure"></a>BEZEICHNETE \_ SYSTEMTIME-Struktur

Die **LABELED \_ SYSTEMTIME-Struktur** definiert eine Bezeichnung, die angezeigt wird, wenn ein bestimmter SYSTEMTIME-Eigenschaftswert erkannt wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _LABELED_SYSTEMTIME {
  SYSTEMTIME Value;
  LPSTR      Label;
} LABELED_SYSTEMTIME, *LPLABELED_SYSTEMTIME;
```



## <a name="members"></a>Member

<dl> <dt>

**Wert**
</dt> <dd>

SYSTEMTIME-Wert einer Eigenschaft, die Sie erkennen möchten.

</dd> <dt>

**Label**
</dt> <dd>

Textbeschreibung oder Bezeichnung, die angezeigt wird, wenn der im **Wertmember** angegebene SYSTEMTIME-Wert erkannt wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der **lpLabeledSystemTimeTable-Member** der [SET-Struktur](set.md) verweist auf ein Array von **SET-Strukturen,** die ein oder mehrere Bezeichnungswertpaare definieren. Die Paare werden verwendet, wenn Sie eine Bezeichnung anstelle eines bestimmten LARGEINT-Werts anzeigen möchten, der im Protokollpaket gefunden wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 




