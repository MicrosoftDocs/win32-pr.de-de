---
description: Die \_ PRINTER INFO \_ 1-Struktur gibt allgemeine Druckerinformationen an.
ms.assetid: 0b0e2d0e-2625-4cab-a8f9-536185479443
title: PRINTER_INFO_1-Struktur (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_1
- _PRINTER_INFO_1A
- _PRINTER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ab70662371ef4ebe80b1d10f7f61700c97e979959c337bb5e81b3bc688e8c36b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234207"
---
# <a name="printer_info_1-structure"></a>PRINTER \_ INFO \_ 1-Struktur

Die **PRINTER \_ INFO \_ 1-Struktur** gibt allgemeine Druckerinformationen an.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTER_INFO_1 {
  DWORD  Flags;
  LPTSTR pDescription;
  LPTSTR pName;
  LPTSTR pComment;
} PRINTER_INFO_1, *PPRINTER_INFO_1;
```



## <a name="members"></a>Member

<dl> <dt>

**Flags**
</dt> <dd>

Gibt Informationen zu den zurückgegebenen Daten an. Im Folgenden sind die Werte für diesen Member angegeben.



| Wert                    | Bedeutung                                                                                                                                                                                                                                                   |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERWEITERN DER \_ DRUCKERENUMERSUMME \_    | Ein Druckanbieter kann dieses Flag als Hinweis auf eine aufrufende Anwendung festlegen, um dieses Objekt weiter aufzuzählen, wenn die Standarderweiterung aktiviert ist. Wenn domänen beispielsweise aufzählt werden, kann ein Druckanbieter die Domäne des Benutzers angeben, indem er dieses Flag festlegt. |
| \_ \_ DRUCKERENUMERCONTAINER | Wenn dieses Flag festgelegt ist, kann das Druckerobjekt aufzählbare Objekte enthalten. Das -Objekt kann beispielsweise ein Druckerserver sein, der Drucker enthält.                                                                                                             |
| \_ \_ DRUCKERENUMERSYMBOL1     | Gibt an, dass eine Anwendung ggf. ein Symbol anzeigen soll, das das Objekt als Netzwerknamen der obersten Ebene identifiziert, z. B. Microsoft Windows Network.                                                                                           |
| \_ \_ DRUCKERENUMERSYMBOL2     | Gibt an, dass eine Anwendung ggf. ein Symbol anzeigen soll, das das Objekt als Netzwerkdomäne identifiziert.                                                                                                                                  |
| \_ \_ DRUCKERENUMERSYMBOL3     | Gibt an, dass eine Anwendung ggf. ein Symbol anzeigen soll, das das Objekt als Druckserver identifiziert.                                                                                                                                    |
| \_ \_ DRUCKERENUMERSYMBOL4     | Reserviert.                                                                                                                                                                                                                                                 |
| \_ \_ DRUCKERENUMERSYMBOL5     | Reserviert.                                                                                                                                                                                                                                                 |
| \_ \_ DRUCKERENUMERSYMBOL6     | Reserviert.                                                                                                                                                                                                                                                 |
| \_ \_ DRUCKERENUMERSYMBOL7     | Reserviert.                                                                                                                                                                                                                                                 |
| \_ \_ DRUCKERENUMERSYMBOL8     | Gibt an, dass eine Anwendung ggf. ein Symbol anzeigen soll, das das Objekt als Drucker identifiziert.                                                                                                                                         |



 

</dd> <dt>

**pDescription**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Inhalt der -Struktur beschreibt.

</dd> <dt>

**pName**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Inhalt der Struktur benennt.

</dd> <dt>

**pComment**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die zusätzliche Daten enthält, die die Struktur beschreiben.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ PRINTER \_ INFO \_ 1W** (Unicode) und **\_ PRINTER INFO \_ \_ 1A** (ANSI)<br/>                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 3**](printer-info-3.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 4**](printer-info-4.md)
</dt> </dl>

 

 




