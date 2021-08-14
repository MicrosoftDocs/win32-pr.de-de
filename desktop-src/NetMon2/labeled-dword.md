---
description: Die LABELED \_ DWORD-Struktur definiert eine Bezeichnung, die angezeigt wird, wenn ein bestimmter DWORD-Eigenschaftswert erkannt wird.
ms.assetid: 1aed3226-6d69-41b0-860b-4ffb5b905f1a
title: LABELED_DWORD -Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_DWORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 10f3e0dd09b37821a00f2c10f99c0ea6d509ff388e9d7394a8b2c4958438f979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364845"
---
# <a name="labeled_dword-structure"></a>LABELED \_ DWORD-Struktur

Die **LABELED \_ DWORD-Struktur** definiert eine Bezeichnung, die angezeigt wird, wenn ein bestimmter DWORD-Eigenschaftswert erkannt wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _LABELED_DWORD {
  DWORD Value;
  LPSTR Label;
} LABELED_DWORD, *LPLABELED_DWORD;
```



## <a name="members"></a>Member

<dl> <dt>

**Wert**
</dt> <dd>

DWORD-Wert der Eigenschaft, die Sie erkennen möchten.

</dd> <dt>

**Label**
</dt> <dd>

Textbeschreibung oder Bezeichnung, die angezeigt wird, wenn der im **Value-Member** angegebene DWORD-Wert erkannt wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der **lpLabeledDwordTable-Member** der [SET-Struktur](set.md) verweist auf ein Array von **SET-Strukturen,** die einen oder mehrere **Label-Member** der DWORD-Wertpaare definieren. Die Paare werden verwendet, wenn Sie eine Bezeichnung statt eines bestimmten DWORD-Werts anzeigen möchten, der im Protokollpaket gefunden wird.

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

 

 




