---
description: Die PF-nach \_ Verfolgungs Struktur definiert die Protokolle, die möglicherweise vor oder nach einem Protokoll stehen.
ms.assetid: ef444af9-edae-4547-9548-8a682c279f08
title: PF_FOLLOWSET Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f5c286d3b137df24f7da7f0fc5ae269a7a3d946d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373136"
---
# <a name="pf_followset-structure"></a>PF-nach Verfolgungs \_ Struktur

Die **PF \_** -nach Verfolgungs Struktur definiert die Protokolle, die möglicherweise vor oder nach einem Protokoll stehen.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PF_FOLLOWSET {
  DWORD          nEntries;
  PF_FOLLOWENTRY Entry[];
} PF_FOLLOWSET, *PPF_FOLLOWSET;
```



## <a name="members"></a>Member

<dl> <dt>

**nentries**
</dt> <dd>

Anzahl der Protokolle in der Liste.

</dd> <dt>

**Eingabe**
</dt> <dd>

[ \_ Ein](pf-followentry.md) Array von PF-nach Verfolgungs Strukturen, die die einzelnen Protokolle beschreiben.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [PF \_ parserinfo](pf-parserinfo.md) -Struktur verwendet die PF-nach Verfolgungs Struktur, um die Protokolle aufzulisten, die möglicherweise dem vom Parser erkannten Protokoll vorangestellt sind. **\_**

In Netzwerkmonitor werden die Informationen in der **PF- \_ nachfolg** enden Struktur verwendet, um die folgenden Sätze spezifischer Parser zu aktualisieren. Die PF-nach Verfolgungs Struktur muss mithilfe von **heapzuw** zugeordnet werden. **\_**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[PF-nach \_ Verfolgung](pf-followentry.md)
</dt> <dt>

[PF-Parameter \_ Info](pf-parserinfo.md)
</dt> </dl>

 

 




