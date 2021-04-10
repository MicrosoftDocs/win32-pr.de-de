---
description: In der doc \_ Info \_ 1-Struktur wird ein Dokument beschrieben, das gedruckt wird.
ms.assetid: 142d988b-dd74-4312-8b27-331a7ec70344
title: DOC_INFO_1 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_1
- _DOC_INFO_1A
- _DOC_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 6f905a89163b46743a92c8616ee0fa3d0564590c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215860"
---
# <a name="doc_info_1-structure"></a>DOC \_ Info \_ 1-Struktur

In der **doc \_ Info \_ 1** -Struktur wird ein Dokument beschrieben, das gedruckt wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DOC_INFO_1 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
} DOC_INFO_1;
```



## <a name="members"></a>Member

<dl> <dt>

**pdocname**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Dokuments angibt.

</dd> <dt>

**poutputfile**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen einer Ausgabedatei angibt. Legen Sie diese Einstellung auf **null** fest, um Sie auf einen Drucker zu drucken.

</dd> <dt>

**pdatatype**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Datentyp identifiziert, der zum Aufzeichnen des Dokuments verwendet wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Doc \_ Info \_ 1W** (Unicode) und **\_ doc \_ Info \_ 1a** (ANSI)<br/>                                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> </dl>

 

 




