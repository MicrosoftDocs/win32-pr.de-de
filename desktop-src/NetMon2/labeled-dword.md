---
description: Die Bezeichnung \_ DWORD-Struktur definiert eine Bezeichnung, die angezeigt wird, wenn ein bestimmter DWORD-Eigenschafts Wert erkannt wird.
ms.assetid: 1aed3226-6d69-41b0-860b-4ffb5b905f1a
title: LABELED_DWORD Struktur (Netmon. h)
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
ms.openlocfilehash: 0bec068622683172116bf8c4f6e88450d5752920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217171"
---
# <a name="labeled_dword-structure"></a>Bezeichnete \_ DWORD-Struktur

Die **Bezeichnung \_ DWORD** -Struktur definiert eine Bezeichnung, die angezeigt wird, wenn ein bestimmter DWORD-Eigenschafts Wert erkannt wird.

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

Der DWORD-Wert der Eigenschaft, die Sie erkennen möchten.

</dd> <dt>

**Label**
</dt> <dd>

Die Textbeschreibung oder Bezeichnung, die angezeigt wird, wenn der im **Wertmember** angegebene DWORD-Wert erkannt wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der **lplabeleddwordtable** -Member der [set](set.md) -Struktur verweist auf ein Array von **set** -Strukturen, die ein **oder mehrere** Bezeichnungs Member der DWORD-Wertpaare definieren. Die Paare werden verwendet, wenn Sie eine Bezeichnung anstelle eines bestimmten DWORD-Werts anzeigen möchten, der im Protokoll Paket enthalten ist.

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

 

 




