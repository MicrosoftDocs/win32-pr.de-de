---
description: Die MONITOR \_ INFO \_ 1-Struktur identifiziert einen installierten Monitor.
ms.assetid: 7a4660bd-5df8-49dd-92f6-9574f451f10d
title: MONITOR_INFO_1 -Struktur (Winspool.h)
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
ms.openlocfilehash: dff4fa4913be25d8a7cb5cd3324bd6e13d68761147fa76c451b587fb9569257d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099084"
---
# <a name="monitor_info_1-structure"></a>MONITOR \_ INFO \_ 1-Struktur

Die **MONITOR \_ INFO \_ 1-Struktur** identifiziert einen installierten Monitor.

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

Ein Zeiger auf eine auf NULL terminierte Zeichenfolge, die einen installierten Monitor identifiziert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ MONITOR \_ INFO \_ 1W** (Unicode) und **\_ MONITOR INFO \_ \_ 1A** (ANSI)<br/>                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumMonitors**](enummonitors.md)
</dt> <dt>

[**ÜBERWACHEN \_ VON INFORMATIONEN \_ 2**](monitor-info-2.md)
</dt> </dl>

 

 




