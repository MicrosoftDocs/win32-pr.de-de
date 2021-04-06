---
description: Die Struktur von Monitor \_ Info \_ 2 identifiziert einen Monitor.
ms.assetid: 4dd1ca15-6983-403e-8159-1a6d35a88162
title: MONITOR_INFO_2 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_2
- _MONITOR_INFO_2A
- _MONITOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 9d3ad70a0728ca6e73c4dbefb248df58e858a996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759655"
---
# <a name="monitor_info_2-structure"></a>Überwachen der \_ Info \_ 2-Struktur

Die Struktur von **Monitor \_ Info \_ 2** identifiziert einen Monitor.

## <a name="syntax"></a>Syntax


```C++
typedef struct _MONITOR_INFO_2 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} MONITOR_INFO_2, *PMONITOR_INFO_2;
```



## <a name="members"></a>Member

<dl> <dt>

**pName**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Monitors ist.

</dd> <dt>

**nach-oben**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Umgebung angibt, für die der Monitor geschrieben wurde (z. b. Windows NT x86, Windows ia64, Windows x64).

</dd> <dt>

**pdllname**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die der Name der Monitor-dll ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Monitor \_ Info \_ 2W** (Unicode) und **\_ Monitor \_ Info \_ 2a** (ANSI)<br/>                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Addmonitor**](addmonitor.md)
</dt> <dt>

[**Enumüberwachungen**](enummonitors.md)
</dt> <dt>

[**Überwachen von \_ Informationen \_ 1**](monitor-info-1.md)
</dt> </dl>

 

 




