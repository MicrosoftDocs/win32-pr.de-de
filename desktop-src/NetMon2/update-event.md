---
description: Die Update- \_ Ereignis Struktur aktualisiert Ereignisse. Diese Struktur wird über die Ereignis Status-Rückruf Prozedur vom NPP an die aufrufenden Anwendung zurückgegeben.
ms.assetid: 6896be5a-f986-44ff-a18b-010f7b9858aa
title: UPDATE_EVENT Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UPDATE_EVENT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3da45020a68114182a71b25ff9bba380d3f89eee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348328"
---
# <a name="update_event-structure"></a>Aktualisieren der \_ Ereignis Struktur

Die **Update- \_ Ereignis** Struktur aktualisiert Ereignisse. Diese Struktur wird über die Ereignis Status-Rückruf Prozedur vom NPP an die aufrufenden Anwendung zurückgegeben.

## <a name="syntax"></a>Syntax


```C++
typedef struct _UPDATE_EVENT {
  USHORT       Event;
  DWORD        Action;
  DWORD        Status;
  DWORD        Value;
  __int64      TimeStamp;
  DWORD_PTR    lpUserContext;
  DWORD_PTR    lpReserved;
  UINT         FramesDropped;
  union {
    DWORD                        Reserved;
    LPFRAMETABLE                 lpFrameTable;
    DWORD_PTR                    lpPacketQueue;
    SECURITY_PERMISSION_RESPONSE SecurityResponse;
  };
  LPSTATISTICS lpFinalStats;
} UPDATE_EVENT, *PUPDATE_EVENT;
```



## <a name="members"></a>Member

<dl> <dt>

**Event**
</dt> <dd>

Tatsächliches Ereignis, das aufgezeichnet wird.

</dd> <dt>

**Aktion**
</dt> <dd>

Die ausgeführte Aktion.

</dd> <dt>

**Status**
</dt> <dd>

Netzwerkstatus Anzeige.

</dd> <dt>

**Wert**
</dt> <dd>

Zusätzliche Counter-Variable.

</dd> <dt>

**Zeitstempel**
</dt> <dd>

Die markierten Ereignisse in Mikrosekunden.

</dd> <dt>

**lpusercontext**
</dt> <dd>

Der Benutzer Kontext, der von der Anwendung angegeben wird.

</dd> <dt>

**lpReserved**
</dt> <dd>

Treiber-oder nal-Verwendung.

</dd> <dt>

**Framesdrop**
</dt> <dd>

RTF-Frames wurden im angegebenen Puffer abgelegt.

</dd> <dt>

**Reserved**
</dt> <dd>

Diese Switch-Option gibt keine Daten zurück.

</dd> <dt>

**lpframetable**
</dt> <dd>

Nur RTF.

</dd> <dt>

**lppacketqueue**
</dt> <dd>

Für überträgt.

</dd> <dt>

**Securityresponse**
</dt> <dd>

Antwort des Remote Sicherheits Monitors.

</dd> <dt>

**lpfinalstats**
</dt> <dd>

Dies wird nur bei nicht sicherheitsbezogenen Stopps (z. b. Triggern) ausgefüllt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

C++ Benutzer sollten beachten, dass sich die Deklaration für diesen Rückruf im öffentlichen Teil der Header Datei befinden sollte:

``` syntax
static WINAPI DWORD NetworkCallback( UPDATE_EVENT events);
```

Die Implementierung sollte sich im geschützten Abschnitt der CPP-Datei befinden:

``` syntax
DWORD WINAPI ClassName::NetworkCallback( UPDATE_EVENT events) {};
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




