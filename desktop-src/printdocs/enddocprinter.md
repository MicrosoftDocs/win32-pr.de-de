---
description: Die enddocprinter-Funktion beendet einen Druckauftrag für den angegebenen Drucker.
ms.assetid: 13c713e8-cc24-4191-8b1e-967b9e20e541
title: Enddocprinter-Funktion (winspool. h)
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
ms.openlocfilehash: 8d3e2bc110e5ee9412bb1edb89779f896edb015a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363513"
---
# <a name="enddocprinter-function"></a>Enddocprinter-Funktion

Die **enddocprinter** -Funktion beendet einen Druckauftrag für den angegebenen Drucker.

## <a name="syntax"></a>Syntax


```C++
BOOL EndDocPrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprinter* \[ in\]
</dt> <dd>

Handle für einen Drucker, für den der Druckauftrag beendet werden soll. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Die **enddocprinter** -Funktion gibt einen Fehler zurück, wenn der Druckauftrag nicht durch Aufrufen der [**StartDocPrinter**](startdocprinter.md) -Funktion gestartet wurde.

Die Reihenfolge für einen Druckauftrag lautet wie folgt:

1.  Zum Starten eines Druckauftrags aufrufen Sie [**StartDocPrinter**](startdocprinter.md).
2.  Um jede Seite zu starten, aufrufen Sie [**startpageprinter**](startpageprinter.md).
3.  Um Daten auf eine Seite zu schreiben, müssen Sie " [**Write-Printer**](writeprinter.md)" anrufen.
4.  Um jede Seite zu beenden, nennen Sie [**endpageprinter**](endpageprinter.md).
5.  Wiederholen Sie den Vorgang 2, 3 und 4 für beliebig viele Seiten.
6.  Um den Druckauftrag zu beenden, nennen Sie **enddocprinter**.

Wenn eine Seite in einer Spooldatei ungefähr 350 MB überschreitet, kann Sie nicht gedruckt werden, und es wird keine Fehlermeldung gesendet. Dies kann z. b. vorkommen, wenn große EMF-Dateien gedruckt werden. Der Grenzwert für die Seitengröße hängt von vielen Faktoren ab, z. b. von der Menge des verfügbaren virtuellen Speichers, von der durch den Aufruf von Prozessen belegten Arbeitsspeicher Menge und von der Fragmentierung im Prozess Heap.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Enddocprinter**](enddocprinter.md)
</dt> <dt>

[**Endpageprinter**](endpageprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**Startpageprinter**](startpageprinter.md)
</dt> <dt>

[**"Write Printer"**](writeprinter.md)
</dt> </dl>

 

 




