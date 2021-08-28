---
description: Die MONITOR \_ INFO \_ 2-Struktur identifiziert einen Monitor.
ms.assetid: 4dd1ca15-6983-403e-8159-1a6d35a88162
title: MONITOR_INFO_2-Struktur (Winspool.h)
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
ms.openlocfilehash: c01377740c77ef4cb2be15e785b9ea3e93449944c11f2014ed660d8c3e3245b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112330"
---
# <a name="monitor_info_2-structure"></a>MONITOR \_ INFO \_ 2-Struktur

Die **MONITOR \_ INFO \_ 2-Struktur** identifiziert einen Monitor.

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

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die dem Namen des Monitors entspricht.

</dd> <dt>

**pEnvironment**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Umgebung angibt, für die der Monitor geschrieben wurde (z. B. Windows NT x86, Windows IA64, Windows x64).

</dd> <dt>

**pDLLName**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die dem Namen der Monitor-DLL entspricht.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ MONITOR \_ INFO \_ 2W** (Unicode) und **\_ MONITOR INFO \_ \_ 2A** (ANSI)<br/>                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddMonitor**](addmonitor.md)
</dt> <dt>

[**EnumMonitors**](enummonitors.md)
</dt> <dt>

[**MONITOR \_ INFO \_ 1**](monitor-info-1.md)
</dt> </dl>

 

 




