---
description: In der doc \_ Info \_ 2-Struktur wird ein Dokument beschrieben, das gedruckt wird.
ms.assetid: d62333f3-cc39-4c9b-8fb3-02a2d24bbbad
title: DOC_INFO_2 Struktur (winspool. h)
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
ms.openlocfilehash: c76b66711883e2238e971cb26d071716bd52ca54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364150"
---
# <a name="doc_info_2-structure"></a>DOC \_ Info \_ 2-Struktur

In der **doc \_ Info \_ 2** -Struktur wird ein Dokument beschrieben, das gedruckt wird.

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

**pdocname**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Dokuments angibt.

</dd> <dt>

**poutputfile**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen einer Ausgabedatei angibt.

</dd> <dt>

**pdatatype**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Datentyp identifiziert, der zum Aufzeichnen des Dokuments verwendet wird.

</dd> <dt>

**dwmode**
</dt> <dd>

Informiert den Druck Spooler über die Art der Daten, die befolgt werden sollen. Wenn dieser Wert 0 (null) ist, behandelt der Druck Spooler die Daten, die durch nachfolgende Aufrufe an den [**Schreib Drucker**](writeprinter.md) als normaler Druckauftrag gesendet werden (unabhängig davon, ob er gespooltet ist, hängt von der Drucker Eigenschaft ab). Wenn dieser Wert di- \_ Channel ist, wird nur ein Kommunikationskanal geöffnet. In diesem Fall werden die an nachfolgende Aufrufe von " **Write Printer** " übergebenen Daten an den Drucker gesendet, oder bei nachfolgenden Aufrufen von "read [**Printer**](readprinter.md) " werden Daten vom Drucker abgerufen. Dieser Modus bleibt wirksam, bis [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) aufgerufen wird.

</dd> <dt>

**JobId**
</dt> <dd>

Für die interne Verwendung reserviert. muss 0 (null) sein.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Doc \_ Info \_ 2W** (Unicode) und **\_ doc \_ Info \_ 2a** (ANSI)<br/>                                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)
</dt> <dt>

[**Lesen von Druckern**](readprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**"Write Printer"**](writeprinter.md)
</dt> </dl>

 

 




