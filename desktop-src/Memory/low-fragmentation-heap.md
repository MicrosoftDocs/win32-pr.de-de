---
description: Heapfragmentierung ist ein Zustand, in dem verfügbarer Arbeitsspeicher in kleine, nicht zusammenhängende Blöcke zerbrochen wird.
ms.assetid: d10abf82-423c-4942-b05e-55de3a5c4219
title: Heap mit geringer Fragmentierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d4cc6f7f0e2427a20532f5e32cc1460f9b6601d1e6dddf0de603757895005e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067740"
---
# <a name="low-fragmentation-heap"></a>Heap mit geringer Fragmentierung

\[Die Informationen in diesem Thema gelten für Windows Server 2003 und Windows XP. Ab Windows Vista verwendet das System den Heap mit geringer Fragmentierung (Low Fragmentation Heap, LFH) nach Bedarf, um Speicherbelegungsanforderungen zu verarbeiten. Anwendungen müssen LFH nicht für ihre Heaps aktivieren.\]

Heapfragmentierung ist ein Zustand, in dem verfügbarer Arbeitsspeicher in kleine, nicht zusammenhängende Blöcke zerbrochen wird. Wenn ein Heap fragmentiert ist, kann die Speicherzuweisung auch dann fehlschlagen, wenn der gesamte verfügbare Arbeitsspeicher im Heap ausreicht, um eine Anforderung zu erfüllen, da kein einzelner Speicherblock groß genug ist. Der Heap mit geringer Fragmentierung (Low Fragmentation Heap, LFH) trägt zur Reduzierung der Heapfragmentierung bei.

Die LFH ist kein separater Heap. Stattdessen handelt es sich um eine Richtlinie, die Anwendungen für ihre Heaps aktivieren können. Wenn LFH aktiviert ist, weist das System Arbeitsspeicher in bestimmten vordefinierten Größen zu. Wenn eine Anwendung eine Speicherbelegung von einem Heap anfragt, auf dem LFH aktiviert ist, ordnet das System den kleinsten Speicherblock zu, der groß genug ist, um die angeforderte Größe zu enthalten. Das System verwendet LFH nicht für Zuordnungen, die größer als 16 KB sind, unabhängig davon, ob die LFH aktiviert ist oder nicht.

Eine Anwendung sollte LFH nur für den Standardhap des aufrufenden Prozesses oder für [private Heaps](heap-functions.md) aktivieren, die die Anwendung erstellt hat. Um die LFH für einen Heap zu aktivieren, verwenden Sie die [**GetProcessHeap-Funktion,**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) um ein Handle für den Standardheap des aufrufenden Prozesses zu erhalten, oder verwenden Sie das Handle für einen privaten Heap, der von der [**HeapCreate-Funktion erstellt**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) wurde. Rufen Sie dann die [**HeapSetInformation-Funktion**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation) mit dem Handle auf.

Die LFH kann nicht für Heaps aktiviert werden, die mit **HEAP \_ NO \_ SERIALIZE** erstellt wurden, oder für Heaps, die mit einer festen Größe erstellt wurden. Die LFH kann auch nicht aktiviert werden, wenn Sie die Heapdebuggingtools in [Debugtools](/windows-hardware/drivers/debugger/) für Windows [oder Microsoft Application Verifier.](https://www.microsoft.com/downloads/details.aspx?FamilyID=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18&displaylang=en)

Nachdem die LFH für einen Heap aktiviert wurde, kann sie nicht mehr deaktiviert werden.

Anwendungen, die am meisten von LFH profitieren, sind Multithreadanwendungen, die häufig Arbeitsspeicher zuweisen und eine Vielzahl von Zuordnungsgrößen unter 16 KB verwenden. Allerdings profitieren nicht alle Anwendungen von LFH. Verwenden Sie Leistungsprofilerstellungsdaten, um die Auswirkungen der Aktivierung von LFH in Ihrer Anwendung zu bewerten.

 

 
