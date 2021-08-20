---
description: Speichert Informationen zu Shared Memory-Abschnitten.
ms.assetid: 73a650ee-110c-43f2-a5e2-783d52fd29ee
title: SHAREDMEMORY_HEADER Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHAREDMEMORY_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9ae596819feb4bd70aa47e7881521e5a69e5bd0a509b974e591d08907efda51c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966799"
---
# <a name="sharedmemory_header-structure"></a>SHAREDMEMORY \_ HEADER-Struktur

Speichert Informationen zu Shared Memory-Abschnitten.

## <a name="syntax"></a>Syntax


```C++
typedef struct _SHAREDMEMORY_HEADER {
  DWORD             cbTotal;
  DWORD             cbOffsetSns;
  DWORD             idxEvent;
  DWORD             dwEvent;
  CURSOR_ID         cid;
  DWORD             sn;
  SYSTEM_EVENT      sysEvt;
  SYSTEM_EVENT_DATA sysEvtData;
  DWORD             cPackets;
  DWORD             cbPackets;
  BOOL              fSnsPresent;
} SHAREDMEMORY_HEADER, *PSHAREDMEMORY_HEADER;
```



## <a name="members"></a>Member

<dl> <dt>

**cbTotal**
</dt> <dd>

Die Größe der Daten in Bytes, auf die von dieser Headerstruktur verwiesen wird.

</dd> <dt>

**cbOffsetSns**
</dt> <dd>

Die Größe in Bytes, in der die Seriennummern von der Headerstruktur versetzt werden.

</dd> <dt>

**idxEvent**
</dt> <dd>

Der Ereignisindex. Dieser Wert wird mit aufeinander folgenden Ereignissen erhöht.

</dd> <dt>

**dwEvent**
</dt> <dd>

Das diesem Header zugeordnete Ereignis.

</dd> <dt>

**Cid**
</dt> <dd>

Der Cursorbezeichner, auf den der Shared Memory-Header verweist.

</dd> <dt>

**sn**
</dt> <dd>

Die Seriennummer für den Shared Memory-Header.

</dd> <dt>

**sysEvt**
</dt> <dd>

Das Systemereignis mit dem Präfix SE \_ \* , das diesem Header zugeordnet ist. Weitere Informationen finden Sie im Abschnitt "Hinweise".

</dd> <dt>

**sysEvtData**
</dt> <dd>

Die [**SYSTEM \_ EVENT \_ DATA-Struktur,**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data) die dem Systemereignis zugeordnet ist.

</dd> <dt>

**cPackets**
</dt> <dd>

Die Anzahl der Pakete, die dem aktuellen Shared Memory-Abschnitt zugeordnet sind.

</dd> <dt>

**cbPackets**
</dt> <dd>

Die Größe der Pakete, die dem aktuellen Shared Memory-Abschnitt zugeordnet sind, in Bytes.

</dd> <dt>

**fSnsPresent**
</dt> <dd>

Ein Flag, das angibt, ob Seriennummern im aktuellen Shared Memory-Abschnitt vorhanden sind.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die folgenden Werte werden für den **sysEvt-Member** definiert.


```C++
#define SE_NONE                  0x00000000
#define SE_TAP                   0x00000010
#define SE_DBL_TAP               0x00000011
#define SE_RIGHT_TAP             0x00000012
#define SE_DRAG                  0x00000013
#define SE_RIGHT_DRAG            0x00000014
#define SE_HOLD_ENTER            0x00000015
#define SE_HOLD_LEAVE            0x00000016
#define SE_HOVER_ENTER           0x00000017
#define SE_HOVER_LEAVE           0x00000018
#define SE_FLICK                 0x0000001F
```



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_ \_ SYSTEMEREIGNISDATEN**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data)
</dt> </dl>

 

 



