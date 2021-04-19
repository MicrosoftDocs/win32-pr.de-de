---
description: Speichert Informationen zu freigegebenen Speicherabschnitten.
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
ms.openlocfilehash: 695f3ef09cb5e7e67de757ee3926df6fde7ddff5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363225"
---
# <a name="sharedmemory_header-structure"></a>SharedMemory- \_ Header Struktur

Speichert Informationen zu freigegebenen Speicherabschnitten.

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

**cbtotal**
</dt> <dd>

Die Größe der Daten in Bytes, auf die von dieser Header Struktur verwiesen wird.

</dd> <dt>

**cboffsekunden**
</dt> <dd>

Die Größe in Bytes, in der die Seriennummern von der Header Struktur versetzt werden.

</dd> <dt>

**idxevent**
</dt> <dd>

Der Ereignis Index. Dieser Wert wird mit aufeinander folgenden Ereignissen inkrementiert.

</dd> <dt>

**dwevent**
</dt> <dd>

Das Ereignis, das diesem Header zugeordnet ist.

</dd> <dt>

**zid**
</dt> <dd>

Der Cursor Bezeichner, auf den vom Shared Memory-Header verwiesen wird.

</dd> <dt>

**sn**
</dt> <dd>

Die Seriennummer für den Header des freigegebenen Speichers.

</dd> <dt>

**sysegvt**
</dt> <dd>

Das System Ereignis, dem vorangestellten Präfix \_ \* , das diesem Header zugeordnet ist. Weitere Informationen finden Sie im Abschnitt "Hinweise".

</dd> <dt>

**syabvtdata**
</dt> <dd>

Die [**System \_ Ereignis \_ Daten**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data) Struktur, die dem System Ereignis zugeordnet ist.

</dd> <dt>

**cpakete**
</dt> <dd>

Gibt die Anzahl der Pakete an, die dem aktuellen Shared Memory-Abschnitt zugeordnet sind.

</dd> <dt>

**CB-Pakete**
</dt> <dd>

Die Größe der dem aktuellen Shared Memory-Abschnitt zugeordneten Pakete in Bytes.

</dd> <dt>

**"f"**
</dt> <dd>

Ein Flag, das angibt, ob Seriennummern im aktuellen Shared Memory-Abschnitt vorhanden sind.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die folgenden Werte sind für den **sysegvt** -Member definiert.


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

[**System \_ Ereignis \_ Daten**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data)
</dt> </dl>

 

 



