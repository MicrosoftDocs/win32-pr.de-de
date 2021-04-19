---
description: Die Struktur von Monitor \_ Info \_ 1 identifiziert einen installierten Monitor.
ms.assetid: 7a4660bd-5df8-49dd-92f6-9574f451f10d
title: MONITOR_INFO_1 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_1
- _MONITOR_INFO_1A
- _MONITOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b6af1e1b9111ac6221273f2faf68fc6ed70e07a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353448"
---
# <a name="monitor_info_1-structure"></a>Überwachen der \_ Info \_ 1-Struktur

Die Struktur von **Monitor \_ Info \_ 1** identifiziert einen installierten Monitor.

## <a name="syntax"></a>Syntax


```C++
typedef struct _MONITOR_INFO_1 {
  LPTSTR pName;
} MONITOR_INFO_1, *PMONITOR_INFO_1;
```



## <a name="members"></a>Member

<dl> <dt>

**pName**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen installierten Monitor identifiziert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Überwachen von \_ Informationen \_ 1W** (Unicode) und **\_ Überwachen von \_ Informationen \_ 1a** (ANSI)<br/>                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Enumüberwachungen**](enummonitors.md)
</dt> <dt>

[**Überwachen von \_ Informationen \_ 2**](monitor-info-2.md)
</dt> </dl>

 

 




