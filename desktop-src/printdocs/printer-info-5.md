---
description: Die Drucker \_ Info \_ 5-Struktur gibt ausführliche Drucker Informationen an.
ms.assetid: c8599f2e-3b7c-4fde-a340-ca7d3ddaa106
title: PRINTER_INFO_5 Struktur (winspool. h)
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
ms.openlocfilehash: 2ec207b60eca8cc20f6f24e2bb08bb1e3b191fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352400"
---
# <a name="printer_info_5-structure"></a>Drucker \_ Info \_ 5-Struktur

Die **Drucker \_ Info \_ 5** -Struktur gibt ausführliche Drucker Informationen an.

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

**pprintername**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druckers angibt.

</dd> <dt>

**pportname**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Ports identifiziert, die zum Übertragen von Daten an den Drucker verwendet werden. Wenn ein Drucker mit mehr als einem Port verbunden ist, müssen die Namen der einzelnen Ports durch Kommas getrennt werden (z. b. "LPT1:, LPT2:, LPT3:").

</dd> <dt>

**Attribute**
</dt> <dd>

Die Drucker Attribute. Dieser Member kann eine beliebige Kombination der folgenden Werte sein.

| Wert                                   | Bedeutung                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Drucker \_ Attribut \_ Direct              | Der Auftrag wird direkt an den Drucker gesendet (er ist nicht Spoolvorgang).                                                                                                                                |
| das Drucker \_ Attribut ist \_ \_ \_ zuerst fertig. | Wenn Set und Printer für Druck-während-Spoolvorgänge festgelegt sind, werden alle Aufträge, für die das Spoolvorgang abgeschlossen wurde, vor Aufträgen gedruckt, für die das Spoolvorgang noch nicht abgeschlossen wurde.                          |
| Drucker \_ Attribut \_ Aktivieren von \_ devq        | Wenn festgelegt, wird **devqueryprint** aufgerufen. **Devqueryprint** schlägt möglicherweise fehl, wenn die Dokument-und Drucker Einrichtung nicht identisch ist. Das Festlegen dieses Flags bewirkt, dass nicht übereinstimmende Dokumente in der Warteschlange gespeichert werden. |
| Drucker \_ Attribut \_ ausgeblendet              | Reserviert.                                                                                                                                                                               |
| Drucker \_ Attribut \_ KeepPrintedJobs     | Wenn festgelegt, werden die Aufträge nach dem Drucken beibehalten. Wenn der Wert nicht festgelegt ist, werden Aufträge gelöscht.                                                                                                               |
| Drucker \_ Attribut \_ lokal               | Der Drucker ist ein lokaler Drucker.                                                                                                                                                             |
| Drucker \_ Attribut \_ Netzwerk             | Der Drucker ist eine Netzwerkdrucker Verbindung.                                                                                                                                                |
| Drucker \_ Attribut \_ veröffentlicht           | Gibt an, ob der Drucker im Verzeichnisdienst veröffentlicht wird.                                                                                                                    |
| Drucker \_ Attribut in \_ Warteschlange eingereiht              | Wenn diese Einstellung festgelegt ist, wird der Drucker vor dem Spoolvorgang gedruckt und der Druckvorgang gestartet. Wenn nicht festgelegt und Drucker \_ Attribut \_ Direct nicht festgelegt ist, wird der Drucker beim Spoolvorgang Spool und druckt.      |
| Drucker \_ Attribut \_ \_ nur RAW           | Gibt an, dass nur unformatierte Datentypen Druckaufträge gespoolte werden können.                                                                                                                            |
| Drucker \_ Attribut frei \_ gegeben              | Der Drucker ist freigegeben.                                                                                                                                                                      |



 

In Windows XP und höheren Versionen von Windows kann auch der folgende Wert verwendet werden.

| Wert                   | Bedeutung                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Drucker \_ Attribut \_ Fax | Wenn festgelegt, ist der Drucker ein Faxdrucker. Dies kann nur von [**addprinter**](addprinter.md)festgelegt werden, kann jedoch von [**enumprinter**](enumprinters.md) und [**GetPrinter**](getprinter.md)abgerufen werden. |



 

In Windows Vista und höheren Versionen von Windows können auch die folgenden Werte verwendet werden.

| Wert                               | Bedeutung                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| Anzeige \_ Name des Drucker Attributs \_ \_  | Ein Computer hat eine Verbindung mit diesem Drucker hergestellt und einen anzeigen Amen erhalten.           |
| Drucker \_ Attribut \_ Computer         | Der Drucker ist eine Computer spezifische Verbindung.                                             |
| Drucker \_ Attribut mit \_ pushübertragung für \_ Benutzer    | Der Drucker wurde mithilfe der Benutzer Richtlinie "Push Printer Connections" installiert.     |
| Drucker \_ Attribut \_ mit \_ gedrückter Maschine | Der Drucker wurde mithilfe der Computer Richtlinie "Push Printer Connections" installiert. |



 

</dd> <dt>

**Devicenotselectedtimeout**
</dt> <dd>

Dieser Wert wird nicht verwendet.

</dd> <dt>

**Transmissionretrytimeout**
</dt> <dd>

Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Drucker \_ Info \_ 5W** (Unicode) und **\_ Drucker \_ Info \_ 5A** (ANSI)<br/>                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Enumdrucker**](enumprinters.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 1**](printer-info-1.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 2**](printer-info-2.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 3**](printer-info-3.md)
</dt> <dt>

[**Drucker \_ Info \_ 4**](printer-info-4.md)
</dt> </dl>

 

 




