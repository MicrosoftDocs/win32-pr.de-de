---
description: Die bezeichnete \_ Wort Struktur definiert eine Bezeichnung, die angezeigt wird, wenn ein bestimmter Word-Eigenschafts Wert erkannt wird.
ms.assetid: bfb1d34e-4a07-493f-8e43-508b77cce581
title: LABELED_WORD Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_WORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 445b24245d2e9d15c1c2b6d69de20c464cbf1724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363627"
---
# <a name="labeled_word-structure"></a>Bezeichnete \_ Wort Struktur

Die **bezeichnete \_ Wort** Struktur definiert eine Bezeichnung, die angezeigt wird, wenn ein bestimmter Word-Eigenschafts Wert erkannt wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _LABELED_WORD {
  WORD  Value;
  LPSTR Label;
} LABELED_WORD, *LPLABELED_WORD;
```



## <a name="members"></a>Member

<dl> <dt>

**Wert**
</dt> <dd>

Der Wortwert der Eigenschaft, die Sie erkennen möchten.

</dd> <dt>

**Label**
</dt> <dd>

Die Textbeschreibung oder Bezeichnung, die angezeigt wird, wenn der im **Wertmember** angegebene Wortwert erkannt wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der **lplabeledwordtable** -Member der [set](set.md) -Struktur verweist auf ein Array von Set-Strukturen, um ein oder mehrere Bezeichnungs Wert Paare zu definieren. Diese Paare werden verwendet, wenn Sie eine Bezeichnung anstelle eines bestimmten Wort Werts anzeigen möchten, der in einem Protokoll Paket enthalten ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 




