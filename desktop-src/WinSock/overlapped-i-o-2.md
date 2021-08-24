---
description: Windows Sockets 2 führt überlappende E/A ein und erfordert, dass alle Transportanbieter diese Funktion unterstützen.
ms.assetid: 90d49171-e211-4426-aa56-88aaeac7c578
title: Überlappende Eingabe/Ausgabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d260cccd13bfb8e872e0ac7346c112efff2f77cf115e3fe2f8dd3d3fb94deb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641790"
---
# <a name="overlapped-inputoutput"></a>Überlappende Eingabe/Ausgabe

Windows Sockets 2 führt überlappende E/A ein und erfordert, dass alle Transportanbieter diese Funktion unterstützen. Überlappende E/A-Funktionen können nur für Sockets ausgeführt werden, die mit der [**WSPSocket-Funktion**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) erstellt wurden, für die das Flag WSA FLAG OVERLAPPED festgelegt ist, und das in diesem Artikel eingerichtete \_ \_ Windows.

Für den Empfang verwendet ein Client [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) oder [**WSPRecvFrom,**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) um Puffer für den Empfang von Daten zu liefern. Wenn ein oder mehrere Puffer vor dem Zeitpunkt gesendet werden, zu dem Daten vom Netzwerk empfangen wurden, können Daten sofort beim Eintreffen in den Puffern des Benutzers platziert werden, und so den Kopiervorgang vermeiden, der andernfalls auftreten würde. Wenn Daten empfangen werden, wenn empfangspuffer bereits gesendet wurden, werden sie sofort in die Puffer des Benutzers kopiert. Wenn Daten empfangen werden, wenn keine Empfangspuffer von der Anwendung gesendet wurden, greift der Dienstanbieter auf den synchronen Vorgangsstil zurück, bei dem die eingehenden Daten intern gepuffert werden, bis der Client einen Empfangsaufruf aus gibt und dadurch einen Puffer zur Verfügung stellt, in den die Daten kopiert werden können. Eine Ausnahme wäre, wenn die Anwendung [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) verwendet hat, um die Größe des Empfangspuffers auf 0 (null) zu setzen. In diesem Fall würden zuverlässige Protokolle nur den Daten empfangen, wenn Anwendungspuffer gesendet wurden, und Daten in unzuverlässigen Protokollen würden verloren gehen.

Auf der Sendeseite verwenden Clients [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) oder [**WSPSendTo,**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) um Zeiger auf gefüllte Puffer zu liefern, und stimmen dann zu, die Puffer in irgendeiner Weise zu stören, bis das Netzwerk den Inhalt des Puffers verbraucht hat.

Überlappende Sende- und Empfangsaufrufe werden sofort zurück. Der Rückgabewert 0 (null) gibt an, dass der E/A-Vorgang sofort abgeschlossen wurde und dass die entsprechende Vervollständigungsanzeige bereits aufgetreten ist. Das heißt, das zugeordnete Ereignisobjekt wurde signalisiert, oder die Abschlussroutine wurde über [**WPUQueueApc in die Warteschlange gestellt.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) Der Rückgabewert SOCKET ERROR in Verbindung mit einem Fehlercode von WSA IO PENDING gibt an, dass der überlappende Vorgang erfolgreich initiiert wurde und dass ein nachfolgender Hinweis angezeigt wird, wenn Sendepuffer verbraucht oder Empfangspuffer gefüllt \_ \_ \_ wurden. Jeder andere Fehlercode gibt an, dass der überlappende Vorgang nicht erfolgreich initiiert wurde und keine Vervollständigungsanzeige anstehender ist.

Sowohl Sende- als auch Empfangsvorgänge können überlappen. Die Empfangsfunktionen können mehrmals aufgerufen werden, um Empfangspuffer als Vorbereitung auf eingehende Daten zu senden, und die Sendefunktionen können mehrmals aufgerufen werden, um mehrere zu sendende Puffer in die Warteschlange zu stellen. Beachten Sie, dass zwar eine Reihe von überlappenden Sendepuffern in der angegebenen Reihenfolge gesendet wird, die entsprechenden Vervollständigungsanzeigen jedoch in einer anderen Reihenfolge auftreten können. Auf der empfangenden Seite werden Puffer in der Reihenfolge aufgefüllt, in der sie angegeben werden, aber die Vervollständigungsanzeigen können in einer anderen Reihenfolge auftreten.

Die Verzögerte Vervollständigung von überlappenden E/A-Funktionen ist auch für [**WSPIoctl verfügbar.**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))

## <a name="delivering-completion-indications"></a>Bereitstellen von Vervollständigungsanzeigen

Dienstanbieter haben zwei Möglichkeiten, eine überlappende Vervollständigung anzugeben: Das Festlegen eines vom Client angegebenen Ereignisobjekts oder das Aufrufen einer vom Client angegebenen Vervollständigungsroutine. In beiden Fällen wird jedem überlappenden Vorgang eine [**Datenstruktur, WSAOVERLAPPED,**](/windows/desktop/api/Winsock2/ns-winsock2-wsaoverlapped)zugeordnet. Diese Struktur wird vom Client zugeordnet und von diesem verwendet, um anzugeben, welches Ereignisobjekt (falls möglich) beim Abschluss festgelegt werden soll. Die **WSAOVERLAPPED-Struktur** kann vom Dienstanbieter als Ort zum Speichern eines Handles für die Ergebnisse (z. B. Anzahl der übertragenen Bytes, aktualisierte Flags, Fehlercodes usw.) für einen bestimmten überlappenden Vorgang verwendet werden. Um diese Ergebnisse zu erhalten, müssen Clients [**WSPGetOverlappedResult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult)aufrufen und einen Zeiger auf die entsprechende überlappende Struktur übergeben.

Wenn die ereignisbasierte Vervollständigungsanzeige für eine bestimmte überlappende E/A-Anforderung ausgewählt ist, kann die [**WSPGetOverlappedResult-Routine**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult) von Clients selbst verwendet werden, um den Überlappungsvorgang abzuwarten oder auf den Abschluss zu warten. Wenn die Vervollständigungsroutinen-basierte Vervollständigungsanzeige für eine bestimmte überlappende E/A-Anforderung ausgewählt ist, ist nur die Abrufoption **WSPGetOverlappedResult** verfügbar. Ein Client kann auch andere Mittel verwenden, um zu warten (z. B. [**WSAWaitForMultipleEvents),**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents)bis das entsprechende Ereignisobjekt signalisiert wurde oder die angegebene Abschlussroutine vom Dienstanbieter aufgerufen wurde. Nachdem der Abschluss angegeben wurde, kann der Client **WSPGetOverlappedResult** mit der Annahme aufrufen, dass der Aufruf sofort abgeschlossen wird.

## <a name="invoking-socket-io-completion-routines"></a>Aufrufen von Socket-E/A-Abschlussroutinen

Wenn der *lpCompletionRoutine-Parameter* für einen überlappenden Vorgang nicht **NULL** ist, liegt es in der Verantwortung des Dienstanbieters, den Aufruf der vom Client angegebenen Vervollständigungsroutine zu organisieren, wenn der überlappende Vorgang abgeschlossen ist. Da die Abschlussroutine im Kontext desselben Threads ausgeführt werden muss, der den überlappenden Vorgang initiiert hat, kann sie nicht direkt vom Dienstanbieter aufgerufen werden. Die Ws2-32.DLL bietet einen APC-Mechanismus (Asynchronous Procedure Call), um den Aufruf von \_ Abschlussroutinen zu erleichtern.

Ein Dienstanbieter sorgt dafür, dass eine Funktion im richtigen Thread ausgeführt wird, indem [**WPUQueueApc aufgerufen wird.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) Diese Funktion kann von jedem Prozess- und Threadkontext aufgerufen werden, auch in einem anderen Kontext als der Thread und Prozess, der zum Initiieren des überlappenden Vorgangs verwendet wurde.

[**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) verwendet als Eingabeparameter einen Zeiger auf eine [**WSATHREADID-Struktur,**](/windows/desktop/api/Ws2spi/ns-ws2spi-wsathreadid) einen Zeiger auf eine aufrufbare APC-Funktion und einen 32-Bit-Kontextwert, der anschließend an die APC-Funktion übergeben wird. Dienstanbieter werden immer mit einem Zeiger auf die richtige **WSATHREADID-Struktur** über den *lpThreadId-Parameter* auf die überlappende Funktion bereitgestellt. Der Anbieter sollte die **WSATHREADID-Struktur** lokal speichern und einen Zeiger auf diese Kopie der **WSATHREADID-Struktur** als Eingabeparameter für **WPUQueueApc angeben.** Sobald die **WPUQueueApc-Funktion** zurückgegeben wird, kann der Anbieter seine Kopie von **WSATHREADID veräußern.**

Die [**Prozedur WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) stellt lediglich genügend Informationen in die Queue ein, um die angegebene APC-Funktion mit den angegebenen Parametern auf aufruft, aber nicht. Wenn der Zielthread in einen wartbaren Wartezustand versetzt wird, werden diese Informationen aus der Quequetierung entfernt, und die APC-Funktion wird in diesem Zielthread und Prozesskontext aufgerufen. Da der APC-Mechanismus nur einen einzelnen 32-Bit-Kontextwert unterstützt, kann die APC-Funktion nicht selbst die vom Client angegebene Vervollständigungsroutine sein, die mehr Parameter umfasst. Der Dienstanbieter muss stattdessen einen Zeiger auf seine eigene APC-Funktion angeben, die den angegebenen Kontextwert verwendet, um auf die erforderlichen Ergebnisinformationen für den überlappenden Vorgang zu zugreifen, und dann die vom Client angegebene Vervollständigungsroutine aufruft.

Bei Dienstanbietern, bei denen eine Benutzermoduskomponente überlappende E/A implementiert, wird der APC-Mechanismus in der Regel wie folgt verwendet:

-   Wenn der E/A-Vorgang abgeschlossen ist, ordnet der Anbieter einen kleinen Puffer zu und packt ihn mit einem Zeiger auf die vom Client bereitgestellte Vervollständigungsprozedur und Parameterwerte, die an die Prozedur übergeben werden.
-   Er stellt einen APC in die Warteschlange und gibt den Zeiger auf den Puffer als Kontextwert und seine eigene Zwischenprozedur als Zielprozedur an.
-   Wenn der Zielthread schließlich den wartbaren Wartezustand erreicht, wird die Zwischenprozedur des Dienstanbieters im richtigen Threadkontext aufgerufen.
-   Die Zwischenprozedur entpackt einfach Parameter, entpackt den Puffer und ruft die vom Client bereitgestellte Vervollständigungsprozedur auf.
-   Bei Dienstanbietern, bei denen eine Kernelmoduskomponente überlappende E/A implementiert, ist eine typische Implementierung ähnlich, mit der Ausnahme, dass die Implementierung Standardkernelschnittstellen verwendet, um den APC in die Enqueue zu setzen.

Die Beschreibung der relevanten Kernelschnittstellen liegt außerhalb des Bereichs der Windows Sockets 2-Spezifikation.

> [!Note]  
> Dienstanbieter müssen Windows Sockets 2-Clients das Aufrufen von Sende- und Empfangsvorgängen innerhalb des Kontexts der Socket-E/A-Abschlussroutine gestatten und gewährleisten, dass E/A-Abschlussroutinen für einen bestimmten Socket nicht geschachtelt werden.

 

Unter bestimmten Umständen muss ein mehrschichtiger Dienstanbieter möglicherweise überlappende Vorgänge innerhalb eines internen Arbeitsthreads initiieren und abschließen. In diesem Fall wäre [**eine WSATHREADID**](/windows/desktop/api/Ws2spi/ns-ws2spi-wsathreadid) nicht über einen eingehenden Funktionsaufruf verfügbar. Die Dienstanbieterschnittstelle stellt einen Upcall( [**WPUOpenCurrentThread)**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuopencurrentthread)bereit, um **eine WSATHREADID** für den aktuellen Thread zu erhalten. Wenn diese **WSATHREADID** nicht mehr benötigt wird, sollten ihre Ressourcen durch Aufrufen von [**WPUCloseThread zurückgegeben werden.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosethread)

 

 
