---
description: Ein tatsächlicher Frame des Treibers.
ms.assetid: 867082c1-196a-4580-ba24-187b0752f6f8
title: Frame-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b4ff8d66f88b18988cbb33bbcd8196cc01177b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344661"
---
# <a name="frame-structure"></a>Frame Struktur

Die **Frame** -Struktur ist ein tatsächlicher Frame des Treibers.

## <a name="syntax"></a>Syntax


```C++
typedef struct _FRAME {
  __int64 TimeStamp;
  DWORD   FrameLength;
  DWORD   nBytesAvail;
  BYTE    MacFrame[];
} FRAME, *LPFRAME, *ULPFRAME;
```



## <a name="members"></a>Member

<dl> <dt>

**Zeitstempel**
</dt> <dd>

Verstrichene Zeit (in Mikrosekunden) zwischen dem Start der Erfassung und dem Zeitpunkt, zu dem der Rahmen aufgezeichnet wurde.

</dd> <dt>

**Framelength**
</dt> <dd>

Mac-Frame Länge.

</dd> <dt>

**nbytesnütz**
</dt> <dd>

Die tatsächliche kopierte Frame Länge.

</dd> <dt>

**Macframe**
</dt> <dd>

Frame-Daten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




