---
description: In der doc \_ Info \_ 3-Struktur wird ein Dokument beschrieben, das gedruckt wird.
ms.assetid: 6e7b6727-da04-4f67-af77-6b51c68a4eb3
title: DOC_INFO_3 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_3
- _DOC_INFO_3A
- _DOC_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 85d1d0f6af2eece8f9bd58112347478ec384642a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347557"
---
# <a name="doc_info_3-structure"></a>DOC \_ Info \_ 3-Struktur

In der **doc \_ Info \_ 3** -Struktur wird ein Dokument beschrieben, das gedruckt wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DOC_INFO_3 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwFlags;
} DOC_INFO_3, *PDOC_INFO_3;
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

**dwFlags**
</dt> <dd>

Fahren. Derzeit kann der Wert **null** oder der folgende sein.



| Flag                 | Bedeutung                                                                                                                                          |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| DI \_ memorymap \_ schreiben | Bewirkt, dass [**StartDocPrinter**](startdocprinter.md) [**AddJob**](addjob.md) und [**schedulejob**](schedulejob.md) nicht für das lokale Drucken verwendet. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die \_ Schreib Einstellung di memorymap \_ in **doc \_ Info \_ 3** ist eine Optimierung. Dadurch kann GDI Spooldateien in der Anwendung zuordnen und die Aufzeichnung beschleunigen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Doc \_ Info \_ 3W** (Unicode) und **\_ doc \_ Info \_ 3a** (ANSI)<br/>                                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**ScheduleJob**](schedulejob.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> </dl>

 

 




