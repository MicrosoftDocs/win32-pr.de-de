---
Description: Im Folgenden werden die verschiedenen Speicherbelegungsmethoden kurz verglichen.
ms.assetid: b6101014-02d2-4b19-aec6-8772a2793d38
title: Vergleichen von Speicherbelegungsmethoden
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 418ebbf96b1d6f714e1ae7f23f1c15e918ea0c6fa7eabdf7bb9157bb14808bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067900"
---
# <a name="comparing-memory-allocation-methods"></a>Vergleichen von Speicherbelegungsmethoden

Im Folgenden werden die verschiedenen Speicherbelegungsmethoden kurz verglichen:

-   [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
-   [**Globalalloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)
-   [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc)
-   [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)
-   **malloc**
-   **new**
-   [**Virtualalloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)

Obwohl die Funktionen [**GlobalAlloc,**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)und [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) letztendlich Arbeitsspeicher aus demselben Heap zuordnen, bietet jede eine etwas andere Funktionalität. Beispielsweise kann **HeapAlloc** angewiesen werden, eine Ausnahme auszu auslösen, wenn kein Arbeitsspeicher zugeordnet werden konnte, eine Funktion, die mit **LocalAlloc** nicht verfügbar ist. **LocalAlloc** unterstützt die Zuordnung von Handles, die es ermöglichen, den zugrunde liegenden Speicher durch eine Neuzuordnung zu verschieben, ohne den Handlewert zu ändern. Dies ist eine Funktion, die mit **HeapAlloc** nicht verfügbar ist.

Ab 32-Bit-Windows werden [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) und [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) als Wrapperfunktionen implementiert, die [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) mithilfe eines Handles für den Standardheap des Prozesses aufrufen. Daher haben **GlobalAlloc** und **LocalAlloc** einen höheren Mehraufwand als **HeapAlloc.**

Da die verschiedenen Heapbeweiser unterschiedliche Funktionen mithilfe verschiedener Mechanismen bereitstellen, müssen Sie Arbeitsspeicher mit der richtigen Funktion freigeben. Beispielsweise muss der mit [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) belegte Arbeitsspeicher mit [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) und nicht [**mit LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) oder [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree)freigegeben werden. Der mit [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) oder [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) belegte Arbeitsspeicher muss mit der entsprechenden globalen oder lokalen Funktion abgefragt, überprüft und freigegeben werden.

Mit [**der VirtualAlloc-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) können Sie zusätzliche Optionen für die Speicherbelegung angeben. Die Zuordnungen verwenden jedoch eine Seitengranularität, sodass die Verwendung von **VirtualAlloc** zu einer höheren Speicherauslastung führen kann.

Die **malloc-Funktion** hat den Nachteil, dass sie von der Laufzeit abhängig ist. Der **neue** Operator hat den Nachteil, dass er vom Compiler abhängig und sprachabhängig ist.

Die [**CoTaskMemAlloc-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) hat den Vorteil, dass sie in C, C++ oder Visual Basic gut funktioniert. Es ist auch die einzige Möglichkeit, Arbeitsspeicher in einer COM-basierten Anwendung freizugeben, da MIDL **CoTaskMemAlloc** und [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) zum Marshallen des Arbeitsspeichers verwendet.


## <a name="examples"></a>Beispiele

* [Reservieren und Committen von Arbeitsspeicher](./reserving-and-committing-memory.md)

* [AWE-Beispiel](./awe-example.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Globale und lokale Funktionen](global-and-local-functions.md)
</dt> <dt>

[Heapfunktionen](heap-functions.md)
</dt> <dt>

[Funktionen des virtuellen Arbeitsspeichers](virtual-memory-functions.md)
</dt> </dl>

 

 