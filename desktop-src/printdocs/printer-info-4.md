---
description: Die \_ PRINTER INFO \_ 4-Struktur gibt allgemeine Druckerinformationen an. Die -Struktur kann verwendet werden, um minimale Druckerinformationen bei einem Aufruf von EnumPrinters abzurufen.
ms.assetid: 81bd0eab-dc1e-4cf1-8f63-3686f1711c1f
title: PRINTER_INFO_4-Struktur (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_4
- _PRINTER_INFO_4A
- _PRINTER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3ba6e372b495c47dd92e61e51ba6487e6d9c2c0aca924bf6ed3a092ba0816820
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119446990"
---
# <a name="printer_info_4-structure"></a>PRINTER \_ INFO \_ 4-Struktur

Die **PRINTER \_ INFO \_ 4-Struktur** gibt allgemeine Druckerinformationen an.

Die -Struktur kann verwendet werden, um minimale Druckerinformationen bei einem Aufruf von [**EnumPrinters**](enumprinters.md)abzurufen. Ein solcher Aufruf ist eine schnelle und einfache Möglichkeit zum Abrufen der Namen und Attribute aller lokal installierten Drucker auf einem System und aller Remotedruckerverbindungen, die ein Benutzer hergestellt hat.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTER_INFO_4 {
  LPTSTR pPrinterName;
  LPTSTR pServerName;
  DWORD  Attributes;
} PRINTER_INFO_4, *PPRINTER_INFO_4;
```



## <a name="members"></a>Member

<dl> <dt>

**pPrinterName**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Druckers angibt (lokal oder remote).

</dd> <dt>

**pServerName**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die dem Namen des Servers entspricht.

</dd> <dt>

**Attribute**
</dt> <dd>

Gibt Informationen zu den zurückgegebenen Daten an.



| Wert                       | Bedeutung                          |
|-----------------------------|----------------------------------|
| \_DRUCKERATTRIBUT \_ LOKAL   | Der Drucker ist ein lokaler Drucker.  |
| \_DRUCKERATTRIBUTNETZWERK \_ | Der Drucker ist ein Remotedrucker. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **PRINTER \_ INFO \_ 4-Struktur** bietet eine einfache und äußerst schnelle Möglichkeit, die Namen der drucker, die auf einem lokalen Computer installiert sind, sowie die Remoteverbindungen abzurufen, die ein Benutzer hergestellt hat. Wenn [**EnumPrinters**](enumprinters.md) mit einer **PRINTER INFO \_ \_ 4-Datenstruktur** aufgerufen wird, fragt diese Funktion die Registrierung nach den angegebenen Informationen ab und gibt dann sofort zurück. Dies unterscheidet sich vom Verhalten von **EnumPrinters,** wenn es mit anderen Ebenen von **PRINTER INFO \_ \_ xxx-Datenstrukturen** aufgerufen wird. Insbesondere wenn **EnumPrinters** mit einer Datenstruktur der Ebene 2 (**PRINTER \_ INFO \_ 2** ) aufgerufen wird, wird für jede Remoteverbindung ein **OpenPrinter-Aufruf** ausgeführt. Wenn eine Remoteverbindung getrennt ist, der Remoteserver nicht mehr vorhanden ist oder der Remotedrucker nicht mehr vorhanden ist, muss die Funktion warten, bis für RPC ein Time out aufgetreten ist, und der **OpenPrinter-Aufruf** schlägt daher fehl. Dies kann eine Weile dauern. Wenn eine **PRINTER \_ INFO \_ 4-Struktur** übergeben wird, kann eine Anwendung ein absolutes Minimum an erforderlichen Informationen abrufen. Wenn ausführlichere Informationen gewünscht werden, kann ein **nachfolgender EnumPrinter** Level 2-Aufruf erfolgen.

**Attribute** können auch Werte enthalten, die im Feld **Attribute** von **PRINTER INFO \_ \_ 2** definiert sind.

Einige Druckerkonfigurationen, z. B. Druckerverbindungen mit einigen nicht Windows-basierten Druckerservern, geben möglicherweise sowohl **PRINTER \_ ATTRIBUTE \_ LOCAL** als auch **PRINTER ATTRIBUTE \_ \_ NETWORK** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ PRINTER \_ INFO \_ 4W** (Unicode) und **\_ PRINTER INFO \_ \_ 4A** (ANSI)<br/>                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 1**](printer-info-1.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 3**](printer-info-3.md)
</dt> </dl>

 

 




