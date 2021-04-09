---
description: Die bezeichnete \_ largeint-Struktur definiert eine Bezeichnung, die angezeigt wird, wenn ein bestimmter largeint-Eigenschafts Wert erkannt wird.
ms.assetid: ca565be0-96bb-4265-9422-793db0723563
title: LABELED_LARGEINT Struktur (Netmon. h)
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
ms.openlocfilehash: 4de92c3e67567ef86bb3d46905e595bd9d54c194
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042325"
---
# <a name="labeled_largeint-structure"></a>Bezeichnung \_ largeint-Struktur

Die **bezeichnete \_ largeint** -Struktur definiert eine Bezeichnung, die angezeigt wird, wenn ein bestimmter largeint-Eigenschafts Wert erkannt wird.

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

Largeint-Wert der Eigenschaft, die Sie erkennen möchten.

</dd> <dt>

**Label**
</dt> <dd>

Die Textbeschreibung oder Bezeichnung, die angezeigt wird, wenn der im **Wertmember** angegebene largeint-Wert erkannt wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der **lplabeledlargeintting** -Member der [set](set.md) -Struktur verweist auf ein Array von **set** -Strukturen, die ein **oder mehrere** Bezeichnungs Member der largeint-Wertpaare definieren. Die Paare werden verwendet, wenn Sie eine Bezeichnung anstelle eines bestimmten largeint-Werts anzeigen möchten, der in einem Protokoll Paket enthalten ist.

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

 

 




