---
description: 'Es gibt zwei Arten der Eingabe-/ausgabesynchronisierung (e/a): Synchrone e/a-Vorgänge und asynchrone e/a-Vorgänge. Asynchrone e/a-Vorgänge werden auch als überlappende e/a-Vorgänge bezeichnet.'
ms.assetid: ade51d98-cc9d-4b33-9c52-559a9cb14707
title: Synchrone und asynchrone e/a
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 071dd2943537dcb6aff67a95cb5e2c3d514f4c1a
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "106355251"
---
# <a name="synchronous-and-asynchronous-io"></a>Synchrone und asynchrone e/a

Siehe auch e [/a-bezogene Beispielanwendungen](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winbase/io).

Es gibt zwei Arten der Eingabe-/ausgabesynchronisierung (e/a): Synchrone e/a-Vorgänge und asynchrone e/a-Vorgänge. Asynchrone e/a-Vorgänge werden auch als überlappende e/a-Vorgänge bezeichnet.

In *synchronen Datei-e/* a startet ein Thread einen e/a-Vorgang und wechselt sofort in den Wartezustand, bis die e/a-Anforderung abgeschlossen ist. Ein Thread, der *asynchrone Datei-e/* a-Vorgänge ausführt, sendet eine e/a-Anforderung an den Kernel, indem eine entsprechende Funktion aufgerufen wird. Wenn die Anforderung vom Kernel akzeptiert wird, setzt der aufrufende Thread die Verarbeitung eines anderen Auftrags fort, bis der Kernel dem Thread signalisiert, dass der e/a-Vorgang beendet ist. Er unterbricht dann seinen aktuellen Auftrag und verarbeitet die Daten aus dem e/a-Vorgang bei Bedarf.

Die zwei Synchronisierungs Typen sind in der folgenden Abbildung dargestellt.

![synchrone und asynchrone e/a](images/fig2bedit.png)

Wenn erwartet wird, dass eine e/a-Anforderung sehr lange dauert, wie z. b. eine Aktualisierung oder Sicherung einer großen Datenbank oder einer langsamen Kommunikationsverbindung, ist asynchrone e/a-Vorgänge im Allgemeinen eine gute Möglichkeit zur Optimierung der Verarbeitungseffizienz. Bei relativ schnellen e/a-Vorgängen kann der Aufwand für die Verarbeitung von Kernel-e/a-Anforderungen und Kernel Signalen jedoch dazu führen, dass asynchrone e/a-Vorgänge weniger vorteilhaft sind, insbesondere, wenn viele schnelle e/a-Vorgänge durchgeführt werden müssen. In diesem Fall wäre die synchrone e/a besser. Die Mechanismen und Implementierungsdetails zum Ausführen dieser Aufgaben hängen von der Art des verwendeten Geräte Handles und den speziellen Anforderungen der Anwendung ab. Anders ausgedrückt, gibt es in der Regel mehrere Möglichkeiten, um das Problem zu beheben.

## <a name="synchronous-and-asynchronous-io-considerations"></a>Synchrone und asynchrone e/a-Überlegungen

Wenn eine Datei oder ein Gerät für synchrone e/a-Vorgänge geöffnet ist (d. h., das überlappende **\_ Dateiflag \_** ist nicht angegeben), können nachfolgende Aufrufe von Funktionen wie z. b. " [**Write File**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) " die Ausführung des aufrufenden Threads blockieren, bis eines der folgenden Ereignisse eintritt:

-   Der e/a-Vorgang wird abgeschlossen (in diesem Beispiel ein Daten Schreibvorgang).
-   Ein E/A-Fehler tritt auf. (Die Pipe wird z. b. vom anderen Ende geschlossen.)
-   Fehler im eigentlichen Rückruf (z. b. mindestens ein Parameter ist ungültig).
-   Ein anderer Thread im Prozess ruft die Funktion [**CancelSynchronousIo**](cancelsynchronousio-func.md) mithilfe des Thread Handles des blockierten Threads auf, der die e/a-Vorgänge für diesen Thread beendet und den e/a-Vorgang nicht ausführt.
-   Der blockierte Thread wird vom System beendet. der Prozess selbst wird z. b. beendet, oder ein anderer Thread ruft die [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) -Funktion mit dem Handle des blockierten Threads auf. (Dies wird im Allgemeinen als letztes Mittel und nicht als geeignetes Anwendungsdesign angesehen.)

In einigen Fällen kann diese Verzögerung für den Entwurf und Zweck der Anwendung nicht akzeptabel sein. Daher sollten Anwendungsentwickler die Verwendung asynchroner e/a-Vorgänge mit entsprechenden Thread Synchronisierungs Objekten wie z. b. e [/a-Abschlussports](i-o-completion-ports.md)in Erwägung ziehen. Weitere Informationen zur Synchronisierung von Threads finden Sie unter Informationen [zur Synchronisierung](/windows/desktop/Sync/about-synchronization).

Ein Prozess öffnet eine Datei für asynchrone e/a-Vorgänge in seinem Aufrufen von " [**anatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " durch Angabe des überlappenden Flag " **\_ Dateiflag \_** " im Parameter " *dwflagsandattributs* ". Wenn das überlappende **\_ Dateiflag \_** nicht angegeben ist, wird die Datei für die synchrone e/a-Vorgänge geöffnet. Wenn die Datei für asynchrone e/a-Vorgänge geöffnet wurde, wird ein Zeiger auf eine überlappende Struktur an den-Aufrufe von "read [**File**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) " und " [**Write File**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)" [**über**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) mittelt. Wenn synchrone e/a-Vorgänge durchgeführt werden, ist diese Struktur in Aufrufen von "read **File** " und " **Write File**" nicht erforderlich.

> [!Note]  
> Wenn eine Datei oder ein Gerät für asynchrone e/a-Vorgänge geöffnet wird, geben nachfolgende Aufrufe von Funktionen wie z. b. " [**Write File**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) " mit diesem Handle in der Regel sofort zurück, können sich jedoch auch synchron in Bezug auf die blockierte Ausführung Verhalten Weitere Informationen finden Sie unter [https://support.microsoft.com/kb/156932](https://support.microsoft.com/kb/156932).

 

Obwohl " [**anatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " die gängigste Funktion für das Öffnen von Dateien, Datenträgervolumes, anonymen Pipes und anderen ähnlichen Geräten ist, können e/a-Vorgänge auch mithilfe eines Handle- *Typumwandlung* aus anderen System Objekten, wie z. b. einem durch die [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) -oder [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) -Funktionen erstellten Socket, ausgeführt werden.

Handles zu Verzeichnis Objekten werden durch Aufrufen der [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) -Funktion mit dem **\_ Dateiflag \_ Sicherungs \_ Semantik** Attribut abgerufen. Verzeichnis Handles werden fast nie verwendet – bei Sicherungs Anwendungen handelt es sich um eine der wenigen Anwendungen, die Sie normalerweise verwenden.

Nachdem das Datei Objekt für asynchrone e/a-Vorgänge geöffnet wurde, muss eine [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur ordnungsgemäß erstellt, initialisiert und an jeden Aufrufe von Funktionen wie " [**Infofile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) " und " [**Write File**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)" übermittelt werden. Beachten Sie Folgendes, wenn Sie die [**über**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) Lapp Ende Struktur in asynchronen Lese-und Schreibvorgängen verwenden:

-   Sie dürfen die [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur oder den Datenpuffer erst dann erneut zuweisen oder ändern, wenn alle asynchronen e/a-Vorgänge für das Datei Objekt abgeschlossen wurden.
-   Wenn Sie den Zeiger auf die [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur als lokale Variable deklarieren, beenden Sie die lokale Funktion erst, wenn alle asynchronen e/a-Vorgänge für das Datei Objekt abgeschlossen wurden. Wenn die lokale Funktion vorzeitig beendet wird, wechselt die **über** Lapp Ende Struktur in den Gültigkeitsbereich, und es ist nicht mehr auf die Funktionen von "read [**File**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) " und " [**Write File**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) ", die außerhalb dieser Funktion gefunden werden, zugänglich.

Sie können auch ein Ereignis erstellen und das Handle in die [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur einfügen. die [Wait-Funktionen](/windows/desktop/Sync/wait-functions) können dann verwendet werden, um auf den Abschluss des e/a-Vorgangs zu warten, indem auf das Ereignis handle gewartet wird.

Wie bereits erwähnt, sollten Anwendungen beim Arbeiten mit einem asynchronen handle sorgfältig vorgehen, wenn Sie bestimmen möchten, wann Ressourcen freigegeben werden sollen, die einem angegebenen e/a-Vorgang für dieses Handle zugeordnet sind. Wenn die Zuordnung des Handles vorzeitig aufgehoben wird, meldet "read [**File**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) " oder " [**Write File**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) " fälschlicherweise, dass der e/a-Vorgang beendet ist. Außerdem gibt die Funktion " **Write File** " manchmal " **true** " zurück, wenn der Wert " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) " den Wert " **Fehler \_ erfolgreich**" hat, obwohl Sie ein asynchrones Handle verwendet (das ebenfalls " **false** " zurückgeben kann, wenn die **Fehler \_ \_**-e/a Programmierer, die mit dem synchronen e/a-Entwurf vertraut sind, geben in der Regel Datenpuffer Ressourcen frei, da **true** und **Fehler \_ Erfolg** darauf hinweisen, dass der Vorgang abgeschlossen ist. Wenn jedoch e [/a-Abschlussports](i-o-completion-ports.md) mit diesem asynchronen Handle verwendet werden, wird auch dann ein abschlusspaket gesendet, wenn der e/a-Vorgang sofort abgeschlossen ist. Anders ausgedrückt: Wenn die Anwendung Ressourcen freigibt, nachdem " **Write File** " den Wert " **true** " zurückgegeben hat, zusätzlich zu der e/a-Abschluss Port Routine, tritt ein Fehler auf, der einen doppelten freien Fehler enthält. **\_** In diesem Beispiel empfiehlt es sich, die Vervollständigungs Port Routine ausschließlich für alle Freigabe Vorgänge für solche Ressourcen zu übernehmen.

Das System behält den Dateizeiger für asynchrone Handles nicht für Dateien und Geräte bei, die Dateizeiger unterstützen (d. h. Geräte suchen). Daher muss die Dateiposition an die Lese-und Schreibfunktionen in den zugehörigen Offset Datenmembern der [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp enden Struktur weitergegeben werden. Weitere Informationen finden Sie unter " [**Write File**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) " und " [**Infofile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)".

Die Dateizeiger Position eines synchronen Handles wird vom System beibehalten, wenn Daten gelesen oder geschrieben werden, und kann auch mit der Funktion " [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) " oder " [**setfilepointerex**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointerex) " aktualisiert werden.

Eine Anwendung kann auch auf das Datei Handle warten, um den Abschluss eines e/a-Vorgangs zu synchronisieren. Dies erfordert jedoch eine extrem Vorsicht. Jedes Mal, wenn ein e/a-Vorgang gestartet wird, legt das Betriebssystem das Datei Handle auf den nicht signalisierten Zustand fest. Jedes Mal, wenn ein e/a-Vorgang abgeschlossen ist, legt das Betriebssystem das Datei Handle auf den signalisierten Zustand fest. Wenn eine Anwendung also zwei e/a-Vorgänge startet und auf das Datei Handle wartet, gibt es keine Möglichkeit, den Vorgang zu bestimmen, der abgeschlossen wird, wenn das Handle auf den signalisierten Zustand festgelegt ist. Wenn eine Anwendung mehrere asynchrone e/a-Vorgänge für eine einzelne Datei ausführen muss, sollte Sie auf das Ereignis Handle in der spezifischen [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp enden Struktur für jeden e/a-Vorgang und nicht auf das Common File Handle warten.

Um alle ausstehenden asynchronen e/a-Vorgänge abzubrechen, verwenden Sie Folgendes:

-   [**CancelIo**](cancelio.md)– diese Funktion bricht nur Vorgänge ab, die vom aufrufenden Thread für das angegebene Datei Handle ausgegeben werden.
-   [**CancelIoEx**](cancelioex-func.md)– diese Funktion bricht alle Vorgänge ab, die von den Threads für das angegebene Datei Handle ausgegeben werden.

Verwenden Sie [**CancelSynchronousIo**](cancelsynchronousio-func.md) , um ausstehende synchrone e/a-Vorgänge abzubrechen.

Mit den Funktionen "read [**fileex**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) " und " [**Write fileex**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) " kann eine Anwendung eine auszuführende Routine angeben (siehe [**fileiocompletionroutine**](/windows/win32/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine)), wenn die asynchrone e/a-Anforderung abgeschlossen ist.

 

 
