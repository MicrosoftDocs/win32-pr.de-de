---
description: Die Funktion StartDocPrinter benachrichtigt den Druck Spooler, dass ein Dokument zum Drucken gespoolt werden soll.
ms.assetid: caa2bd80-4af3-4968-a5b9-d12f16cac6fc
title: StartDocPrinter-Funktion (winspool. h)
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
ms.openlocfilehash: f8bdb0ae08c88e553dad3a91f0f1a578bed4ad39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868024"
---
# <a name="startdocprinter-function"></a>StartDocPrinter-Funktion

Die Funktion **StartDocPrinter** benachrichtigt den Druck Spooler, dass ein Dokument zum Drucken gespoolt werden soll.

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

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für den Drucker. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

</dd> <dt>

*Ebene* \[ in\]
</dt> <dd>

Die Version der-Struktur, auf die *pdocinfo* verweist. Dieser Wert muss 1 sein.

</dd> <dt>

*pdocinfo* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**doc \_ Info \_ 1**](doc-info-1.md) -Struktur, die das zu druckende Dokument beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, identifiziert der Rückgabewert den Druckauftrag.

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Die typische Reihenfolge für einen Druckauftrag lautet wie folgt:

1.  Zum Starten eines Druckauftrags aufrufen Sie **StartDocPrinter**.
2.  Um jede Seite zu starten, aufrufen Sie [**startpageprinter**](startpageprinter.md).
3.  Um Daten auf eine Seite zu schreiben, müssen Sie " [**Write-Printer**](writeprinter.md)" anrufen.
4.  Um jede Seite zu beenden, nennen Sie [**endpageprinter**](endpageprinter.md).
5.  Wiederholen Sie den Vorgang 2, 3 und 4 für beliebig viele Seiten.
6.  Um den Druckauftrag zu beenden, nennen Sie [**enddocprinter**](enddocprinter.md).

Beachten Sie, dass das Aufrufen von [**startpageprinter**](startpageprinter.md) und [**endpageprinter**](endpageprinter.md) möglicherweise nicht erforderlich ist, z. b. wenn der Print-Datentyp die Seiten Informationen enthält.

Wenn eine Seite in einer Spooldatei ungefähr 350 MB überschreitet, kann Sie nicht gedruckt werden, und es wird keine Fehlermeldung gesendet. Dies kann z. b. vorkommen, wenn große EMF-Dateien gedruckt werden. Der Grenzwert für die Seitengröße hängt von vielen Faktoren ab, z. b. von der Menge des verfügbaren virtuellen Speichers, von der durch den Aufruf von Prozessen belegten Arbeitsspeicher Menge und von der Fragmentierung im Prozess Heap.

## <a name="examples"></a>Beispiele

Ein Beispielprogramm, das diese Funktion verwendet, finden [Sie unter Gewusst wie: Drucken mit der GDI-Druck-API](how-to--print-using-the-gdi-print-api.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Startdocprinterw** (Unicode) und **startdocprintera** (ANSI)<br/>                                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**DOC \_ Info \_ 1**](doc-info-1.md)
</dt> <dt>

[**DOC \_ Info \_ 2**](doc-info-2.md)
</dt> <dt>

[**Enddocprinter**](enddocprinter.md)
</dt> <dt>

[**Endpageprinter**](endpageprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**Startpageprinter**](startpageprinter.md)
</dt> <dt>

[**"Write Printer"**](writeprinter.md)
</dt> </dl>

 

 




