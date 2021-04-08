---
description: Die PF- \_ nach Verfolgungs Struktur definiert ein Protokoll, das Netzwerkmonitor dem nachfolgenden Satz eines Parsers hinzufügt.
ms.assetid: 931ae70f-8c5e-4b7a-aae6-64a33dac3b23
title: PF_FOLLOWENTRY Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f93ec4784fc8d0f92f68fdff3914e230ffd3cdce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866263"
---
# <a name="pf_followentry-structure"></a>PF-nach Verfolgungs \_ Struktur

Die **PF \_** -nach Verfolgungs Struktur definiert ein Protokoll, das Netzwerkmonitor dem nachfolgenden Satz eines Parsers hinzufügt.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PF_FOLLOWENTRY {
  char szProtocol[MAX_PROTOCOL_NAME_LEN];
} PF_FOLLOWENTRY, *PPF_FOLLOWENTRY;
```



## <a name="members"></a>Member

<dl> <dt>

**szprotocol**
</dt> <dd>

Der Name des Protokolls.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [PF \_](pf-followset.md) -nach Verfolgungs Struktur verwendet ein Array von **PF \_** -after-Entry-Strukturen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[PF-nach \_ Verfolgung](pf-followset.md)
</dt> </dl>

 

 




