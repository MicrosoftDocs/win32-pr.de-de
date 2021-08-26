---
title: HTTP-Vervollständigungsroutinen
description: Anwendungen haben mehrere Optionen zum Empfangen von Vervollständigungshinweisen und bieten Entwicklern eine gewisse Flexibilität.
ms.assetid: c48a64d2-b6c8-4694-8600-f84751954bad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd80259d806d81153a649ad606e40c10986090442e3cab5e04bd864367441871
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981670"
---
# <a name="http-completion-routines"></a>HTTP-Vervollständigungsroutinen

Anwendungen haben mehrere Optionen zum Empfangen von Vervollständigungshinweisen und bieten Entwicklern eine gewisse Flexibilität. Die Optionen sind das Blockieren während des Wartens auf den Abschluss eines API-Aufrufs oder die Verwendung von Vervollständigungsroutinen für asynchrone Vorgänge. Der Vorteil der Verwendung asynchroner Vorgänge ist eine höhere Reaktionsfähigkeit der Anwendung.

## <a name="blocked-io"></a>Blockierte E/A

Anwendungen können blockieren, während auf den Abschluss des API-Aufrufs gewartet wird, indem die [**OVERLAPPED-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) auf **NULL** festgelegt wird. Dadurch werden alle Vorgänge im Thread blockiert. Bei Aufrufen von [**HttpWaitForDisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)wird der Aufruf beispielsweise blockiert, bis die Verbindung unterbrochen wird.

## <a name="asynchronous-io"></a>Asynchrone E/A

Anwendungen, die nicht blockieren möchten, können die [**OVERLAPPED-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) verwenden, um die Abschlussergebnisse zu erhalten. Die Anwendung stellt einen Zeiger auf eine **OVERLAPPED-Struktur** bereit, die mit einem Ereignisobjekt oder einem Abschlussport verwendet wird. Bei einem E/A-Abschlussport wird ein HTTP-Handle als Dateihandle in einem asynchronen Datei-E/A-Vorgang verwendet. In der folgenden Tabelle sind die vervollständigungsoptionen zusammengefasst, die den Anwendungen zur Verfügung stehen.



| Überlappende Struktur | Ereignisobjekt   | Abschlussport | Completion                                                                                                   |
|----------------------|----------------|-----------------|--------------------------------------------------------------------------------------------------------------|
| **NULL**             | Nicht zutreffend | Wird ignoriert.         | Der Vorgang wird synchron abgeschlossen.                                                                           |
| Ungleich **NULL**         | Ungleich **NULL**   | **NULL**        | Der Vorgang wird asynchron abgeschlossen. Überlappende Benachrichtigungen werden ausgeführt, indem ein Ereignisobjekt signalisiert wird.       |
| Ungleich **NULL**         | Wird ignoriert.        | Ungleich **NULL**    | Der Vorgang wird asynchron abgeschlossen. Überlappende Benachrichtigungen werden ausgeführt, indem eine Abschlussroutine geplant wird. |



 

## <a name="returning-the-number-of-bytes-read"></a>Zurückgeben der Anzahl gelesener Bytes

Einige der Funktionen, die die [**OVERLAPPED-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) für die asynchrone Vervollständigung verwenden, geben einen *pBytesReceived-Parameter* (oder *pBytesSent* oder *pBytesRead)* zurück, der die Anzahl der synchron übertragenen Bytes angibt. Bei asynchronen Aufrufen sollte dieser Parameter auf **NULL** festgelegt werden. Bei synchronen Aufrufen ist der *pBytesReceived-Parameter* optional und kann entweder **NULL** oder ungleich **NULL** sein.

Wenn das Ereignisobjekt für die asynchrone Vervollständigung verwendet wird, wird die [**GetOverlappedResult-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) aufgerufen, um die Anzahl der gelesenen Bytes zu bestimmen. Wenn der Abschlussport verwendet wird (der *hFile-Parameter* ist einem E/A-Abschlussport zugeordnet), ruft die Anwendung die [**GetQueuedCompletionStatus-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) auf, um die Anzahl der gelesenen Bytes zu bestimmen. Wenn die asynchronen Vorgänge nicht abgeschlossen wurden, können Anwendungen die [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) aufrufen, um erweiterte Fehlerinformationen abzurufen.

In der folgenden Tabelle wird das Vervollständigungsverhalten für die synchrone und asynchrone Vervollständigung in Funktionen wie [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) zusammengefasst, die den *pBytesReceived-Parameter* verwenden.



| pBytesReceived\* | pOverlapped  | Beschreibung                                                                             |
|------------------|--------------|-----------------------------------------------------------------------------------------|
| **NULL**         | **NULL**     | Die Anwendung empfängt keine Informationen zur Anzahl der zurückgegebenen Bytes.           |
| **NULL**         | Ungleich **NULL** | Der asynchrone Vorgang *pBytesReceived* ist bedeutungslos.                                |
| Ungleich **NULL**     | **NULL**     | Synchroner Vorgang, Anzahl der in *pBytesReceived zurückgegebenen* Bytes.                    |
| Ungleich **NULL**     | Ungleich **NULL** | Der asynchrone Vorgang *pBytesReceived* wird ignoriert, obwohl er nicht **NULL** ist.\*\* |



 

> [!Note]  
> \*Dieser Parameter kann auch *pBytesSent* oder *pBytesRead* sein.

 

> [!Note]  
> \*\*Es wird empfohlen, dass Anwendungen einen **NULL-Wert** in *pBytesReceived* für asynchrone Vorgänge übergeben und die Anzahl der Bytes abrufen, die von [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) oder [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)empfangen werden.

 

## <a name="return-codes"></a>Rückgabecodes

Die HTTP-Server-API gibt drei Klassen von Codes für asynchrone Funktionsaufrufe zurück.

-   KEIN \_ FEHLER
-   FEHLER \_ \_ E/A AUSSTEHEND
-   Jeder andere [Systemfehlercode.](/windows/desktop/Debug/system-error-codes)

Wenn ERROR \_ IO \_ PENDING oder NO \_ ERROR vom asynchronen Funktionsaufruf zurückgegeben wird, sollten Benutzer erwarten, dass die Ereignis- oder Abschlussroutine signalisiert wird. Durch Aufrufen der [**GetOverlappedResult-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) für das Ereignis oder der [**GetQueuedCompletionStatus-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) für den Abschlussport wird der Abschlussstatus zurückgegeben. Wenn NO ERROR zurückgegeben wird, können Anwendungen außerdem \_ die Nachverarbeitung für denselben Thread durchführen, der den API-Aufruf ausgeführt hat.

Wenn die HTTP-Server-API vom asynchronen Funktionsaufruf etwas anderes als ERROR \_ IO \_ PENDING oder NO ERROR zurückgibt, \_ wird die Abschlussroutine nicht signalisiert, und der Fehler wird direkt von der API zurückgegeben.

 

 