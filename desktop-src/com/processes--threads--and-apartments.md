---
title: Prozesse, Threads und Apartment
description: Ein Prozess ist eine Sammlung von virtuellem Arbeitsspeicher, Code, Daten und Systemressourcen.
ms.assetid: cb62412a-d079-40f9-89dc-cce0bf3889af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320b09d76200739c77c7202af4d53a35089b2eca2e6fd282dd507f048aa7a10b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130032"
---
# <a name="processes-threads-and-apartments"></a>Prozesse, Threads und Apartment

Ein *Prozess* ist eine Sammlung von virtuellem Arbeitsspeicher, Code, Daten und Systemressourcen. Ein *Thread* ist Code, der in einem Prozess seriell ausgeführt werden soll. Ein Prozessor führt Threads und keine Prozesse aus, sodass jede Anwendung über mindestens einen Prozess verfügt und ein Prozess immer über mindestens einen Ausführungsthread verfügt, der als primärer Thread bezeichnet wird. Ein Prozess kann zusätzlich zum primären Thread mehrere Threads haben.

Prozesse kommunizieren über Nachrichten miteinander, indem sie die RPC-Technologie (Remote Procedure Call) von Microsoft verwenden, um Informationen aneinander zu übergeben. Es gibt keinen Unterschied zwischen einem Aufruf, der von einem Prozess auf einem Remotecomputer kommt, und einem Aufruf, der von einem anderen Prozess auf demselben Computer kommt.

Wenn die Ausführung eines Threads beginnt, wird er fortgesetzt, bis er abgebrochen oder durch einen Thread mit höherer Priorität unterbrochen wird (durch eine Benutzeraktion oder den Threadplaner des Kernels). Jeder Thread kann separate Codeabschnitte ausführen, oder mehrere Threads können denselben Codeabschnitt ausführen. Threads, die denselben Codeblock ausführen, verwalten separate Stapel. Jeder Thread in einem Prozess teilt sich die globalen Variablen und Ressourcen dieses Prozesses.

Der Threadplaner bestimmt anhand einer Kombination aus dem Prioritätsklassenattribut des Prozesses und der Basispriorität des Threads, wann und wie oft ein Thread ausgeführt werden soll. Sie legen das Prioritätsklassenattribut eines Prozesses fest, indem Sie die [**SetPriorityClass-Funktion**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) aufrufen, und Sie legen die Basispriorität eines Threads mit einem Aufruf von [**SetThreadPriority fest.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadpriority)

Multithreadanwendungen müssen zwei Threadingprobleme vermeiden: *Deadlocks* und *.* Ein Deadlock tritt auf, wenn jeder Thread darauf wartet, dass der andere etwas macht. Die COM-Aufrufsteuerung hilft, Deadlocks in Aufrufen zwischen Objekten zu verhindern. Eine Racebedingung tritt auf, wenn ein Thread vor einem anderen abgeschlossen wird, von dem er abhängt, was dazu führt, dass ersterer einen nicht initialisierten Wert verwendet, da letzterer noch keinen gültigen bereitgestellt hat. COM bietet einige Funktionen, die speziell entwickelt wurden, um Racebedingungen auf Out-of-Process-Servern zu vermeiden. (Weitere Informationen [finden Sie unter Out-of-Process Server Implementation Helpers](out-of-process-server-implementation-helpers.md).)

## <a name="the-apartment-and-the-com-threading-architecture"></a>Das Apartment und die COM-Threadingarchitektur

Com unterstützt zwar das Singlethread-pro-Prozess-Modell, das vor der Einführung mehrerer Ausführungsthreads weit verbreitet war, aber Sie können Code schreiben, um mehrere Threads zu nutzen, was zu effizienteren Anwendungen führt, indem ein Thread ausgeführt werden kann, während ein anderer Thread auf den Abschluss eines zeitaufwändigen Vorgangs wartet.

> [!Note]  
> Die Verwendung mehrerer Threads ist keine Garantie für eine bessere Leistung. Da thread factoring ein schwieriges Problem ist, führt die Verwendung mehrerer Threads häufig zu Leistungsproblemen. Der Schlüssel ist, nur dann mehrere Threads zu verwenden, wenn Sie sicher sind, was Sie tun.

 

Im Allgemeinen besteht die einfachste Möglichkeit zum Anzeigen der COM-Threadingarchitektur in der Ansicht aller COM-Objekte im Prozess in Gruppen, die als *"Apartment" bezeichnet werden.* Ein COM-Objekt befindet sich in genau einem Apartment, in dem Sinne, dass seine Methoden nur direkt von einem Thread aufgerufen werden können, der zu diesem Apartment gehört. Jeder andere Thread, der das Objekt aufrufen möchte, muss einen Proxy verwenden.

Es gibt zwei Arten von Apartment: [Singlethread-Apartment und](single-threaded-apartments.md) [Multithread-Apartment.](multithreaded-apartments.md)

-   Singlethread-Apartment besteht aus genau einem Thread, sodass alle COM-Objekte, die in einem Singlethread-Apartment leben, Methodenaufrufe nur von dem einen Thread empfangen können, der zu diesem Apartment gehört. Alle Methodenaufrufe an ein COM-Objekt in einem Singlethread-Apartment werden mit der Windows-Nachrichtenwarteschlange für den Thread des Singlethread-Apartment synchronisiert. Ein Prozess mit einem einzelnen Ausführungsthread ist einfach ein Sonderfall dieses Modells.
-   Multithread-Apartment besteht aus einem oder mehreren Threads, sodass alle COM-Objekte, die in einem Multithread-Apartment leben, Methodenaufrufe direkt von jedem der Threads empfangen können, die zum Multithread-Apartment gehören. Threads in einem Multithread-Apartment verwenden ein Modell namens *Freethreading.* Aufrufe von COM-Objekten in einem Multithread-Apartment werden von den Objekten selbst synchronisiert.

> [!Note]  
> Eine Beschreibung der Kommunikation zwischen Singlethread-Apartment und Multithread-Apartment innerhalb desselben Prozesses finden Sie unter [Singlethread-Kommunikation und Multithreadkommunikation](single-threaded-and-multithreaded-communication.md).

 

Ein Prozess kann null oder mehr Singlethread-Apartment und null oder ein Multithread-Apartment haben.

In einem Prozess ist das Haupta apartment das erste, das initialisiert wird. In einem Singlethreadprozess ist dies das einzige Apartment. Aufrufparameter werden zwischen Apartments gemarshallt, und COM übernimmt die Synchronisierung per Messaging. Wenn Sie mehrere Threads in einem Prozess als Freethread festlegen, befinden sich alle freien Threads in einem einzigen Apartment, Parameter werden direkt an jeden Thread im Apartment übergeben, und Sie müssen die Synchronisierung durchführen. Bei einem Prozess mit Freethreading und Apartmentthreading befinden sich alle freien Threads in einem einzigen Apartment, und alle anderen Apartment-Threads sind Singlethread-Apartments. Ein Prozess, der COM-Arbeit abarbeitet, ist eine Sammlung von Apartments mit mindestens einem Multithread-Apartment, aber einer beliebigen Anzahl von Singlethread-Apartments.

Die Threadingmodelle in COM stellen den Mechanismus für Clients und Server dar, die unterschiedliche Threadingarchitekturen verwenden, um zusammen zu arbeiten. Aufrufe zwischen Objekten mit unterschiedlichen Threadingmodellen in verschiedenen Prozessen werden natürlich unterstützt. Aus Sicht des aufrufenden Objekts verhalten sich alle Aufrufe von Objekten außerhalb eines Prozesses identisch, unabhängig davon, wie das aufgerufene Objekt gethreadt wird. Aus Sicht des aufgerufenen Objekts verhalten sich die eintreffenden Aufrufe unabhängig vom Threadingmodell des Aufrufers identisch.

Die Interaktion zwischen einem Client und einem Out-of-Process-Objekt ist unkompliziert, auch wenn sie unterschiedliche Threadingmodelle verwenden, da sich Client und Objekt in unterschiedlichen Prozessen befinden. COM, das zwischen dem Client und dem Server erstellt wurde, kann den Code für die Interoperabilität der Threadingmodelle bereitstellen, indem Standard-Marshalling und RPC verwendet werden. Wenn beispielsweise ein Singlethreadobjekt gleichzeitig von mehreren Freethreadclients aufgerufen wird, werden die Aufrufe von COM synchronisiert, indem entsprechende Fenstermeldungen in der Nachrichtenwarteschlange des Servers platziert werden. Das Apartment des Objekts erhält bei jedem Abrufen und Senden von Nachrichten einen Aufruf. Es muss jedoch mit Vorsicht sichergestellt werden, dass Prozessserver ordnungsgemäß mit ihren Clients interagieren. (Weitere Informationen [finden Sie unter In-Process Server Threading Issues](in-process-server-threading-issues.md).)

Das wichtigste Problem bei der Programmierung mit einem Multithreadmodell besteht in der Threadsicherheit Ihres Codes, sodass Nachrichten, die für einen bestimmten Thread vorgesehen sind, nur an diesen Thread gesendet werden und der Zugriff auf Threads geschützt ist.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Auswählen des Threadingmodells](choosing-the-threading-model.md)
-   [Singlethread-Apartment](single-threaded-apartments.md)
-   [Multithread-Apartment](multithreaded-apartments.md)
-   [Singlethread- und Multithreadkommunikation](single-threaded-and-multithreaded-communication.md)
-   [In-Process-Serverthreadingprobleme](in-process-server-threading-issues.md)
-   [Zugriff auf Schnittstellen über Mehrere Schnittstellen hinweg](accessing-interfaces-across-apartments.md)

 

 