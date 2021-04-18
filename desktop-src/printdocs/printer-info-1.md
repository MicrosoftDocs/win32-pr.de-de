---
description: Die Struktur der Drucker \_ Info \_ 1 gibt allgemeine Drucker Informationen an.
ms.assetid: 0b0e2d0e-2625-4cab-a8f9-536185479443
title: PRINTER_INFO_1 Struktur (winspool. h)
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
ms.openlocfilehash: cbeff42a9125331c45ffd8bbbee5758fd864648c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351752"
---
# <a name="printer_info_1-structure"></a>Drucker \_ Info \_ 1-Struktur

Die Struktur der **Drucker \_ Info \_ 1** gibt allgemeine Drucker Informationen an.

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

Gibt Informationen zu den zurückgegebenen Daten an. Im folgenden finden Sie die Werte für diesen Member.



| Wert                    | Bedeutung                                                                                                                                                                                                                                                   |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Druckeraufzählung \_ \_ erweitern    | Ein Druckanbieter kann dieses Flag als Hinweis auf eine aufrufende Anwendung festlegen, um dieses Objekt weiter aufzuzählen, wenn die Standard Erweiterung aktiviert ist. Wenn z. b. Domänen aufgelistet werden, kann ein Druckanbieter die Domäne des Benutzers angeben, indem dieses Flag festgelegt wird. |
| druckeraufzählungs \_ \_ Container | Wenn dieses Flag festgelegt ist, kann das Drucker Objekt Aufzähl Bare-Objekte enthalten. Beispielsweise kann das Objekt ein Druckserver sein, der Drucker enthält.                                                                                                             |
| Druckeraufzählung \_ \_ ICON1     | Gibt an, dass eine Anwendung ggf. ein Symbol anzeigt, das das Objekt als Netzwerknamen der obersten Ebene (z. b. Microsoft Windows-Netzwerk) identifiziert.                                                                                           |
| Druckeraufzählung \_ \_ icon2     | Gibt an, dass eine Anwendung ggf. ein Symbol anzeigt, das das Objekt als Netzwerk Domäne identifiziert.                                                                                                                                  |
| Druckeraufzählung \_ \_ ICON3     | Gibt an, dass eine Anwendung ggf. ein Symbol anzeigt, das das Objekt als Druckserver identifiziert.                                                                                                                                    |
| Druckeraufzählung \_ \_ ICON4     | Reserviert.                                                                                                                                                                                                                                                 |
| Druckeraufzählung \_ \_ ICON5     | Reserviert.                                                                                                                                                                                                                                                 |
| Druckeraufzählung \_ \_ ICON6     | Reserviert.                                                                                                                                                                                                                                                 |
| Druckeraufzählung \_ \_ ICON7     | Reserviert.                                                                                                                                                                                                                                                 |
| Druckeraufzählung \_ \_ ICON8     | Gibt an, dass eine Anwendung ggf. ein Symbol anzeigt, das das Objekt als Drucker bezeichnet.                                                                                                                                         |



 

</dd> <dt>

**pdescription**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Inhalt der-Struktur beschreibt.

</dd> <dt>

**pName**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Inhalt der-Struktur benennt.

</dd> <dt>

**pcomment**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die zusätzliche Daten enthält, die die Struktur beschreiben.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Drucker \_ Info \_ 1W** (Unicode) und **\_ Drucker \_ Info \_ 1a** (ANSI)<br/>                           |



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

[**Drucker \_ Informationen \_ 2**](printer-info-2.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 3**](printer-info-3.md)
</dt> <dt>

[**Drucker \_ Info \_ 4**](printer-info-4.md)
</dt> </dl>

 

 




