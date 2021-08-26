---
description: Die AbortPrinter-Funktion löscht eine Druckerspooldatei, wenn der Drucker für das Spooling konfiguriert ist.
ms.assetid: b361fba5-e4e7-4c9e-ab32-b8ab88dcb1dc
title: AbortPrinter-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AbortPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: c4d3bd7af58c0c927d01fad734ad58f59941815b1680e730f2569efcc6c00b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951030"
---
# <a name="abortprinter-function"></a>AbortPrinter-Funktion

Die **AbortPrinter-Funktion** löscht die Spooldatei eines Druckers, wenn der Drucker für das Spooling konfiguriert ist.

## <a name="syntax"></a>Syntax


```C++
BOOL AbortPrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Handle für den Drucker, aus dem die Spooldatei gelöscht wird. Verwenden Sie die [**OpenPrinter-**](openprinter.md) oder [**AddPrinter-Funktion,**](addprinter.md) um ein Druckerhandle abzurufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

Wenn der Drucker nicht für das Spooling konfiguriert ist, hat die **AbortPrinter-Funktion** keine Auswirkungen.

Die Sequenz für einen Druckauftrag sieht wie folgt aus:

1.  Um einen Druckauftrag zu starten, rufen [**Sie StartDocPrinter**](startdocprinter.md)auf.
2.  Um jede Seite zu starten, rufen [**Sie StartPagePrinter**](startpageprinter.md)auf.
3.  Um Daten auf eine Seite zu schreiben, rufen [**Sie WritePrinter**](writeprinter.md)auf.
4.  Um jede Seite zu beenden, rufen [**Sie EndPagePrinter**](endpageprinter.md)auf.
5.  Wiederholen Sie 2, 3 und 4 für so viele Seiten wie nötig.
6.  Um den Druckauftrag zu beenden, rufen [**Sie EndDocPrinter auf.**](enddocprinter.md)

Wenn eine Seite in einer datei mit Spooling ca. 350 MB überschreitet, kann sie nicht gedruckt werden und keine Fehlermeldung senden. Dies kann z. B. beim Drucken großer EMF-Dateien auftreten. Die Begrenzung der Seitengröße hängt von vielen Faktoren ab, einschließlich der Menge des verfügbaren virtuellen Arbeitsspeichers, der Durch aufrufenden Prozesse belegten Arbeitsspeichers und der Fragmentierung im Prozessheap.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EndDocPrinter**](enddocprinter.md)
</dt> <dt>

[**EndPagePrinter**](endpageprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**StartPagePrinter**](startpageprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




