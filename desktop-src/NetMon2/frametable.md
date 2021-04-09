---
description: Die Frametable-Struktur, ein Zirkel Puffer von Frame Zeigern, wird an Anwendungen zurückgegeben, die an die ITRC-Schnittstelle der NPP angefügt sind.
ms.assetid: 6e2d4f8d-46f2-4d53-bc28-7b0706663490
title: Frametable-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAMETABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 95d7930d7943b26ebba1bb194d083ca8beb9dcf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128352"
---
# <a name="frametable-structure"></a>Frametable-Struktur

Die **Frametable** -Struktur, ein Zirkel Puffer von Frame Zeigern, wird an Anwendungen zurückgegeben, die an die **ITRC** -Schnittstelle der NPP angefügt sind.

## <a name="syntax"></a>Syntax


```C++
typedef struct _FRAMETABLE {
  DWORD            FrameTableLength;
  DWORD            StartIndex;
  DWORD            EndIndex;
  DWORD            FrameCount;
  FRAME_DESCRIPTOR Frames[1];
} FRAMETABLE, *LPFRAMETABLE;
```



## <a name="members"></a>Member

<dl> <dt>

**Frametablelength**
</dt> <dd>

Die Gesamtlänge der Tabelle.

</dd> <dt>

**Start Index**
</dt> <dd>

Der erste Index in der Tabelle.

</dd> <dt>

**EndIndex sein**
</dt> <dd>

Der letzte Index in der Tabelle.

</dd> <dt>

**FrameCount**
</dt> <dd>

Die Anzahl der Frames, die von dieser Tabelle beschrieben werden.

</dd> <dt>

**Frames**
</dt> <dd>

Das tatsächliche Array von Frame Deskriptoren.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




