---
description: Jeder Prozess verfügt über einen vom System bereitgestellten Standardheap. Anwendungen, die häufig Zuordnungen aus dem Heap vornehmen, können die Leistung mit privaten Heaps verbessern.
ms.assetid: cfb683fa-4f46-48b5-9a28-f4625a9cb8cd
title: Heapfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8171b75abf879eb50204d55541557bdbf5359bd1e8f956d147e49a9d61656d06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067820"
---
# <a name="heap-functions"></a>Heapfunktionen

Jeder Prozess verfügt über einen vom System bereitgestellten Standardheap. Anwendungen, die häufig Zuordnungen aus dem Heap vornehmen, können die Leistung mit privaten Heaps verbessern.

Ein privater Heap ist ein Block einer oder mehrerer Seiten im Adressraum des aufrufenden Prozesses. Nach dem Erstellen des privaten Heaps verwendet der Prozess Funktionen wie [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) und [**HeapFree,**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) um den Arbeitsspeicher in diesem Heap zu verwalten.

Die Heapfunktionen können auch zum Verwalten des Arbeitsspeichers im Standardheap des Prozesses verwendet werden, indem das von der [**GetProcessHeap-Funktion**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) zurückgegebene Handle verwendet wird. Neue Anwendungen sollten zu diesem Zweck die Heapfunktionen anstelle der [globalen und lokalen Funktionen](global-and-local-functions.md) verwenden.

Es gibt keinen Unterschied zwischen dem Arbeitsspeicher, der von einem privaten Heap belegt wird, und dem Arbeitsspeicher, der mithilfe der anderen Speicherbelegungsfunktionen belegt wird. Eine vollständige Liste der Funktionen finden Sie in der Tabelle unter [Speicherverwaltungsfunktionen.](memory-management-functions.md)

> [!Note]  
> Ein Thread sollte Heapfunktionen nur für den Standardheap und die privaten Heaps des Prozesses aufrufen, die vom Thread erstellt und verwaltet werden, wobei von der [**GetProcessHeap-**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) oder [**HeapCreate-Funktion**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) zurückgegebene Handles verwendet werden.

 

Die [**HeapCreate-Funktion**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) erstellt ein privates Heapobjekt, aus dem der aufrufende Prozess Speicherblöcke mithilfe der [**HeapAlloc-Funktion**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) zuordnen kann. **HeapCreate** gibt sowohl eine Anfangsgröße als auch eine maximale Größe für den Heap an. Die Anfangsgröße bestimmt die Anzahl der seiten mit Commit, Lese-/Schreibzugriff, die dem Heap anfänglich zugeordnet wurden. Die maximale Größe bestimmt die Gesamtzahl der reservierten Seiten. Diese Seiten erstellen einen zusammenhängenden Block im virtuellen Adressraum eines Prozesses, in den der Heap vergrößert werden kann. Zusätzliche Seiten werden automatisch aus diesem reservierten Speicherplatz übernommen, wenn Anforderungen von **HeapAlloc** die aktuelle Größe der zu übernehmenden Seiten überschreiten, vorausgesetzt, dass der physische Speicher dafür verfügbar ist. Sobald für die Seiten ein Commit ausgeführt wurde, wird der Commit erst aufgehoben, wenn der Prozess beendet wird oder der Heap durch Aufrufen der [**HeapDestroy-Funktion**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) zerstört wird.

Der Arbeitsspeicher eines privaten Heapobjekts ist nur für den Prozess zugänglich, der es erstellt hat. Wenn eine Dynamic Link Library (DLL) einen privaten Heap erstellt, erfolgt dies im Adressraum des Prozesses, der die DLL aufgerufen hat. Der Zugriff ist nur für diesen Prozess möglich.

Die [**HeapAlloc-Funktion**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) ordnet eine angegebene Anzahl von Bytes aus einem privaten Heap zu und gibt einen Zeiger auf den zugeordneten Block zurück. Dieser Zeiger kann in den Funktionen [**HeapFree,**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) [**HeapReAlloc,**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc) [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize)und [**HeapValidate**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) verwendet werden.

Der von [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) belegte Arbeitsspeicher kann nicht verschoben werden. Die von **HeapAlloc** zurückgegebene Adresse ist gültig, bis der Speicherblock freigegeben oder neu zugeordnet wird. Der Speicherblock muss nicht gesperrt werden.

Da das System einen privaten Heap nicht komprimieren kann, kann er fragmentiert werden. Anwendungen, die große Mengen an Arbeitsspeicher in verschiedenen Zuordnungsgrößen zuordnen, können den Heap mit [geringer Fragmentierung](low-fragmentation-heap.md) verwenden, um die Heapfragmentierung zu reduzieren.

Eine mögliche Verwendung für die Heapfunktionen besteht darin, einen privaten Heap zu erstellen, wenn ein Prozess gestartet wird. Dabei wird eine anfangs ausreichende Größe angegeben, um die Arbeitsspeicheranforderungen des Prozesses zu erfüllen. Wenn der Aufruf der [**HeapCreate-Funktion**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) fehlschlägt, kann der Prozess beendet werden oder den Benutzer über den Arbeitsspeichermangel benachrichtigen. Wenn dies erfolgreich ist, ist der Prozess jedoch sicher, dass er über den benötigten Arbeitsspeicher verfügt.

Der von [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) angeforderte Arbeitsspeicher kann zusammenhängend sein. Der von [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) innerhalb eines Heaps belegte Arbeitsspeicher ist zusammenhängend. Sie sollten nicht in den Arbeitsspeicher eines Heaps schreiben oder aus ihm lesen, mit Ausnahme der von **HeapAlloc** zugeordneten . Sie sollten auch keine Beziehung zwischen zwei Bereichen des Arbeitsspeichers annehmen, die von **HeapAlloc** zugeordnet werden.

Sie sollten in keiner Weise auf Arbeitsspeicher verweisen, der von [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree)freigegeben wurde. Nachdem der Arbeitsspeicher freigegeben wurde, sind alle Informationen, die sich möglicherweise darin befinden, für immer verloren gegangen. Wenn Sie Informationen benötigen, geben Sie keinen Arbeitsspeicher frei, der die Informationen enthält. Funktionsaufrufe, die Informationen zum Arbeitsspeicher (z. [**B. HeapSize)**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize)zurückgeben, dürfen nicht mit freigegebenen Arbeitsspeicher verwendet werden, da sie möglicherweise falsche Daten zurückgeben.

Die [**HeapDestroy-Funktion**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) zerstört ein privates Heapobjekt. Er dekommitiert und gibt alle Seiten des Heapobjekts frei und macht das Handle für den Heap ungültig.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vergleichen von Speicherbelegungsmethoden](comparing-memory-allocation-methods.md)
</dt> </dl>

 

 



