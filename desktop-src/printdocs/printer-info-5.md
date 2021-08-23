---
description: Die PRINTER \_ INFO \_ 5-Struktur gibt detaillierte Druckerinformationen an.
ms.assetid: c8599f2e-3b7c-4fde-a340-ca7d3ddaa106
title: PRINTER_INFO_5 -Struktur (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_5
- _PRINTER_INFO_5A
- _PRINTER_INFO_5W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ef50f3bfd83a0c2dd49eb0a15cdae31f25588106926e606887292c705602dd44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731421"
---
# <a name="printer_info_5-structure"></a>PRINTER \_ INFO \_ 5-Struktur

Die **PRINTER \_ INFO \_ 5-Struktur** gibt detaillierte Druckerinformationen an.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTER_INFO_5 {
  LPTSTR pPrinterName;
  LPTSTR pPortName;
  DWORD  Attributes;
  DWORD  DeviceNotSelectedTimeout;
  DWORD  TransmissionRetryTimeout;
} PRINTER_INFO_5, *PPRINTER_INFO_5;
```



## <a name="members"></a>Member

<dl> <dt>

**pPrinterName**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Druckers angibt.

</dd> <dt>

**pPortName**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die die Ports identifiziert, die zum Übertragen von Daten an den Drucker verwendet werden. Wenn ein Drucker mit mehr als einem Anschluss verbunden ist, müssen die Namen der einzelnen Ports durch Kommas getrennt werden (z.B. "LPT1:,LPT2:,LPT3:").

</dd> <dt>

**Attribute**
</dt> <dd>

Die Druckerattribute. Dieser Member kann eine beliebige sinnvolle Kombination der folgenden Werte sein.

| Wert                                   | Bedeutung                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PRINTER \_ ATTRIBUTE \_ DIRECT              | Der Auftrag wird direkt an den Drucker gesendet (er wird nicht in einen Pool pooliert).                                                                                                                                |
| \_ \_ DRUCKERATTRIBUT \_ ZUERST \_ ABGESCHLOSSEN | Wenn set und printer für das Drucken während des Spoolings festgelegt sind, werden alle Aufträge, die das Spooling abgeschlossen haben, so geplant, dass sie vor Aufträgen gedruckt werden, die das Spoolen nicht abgeschlossen haben.                          |
| PRINTER \_ ATTRIBUTE ENABLE DEVQ (DRUCKERATTRIBUT \_ AKTIVIEREN VON \_ DEVQ)        | Wenn festgelegt, **wird DevQueryPrint** aufgerufen. **DevQueryPrint kann** fehlschlagen, wenn die Dokument- und Druckersetups nicht übereinstimmen. Wenn Sie dieses Flag festlegen, werden nicht übereinstimmende Dokumente in der Warteschlange gespeichert. |
| \_DRUCKERATTRIBUT \_ AUSGEBLENDET              | Reserviert.                                                                                                                                                                               |
| \_ \_ DRUCKERATTRIBUT KEEPPRINTEDJOBS     | Wenn festgelegt, werden Aufträge beibehalten, nachdem sie gedruckt wurden. Wenn der Satz nicht geändert wird, werden Aufträge gelöscht.                                                                                                               |
| \_DRUCKERATTRIBUT \_ LOKAL               | Der Drucker ist ein lokaler Drucker.                                                                                                                                                             |
| \_ \_ DRUCKERATTRIBUTNETZWERK             | Drucker ist eine Netzwerkdruckerverbindung.                                                                                                                                                |
| \_DRUCKERATTRIBUT \_ VERÖFFENTLICHT           | Gibt an, ob der Drucker im Verzeichnisdienst veröffentlicht wird.                                                                                                                    |
| \_ \_ DRUCKERATTRIBUT IN WARTESCHLANGE              | Wenn festgelegt, wird der Drucker gepoolt und mit dem Drucken gestartet, nachdem die letzte Seite in die Warteschlange gesetzt wurde. Wenn nicht festgelegt und PRINTER ATTRIBUTE DIRECT nicht festgelegt ist, wird der Drucker beim Spoolen gepoolt \_ \_ und gedruckt.      |
| NUR \_ \_ RAW-DRUCKERATTRIBUT \_           | Gibt an, dass nur Unformatierte Druckaufträge vom Datentyp spoolt werden können.                                                                                                                            |
| \_DRUCKERATTRIBUT \_ FREIGEGEBEN              | Der Drucker wird freigegeben.                                                                                                                                                                      |



 

In Windows XP und neueren Versionen von Windows kann auch der folgende Wert verwendet werden.

| Wert                   | Bedeutung                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_DRUCKERATTRIBUT \_ FAX | Wenn festgelegt, ist der Drucker ein Faxdrucker. Dies kann nur von [**AddPrinter**](addprinter.md)festgelegt werden, kann aber von [**EnumPrinters**](enumprinters.md) und [**GetPrinter abgerufen werden.**](getprinter.md) |



 

In Windows Vista und neueren Versionen von Windows können auch die folgenden Werte verwendet werden.

| Wert                               | Bedeutung                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| ANGEZEIGTER \_ NAME \_ DES \_ DRUCKERATTRIBUTS  | Ein Computer hat mit diesem Drucker verbunden und ihm einen Benutzerfreundlichen Namen gegeben.           |
| \_DRUCKERATTRIBUTCOMPUTER \_         | Drucker ist eine Computerverbindung.                                             |
| \_ \_ DRUCKERATTRIBUT PUSHED \_ USER    | Der Drucker wurde mithilfe der Benutzerrichtlinie Pushdruckerverbindungen installiert.     |
| \_ \_ DRUCKERATTRIBUT – PUSHCOMPUTER \_ | Der Drucker wurde mithilfe der Computerrichtlinie Pushdruckerverbindungen installiert. |



 

</dd> <dt>

**DeviceNotSelectedTimeout**
</dt> <dd>

Dieser Wert wird nicht verwendet.

</dd> <dt>

**TransmissionRetryTimeout**
</dt> <dd>

Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ PRINTER \_ INFO \_ 5W** (Unicode) und **\_ PRINTER INFO \_ \_ 5A** (ANSI)<br/>                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 1**](printer-info-1.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 3**](printer-info-3.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 4**](printer-info-4.md)
</dt> </dl>

 

 




