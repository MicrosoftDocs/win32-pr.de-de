---
title: Multithread-Apartments
description: Multithread-Apartments
ms.assetid: d3e6acd9-cd5c-4a2c-8526-4f43db3b606b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2594f9341fc662b068fb7e007e538282a31273
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106337471"
---
# <a name="multithreaded-apartments"></a>Multithread-Apartments

In einem Multithread-Apartment Modell befinden sich alle Threads im Prozess, die als "freigegeben" initialisiert wurden, in einem einzigen Apartment. Daher ist es nicht erforderlich, zwischen Threads zu Mars Hallen. Die Threads müssen keine Nachrichten abrufen und verteilen, weil com in diesem Modell keine Fenster Meldungen verwendet.

Aufrufe von-Methoden von Objekten im Multithreadapartment können in jedem beliebigen Thread im Apartment ausgeführt werden. Es ist keine Serialisierung von Aufrufen vorhanden. viele Aufrufe können gleichzeitig an dieselbe Methode oder an dasselbe Objekt erfolgen. Objekte, die im Multithreadapartment erstellt werden, müssen jederzeit Aufrufe ihrer Methoden aus anderen Threads verarbeiten können.

Da Aufrufe von Objekten in keiner Weise serialisiert werden, bietet die Parallelität von multithreadobjekten die höchste Leistung und nutzt die Vorteile der Multiprozessorhardware für Thread übergreifende, prozessübergreifende und Computer übergreifende Aufrufe. Dies bedeutet jedoch, dass der Code für-Objekte in den Schnittstellen Implementierungen synchronisiert werden muss, in der Regel durch die Verwendung von Synchronisierungs primitiven, z. b. Ereignis Objekten, kritischen Abschnitten, Mutexen oder Semaphoren, die weiter unten in diesem Abschnitt beschrieben werden. Da das-Objekt die Lebensdauer der Threads, die darauf zugreifen, nicht steuert, kann außerdem kein Thread spezifischer Zustand im-Objekt (im lokalen Thread Speicher) gespeichert werden.

Im folgenden finden Sie einige wichtige Überlegungen bezüglich der Synchronisierung für Multithread-Apartments:

-   COM bietet nur eine Synchronisierung für Single Thread-Apartments.
-   Multithread-Apartments empfangen keine Aufrufe, während Aufrufe (auf demselben Thread) aufgerufen werden.
-   Multithread-Apartments können keine Eingabe synchronisierten Aufrufe durchführen.
-   Asynchrone Aufrufe werden in Multithread-Apartments in synchrone Aufrufe konvertiert.
-   Der Nachrichtenfilter wird nicht für einen Thread in einem Multithread-Apartment aufgerufen.

Um einen Thread als frei Thread zu initialisieren, können Sie [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)aufrufen, indem Sie coinit \_ Multithreaded angeben. Informationen zum Threading in-Process-Server finden Sie unter [Prozess interne Server Threading Probleme](in-process-server-threading-issues.md).

Mehrere Clients können gleichzeitig von unterschiedlichen Threads aus auf ein Objekt, das das kostenlose Threading unterstützt, abrufen. In frei Thread-Prozess externen Servern erstellt com über das RPC-Subsystem einen Thread Pool im Server Prozess, und ein Client Aufruf (oder mehrere Client Aufrufe) kann von jedem dieser Threads jederzeit übermittelt werden. Außerdem muss ein Prozess interner Server die Synchronisierung in seiner Klassenfactory implementieren. Frei Thread interne Objekte können direkte Aufrufe von mehreren Threads des Clients empfangen.

Der Client kann com in mehreren Threads verwenden. Alle Threads gehören zum selben Multithreadapartment. Schnittstellen Zeiger werden direkt von einem Thread an einen Thread in einem Multithread-Apartment übermittelt, sodass Schnittstellen Zeiger nicht zwischen ihren Threads gemarshallt werden. Nachrichtenfilter (Implementierungen von [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter)) werden in Multithread-Apartments nicht verwendet. Der Client Thread wird angehalten, wenn er out-of-Apartment-Objekte aufruft und fortgesetzt wird, wenn der-Rückruf zurückgegeben wird. Aufrufe zwischen Prozessen werden weiterhin von RPC verarbeitet.

Mit dem frei Hand Thread Modell initialisierte Threads müssen eine eigene Synchronisierung implementieren. Wie bereits weiter oben in diesem Abschnitt erwähnt, aktiviert Windows diese Implementierung durch die folgenden Synchronisierungs primitiven:

-   Ereignis Objekte bieten eine Möglichkeit, einen oder mehrere Threads zu signalisieren, dass ein Ereignis aufgetreten ist. Jeder Thread in einem Prozess kann ein Ereignis Objekt erstellen. Ein Handle für das-Ereignis wird von der Ereignis Erstellungsfunktion (" [**kreateevent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)") zurückgegeben. Nachdem ein Ereignis Objekt erstellt wurde, können Threads mit einem Handle für das Objekt darauf warten, bevor die Ausführung fortgesetzt wird.
-   Kritische Abschnitte werden für einen Code Abschnitt verwendet, der exklusiven Zugriff auf einen Satz frei gegebener Daten erfordert, bevor er ausgeführt werden kann und der nur von den Threads innerhalb eines einzelnen Prozesses verwendet wird. Ein kritischer Abschnitt entspricht einem einzigen Thread, über den nur ein Thread zu einem Zeitpunkt ausgeführt werden kann, der wie folgt funktioniert:
    -   Um sicherzustellen, dass nicht mehr als ein Thread gleichzeitig auf freigegebene Daten zugreift, ordnet der primäre Thread eines Prozesses eine globale kritische \_ Abschnitts Datenstruktur zu und initialisiert seine Member. Ein Thread, der einen kritischen Abschnitt eingibt, ruft die Funktion " [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) " auf und ändert die Elemente der Datenstruktur.
    -   Ein Thread, der versucht, einen kritischen Abschnitt einzugeben, Ruft den [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) auf, der überprüft, ob die \_ Datenstruktur des kritischen Abschnitts geändert wurde. Wenn dies der Fall ist, befindet sich derzeit ein anderer Thread im kritischen Abschnitt und der nachfolgende Thread wird in den Standbymodus versetzt. Ein Thread, der einen kritischen Abschnitt verlässt, Ruft den [**LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection)auf, der die Datenstruktur zurücksetzt. Wenn ein Thread einen kritischen Abschnitt verlässt, aktiviert das System einen der inaktiven Threads, der dann in den kritischen Abschnitt gelangt.
-   Mutexes führt die gleiche Funktion wie ein kritischer Abschnitt aus, mit dem Unterschied, dass der Mutex für Threads zugänglich ist, die in verschiedenen Prozessen ausgeführt werden. Das Besitz eines Mutex-Objekts ist wie der Fußboden in einer Debatte. Ein Prozess erstellt ein Mutex-Objekt durch Aufrufen der [**CreateMutex**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa) -Funktion, die ein Handle zurückgibt. Der erste Thread, der ein Mutex-Objekt anfordert, erhält den Besitz. Wenn der Thread mit dem Mutex fertig ist, übergibt der Besitz an andere Threads auf der Grundlage von First-Come, first-served.
-   Semaphoren werden verwendet, um einen Verweis Zähler für eine verfügbare Ressource beizubehalten. Ein Thread erstellt eine Semaphor für eine Ressource, indem er die Funktion [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea) anfordert und einen Zeiger auf die Ressource, eine anfängliche Ressourcen Anzahl und die maximale Ressourcen Anzahl übergibt. Diese Funktion gibt ein Handle zurück. Ein Thread, der eine Ressource anfordert, übergibt seinen Semaphor-Handle in einem Rückruf der [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) -Funktion. Das Semaphor-Objekt fragt die Ressource ab, um zu bestimmen, ob Sie verfügbar ist. Wenn dies der Fall ist, verringert das Semaphor die Ressourcen Anzahl und aktiviert den wartenden Thread. Wenn die Anzahl 0 (null) ist, bleibt der Thread in den Standbymodus, bis ein anderer Thread eine Ressource freigibt, wodurch die Anzahl der Semaphor um 1 erhöht wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf Schnittstellen über mehrere Apartments](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Auswählen des Threading Modells](choosing-the-threading-model.md)
</dt> <dt>

[Threading Probleme im Prozess internen Server](in-process-server-threading-issues.md)
</dt> <dt>

[Prozesse, Threads und Apartments](processes--threads--and-apartments.md)
</dt> <dt>

[Single Thread-und Multithread-Kommunikation](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Single Thread-Apartments](single-threaded-apartments.md)
</dt> </dl>

 

 