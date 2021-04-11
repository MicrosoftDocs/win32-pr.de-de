---
description: Die Struktur von Datatypes \_ Info \_ 1 enthält Informationen zum Datentyp, der zum Aufzeichnen eines Druckauftrags verwendet wird.
ms.assetid: 6169006c-12d4-4608-865c-732f04107f9f
title: DATATYPES_INFO_1 Struktur (winspool. h)
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
ms.openlocfilehash: e7259f6559220697538774fef8d2460318df84c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215981"
---
# <a name="datatypes_info_1-structure"></a>Datatypes \_ Info \_ 1-Struktur

Die Struktur von **Datatypes \_ Info \_ 1** enthält Informationen zum Datentyp, der zum Aufzeichnen eines Druckauftrags verwendet wird.

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

Zeiger auf eine auf NULL endende Zeichenfolge, die den Datentyp identifiziert, der zum Aufzeichnen eines Druckauftrags verwendet wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Datatypes \_ Info \_ 1W** (Unicode) und **\_ Datatypes \_ Info \_ 1a** (ANSI)<br/>                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Enumprintprocessordatatypes**](enumprintprocessordatatypes.md)
</dt> </dl>

 

 




