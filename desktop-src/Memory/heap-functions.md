---
description: Jeder Prozess verfügt über einen Standard Heap, der vom System bereitgestellt wird. Anwendungen, die häufige Zuordnungen aus dem Heap vornehmen, können die Leistung mithilfe privater Heaps verbessern.
ms.assetid: cfb683fa-4f46-48b5-9a28-f4625a9cb8cd
title: Heap Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e591c1e349ed6806cbebe00a178a99e63bb412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864860"
---
# <a name="heap-functions"></a>Heap Funktionen

Jeder Prozess verfügt über einen Standard Heap, der vom System bereitgestellt wird. Anwendungen, die häufige Zuordnungen aus dem Heap vornehmen, können die Leistung mithilfe privater Heaps verbessern.

Ein privater Heap ist ein Block von einer oder mehreren Seiten im Adressraum des aufrufenden Prozesses. Nachdem der private Heap erstellt wurde, verwendet der Prozessfunktionen wie [**heapbelegc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) und [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) , um den Arbeitsspeicher in diesem Heap zu verwalten.

Die Heap Funktionen können auch verwendet werden, um Arbeitsspeicher im Standard Heap des Prozesses zu verwalten, wobei das von der [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) -Funktion zurückgegebene Handle verwendet wird. Neue Anwendungen sollten zu diesem Zweck die Heap Funktionen anstelle der [globalen und lokalen Funktionen](global-and-local-functions.md) verwenden.

Es gibt keinen Unterschied zwischen einem von einem privaten Heap zugewiesenen Arbeitsspeicher, der mithilfe der anderen Speicher Belegungs Funktionen zugeordnet wurde. Eine umfassende Liste der Funktionen finden Sie in der Tabelle unter [Speicherverwaltungsfunktionen](memory-management-functions.md).

> [!Note]  
> Ein Thread sollte Heap Funktionen nur für den Standard Heap des Prozesses und private Heaps aufrufen, die der Thread erstellt und verwaltet, mithilfe von Handles, die von der [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) -Funktion oder der [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) -Funktion zurückgegeben werden.

 

Die [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) -Funktion erstellt ein privates Heap Objekt, aus dem der aufrufenden Prozess Speicherblöcke mithilfe der [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) -Funktion zuordnen kann. **HeapCreate** gibt sowohl eine Anfangs Größe als auch eine maximale Größe für den Heap an. Die Anfangs Größe bestimmt die Anzahl der zugeordneten, Lese-/Schreibseiten, die anfänglich für den Heap reserviert wurden. Die maximale Größe bestimmt die Gesamtzahl der reservierten Seiten. Auf diesen Seiten wird ein zusammenhängender Block im virtuellen Adressraum eines Prozesses erstellt, in den der Heap vergrößert werden kann. Der reservierte Speicherplatz für weitere Seiten wird automatisch zugesichert, wenn die Anforderungen von **heapbelegc** die aktuelle Größe der Seiten mit ausgeführtem Commit überschreiten, vorausgesetzt, dass der physische Speicher für Sie verfügbar ist. Nachdem für die Seiten ein Commit ausgeführt wurde, wird Sie erst dann decommittet, wenn der Prozess beendet oder der Heap zerstört wurde, indem die [**HeapDestroy**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) -Funktion aufgerufen wird.

Der Speicher eines privaten Heap Objekts ist nur für den Prozess zugänglich, der ihn erstellt hat. Wenn eine Dynamic Link Library (dll) einen privaten Heap erstellt, erfolgt dies im Adressraum des Prozesses, der die dll aufgerufen hat. Dieser Vorgang ist nur für diesen Prozess zugänglich.

Die [**heapzugewiesc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) -Funktion ordnet eine angegebene Anzahl von Bytes aus einem privaten Heap zu und gibt einen Zeiger auf den zugeordneten-Block zurück. Dieser Zeiger kann in den Funktionen [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree), [**heaprezuzuordc**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc), [**HEAPSIZE**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize)und [**heapvalidate**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) verwendet werden.

Der von [**heapbelegc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) zugeordnete Arbeitsspeicher ist nicht verschiebbar. Die von **heapbelegc** zurückgegebene Adresse ist gültig, bis der Speicherblock freigegeben oder neu zugewiesen wurde. der Speicherblock muss nicht gesperrt werden.

Da das System einen privaten Heap nicht komprimieren kann, kann es fragmentiert werden. Anwendungen, die große Mengen an Arbeitsspeicher in verschiedenen Zuordnungs Größen belegen, können den [Heap mit niedriger Fragmentierung](low-fragmentation-heap.md) verwenden, um die Heap Fragmentierung zu verringern.

Eine Möglichkeit, die Heap Funktionen zu verwenden, besteht darin, einen privaten Heap zu erstellen, wenn ein Prozess gestartet wird. dabei wird eine anfängliche Größe angegeben, die ausreicht, um die Arbeitsspeicher Anforderungen des Prozesses zu erfüllen. Wenn bei dem [**aufheapcreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) -Funktion ein Fehler auftritt, kann der Prozess den Benutzer beenden oder den Speichermangel benachrichtigen. Wenn dies der Fall ist, ist der Prozess jedoch sicher, dass er über den benötigten Arbeitsspeicher verfügt.

Der von [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) angeforderte Arbeitsspeicher kann zusammenhängend sein. Der Arbeitsspeicher, der von [**heapbelegc innerhalb eines Heaps**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) zugeordnet wird, ist zusammenhängend. Sie sollten nicht in einen Heap schreiben oder aus dem Arbeitsspeicher lesen, außer der von **heapbelegc** zugeordnete. Sie sollten auch keine Beziehung zwischen zwei Bereichen des Arbeitsspeichers annehmen, die von **heapbelegc** zugeordnet werden.

Sie sollten in keiner Weise auf Arbeitsspeicher verweisen, der von [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree)freigegeben wurde. Nachdem der Arbeitsspeicher freigegeben wurde, sind alle Informationen, die möglicherweise darin enthalten waren, nicht mehr verfügbar. Wenn Sie Informationen benötigen, dürfen Sie keinen Speicher freigeben, der die Informationen enthält. Funktionsaufrufe, die Informationen über den Arbeitsspeicher zurückgeben (z. b. [**HEAPSIZE**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize)), dürfen nicht mit frei gegebenes Speicher verwendet werden, da Sie möglicherweise falsche Daten zurückgeben.

Die [**HeapDestroy**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) -Funktion zerstört ein privates Heap Objekt. Er führt einen Commit für alle Seiten des Heap Objekts aus und gibt Sie frei, wodurch das Handle für den Heap ungültig wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vergleichen von Speicher Belegungs Methoden](comparing-memory-allocation-methods.md)
</dt> </dl>

 

 



