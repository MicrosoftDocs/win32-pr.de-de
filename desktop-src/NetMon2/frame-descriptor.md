---
description: Die Frame \_ deskriptorstruktur stellt beschreibende Informationen zu rohframes bereit.
ms.assetid: f2fc256e-8e64-49c1-b2ad-ef656762d5c7
title: FRAME_DESCRIPTOR Struktur (Netmon. h)
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
ms.openlocfilehash: c327ce1568eec07aabe3334013dae8b720ab7446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344404"
---
# <a name="frame_descriptor-structure"></a>Frame \_ deskriptorstruktur

Die **Frame \_ deskriptorstruktur** stellt beschreibende Informationen zu rohframes bereit.

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

**Framezeiger**
</dt> <dd>

Zeiger auf Frame-Daten.

</dd> <dt>

**Zeitstempel**
</dt> <dd>

Die System Zeit in Mikrosekunden, zu der der Frame aufgezeichnet wurde. Diese Zeit wird normalerweise verwendet, um das Intervall zwischen dem Erfassen von zwei Frames zu bestimmen.

</dd> <dt>

**Framelength**
</dt> <dd>

Die Länge des Frames.

</dd> <dt>

**nbytesnütz**
</dt> <dd>

Die tatsächliche kopierte Frame Länge.

</dd> <dt>

**ETYPE**
</dt> <dd>

ETYPE-Name.

</dd> <dt>

**SAP**
</dt> <dd>

SAP-Wert.

</dd> <dt>

**Lowprotocol**
</dt> <dd>

Der Index des gefundenen Protokolls.

</dd> <dt>

**Lowprotocoloffset**
</dt> <dd>

Offset für Protokolldaten, die aus **lowprotocol** abgerufen werden.

</dd> <dt>

**Highport**
</dt> <dd>

Port des hohen Protokolls, identifiziert in **lowprotocol**.

</dd> <dt>

**Highprotocoloffset**
</dt> <dd>

Offset für Protokolldaten, die von **highport** abgerufen werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




