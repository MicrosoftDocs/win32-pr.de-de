---
description: Die TRIGGER-Struktur gibt eine Aktion an, die vom Treiber zu einem bestimmten Zeitpunkt ausgeführt werden soll.
ms.assetid: 63541796-b0d8-456c-8544-697fedbe05f7
title: TRIGGER-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TRIGGER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 99404c8e9fc48e0ab85b956dd84af39b11eb87b22c87b4f9a232bd5b72d32143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363018"
---
# <a name="trigger-structure"></a>TRIGGER-Struktur

Die **TRIGGER-Struktur** gibt eine Aktion an, die vom Treiber zu einem bestimmten Zeitpunkt ausgeführt werden soll.

## <a name="syntax"></a>Syntax


```C++
typedef struct _TRIGGER {
  BOOL         TriggerActive;
  BYTE         TriggerType;
  BYTE         TriggerAction;
  DWORD        TriggerFlags;
  PATTERNMATCH TriggerPatternMatch;
  DWORD        TriggerBufferSize;
  DWORD        Reserved;
} TRIGGER, *LPTRIGGER;
```



## <a name="members"></a>Member

<dl> <dt>

**TriggerActive**
</dt> <dd>

Ein boolescher Wert, der bestimmt, ob der Trigger vom Treiber beachtet werden soll.

</dd> <dt>

**TriggerType**
</dt> <dd>

Der Op-Code des Triggers.

</dd> <dt>

**Triggeraction**
</dt> <dd>

Aktion, die der Trigger ergreifen soll, wenn er ausgelöst wird.

</dd> <dt>

**TriggerFlags**
</dt> <dd>

Triggerflags.

</dd> <dt>

**TriggerPatternMatch**
</dt> <dd>

Die Triggermuster-Übereinstimmung.

</dd> <dt>

**TriggerBufferSize**
</dt> <dd>

Triggerpuffergröße.

</dd> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




