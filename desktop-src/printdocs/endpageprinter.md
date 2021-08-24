---
description: Die EndPagePrinter-Funktion benachrichtigt den Druckspooler, dass sich die Anwendung am Ende einer Seite in einem Druckauftrag befindet.
ms.assetid: aceb88b9-375b-4cd2-996a-c369f590154e
title: EndPagePrinter-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndPagePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 9a152716a295650575fce0fefe5299ca4a214c322afa6570760c988182f9ba65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711860"
---
# <a name="endpageprinter-function"></a>EndPagePrinter-Funktion

Die **EndPagePrinter-Funktion** benachrichtigt den Druckspooler, dass sich die Anwendung am Ende einer Seite in einem Druckauftrag befindet.

## <a name="syntax"></a>Syntax


```C++
BOOL EndPagePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Handle für den Drucker, für den die Seite abgeschlossen wird. Verwenden Sie [**die OpenPrinter-**](openprinter.md) [**oder AddPrinter-Funktion,**](addprinter.md) um einen Druckerhandpunkt abzurufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

Die Sequenz für einen Druckauftrag lautet wie folgt:

1.  Um einen Druckauftrag zu starten, rufen [**Sie StartDocPrinter auf.**](startdocprinter.md)
2.  Um jede Seite zu starten, rufen [**Sie StartPagePrinter auf.**](startpageprinter.md)
3.  Um Daten auf eine Seite zu schreiben, rufen Sie [**WritePrinter auf.**](writeprinter.md)
4.  Um jede Seite zu beenden, rufen Sie **EndPagePrinter auf.**
5.  Wiederholen Sie 2, 3 und 4 für so viele Seiten wie erforderlich.
6.  Um den Druckauftrag zu beenden, rufen Sie [**EndDocPrinter auf.**](enddocprinter.md)

Wenn eine Seite in einer Spooldatei ca. 350 MB überschreitet, kann sie nicht gedruckt werden und sendet keine Fehlermeldung. Dies kann beispielsweise beim Drucken großer EMF-Dateien auftreten. Die Seitengrößenbeschränkung hängt von vielen Faktoren ab, einschließlich der Menge des verfügbaren virtuellen Arbeitsspeichers, der Durch aufrufenden Prozesse zugewiesenen Arbeitsspeichermenge und der Fragmentierung im Prozesshap.

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

 

 




