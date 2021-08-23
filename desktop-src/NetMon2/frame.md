---
description: Ein tatsächlicher Frame des Treibers.
ms.assetid: 867082c1-196a-4580-ba24-187b0752f6f8
title: FRAME-Struktur (Netmon.h)
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
ms.openlocfilehash: 7447e0ba8e13a593af6ac346ad47f8fe992b4a3187f0c46e8ee8fc28ddeb5646
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910950"
---
# <a name="frame-structure"></a>FRAME-Struktur

Die **FRAME-Struktur** ist ein tatsächlicher Frame des Treibers.

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

**Timestamp**
</dt> <dd>

Verstrichene Zeit in Mikrosekunden zwischen dem Start der Erfassung und der Zeit, zu der der Frame erfasst wurde.

</dd> <dt>

**FrameLength**
</dt> <dd>

MAC-Framelänge.

</dd> <dt>

**nBytesAvail**
</dt> <dd>

Die tatsächliche Framelänge, die kopiert wurde.

</dd> <dt>

**MacFrame**
</dt> <dd>

Framedaten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




