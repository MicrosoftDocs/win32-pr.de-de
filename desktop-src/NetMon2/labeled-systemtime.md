---
description: Die bezeichnete \_ SYSTEMTIME-Struktur definiert eine Bezeichnung, die angezeigt wird, wenn ein bestimmter SYSTEMTIME-Eigenschafts Wert erkannt wird.
ms.assetid: 307b490a-af8e-4f2a-a45a-33a84fcb4d5c
title: LABELED_SYSTEMTIME Struktur (Netmon. h)
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
ms.openlocfilehash: 4484d5ec55f700410eb80d11d2249cceceef43ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868827"
---
# <a name="labeled_systemtime-structure"></a>Bezeichnete \_ SYSTEMTIME-Struktur

Die **bezeichnete \_ SYSTEMTIME** -Struktur definiert eine Bezeichnung, die angezeigt wird, wenn ein bestimmter SYSTEMTIME-Eigenschafts Wert erkannt wird.

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

Der SystemTime-Wert einer Eigenschaft, die Sie erkennen möchten.

</dd> <dt>

**Label**
</dt> <dd>

Die Textbeschreibung oder Bezeichnung, die angezeigt wird, wenn der im **Wertmember** angegebene SYSTEMTIME-Wert erkannt wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der **lplabeledsystemtimetable** -Member der [set](set.md) -Struktur verweist auf ein Array von **set** -Strukturen, die ein oder mehrere Bezeichnungs Wert Paare definieren. Die Paare werden verwendet, wenn Sie eine Bezeichnung anstelle eines bestimmten largeint-Werts anzeigen möchten, der im Protokoll Paket enthalten ist.

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

 

 




