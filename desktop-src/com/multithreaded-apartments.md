---
title: Multithread-Apartment
description: Multithread-Apartment
ms.assetid: d3e6acd9-cd5c-4a2c-8526-4f43db3b606b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69271b4fb6447d48c15fa9005d39020075af09bcc327b12ce539a739c33f8d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047918"
---
# <a name="multithreaded-apartments"></a>Multithread-Apartment

In einem Multithread-Apartmentmodell befinden sich alle Threads im Prozess, die als Freethreading initialisiert wurden, in einem einzelnen Apartment. Daher ist es nicht erforderlich, zwischen Threads zu marshallen. Die Threads müssen keine Nachrichten abrufen und senden, da COM keine Fenstermeldungen in diesem Modell verwendet.

Aufrufe von Methoden von Objekten im Multithread-Apartment können in jedem Thread im Apartment ausgeführt werden. Es erfolgt keine Serialisierung von Aufrufen. viele Aufrufe können gleichzeitig an dieselbe Methode oder an dasselbe Objekt erfolgen. Objekte, die im Multithread-Apartment erstellt werden, müssen jederzeit Aufrufe ihrer Methoden aus anderen Threads verarbeiten können.

Da Aufrufe von -Objekten in keiner Weise serialisiert werden, bietet die Multithread-Objektparallelität die höchste Leistung und nutzt den besten Vorteil der Multiprozessorhardware für thread-, prozessübergreifende und computerübergreifende Aufrufe. Dies bedeutet jedoch, dass der Code für Objekte die Synchronisierung in ihren Schnittstellenimplementierungen bereitstellen muss, in der Regel durch die Verwendung von Synchronisierungsprimitiven wie Ereignisobjekten, kritischen Abschnitten, Mutexen oder Semaphoren, die weiter unten in diesem Abschnitt beschrieben werden. Außerdem kann kein threadspezifischer Zustand im -Objekt (im lokalen Threadspeicher) gespeichert werden, da das -Objekt die Lebensdauer der Threads, die darauf zugreifen, nicht steuert.

Im Folgenden sind einige wichtige Überlegungen zur Synchronisierung für Multithread-Apartments zu beachten:

-   COM ermöglicht die Aufrufsynchronisierung nur für Singlethread-Apartments.
-   Multithread-Apartments empfangen keine Aufrufe bei Aufrufen (im gleichen Thread).
-   Multithread-Apartments können keine eingabesynchronisierten Aufrufe durchführen.
-   Asynchrone Aufrufe werden in synchrone Aufrufe in Multithread-Apartments konvertiert.
-   Der Nachrichtenfilter wird für keinen Thread in einem Multithread-Apartment aufgerufen.

Um einen Thread als Freethreading zu initialisieren, rufen [**Sie CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)auf, und geben Sie COINIT \_ MULTITHREADED an. Informationen zum In-Process-Serverthreading finden Sie unter [In-Process Server Threading Issues](in-process-server-threading-issues.md).

Mehrere Clients können gleichzeitig aus verschiedenen Threads ein Objekt aufrufen, das Freethreading unterstützt. In Out-of-Process-Servern mit Freethreading erstellt COM über das RPC-Subsystem einen Threadpool im Serverprozess, und ein Clientaufruf (oder mehrere Clientaufrufe) kann von jedem dieser Threads jederzeit übermittelt werden. Ein Out-of-Process-Server muss auch die Synchronisierung in seiner Klassenfactory implementieren. In-Process-Objekte mit Freethreading können direkte Aufrufe von mehreren Threads des Clients empfangen.

Der Client kann COM-Arbeiten in mehreren Threads durchführen. Alle Threads gehören zum gleichen Multithread-Apartment. Schnittstellenzeiger werden in einem Multithread-Apartment direkt von Thread zu Thread übergeben, sodass Schnittstellenzeiger nicht zwischen ihren Threads gemarshallt werden. Nachrichtenfilter (Implementierungen von [**IMessageFilter)**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter)werden in Multithread-Apartments nicht verwendet. Der Clientthread hält an, wenn er einen COM-Aufruf von Out-of-Apartment-Objekten durchführt, und wird fortgesetzt, wenn der Aufruf zurückgegeben wird. Aufrufe zwischen Prozessen werden weiterhin von RPC verarbeitet.

Threads, die mit dem Freethreadmodell initialisiert wurden, müssen ihre eigene Synchronisierung implementieren. Wie bereits in diesem Abschnitt erwähnt, aktiviert Windows diese Implementierung über die folgenden Synchronisierungsprimitiven:

-   Ereignisobjekte bieten eine Möglichkeit, einen oder mehrere Threads zu signalisieren, dass ein Ereignis aufgetreten ist. Jeder Thread innerhalb eines Prozesses kann ein Ereignisobjekt erstellen. Ein Handle für das Ereignis wird von der Ereigniserstellungsfunktion [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)zurückgegeben. Nachdem ein Ereignisobjekt erstellt wurde, können Threads mit einem Handle für das Objekt darauf warten, bevor die Ausführung fortgesetzt wird.
-   Kritische Abschnitte werden für einen Codeabschnitt verwendet, der exklusiven Zugriff auf einige freigegebene Daten erfordert, bevor sie ausgeführt werden können und die nur von den Threads innerhalb eines einzelnen Prozesses verwendet werden. Ein kritischer Abschnitt ähnelt einem Drehungsstil, durch den jeweils nur ein Thread durchlaufen werden kann und wie folgt funktioniert:
    -   Um sicherzustellen, dass nicht mehr als ein Thread gleichzeitig auf freigegebene Daten zugreift, ordnet der primäre Thread eines Prozesses eine globale CRITICAL \_ SECTION-Datenstruktur zu und initialisiert seine Member. Ein Thread, der einen kritischen Abschnitt eingibt, ruft die [**EnterCriticalSection-Funktion**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) auf und ändert die Member der Datenstruktur.
    -   Ein Thread, der versucht, einen kritischen Abschnitt einzugeben, ruft [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) auf, der überprüft, ob die \_ CRITICAL SECTION-Datenstruktur geändert wurde. Wenn ja, befindet sich derzeit ein anderer Thread im kritischen Abschnitt, und der nachfolgende Thread wird in den Ruhezustand versetzt. Ein Thread, der einen kritischen Abschnitt verlässt, ruft [**LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection)auf, wodurch die Datenstruktur zurückgesetzt wird. Wenn ein Thread einen kritischen Abschnitt verlässt, aktiviert das System einen der im Ruhezustand ausgeführten Threads, der dann in den kritischen Abschnitt eintritt.
-   Mutexes führt dieselbe Funktion wie ein kritischer Abschnitt aus, mit der Ausnahme, dass Threads, die in verschiedenen Prozessen ausgeführt werden, auf den Mutex zugreifen können. Das Besitzen eines Mutexobjekts ist so, als hätten Sie den Boden in einer Diskussion. Ein Prozess erstellt ein Mutex-Objekt, indem die [**CreateMutex-Funktion**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa) aufgerufen wird, die ein Handle zurückgibt. Der erste Thread, der ein Mutexobjekt anfordert, erhält den Besitz des Objekts. Wenn der Thread mit dem Mutex fertig ist, wird der Besitz an andere Threads übergeben, die zuerst kommen und zuerst bedient werden.
-   Semaphoren werden verwendet, um einen Verweiszähler für einige verfügbare Ressourcen beizubehalten. Ein Thread erstellt ein Semaphor für eine Ressource, indem er die [**CreateSemaphore-Funktion aufruft**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea) und einen Zeiger auf die Ressource, eine anfängliche Ressourcenanzahl und die maximale Ressourcenanzahl übergibt. Diese Funktion gibt ein Handle zurück. Ein Thread, der eine Ressource anfordert, übergibt sein Semaphorhandle in einem Aufruf der [**WaitForSingleObject-Funktion.**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) Das Semaphorobjekt fragt die Ressource ab, um zu bestimmen, ob sie verfügbar ist. Wenn ja, dekrementiert das Semaphor die Ressourcenanzahl und aktiviert den wartenden Thread. Wenn die Anzahl 0 (null) ist, bleibt der Thread im Stillstand, bis ein anderer Thread eine Ressource freigibt, wodurch das Semaphor die Anzahl auf eins erhöht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf Schnittstellen zwischen Apartments](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Auswählen des Threadingmodells](choosing-the-threading-model.md)
</dt> <dt>

[Threadingprobleme beim In-Process-Server](in-process-server-threading-issues.md)
</dt> <dt>

[Prozesse, Threads und Apartment](processes--threads--and-apartments.md)
</dt> <dt>

[Singlethread- und Multithreadkommunikation](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Singlethread-Apartment](single-threaded-apartments.md)
</dt> </dl>

 

 