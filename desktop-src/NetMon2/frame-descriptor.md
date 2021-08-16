---
description: Die \_ FRAME-DESCRIPTOR-Struktur stellt beschreibende Informationen zu Unformatierungsframes zur Verfügung.
ms.assetid: f2fc256e-8e64-49c1-b2ad-ef656762d5c7
title: FRAME_DESCRIPTOR -Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1e675c07eae46096878e7c0aa71b53ba5bf22194e82ad8cc5aa5b6070d7e27e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938571"
---
# <a name="frame_descriptor-structure"></a>FRAME \_ DESCRIPTOR-Struktur

Die **\_ FRAME-DESCRIPTOR-Struktur** bietet beschreibende Informationen zu Unformatierungsframes.

## <a name="syntax"></a>Syntax


```C++
typedef struct _FRAME_DESCRIPTOR {
  LPBYTE       FramePointer;
  __int64      TimeStamp;
  DWORD        FrameLength;
  DWORD        nBytesAvail;
  WORD         Etype;
  BYTE         Sap;
  BYTE         LowProtocol;
  WORD         LowProtocolOffset;
  GENERIC_PORT HighPort;
  WORD         HighProtocolOffset;
} FRAME_DESCRIPTOR, *LPFRAME_DESCRIPTOR;
```



## <a name="members"></a>Member

<dl> <dt>

**FramePointer**
</dt> <dd>

Zeiger auf Framedaten.

</dd> <dt>

**Timestamp**
</dt> <dd>

Systemzeit in Mikrosekunden, als der Frame erfasst wurde. Diese Zeit wird in der Regel verwendet, um das Intervall zwischen den Zeiten zu bestimmen, zu der zwei Frames erfasst wurden.

</dd> <dt>

**FrameLength**
</dt> <dd>

Länge des Frames.

</dd> <dt>

**nBytesAvail**
</dt> <dd>

Die tatsächliche Framelänge, die kopiert wurde.

</dd> <dt>

**Etype**
</dt> <dd>

Geben Sie den Namen ein.

</dd> <dt>

**Sap**
</dt> <dd>

SAP-Wert.

</dd> <dt>

**LowProtocol**
</dt> <dd>

Index des gefundenen Protokolls.

</dd> <dt>

**LowProtocolOffset**
</dt> <dd>

Offset zu Protokolldaten, die von **LowProtocol erhalten wurden.**

</dd> <dt>

**HighPort**
</dt> <dd>

Port mit hohem Protokoll, der in **LowProtocol identifiziert wird.**

</dd> <dt>

**HighProtocolOffset**
</dt> <dd>

Offset zu Protokolldaten, die von **HighPort erhalten wurden.**

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




