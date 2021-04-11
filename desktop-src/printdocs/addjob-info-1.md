---
description: Die Struktur AddJob \_ Info \_ 1 identifiziert einen Druckauftrag sowie das Verzeichnis und die Datei, in der eine Anwendung den Auftrag speichern kann.
ms.assetid: de915932-11a7-47e8-9be9-edab76d94189
title: ADDJOB_INFO_1 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDJOB_INFO_1
- _ADDJOB_INFO_1A
- _ADDJOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 08197a6a72da7e38a349014e08d2d2c2c946f6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218228"
---
# <a name="addjob_info_1-structure"></a>AddJob \_ Info \_ 1-Struktur

Die Struktur **AddJob \_ Info \_ 1** identifiziert einen Druckauftrag sowie das Verzeichnis und die Datei, in der eine Anwendung den Auftrag speichern kann.

## <a name="syntax"></a>Syntax


```C++
typedef struct _ADDJOB_INFO_1 {
  LPTSTR Path;
  DWORD  JobId;
} ADDJOB_INFO_1, *PADDJOB_INFO_1;
```



## <a name="members"></a>Member

<dl> <dt>

**Pfad**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Pfad und den Dateinamen enthält, die die Anwendung zum Speichern des Druckauftrags verwenden kann.

</dd> <dt>

**JobId**
</dt> <dd>

Ein Handle für den Druckauftrag.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ AddJob \_ Info \_ 1W** (Unicode) und **\_ AddJob \_ Info \_ 1a** (ANSI)<br/>                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> </dl>

 

 




