---
description: Windows Sockets 2 stellt überlappende e/a vor und erfordert, dass alle Transportanbieter diese Funktion unterstützen.
ms.assetid: 90d49171-e211-4426-aa56-88aaeac7c578
title: Überlappende Eingabe/Ausgabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d8caa13dd3d50e4f0fdaa1b92fa8e99afd8e2e1
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "103869620"
---
# <a name="overlapped-inputoutput"></a>Überlappende Eingabe/Ausgabe

Windows Sockets 2 stellt überlappende e/a vor und erfordert, dass alle Transportanbieter diese Funktion unterstützen. Überlappende e/a-Vorgänge können nur für Sockets ausgeführt werden, die über die [**wspsocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) -Funktion mit dem überlappenden Flag für das WSA \_ -Flag erstellt wurden \_ , und folgen dem in Windows eingerichteten Modell.

Zum empfangen verwendet ein Client [**wsprecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) oder [**wsprecvfrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) , um Puffer anzugeben, in die Daten empfangen werden sollen. Wenn ein oder mehrere Puffer vor dem Zeitpunkt gepostet werden, zu dem Daten vom Netzwerk empfangen wurden, ist es möglich, dass die Daten sofort in die Puffer des Benutzers eingefügt werden, sobald sie eintreffen, und so den Kopiervorgang vermeiden, der andernfalls stattfinden würde. Wenn Daten empfangen werden, wenn Empfangs Puffer bereits gepostet wurden, werden Sie sofort in die Puffer des Benutzers kopiert. Wenn die Daten empfangen werden, wenn von der Anwendung keine Empfangs Puffer gepostet wurden, greift der Dienstanbieter auf den synchronen Vorgangs Stil zu, bei dem die eingehenden Daten intern gepuffert werden, bis der Client einen Empfangs Aufruf ausgibt und damit einen Puffer bereitstellt, in den die Daten kopiert werden können. Eine Ausnahme besteht darin, dass die Anwendung [**wspsetsockopt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) verwendet, um die Größe des Empfangspuffers auf NULL festzulegen. In dieser Instanz können zuverlässige Protokolle nur Daten empfangen, wenn Anwendungs Puffer gepostet wurden, und Daten über unzuverlässige Protokolle würden verloren gehen.

Auf der sendenden Seite stellen Clients mithilfe von [**wspsend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) oder [**wspsendto**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) Zeiger auf gefüllte Puffer bereit und stimmen dann zu, dass die Puffer erst dann gestört werden, wenn das Netzwerk den Pufferinhalt genutzt hat.

Überlappende Sende-und Empfangs Aufrufe werden sofort zurückgegeben. Der Rückgabewert 0 (null) gibt an, dass der e/a-Vorgang sofort abgeschlossen wurde und dass die entsprechende Vervollständigungs Angabe bereits erfolgt ist. Das heißt, das zugeordnete Ereignis Objekt wurde signalisiert, oder die Abschluss Routine wurde über [**wpuqueueapc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)in die Warteschlange eingereiht. Der Rückgabewert \_ Socketfehler gekoppelt mit dem Fehlercode WSA e/A \_ \_ steht aus, dass der überlappende Vorgang erfolgreich initiiert wurde und dass ein weiterer Hinweis bereitgestellt wird, wenn Sendepuffer verarbeitet wurden oder Empfangs Puffer ausgefüllt werden. Jeder andere Fehlercode gibt an, dass der überlappende Vorgang nicht erfolgreich initiiert wurde und keine Vervollständigungs Angabe erfolgt.

Sende-und Empfangs Vorgänge können überlappen. Die Empfangsfunktionen können mehrmals aufgerufen werden, um Empfangs Puffer in Vorbereitung auf eingehende Daten zu senden, und die Sende Funktionen können mehrmals aufgerufen werden, um mehrere zu sendende Puffer in die Warteschlange zu stellen. Beachten Sie Folgendes: während eine Reihe von überlappenden Sende Puffern in der angegebenen Reihenfolge gesendet wird, können die entsprechenden Vervollständigungs Hinweise in einer anderen Reihenfolge auftreten. Ebenso werden Puffer auf der Empfangsseite in der Reihenfolge aufgefüllt, in der Sie bereitgestellt werden, aber Vervollständigungs Hinweise können in einer anderen Reihenfolge auftreten.

Die verzögerte Vervollständigungsfunktion der überlappenden e/a ist auch für [**wspioctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))verfügbar.

## <a name="delivering-completion-indications"></a>Bereitstellung von Abschluss hinweisen

Dienstanbieter haben zwei Möglichkeiten, den überlappenden Abschluss anzugeben: das Festlegen eines vom Client angegebenen Ereignis Objekts oder das Aufrufen einer vom Client angegebenen Vervollständigungs Routine. In beiden Fällen wird eine Datenstruktur ( [**wsaoverllapp**](/windows/desktop/api/Winsock2/ns-winsock2-wsaoverlapped)) jedem überlappenden Vorgang zugeordnet. Diese Struktur wird vom Client zugeordnet und verwendet, um anzugeben, welches Ereignis Objekt (sofern vorhanden) festgelegt werden soll, wenn der Vorgang abgeschlossen ist. Die **wsaoverllapp** -Struktur kann vom Dienstanbieter als Speicherort zum Speichern eines Handles für die Ergebnisse (z. b. Anzahl der übertragenen Bytes, aktualisierte Flags, Fehlercodes usw.) für einen bestimmten überlappenden Vorgang verwendet werden. Zum Abrufen dieser Ergebnisse müssen die Clients [**wspgefliverlappedresult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult)aufrufen und einen Zeiger auf die entsprechende überlappende Struktur übergeben.

Wenn für eine bestimmte überlappende e/a-Anforderung eine ereignisbasierte Vervollständigungs Anzeige ausgewählt ist, kann die [**wspgetoverlappedresult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult) -Routine von Clients verwendet werden, um die Ausführung des überlappenden Vorgangs abzufragen oder zu warten. Wenn für eine bestimmte überlappende e/a-Anforderung ein Vervollständigungs Hinweis auf Vervollständigungs Routine ausgewählt ist, ist nur die Abruf Option von **wspgetoverlappedresult** verfügbar. Ein Client kann auch andere Mittel für den warte Vorgang verwenden (z. b. die Verwendung von [**wsawaitformultipleevents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents)), bis das entsprechende Ereignis Objekt signalisiert wurde oder die angegebene Abschluss Routine vom Dienstanbieter aufgerufen wurde. Nachdem der Abschluss angegeben wurde, ruft der Client möglicherweise **wspgegetverlappedresult** auf, und es wird davon ausgegangen, dass der Aufruf sofort abgeschlossen wird.

## <a name="invoking-socket-io-completion-routines"></a>Aufrufen von Socket-e/a-Abschluss Routinen

Wenn der *lpCompletionRoutine* -Parameter für einen überlappenden Vorgang nicht **null** ist, liegt es in der Verantwortung des Dienstanbieters, den Aufruf der vom Client angegebenen Vervollständigungs Routine zu ordnen, wenn der überlappende Vorgang abgeschlossen ist. Da die Vervollständigungs Routine im Kontext desselben Threads ausgeführt werden muss, der den überlappenden Vorgang initiiert hat, kann Sie nicht direkt vom Dienstanbieter aufgerufen werden. Der Ws2- \_32.DLL bietet einen asynchronen Prozedur Aufruf (APC)-Mechanismus, um den Aufruf von Vervollständigungs Routinen zu vereinfachen.

Ein Dienstanbieter ordnet an, dass eine Funktion im richtigen Thread durch Aufrufen von [**wpuqueueapc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)ausgeführt wird. Diese Funktion kann von jedem Prozess-und Thread Kontext aus aufgerufen werden. Dies gilt auch für einen anderen Kontext als den Thread und den Prozess, der zum Initiieren des überlappenden Vorgangs verwendet wurde.

[**Wpuqueueapc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) übernimmt als Eingabeparameter einen Zeiger auf eine [**wsathreadid**](/windows/desktop/api/Ws2spi/ns-ws2spi-wsathreadid) -Struktur, einen Zeiger auf eine APC-Funktion, die aufgerufen werden soll, und einen 32-Bit-Kontextwert, der anschließend an die APC-Funktion weitergeleitet wird. Dienstanbieter werden stets mit einem Zeiger auf die richtige **wsathreadid** -Struktur über den *lpthreadid* -Parameter für die überlappende Funktion bereitgestellt. Der Anbieter sollte die **wsathreadid** -Struktur lokal speichern und einen Zeiger auf diese Kopie der **wsathreadid** -Struktur als Eingabeparameter für **wpuqueueapc** bereitstellen. Nachdem die **wpuqueueapc** -Funktion zurückgegeben wurde, kann der Anbieter seine Kopie von **wsathreadid** verwerfen.

Die Prozedur [**wpuqueueapc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) stellt einfach genügend Informationen in die Warteschlange, um die angegebene APC-Funktion mit den angegebenen Parametern aufzurufen, aber Sie wird nicht aufgerufen. Wenn der Zielthread in den Wartezustand einer Warn Tabelle wechselt, werden diese Informationen aus der Warteschlange entfernt, und die APC-Funktion wird in diesem Zielthread und Prozess Kontext aufgerufen. Da der APC-Mechanismus nur einen einzelnen 32-Bit-Kontextwert unterstützt, kann die APC-Funktion nicht selbst die vom Client angegebene Vervollständigungs Routine sein, die mehr Parameter umfasst. Der Dienstanbieter muss stattdessen einen Zeiger auf seine eigene APC-Funktion bereitstellen, die den angegebenen Kontextwert verwendet, um auf die erforderlichen Ergebnisinformationen für den überlappenden Vorgang zuzugreifen, und dann die vom Client angegebene Vervollständigungs Routine aufruft.

Für Dienstanbieter, bei denen eine Benutzermoduskomponente überlappende e/a implementiert, ist eine typische Verwendung des APC-Mechanismus wie folgt:

-   Wenn der e/a-Vorgang abgeschlossen ist, ordnet der Anbieter einen kleinen Puffer zu und packt ihn mit einem Zeiger auf die vom Client bereitgestellte Vervollständigungs Prozedur und Parameterwerte, die an die Prozedur übergeben werden.
-   Ein APC wird in die Warteschlange eingereiht, wobei der Zeiger auf den Puffer als Kontextwert und seine eigene zwischen Prozedur als Ziel Prozedur angegeben wird.
-   Wenn der Ziel Thread schließlich in den Wartezustand der Warn Tabelle wechselt, wird die zwischen Prozedur des Dienstanbieters im richtigen Thread Kontext aufgerufen.
-   Die zwischen Prozedur entpackt einfach Parameter, hebt die Zuordnung des Puffers auf und ruft die vom Client bereitgestellte Abschluss Prozedur auf.
-   Für Dienstanbieter, bei denen eine Kernelmoduskomponente überlappende e/a-Vorgänge implementiert, ist eine typische-Implementierung ähnlich, außer dass die-Implementierung standardmäßige Kernel Schnittstellen verwendet, um das APC in die Warteschlange zu stellen.

Die Beschreibung der relevanten Kernel Schnittstellen liegt außerhalb des Bereichs der Windows Sockets 2-Spezifikation.

> [!Note]  
> Dienstanbieter müssen zulassen, dass Windows Sockets 2-Clients Sende-und Empfangs Vorgänge aus dem Kontext der Socket-e/a-Abschluss Routine aufrufen und sicherstellen, dass die e/a-Abschluss Routinen für einen bestimmten Socket nicht geschachtelt werden.

 

Unter bestimmten Umständen muss ein geschichteter Dienstanbieter möglicherweise überlappende Vorgänge innerhalb eines internen Arbeits Threads initiieren und vervollständigen. In diesem Fall wäre eine [**wsathreadid**](/windows/desktop/api/Ws2spi/ns-ws2spi-wsathreadid) nicht in einem eingehenden Funktions aufrufsbefehl verfügbar. Die Dienstanbieter Schnittstelle stellt einen [**upcallwpuopencurrentthread**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuopencurrentthread)bereit, um eine **wsathreadid** für den aktuellen Thread zu erhalten. Wenn diese **wsathreadid** nicht mehr benötigt wird, sollten ihre Ressourcen durch Aufrufen von [**wpuclosethread**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosethread)zurückgegeben werden.

 

 
