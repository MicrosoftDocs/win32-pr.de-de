---
description: Die PF- \_ handoffset-Struktur definiert die Protokolle, die an den Parser übergeben werden, oder die Protokolle, an die der Parser übergibt.
ms.assetid: 2fda399d-a09e-47b4-bb2e-95996de9f950
title: PF_HANDOFFSET Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1b5dc9620f3b1860b27af973432aa4218c05b63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368041"
---
# <a name="pf_handoffset-structure"></a>PF- \_ handoffset-Struktur

Die **PF- \_ handoffset** -Struktur definiert die Protokolle, die an den Parser übergeben werden, oder die Protokolle, an die der Parser übergibt.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PF_HANDOFFSET {
  DWORD           nEntries;
  PF_HANDOFFENTRY Entry[];
} PF_HANDOFFSET, *PPF_HANDOFFSET;
```



## <a name="members"></a>Member

<dl> <dt>

**nentries**
</dt> <dd>

Anzahl von Protokollen.

</dd> <dt>

**Eingabe**
</dt> <dd>

Ein Array von [PF- \_ handoffentry](pf-handoffentry.md) -Strukturen, die jedes Protokoll definieren.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [PF \_](pf-parserinfo.md) -Parameter Info-Struktur verwendet die **PF- \_ handoffset** -Struktur, um Folgendes aufzulisten:

-   Die Protokolle, die an den Parser übergeben werden.
-   Die Protokolle, an die der Parser übergibt.

Die **PF- \_ handoffset** -Struktur muss mithilfe von **heapzuzuordnungs** zugeordnet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[PF-Parameter \_ Info](pf-parserinfo.md)
</dt> <dt>

[PF- \_ handoffentry](pf-handoffentry.md)
</dt> </dl>

 

 




