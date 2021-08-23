---
description: Die DATATYPES INFO 1-Struktur enthält Informationen zum Datentyp, der zum \_ \_ Aufzeichnen eines Druckauftrags verwendet wird.
ms.assetid: 6169006c-12d4-4608-865c-732f04107f9f
title: DATATYPES_INFO_1 -Struktur (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DATATYPES_INFO_1
- _DATATYPES_INFO_1A
- _DATATYPES_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 05defe3d8cc6cd66b15b2cacdd3d3d1d56c348e4946a43700278f100ea17da5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719670"
---
# <a name="datatypes_info_1-structure"></a>DATATYPES \_ INFO \_ 1-Struktur

Die **DATATYPES \_ INFO \_ 1-Struktur** enthält Informationen zum Datentyp, der zum Aufzeichnen eines Druckauftrags verwendet wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DATATYPES_INFO_1 {
  LPTSTR pName;
} DATATYPES_INFO_1, *PDATATYPES_INFO_1;
```



## <a name="members"></a>Member

<dl> <dt>

**pName**
</dt> <dd>

Zeiger auf eine auf NULL beendete Zeichenfolge, die den Datentyp identifiziert, der zum Aufzeichnen eines Druckauftrags verwendet wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ DATATYPES \_ INFO \_ 1W** (Unicode) und **\_ DATATYPES \_ INFO \_ 1A** (ANSI)<br/>                       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md)
</dt> </dl>

 

 




