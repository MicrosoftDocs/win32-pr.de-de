---
description: Die Struktur der Treiber \_ Informationen \_ 1 identifiziert einen Druckertreiber.
ms.assetid: 9435192b-3eba-4937-8cd3-bff4e9eb84d3
title: DRIVER_INFO_1 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_1
- _DRIVER_INFO_1A
- _DRIVER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 21301cdab4449d0a48254660d195d4f2507a80e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360790"
---
# <a name="driver_info_1-structure"></a>Struktur der Treiber \_ Info \_ 1

Die Struktur der **Treiber \_ Informationen \_ 1** identifiziert einen Druckertreiber.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DRIVER_INFO_1 {
  LPTSTR pName;
} DRIVER_INFO_1, *PDRIVER_INFO_1;
```



## <a name="members"></a>Member

<dl> <dt>

**pName**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen eines Druckertreibers angibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Treiber \_ Informationen \_ 1W** (Unicode) und **\_ Treiber \_ Info \_ 1a** (ANSI)<br/>                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Enumprinterdrivers**](enumprinterdrivers.md)
</dt> </dl>

 

 




