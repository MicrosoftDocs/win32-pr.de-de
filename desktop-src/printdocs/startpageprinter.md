---
description: Die StartPagePrinter-Funktion benachrichtigt den Spooler, dass eine Seite auf dem angegebenen Drucker gedruckt werden soll.
ms.assetid: 8ac7c47b-b3a7-4642-bfb7-54e014139fbf
title: StartPagePrinter-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StartPagePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 974c2f5dcc4c821602d29a4eed7ced5ad1caa48f0e5ded664a705940d88305b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470132"
---
# <a name="startpageprinter-function"></a>StartPagePrinter-Funktion

Die **StartPagePrinter-Funktion** benachrichtigt den Spooler, dass eine Seite auf dem angegebenen Drucker gedruckt werden soll.

## <a name="syntax"></a>Syntax


```C++
BOOL StartPagePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Handle für einen Drucker. Verwenden Sie [**die OpenPrinter-**](openprinter.md) [**oder AddPrinter-Funktion,**](addprinter.md) um einen Druckerhandpunkt abzurufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

Die Sequenz für einen Druckauftrag lautet wie folgt:

1.  Um einen Druckauftrag zu starten, rufen [**Sie StartDocPrinter auf.**](startdocprinter.md)
2.  Um jede Seite zu starten, rufen **Sie StartPagePrinter auf.**
3.  Um Daten auf eine Seite zu schreiben, rufen Sie [**WritePrinter auf.**](writeprinter.md)
4.  Um jede Seite zu beenden, rufen Sie [**EndPagePrinter auf.**](endpageprinter.md)
5.  Wiederholen Sie 2, 3 und 4 für so viele Seiten wie erforderlich.
6.  Um den Druckauftrag zu beenden, rufen Sie [**EndDocPrinter auf.**](enddocprinter.md)

Wenn eine Seite in einer Spooldatei ca. 350 MB überschreitet, kann sie nicht gedruckt werden und sendet keine Fehlermeldung. Dies kann beispielsweise beim Drucken großer EMF-Dateien auftreten. Die Seitengrößenbeschränkung hängt von vielen Faktoren ab, einschließlich der Menge des verfügbaren virtuellen Arbeitsspeichers, der Durch aufrufenden Prozesse zugewiesenen Arbeitsspeichermenge und der Fragmentierung im Prozesshap.

## <a name="examples"></a>Beispiele

Ein Beispielprogramm, das diese Funktion verwendet, finden Sie unter How To: Print Using the GDI Print API (How [To: Drucken mithilfe der GDI-Druck-API).](how-to--print-using-the-gdi-print-api.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Weitere Informationen

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

 

 




