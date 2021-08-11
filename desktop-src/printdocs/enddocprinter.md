---
description: Die EndDocPrinter-Funktion beendet einen Druckauftrag für den angegebenen Drucker.
ms.assetid: 13c713e8-cc24-4191-8b1e-967b9e20e541
title: EndDocPrinter-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndDocPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 4bad07cd965d3a0c1ed16b508af025cfcadcf3fb8a5cf465f8e1fb2541bc7552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234750"
---
# <a name="enddocprinter-function"></a>EndDocPrinter-Funktion

Die **EndDocPrinter-Funktion** beendet einen Druckauftrag für den angegebenen Drucker.

## <a name="syntax"></a>Syntax


```C++
BOOL EndDocPrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Handle für einen Drucker, für den der Druckauftrag beendet werden soll. Verwenden Sie [**die OpenPrinter-**](openprinter.md) oder [**AddPrinter-Funktion,**](addprinter.md) um einen Druckerhandpunkt abzurufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu kommen, dass die Anwendung nicht reagiert.

 

Die **EndDocPrinter-Funktion** gibt einen Fehler zurück, wenn der Druckauftrag nicht durch Aufrufen der [**StartDocPrinter-Funktion gestartet**](startdocprinter.md) wurde.

Die Sequenz für einen Druckauftrag lautet wie folgt:

1.  Um einen Druckauftrag zu starten, rufen [**Sie StartDocPrinter auf.**](startdocprinter.md)
2.  Um jede Seite zu starten, rufen [**Sie StartPagePrinter auf.**](startpageprinter.md)
3.  Um Daten auf eine Seite zu schreiben, rufen Sie [**WritePrinter auf.**](writeprinter.md)
4.  Um jede Seite zu beenden, rufen Sie [**EndPagePrinter auf.**](endpageprinter.md)
5.  Wiederholen Sie 2, 3 und 4 für so viele Seiten wie erforderlich.
6.  Um den Druckauftrag zu beenden, rufen Sie **EndDocPrinter auf.**

Wenn eine Seite in einer Spooldatei ca. 350 MB überschreitet, kann sie möglicherweise nicht gedruckt werden und sendet keine Fehlermeldung. Dies kann beispielsweise beim Drucken großer EMF-Dateien auftreten. Die Seitengrößenbeschränkung hängt von vielen Faktoren ab, einschließlich der Menge des verfügbaren virtuellen Arbeitsspeichers, der Durch aufrufenden Prozesse zugeordneten Arbeitsspeichermenge und der Fragmentierung im Prozesshap.

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

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**StartPagePrinter**](startpageprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




