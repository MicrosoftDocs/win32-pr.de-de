---
description: Die Drucker \_ Info \_ 4-Struktur gibt allgemeine Drucker Informationen an. Die-Struktur kann verwendet werden, um beim Aufrufen von enumdruckern minimale Drucker Informationen abzurufen.
ms.assetid: 81bd0eab-dc1e-4cf1-8f63-3686f1711c1f
title: PRINTER_INFO_4 Struktur (winspool. h)
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
ms.openlocfilehash: 9a1501008f0235ea303dd1457fc8756c28abc21c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217390"
---
# <a name="printer_info_4-structure"></a>Drucker \_ Info \_ 4-Struktur

Die **Drucker \_ Info \_ 4** -Struktur gibt allgemeine Drucker Informationen an.

Die-Struktur kann verwendet werden, um beim Aufrufen von [**enumdruckern**](enumprinters.md)minimale Drucker Informationen abzurufen. Ein solcher Rückruf ist eine schnelle und einfache Möglichkeit zum Abrufen der Namen und Attribute aller lokal installierten Drucker auf einem System und aller Remote Drucker Verbindungen, die ein Benutzer eingerichtet hat.

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

**pprintername**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Druckers angibt (lokal oder Remote).

</dd> <dt>

**pservername**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Servers ist.

</dd> <dt>

**Attribute**
</dt> <dd>

Gibt Informationen zu den zurückgegebenen Daten an.



| Wert                       | Bedeutung                          |
|-----------------------------|----------------------------------|
| Drucker \_ Attribut \_ lokal   | Der Drucker ist ein lokaler Drucker.  |
| Drucker \_ Attribut \_ Netzwerk | Der Drucker ist ein Remote Drucker. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Drucker \_ Info \_ 4** -Struktur bietet eine einfache und äußerst schnelle Möglichkeit, die Namen der Drucker, die auf einem lokalen Computer installiert sind, sowie die von einem Benutzer eingerichteten Remote Verbindungen abzurufen. Wenn [**enumprinter**](enumprinters.md) mit einer Datenstruktur vom Typ " **Printer \_ Info \_ 4** " aufgerufen wird, fragt diese Funktion die Registrierung nach den angegebenen Informationen ab und wird dann sofort zurückgegeben. Dies unterscheidet sich vom Verhalten von **enumdruckern** , wenn es mit anderen Ebenen von **Drucker \_ Informationen \_ xxx** -Datenstrukturen aufgerufen wird. Insbesondere, wenn **enumprinter** mit einer Datenstruktur der Ebene 2 (**Printer \_ Info \_ 2** ) aufgerufen wird, führt Sie einen **OpenPrinter** -Aufruf für jede Remote Verbindung aus. Wenn eine Remote Verbindung nicht mehr vorhanden ist, wenn der Remote Server nicht mehr vorhanden ist oder der Remote Drucker nicht mehr vorhanden ist, muss die Funktion auf das Timeout von RPC warten und somit den **OpenPrinter** -Aufruf fehlschlagen. Dies kann eine Weile dauern. Durch die Übergabe einer **Drucker \_ Info \_ 4** -Struktur kann eine Anwendung ein Minimum an erforderlichen Informationen abrufen. wenn ausführlichere Informationen gewünscht werden, kann ein nachfolgende **aufrufergrad** 2 aufgerufen werden.

**Attribute** können auch Werte enthalten, die im Feld **Attribute** von **Printer \_ Info \_ 2** definiert sind.

Einige Drucker Konfigurationen, wie z. b. Drucker Verbindungen mit einigen nicht auf Windows basierenden Druckservern, geben möglicherweise sowohl das **\_ \_ lokale Drucker Attribut** als auch das **Drucker Attribut \_ \_ Netzwerk** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Drucker \_ Info \_ 4W** (Unicode) und **\_ Drucker \_ Info \_ 4a** (ANSI)<br/>                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**Enumdrucker**](enumprinters.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 1**](printer-info-1.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 2**](printer-info-2.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 3**](printer-info-3.md)
</dt> </dl>

 

 




