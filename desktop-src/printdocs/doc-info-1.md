---
description: Die \_ DOC INFO \_ 1-Struktur beschreibt ein Dokument, das gedruckt wird.
ms.assetid: 142d988b-dd74-4312-8b27-331a7ec70344
title: DOC_INFO_1-Struktur (Winspool.h)
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
ms.openlocfilehash: f534031da1c8f8f50309d4a2db0bfa39fe272ac34f59d1b490c24026d8fee261
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950000"
---
# <a name="doc_info_1-structure"></a>\_DOC INFO \_ 1-Struktur

Die **DOC \_ INFO \_ 1-Struktur** beschreibt ein Dokument, das gedruckt wird.

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

**pDocName**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Dokuments angibt.

</dd> <dt>

**pOutputFile**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen einer Ausgabedatei angibt. Um auf einem Drucker zu drucken, legen Sie diesen auf **NULL** fest.

</dd> <dt>

**pDatatype**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Datentyp identifiziert, der zum Aufzeichnen des Dokuments verwendet wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ DOC \_ INFO \_ 1W** (Unicode) und **\_ DOC INFO \_ \_ 1A** (ANSI)<br/>                                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> </dl>

 

 




