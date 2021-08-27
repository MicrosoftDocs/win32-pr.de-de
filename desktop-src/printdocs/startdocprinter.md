---
description: Die StartDocPrinter-Funktion benachrichtigt den Druckspooler, dass ein Dokument zum Drucken in einen Pool poolt werden soll.
ms.assetid: caa2bd80-4af3-4968-a5b9-d12f16cac6fc
title: StartDocPrinter-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StartDocPrinter
- StartDocPrinterA
- StartDocPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 047784a7debd0c12fa7a5ad144dbc1e81c4715d990be794c180e86555c8e9f37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060010"
---
# <a name="startdocprinter-function"></a>StartDocPrinter-Funktion

Die **StartDocPrinter-Funktion** benachrichtigt den Druckspooler, dass ein Dokument zum Drucken spoolt werden soll.

## <a name="syntax"></a>Syntax


```C++
DWORD StartDocPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pDocInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für den Drucker. Verwenden Sie [**die OpenPrinter-**](openprinter.md) [**oder AddPrinter-Funktion,**](addprinter.md) um einen Druckerhandpunkt abzurufen.

</dd> <dt>

*Ebene* \[ In\]
</dt> <dd>

Die Version der -Struktur, auf die *pDocInfo* verweist. Dieser Wert muss 1 sein.

</dd> <dt>

*pDocInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**DOC \_ INFO \_ 1-Struktur,**](doc-info-1.md) die das zu druckende Dokument beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, identifiziert der Rückgabewert den Druckauftrag.

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

Die typische Sequenz für einen Druckauftrag lautet wie folgt:

1.  Um einen Druckauftrag zu starten, rufen **Sie StartDocPrinter auf.**
2.  Um jede Seite zu starten, rufen [**Sie StartPagePrinter auf.**](startpageprinter.md)
3.  Um Daten auf eine Seite zu schreiben, rufen Sie [**WritePrinter auf.**](writeprinter.md)
4.  Um jede Seite zu beenden, rufen Sie [**EndPagePrinter auf.**](endpageprinter.md)
5.  Wiederholen Sie 2, 3 und 4 für so viele Seiten wie erforderlich.
6.  Um den Druckauftrag zu beenden, rufen Sie [**EndDocPrinter auf.**](enddocprinter.md)

Beachten Sie, dass das Aufrufen von [**StartPagePrinter**](startpageprinter.md) und [**EndPagePrinter**](endpageprinter.md) möglicherweise nicht erforderlich ist, z. B. wenn der Print-Datentyp die Seiteninformationen enthält.

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
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **StartDocPrinterW** (Unicode) und **StartDocPrinterA** (ANSI)<br/>                                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Addjob**](addjob.md)
</dt> <dt>

[**DOC \_ INFO \_ 1**](doc-info-1.md)
</dt> <dt>

[**DOC \_ INFO \_ 2**](doc-info-2.md)
</dt> <dt>

[**EndDocPrinter**](enddocprinter.md)
</dt> <dt>

[**EndPagePrinter**](endpageprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**StartPagePrinter**](startpageprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




