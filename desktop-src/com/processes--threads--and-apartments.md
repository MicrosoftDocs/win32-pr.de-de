---
title: Prozesse, Threads und Apartments
description: Bei einem Prozess handelt es sich um eine Sammlung von virtuellem Speicherbereich, Code, Daten und Systemressourcen.
ms.assetid: cb62412a-d079-40f9-89dc-cce0bf3889af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d598fc9d7dd39ab070b58aa7ba45a6e2fcae90db
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391050"
---
# <a name="processes-threads-and-apartments"></a>Prozesse, Threads und Apartments

Bei einem *Prozess* handelt es sich um eine Sammlung von virtuellem Speicherbereich, Code, Daten und Systemressourcen. Ein *Thread* ist ein Code, der in einem Prozess seriell ausgeführt werden soll. Ein Prozessor führt Threads und keine Prozesse aus, sodass jede Anwendung mindestens einen Prozess aufweist und ein Prozess immer mindestens einen Ausführungs Thread aufweist, der als primärer Thread bezeichnet wird. Ein Prozess kann neben dem primären Thread mehrere Threads aufweisen.

Prozesse kommunizieren über Nachrichten miteinander und verwenden die RPC-Technologie (Remote Procedure Aufruf) von Microsoft, um Informationen an einander zu übergeben. Es gibt keinen Unterschied zwischen einem Aufruf von einem Prozess auf einem Remote Computer und einem Aufruf von einem anderen Prozess auf demselben Computer.

Wenn ein Thread gestartet wird, wird er so lange fortgesetzt, bis er abgebrochen wird, oder bis er von einem Thread mit höherer Priorität (durch eine Benutzeraktion oder den Thread Planer des Kernels) unterbrochen wird. Jeder Thread kann separate Code Abschnitte ausführen, oder mehrere Threads können denselben Code Abschnitt ausführen. Threads, die denselben Codeblock ausführen, behalten separate Stapel. Jeder Thread in einem Prozess teilt die globalen Variablen und Ressourcen dieses Prozesses.

Der Thread Planer legt fest, wann und wie oft ein Thread ausgeführt werden soll. Dies entspricht einer Kombination des Prioritäts Klassen Attributs des Prozesses und der Basis Priorität des Threads. Sie legen das Prioritäts Klassen Attribut eines Prozesses fest, indem Sie die [**setpriorityclass**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) -Funktion aufrufen, und Sie legen die Basis Priorität eines Threads mit einem Aufruf von [**SetThreadPriority**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadpriority)fest.

Multithreadanwendungen müssen zwei Threading Probleme vermeiden: *Deadlocks* und *Races*. Ein Deadlock tritt auf, wenn jeder Thread darauf wartet, etwas auszuführen. Das com-Aufruf Steuerelement hilft dabei, Deadlocks in Aufrufen zwischen Objekten zu verhindern. Eine Racebedingung tritt auf, wenn ein Thread vor einem anderen beendet wird, von dem er abhängt, sodass der erste einen nicht initialisierten Wert verwendet, da letztere noch keinen gültigen Wert bereitgestellt hat. COM bietet einige Funktionen, die speziell entwickelt wurden, um Racebedingungen in Prozess externen Servern zu vermeiden. (Siehe [Implementierungs Hilfen für Out-of-Process-Server](out-of-process-server-implementation-helpers.md).)

## <a name="the-apartment-and-the-com-threading-architecture"></a>Das Apartment und die COM-Threading Architektur

COM unterstützt das Modell mit einem Thread pro Prozess, das vor der Einführung mehrerer Ausführungs Threads weit verbreitet ist, aber Sie können Code schreiben, um mehrere Threads zu nutzen, was zu effizienteren Anwendungen führt, indem ein Thread ausgeführt werden kann, während ein anderer Thread auf den Abschluss eines zeitaufwändigen Vorgangs wartet.

> [!Note]  
> Die Verwendung mehrerer Threads ist keine Garantie für eine bessere Leistung. Tatsächlich verursacht die Verwendung mehrerer Threads häufig Leistungsprobleme, da die Thread Factoring ein schwieriges Problem ist. Der Schlüssel besteht darin, mehrere Threads nur zu verwenden, wenn Sie sich sehr sicher sind, was Sie tun.

 

Im Allgemeinen besteht die einfachste Möglichkeit zum Anzeigen der com-Threading Architektur darin, alle COM-Objekte im Prozess als unterteilt in Gruppen, die als " *Apartments*" bezeichnet werden, zu betrachten. Ein COM-Objekt befindet sich in genau einem Apartment, in dem Sinne, dass seine Methoden rechtmäßig direkt von einem Thread aufgerufen werden können, der zu diesem Apartment gehört. Jeder andere Thread, der das-Objekt aufrufen möchte, muss über einen Proxy verfügen.

Es gibt zwei Arten von Apartments: [Single Thread-Apartments](single-threaded-apartments.md)und [Multithread-Apartments](multithreaded-apartments.md).

-   Single Thread-Apartments bestehen aus genau einem Thread, sodass alle COM-Objekte, die in einem Single Thread-Apartment Leben, nur Methodenaufrufe von einem Thread empfangen können, der zu diesem Apartment gehört. Alle Methodenaufrufe an ein COM-Objekt in einem Single Thread-Apartment werden mit der Windows-Nachrichten Warteschlange für den Thread des Single Thread-Apartment synchronisiert. Ein Prozess mit einem einzigen Ausführungs Thread ist einfach ein Sonderfall dieses Modells.
-   Multithreadwohnungen bestehen aus mindestens einem Thread, sodass alle COM-Objekte, die sich in einem Multithreadapartment befinden, Methodenaufrufe direkt von jedem Thread empfangen können, der zum Multithreadapartment gehört. Für Threads in einem Multithreadapartment wird ein Modell namens " *Free-Threading*" verwendet. Aufrufe von COM-Objekten in einem Multithread-Apartment werden von den Objekten selbst synchronisiert.

> [!Note]  
> Eine Beschreibung der Kommunikation zwischen Single Thread-Apartments und Multithread-Apartments innerhalb desselben Prozesses finden Sie unter [Single Thread-und Multithread-Kommunikation](single-threaded-and-multithreaded-communication.md).

 

Ein Prozess kann über NULL oder mehr Single Thread-Apartments und NULL oder ein Multithread-Apartment verfügen.

In einem Prozess ist das Haupt Apartment das erste, das initialisiert werden soll. In einem Single Thread-Prozess ist dies das einzige Apartment. Die Rückruf Parameter werden zwischen den Apartments gemarshallt, und com behandelt die Synchronisierung über Messaging. Wenn Sie mehrere Threads in einem Prozess als frei Thread festgelegt haben, befinden sich alle freien Threads in einem einzelnen Apartment, und die Parameter werden direkt an jeden Thread im Apartment übermittelt, und Sie müssen die gesamte Synchronisierung verarbeiten. In einem Prozess, der sowohl das kostenlose Threading als auch das Apartment Threading hat, befinden sich alle freien Threads in einem einzigen Apartment, und alle anderen Apartments sind Single Thread-Apartments. Ein Prozess, bei dem com funktioniert, ist eine Sammlung von Apartments, bei denen höchstens ein Multithread-Apartment, aber eine beliebige Anzahl von Single Thread-Apartments vorhanden ist.

Die Threading Modelle in com bieten den Mechanismus für Clients und Server, die verschiedene Threading Architekturen für die Zusammenarbeit verwenden. Aufrufe zwischen Objekten mit unterschiedlichen Threading Modellen in verschiedenen Prozessen werden natürlich unterstützt. Aus der Perspektive des aufrufenden Objekts Verhalten sich alle Aufrufe von Objekten außerhalb eines Prozesses identisch, unabhängig davon, wie das Objekt, das aufgerufen wird, Thread Weise ist. Ebenso verhalten sich eintreffende Aufrufe aus der Perspektive des aufgerufenen Objekts identisch, unabhängig vom Threading Modell des Aufrufers.

Die Interaktion zwischen einem Client und einem Out-of-Process-Objekt ist einfach, auch wenn es verschiedene Threading Modelle verwendet, da sich der Client und das Objekt in verschiedenen Prozessen befinden. COM, das zwischen dem Client und dem Server interagiert, kann den Code für die Zusammenarbeit der Threading Modelle bereitstellen, indem Standard-Marshalling und RPC verwendet werden. Wenn z. b. ein Single Thread-Objekt gleichzeitig von mehreren frei Thread Clients aufgerufen wird, werden die Aufrufe durch com synchronisiert, indem entsprechende Fenster Meldungen in der Nachrichten Warteschlange des Servers platziert werden. Das Apartment des Objekts erhält jedes Mal einen Aufruf, wenn Nachrichten abgerufen und gesendet werden. Es muss jedoch ein gewisses Vorsicht geboten werden, um sicherzustellen, dass Prozess interne Server ordnungsgemäß mit ihren Clients interagieren. (Siehe [Threading Probleme in Process Server](in-process-server-threading-issues.md).)

Das wichtigste Problem bei der Programmierung mit einem multithreadmodell besteht darin, den Code Thread sicher zu machen, sodass Nachrichten, die für einen bestimmten Thread vorgesehen sind, nur an diesen Thread gesendet werden und der Zugriff auf Threads geschützt ist.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Auswählen des Threading Modells](choosing-the-threading-model.md)
-   [Single Thread-Apartments](single-threaded-apartments.md)
-   [Multithread-Apartments](multithreaded-apartments.md)
-   [Single Thread-und Multithread-Kommunikation](single-threaded-and-multithreaded-communication.md)
-   [Threading Probleme im Prozess internen Server](in-process-server-threading-issues.md)
-   [Zugreifen auf Schnittstellen über mehrere Apartments](accessing-interfaces-across-apartments.md)

 

 