---
title: HTTP-Vervollständigungs Routinen
description: Anwendungen verfügen über mehrere Optionen, um Vervollständigungs Hinweise zu erhalten und Entwicklern eine gewisse Flexibilität zu bieten.
ms.assetid: c48a64d2-b6c8-4694-8600-f84751954bad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aee05efc8284cb29130efae4bcaefb4834a3fb4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948725"
---
# <a name="http-completion-routines"></a>HTTP-Vervollständigungs Routinen

Anwendungen verfügen über mehrere Optionen, um Vervollständigungs Hinweise zu erhalten und Entwicklern eine gewisse Flexibilität zu bieten. Die Optionen werden blockiert, während darauf gewartet wird, dass ein API-Befehl abgeschlossen wird, oder um Vervollständigungs Routinen für asynchrone Vorgänge zu verwenden. Der Vorteil der Verwendung von asynchronen Vorgängen ist eine Erhöhung der Reaktionsfähigkeit der Anwendung.

## <a name="blocked-io"></a>Blockierte e/a

Anwendungen können blockieren, während auf den Abschluss der API-Aufrufe gewartet wird, indem die [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur auf **null** festgelegt wird. Dies blockiert wirklich alle Vorgänge im Thread. Beispielsweise wird bei Aufrufen von [**httpwaitfordisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)der Aufruf so lange blockiert, bis die Verbindung unterbrochen wird.

## <a name="asynchronous-io"></a>Asynchrone e/a

Anwendungen, die nicht blockieren möchten, können die [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur verwenden, um die Vervollständigungs Ergebnisse zu erhalten. Die Anwendung stellt einen Zeiger auf eine **über** Lapp Ende Struktur bereit, die mit einem Ereignis Objekt oder einem Abschlussport verwendet wird. Bei einem e/a-Abschlussport wird ein HTTP-Handle als Datei Handle verwendet, das sich in einem asynchronen Datei-e/a-Vorgang befindet. In der folgenden Tabelle werden die für die-Anwendungen verfügbaren Abschluss Optionen zusammengefasst.



| Überlappende Struktur | Ereignis Objekt   | Abschlussport | Completion                                                                                                   |
|----------------------|----------------|-----------------|--------------------------------------------------------------------------------------------------------------|
| **NULL**             | Nicht zutreffend | Wird ignoriert.         | Der Vorgang wird synchron abgeschlossen.                                                                           |
| Ungleich **null**         | Ungleich **null**   | **NULL**        | Der Vorgang wird asynchron abgeschlossen. Überlappende Benachrichtigungen werden durch Signalisieren eines Ereignis Objekts ausgeführt.       |
| Ungleich **null**         | Wird ignoriert.        | Ungleich **null**    | Der Vorgang wird asynchron abgeschlossen. Überlappende Benachrichtigungen werden durch Planen einer Abschluss Routine ausgeführt. |



 

## <a name="returning-the-number-of-bytes-read"></a>Zurückgeben der Anzahl der gelesenen Bytes

Einige der Funktionen, die die [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur für den asynchronen Abschluss verwenden, geben einen *pbytesempfang-Parameter* (oder *pbytess* -oder *pbytesread*-Parameter) zurück, der die Anzahl der synchron übertragenen Bytes angibt. Für asynchrone Aufrufe sollte dieser Parameter auf **null** festgelegt werden. Bei synchronen Aufrufen ist der *pbytesempfangene* Parameter optional und kann entweder **null** oder nicht **null** sein.

Wenn das Ereignis Objekt für den asynchronen Abschluss verwendet wird, wird die Funktion [**gejeverlappedresult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) aufgerufen, um die Anzahl der gelesenen Bytes zu bestimmen. Wenn der Abschlussport verwendet wird (der *hFile* -Parameter ist einem e/a-Abschlussport zugeordnet), ruft die Anwendung die [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion auf, um die Anzahl der gelesenen Bytes zu bestimmen. Wenn die asynchronen Vorgänge nicht abgeschlossen wurden, können Anwendungen die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion aufrufen, um erweiterte Fehlerinformationen zu erhalten.

In der folgenden Tabelle wird das Abschluss Verhalten für die synchrone und asynchrone Vervollständigung in Funktionen, wie z. b. [**httpreceivehttprequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) , mit dem *pbytesempfangparameter* zusammengefasst.



| pbytesempfangene\* | poverlt  | BESCHREIBUNG                                                                             |
|------------------|--------------|-----------------------------------------------------------------------------------------|
| **NULL**         | **NULL**     | Die Anwendung empfängt keine Informationen über die Anzahl der zurückgegebenen Bytes.           |
| **NULL**         | Ungleich **null** | Asynchroner Vorgang, *pbytesempfangener* ist bedeutungslos.                                |
| Ungleich **null**     | **NULL**     | Synchroner Vorgang, Anzahl der in *pbytesempfangenen* bytes.                    |
| Ungleich **null**     | Ungleich **null** | Asynchroner Vorgang, *pbytesempfangsvorgang* wird ignoriert, auch wenn er nicht **null** ist.\*\* |



 

> [!Note]  
> \*Dieser Parameter kann auch " *pbytess ent* " oder " *pbytesread*" lauten.

 

> [!Note]  
> \*\*Es wird empfohlen, dass Anwendungen für asynchrone Vorgänge einen **null** -Wert in " *pbytesget* " übergeben und die Anzahl von Bytes abrufen, die von [**gegeverlappedresult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) oder [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)empfangen werden.

 

## <a name="return-codes"></a>Rückgabecodes

Die HTTP-Server-API gibt drei Klassen von Codes für asynchrone Funktionsaufrufe zurück.

-   kein \_ Fehler
-   Fehler- \_ IO steht \_ aus
-   Alle anderen [Systemfehler Codes](/windows/desktop/Debug/system-error-codes).

Wenn die Fehler-e/a-Vorgänge \_ \_ Ausstehend oder kein \_ Fehler vom asynchronen Funktionsaufrufen zurückgegeben wird, sollten die Benutzer erwarten, dass das Ereignis oder die Abschluss Routine signalisiert wird. Wenn Sie die [**GetOverLappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) -Funktion für das-Ereignis oder die [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion für den Abschlussport aufrufen, wird der Abschluss Status zurückgegeben. Wenn kein \_ Fehler zurückgegeben wird, können Anwendungen außerdem die Nachbearbeitung in demselben Thread ausführen, der den API-Befehl durchgeführt hat.

Wenn die HTTP-Server-API einen anderen Wert als Fehler-e/a \_ \_ oder keinen Fehler zurückgibt \_ , wird die Abschluss Routine vom asynchronen Funktionsaufrufen nicht signalisiert, und der Fehler wird direkt von der API zurückgegeben.

 

 