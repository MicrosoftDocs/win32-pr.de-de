---
description: 'Es gibt zwei Arten von E/A-Synchronisierung(E/A): synchrone E/A und asynchrone E/A. Asynchrone E/A wird auch als überlappende E/A bezeichnet.'
ms.assetid: ade51d98-cc9d-4b33-9c52-559a9cb14707
title: Synchrone und asynchrone E/A
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 99ab06fac66c0ff3033407326c190ce0d08e643ca30b24ff17b7420e61782222
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981824"
---
# <a name="synchronous-and-asynchronous-io"></a>Synchrone und asynchrone E/A

Siehe auch [E/A-bezogene Beispielanwendungen.](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winbase/io)

Es gibt zwei Arten von E/A-Synchronisierung(E/A): synchrone E/A und asynchrone E/A. Asynchrone E/A wird auch als überlappende E/A bezeichnet.

Bei *synchronen Datei-E/A* startet ein Thread einen E/A-Vorgang und wechselt sofort in einen Wartezustand, bis die E/A-Anforderung abgeschlossen ist. Ein Thread, der *asynchrone Datei-E/A-Vorgänge* ausführt, sendet eine E/A-Anforderung an den Kernel, indem er eine entsprechende Funktion aufruft. Wenn die Anforderung vom Kernel akzeptiert wird, setzt der aufrufende Thread die Verarbeitung eines anderen Auftrags fort, bis der Kernel dem Thread signalisiert, dass der E/A-Vorgang abgeschlossen ist. Anschließend unterbricht es den aktuellen Auftrag und verarbeitet die Daten aus dem E/A-Vorgang nach Bedarf.

Die beiden Synchronisierungstypen sind in der folgenden Abbildung dargestellt.

![synchrone und asynchrone E/A-Vorgänge](images/fig2bedit.png)

In Situationen, in denen eine E/A-Anforderung voraussichtlich viel Zeit in Anspruch nimmt, z. B. eine Aktualisierung oder Sicherung einer großen Datenbank oder eine langsame Kommunikationsverbindung, ist asynchrone E/A im Allgemeinen eine gute Möglichkeit, die Verarbeitungseffizienz zu optimieren. Bei relativ schnellen E/A-Vorgängen kann der Mehraufwand für die Verarbeitung von Kernel-E/A-Anforderungen und Kernelsignalen asynchrone E/A jedoch weniger vorteilhaft machen, insbesondere wenn viele schnelle E/A-Vorgänge durchgeführt werden müssen. In diesem Fall wäre synchrone E/A besser. Die Mechanismen und Implementierungsdetails zur Durchführung dieser Aufgaben variieren je nach Art des verwendeten Gerätehandle und den speziellen Anforderungen der Anwendung. Anders ausgedrückt: Es gibt in der Regel mehrere Möglichkeiten, das Problem zu lösen.

## <a name="synchronous-and-asynchronous-io-considerations"></a>Synchrone und asynchrone E/A-Überlegungen

Wenn eine Datei oder ein Gerät für synchrone E/A geöffnet wird (d. h., **FILE \_ FLAG \_ OVERLAPPED** ist nicht angegeben), können nachfolgende Aufrufe von Funktionen wie [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) die Ausführung des aufrufenden Threads blockieren, bis eines der folgenden Ereignisse eintritt:

-   Der E/A-Vorgang wird abgeschlossen (in diesem Beispiel ein Datenschreibvorgang).
-   Ein E/A-Fehler tritt auf. (Beispielsweise wird die Pipe vom anderen Ende geschlossen.)
-   Im Aufruf selbst ist ein Fehler aufgetreten (z. B. sind mindestens ein Parameter ungültig).
-   Ein anderer Thread im Prozess ruft die [**CancelSynchronousIo-Funktion**](cancelsynchronousio-func.md) mithilfe des Threadhandle des blockierten Threads auf, das die E/A für diesen Thread beendet, wodurch der E/A-Vorgang fehlschlägt.
-   Der blockierte Thread wird vom System beendet. Beispielsweise wird der Prozess selbst beendet, oder ein anderer Thread ruft die [**TerminateThread-Funktion**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) mithilfe des Handles des blockierten Threads auf. (Dies gilt im Allgemeinen als letztes Mittel und nicht als guter Anwendungsentwurf.)

In einigen Fällen kann diese Verzögerung für den Entwurf und Zweck der Anwendung nicht akzeptabel sein, daher sollten Anwendungsdesigner die Verwendung asynchroner E/A mit entsprechenden Threadsynchronisierungsobjekten wie [E/A-Abschlussports](i-o-completion-ports.md)in Betracht ziehen. Weitere Informationen zur Threadsynchronisierung finden Sie unter [Informationen zur Synchronisierung.](/windows/desktop/Sync/about-synchronization)

Ein Prozess öffnet eine Datei für asynchrone E/A im Aufruf von [**CreateFile,**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) indem das **FLAG FILE FLAG \_ \_ OVERLAPPED** im *dwFlagsAndAttributes-Parameter* angegeben wird. Wenn **FILE \_ FLAG \_ OVERLAPPED** nicht angegeben ist, wird die Datei für synchrone E/A geöffnet. Wenn die Datei für asynchrone E/A geöffnet wurde, wird ein Zeiger auf eine [**OVERLAPPED-Struktur**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) an den Aufruf von [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) und [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)übergeben. Bei der Ausführung synchroner E/A ist diese Struktur bei Aufrufen von **ReadFile** und **WriteFile** nicht erforderlich.

> [!Note]  
> Wenn eine Datei oder ein Gerät für asynchrone E/A geöffnet wird, werden nachfolgende Aufrufe von Funktionen wie [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) mit diesem Handle in der Regel sofort zurückgegeben, können sich aber auch synchron in Bezug auf die blockierte Ausführung verhalten. Weitere Informationen finden Sie unter [https://support.microsoft.com/kb/156932](https://support.microsoft.com/kb/156932).

 

Obwohl [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) die gängigste Funktion ist, die zum Öffnen von Dateien, Datenträgervolumes, anonymen Pipes und anderen ähnlichen Geräten verwendet wird, können E/A-Vorgänge auch mithilfe eines *Handletypcasts* von anderen Systemobjekten ausgeführt werden, z. B. einem Socket, der vom [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) erstellt wurde, oder [**accept-Funktionen.**](/windows/desktop/api/winsock2/nf-winsock2-accept)

Handles für Verzeichnisobjekte werden abgerufen, indem die [**CreateFile-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) mit dem **FILE FLAG BACKUP \_ \_ \_ SEMANTICS-Attribut** aufgerufen wird. Verzeichnishandles werden fast nie verwendet– Sicherungsanwendungen sind eine der wenigen Anwendungen, die sie normalerweise verwenden.

Nach dem Öffnen des Dateiobjekts für asynchrone E/A muss eine [**OVERLAPPED-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) ordnungsgemäß erstellt, initialisiert und an jeden Aufruf von Funktionen wie [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) und [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)übergeben werden. Beachten Sie Folgendes, wenn Sie die [**OVERLAPPED-Struktur**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) in asynchronen Lese- und Schreibvorgängen verwenden:

-   Die Zuordnung der [**OVERLAPPED-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) oder des Datenpuffers wird erst freigegeben oder geändert, wenn alle asynchronen E/A-Vorgänge für das Dateiobjekt abgeschlossen wurden.
-   Wenn Sie den Zeiger auf die [**OVERLAPPED-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) als lokale Variable deklarieren, beenden Sie die lokale Funktion erst, nachdem alle asynchronen E/A-Vorgänge für das Dateiobjekt abgeschlossen wurden. Wenn die lokale Funktion vorzeitig beendet wird, verlässt die **OVERLAPPED-Struktur** den Gültigkeitsbereich und ist für alle [**ReadFile-**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) oder [**WriteFile-Funktionen,**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) die sie außerhalb dieser Funktion findet, nicht zugänglich.

Sie können auch ein Ereignis erstellen und das Handle in die [**OVERLAPPED-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) aufnehmen. Die [Wait-Funktionen](/windows/desktop/Sync/wait-functions) können dann verwendet werden, um auf den Abschluss des E/A-Vorgangs zu warten, indem auf das Ereignishandle gewartet wird.

Wie bereits erwähnt, sollten Anwendungen beim Arbeiten mit einem asynchronen Handle vorsichtshalber bestimmen, wann Ressourcen freigegeben werden sollen, die einem angegebenen E/A-Vorgang für dieses Handle zugeordnet sind. Wenn die Zuordnung des Handles vorzeitig freigegeben wird, meldet [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) oder [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) möglicherweise fälschlicherweise, dass der E/A-Vorgang abgeschlossen ist. Darüber hinaus gibt die **WriteFile-Funktion** manchmal **TRUE** mit dem [**GetLastError-Wert**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) **ERROR \_ SUCCESS** zurück, obwohl sie ein asynchrones Handle verwendet (das auch **FALSE** mit **ERROR IO \_ \_ PENDING** zurückgeben kann). Programmierer, die an den synchronen E/A-Entwurf gewohnt sind, geben an diesem Punkt normalerweise Datenpufferressourcen frei, da **TRUE** und **ERROR \_ SUCCESS** den Vorgang als abgeschlossen kennzeichnen. Wenn jedoch [E/A-Abschlussports](i-o-completion-ports.md) mit diesem asynchronen Handle verwendet werden, wird auch ein Abschlusspaket gesendet, obwohl der E/A-Vorgang sofort abgeschlossen wurde. Anders ausgedrückt: Wenn die Anwendung Ressourcen freigibt, nachdem **WriteFile** zusätzlich zur E/A-Abschlussportroutine **TRUE** mit **ERROR \_ SUCCESS** zurückgegeben hat, weist sie eine doppelte Fehlerbedingung auf. In diesem Beispiel wird empfohlen, zuzulassen, dass die Abschlussportroutine ausschließlich für alle Freilaufvorgänge für solche Ressourcen verantwortlich ist.

Das System verwaltet den Dateizeiger nicht auf asynchronen Handles für Dateien und Geräte, die Dateizeiger unterstützen (d. h. Geräte suchen). Daher muss die Dateiposition an die Lese- und Schreibfunktionen in den zugehörigen Offsetdatenmembern der [**OVERLAPPED-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) übergeben werden. Weitere Informationen finden Sie unter [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) und [**ReadFile.**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)

Die Position des Dateizeigers für ein synchrones Handle wird vom System beibehalten, wenn Daten gelesen oder geschrieben werden, und kann auch mithilfe der [**SetFilePointer-**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) oder [**SetFilePointerEx-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointerex) aktualisiert werden.

Eine Anwendung kann auch auf das Dateihandle warten, um den Abschluss eines E/A-Vorgangs zu synchronisieren. Dies erfordert jedoch äußerste Vorsicht. Jedes Mal, wenn ein E/A-Vorgang gestartet wird, legt das Betriebssystem das Dateihandle auf den nicht signalisierten Zustand fest. Jedes Mal, wenn ein E/A-Vorgang abgeschlossen wird, legt das Betriebssystem das Dateihandle auf den signalisierten Zustand fest. Wenn eine Anwendung zwei E/A-Vorgänge startet und auf das Dateihandle wartet, gibt es daher keine Möglichkeit, zu bestimmen, welcher Vorgang abgeschlossen ist, wenn das Handle auf den signalisierten Zustand festgelegt ist. Wenn eine Anwendung mehrere asynchrone E/A-Vorgänge für eine einzelne Datei ausführen muss, sollte sie nicht auf das allgemeine Dateihandle, sondern auf das Ereignishandle in der spezifischen [**OVERLAPPED-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) für jeden E/A-Vorgang warten.

Um alle ausstehenden asynchronen E/A-Vorgänge abzubrechen, verwenden Sie eine der beiden optionen:

-   [**CancelIo**](cancelio.md): Diese Funktion bricht nur Vorgänge ab, die vom aufrufenden Thread für das angegebene Dateihandle ausgegeben werden.
-   [**CancelIoEx**](cancelioex-func.md): Diese Funktion bricht alle Vorgänge ab, die von den Threads für das angegebene Dateihandle ausgegeben werden.

Verwenden Sie [**CancelSynchronousIo,**](cancelsynchronousio-func.md) um ausstehende synchrone E/A-Vorgänge abzubrechen.

Die Funktionen [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) und [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) ermöglichen es einer Anwendung, eine auszuführende Routine anzugeben (siehe [**FileIOCompletionRoutine),**](/windows/win32/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine)wenn die asynchrone E/A-Anforderung abgeschlossen ist.

 

 
