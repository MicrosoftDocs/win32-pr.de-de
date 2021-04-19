---
description: Die triggerstruktur zeigt eine Aktion an, die vom Treiber zu einem bestimmten Zeitpunkt ausgeführt werden soll.
ms.assetid: 63541796-b0d8-456c-8544-697fedbe05f7
title: Auslöse Struktur (Netmon. h)
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
ms.openlocfilehash: d9b385557e3c34bdf75f2bf959d4e5e3e47e0750
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349592"
---
# <a name="trigger-structure"></a>Auslöse Struktur

Die **triggerstruktur** zeigt eine Aktion an, die vom Treiber zu einem bestimmten Zeitpunkt ausgeführt werden soll.

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

**Triggeractive**
</dt> <dd>

Ein boolescher Wert, der bestimmt, ob der-Treiber dem Treiber Aufmerksamkeit geschenkt werden sollte.

</dd> <dt>

**TriggerType**
</dt> <dd>

Der OP-Code des Auslösers.

</dd> <dt>

**TriggerAction**
</dt> <dd>

Aktion, die der-Triggervorgang ausführen soll, wenn er ausgelöst wird.

</dd> <dt>

**Triggerflags**
</dt> <dd>

Auslöserflags.

</dd> <dt>

**Triggerpatternmatch**
</dt> <dd>

Die auslösende Muster Übereinstimmung

</dd> <dt>

**Triggerbuffersize**
</dt> <dd>

Puffergröße des Auslösers.

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
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




