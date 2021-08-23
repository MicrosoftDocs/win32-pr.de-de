---
description: Die \_ DOC INFO \_ 2-Struktur beschreibt ein Dokument, das gedruckt wird.
ms.assetid: d62333f3-cc39-4c9b-8fb3-02a2d24bbbad
title: DOC_INFO_2-Struktur (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_2
- _DOC_INFO_2A
- _DOC_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 27d7753fa16abcfbc30b28bcc4343b2e1ef7996cad408b54fefb850feac9b17e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846260"
---
# <a name="doc_info_2-structure"></a>\_DOC INFO \_ 2-Struktur

Die **DOC \_ INFO \_ 2-Struktur** beschreibt ein Dokument, das gedruckt wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DOC_INFO_2 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwMode;
  DWORD  JobId;
} DOC_INFO_2, *PDOC_INFO_2;
```



## <a name="members"></a>Member

<dl> <dt>

**pDocName**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Dokuments angibt.

</dd> <dt>

**pOutputFile**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen einer Ausgabedatei angibt.

</dd> <dt>

**pDatatype**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Datentyp identifiziert, der zum Aufzeichnen des Dokuments verwendet wird.

</dd> <dt>

**dwMode**
</dt> <dd>

Informiert den Druckspooler über die Art der zu befolgenden Daten. Wenn dieser Wert 0 (null) ist, behandelt der Druckspooler die daten, die durch nachfolgende Aufrufe von [**WritePrinter**](writeprinter.md) gesendet werden, als normalen Druckauftrag (ob er gespoolt wird, hängt von der Druckereigenschaft ab). Wenn dieser Wert DI \_ CHANNEL ist, wird nur ein Kommunikationskanal geöffnet. In diesem Fall werden die an nachfolgende Aufrufe von **WritePrinter** übergebenen Daten an den Drucker gesendet, oder nachfolgende Aufrufe von [**ReadPrinter**](readprinter.md) rufen Daten vom Drucker ab. Dieser Modus bleibt wirksam, bis [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) aufgerufen wird.

</dd> <dt>

**Jobid**
</dt> <dd>

Für die interne Verwendung reserviert; sollte 0 (null) sein.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ DOC \_ INFO \_ 2W** (Unicode) und **\_ DOC INFO \_ \_ 2A** (ANSI)<br/>                                   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)
</dt> <dt>

[**ReadPrinter**](readprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




