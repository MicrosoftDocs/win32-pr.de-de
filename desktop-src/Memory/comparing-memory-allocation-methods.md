---
Description: Im folgenden finden Sie einen kurzen Vergleich der verschiedenen Speicher Belegungs Methoden.
ms.assetid: b6101014-02d2-4b19-aec6-8772a2793d38
title: Vergleichen von Speicher Belegungs Methoden
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 541b314c4ff0553ff8812e591c47c87962866bbe
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "103961535"
---
# <a name="comparing-memory-allocation-methods"></a>Vergleichen von Speicher Belegungs Methoden

Im folgenden finden Sie einen kurzen Vergleich der verschiedenen Speicher Belegungs Methoden:

-   [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
-   [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)
-   [**Heapzuweisung**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc)
-   [**Localzuweisung**](/windows/desktop/api/WinBase/nf-winbase-localalloc)
-   **malloc**
-   **new**
-   [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)

Obwohl die Funktionen [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)und [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) letztendlich Arbeitsspeicher aus demselben Heap zuweisen, bietet jede Funktion einen etwas anderen Funktions Satz. **Heapbelegc** kann z. b. angewiesen werden, eine Ausnahme zuzuweisen, wenn der Arbeitsspeicher nicht reserviert werden konnte, eine Funktion, die nicht mit **localbelegc** verfügbar ist. **LocalAlloc** unterstützt die Zuordnung von Handles, die es ermöglichen, dass der zugrunde liegende Speicher durch eine erneute Zuordnung verschoben wird, ohne den Handle-Wert zu ändern. eine Funktion, die mit **HeapAlloc** nicht verfügbar ist

Beginnend mit 32-Bit-Fenstern werden [**Globalzuweisung**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) und [**localzuweisung**](/windows/desktop/api/WinBase/nf-winbase-localalloc) als Wrapper Funktionen implementiert, die [**Heapzuweisung**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) mithilfe eines Handles für den Standard Heap des Prozesses aufzurufen. Daher haben **Globalzuweisung** und **localzuweisung** mehr Aufwand als **Heapzuweisung**.

Da die verschiedenen Heap Zuordnungen mithilfe verschiedener Mechanismen eine besondere Funktionalität bereitstellen, müssen Sie Arbeitsspeicher mit der richtigen Funktion freigeben. Beispielsweise muss der mit [**heapbelegc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) zugeordnete Arbeitsspeicher mit [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) , nicht [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) oder [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree)freigegeben werden. Der mit [**globalzuordnungs**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) -oder [**localzugewiesenc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) zugeordnete Arbeitsspeicher muss abgefragt, überprüft und mit der entsprechenden globalen oder lokalen Funktion freigegeben werden.

Mit der [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) -Funktion können Sie zusätzliche Optionen für die Speicher Belegung angeben. Die Zuordnungen verwenden jedoch eine Seiten Granularität, sodass die Verwendung von **VirtualAlloc** zu einer höheren Speicherauslastung führen kann.

Die **malloc** -Funktion hat den Nachteil, dass Sie von der Laufzeit abhängig ist. Der **New** -Operator hat den Nachteil, dass der Compiler abhängig ist und sprachabhängig ist.

Die Funktion " [**cotaskmemzuweisung**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) " hat den Vorteil, dass Sie in C, C++ oder Visual Basic gut funktioniert. Es ist auch die einzige Möglichkeit, Arbeitsspeicher in einer COM-basierten Anwendung freizugeben, da in der Mitte **cotaskmembelegc** und [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) verwendet werden, um Speicher zu Mars Hallen.


## <a name="examples"></a>Beispiele

* [Reservieren und Commit des Arbeitsspeichers](./reserving-and-committing-memory.md)

* [AWE-Beispiel](./awe-example.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Globale und lokale Funktionen](global-and-local-functions.md)
</dt> <dt>

[Heap Funktionen](heap-functions.md)
</dt> <dt>

[Funktionen des virtuellen Arbeitsspeichers](virtual-memory-functions.md)
</dt> </dl>

 

 