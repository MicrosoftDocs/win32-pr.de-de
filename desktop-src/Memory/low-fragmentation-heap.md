---
description: Die Heap Fragmentierung ist ein Status, in dem der verfügbare Arbeitsspeicher in kleine, nicht zusammenhängende Blöcke unterteilt ist.
ms.assetid: d10abf82-423c-4942-b05e-55de3a5c4219
title: Heap mit niedriger Fragmentierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad14a97fa6d95b663f63b21f0982332ba0de01e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349398"
---
# <a name="low-fragmentation-heap"></a>Heap mit niedriger Fragmentierung

\[Die Informationen in diesem Thema gelten für Windows Server 2003 und Windows XP. Ab Windows Vista verwendet das System den Low-Fragmentierung-Heap (LFH), der für die Speicher Belegungs Anforderungen benötigt wird. Anwendungen müssen die LFH nicht für Ihre Heaps aktivieren.\]

Die Heap Fragmentierung ist ein Status, in dem der verfügbare Arbeitsspeicher in kleine, nicht zusammenhängende Blöcke unterteilt ist. Wenn ein Heap fragmentiert ist, kann die Speicher Belegung auch dann fehlschlagen, wenn der gesamte verfügbare Arbeitsspeicher im Heap ausreichend ist, um eine Anforderung zu erfüllen, da kein einzelner Speicherblock groß genug ist. Der Heap mit niedriger Fragmentierung (LFH) trägt dazu bei, die Heap Fragmentierung zu verringern.

Der LFH ist kein separater Heap. Stattdessen handelt es sich um eine Richtlinie, die Anwendungen für Ihre Heaps aktivieren können. Wenn die LFH aktiviert ist, ordnet das Systemspeicher in bestimmten vordefinierten Größen zu. Wenn eine Anwendung eine Speicher Belegung von einem Heap anfordert, für den LFH aktiviert ist, ordnet das System den kleinsten Speicherblock zu, der groß genug ist, um die angeforderte Größe zu enthalten. Das System verwendet nicht die LFH für Zuordnungen, die größer als 16 KB sind, unabhängig davon, ob die LFH aktiviert ist.

Eine Anwendung sollte die LFH nur für den Standard Heap des aufrufenden Prozesses oder für [private Heaps](heap-functions.md) aktivieren, die von der Anwendung erstellt wurden. Um die LFH für einen Heap zu aktivieren, verwenden Sie die [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) -Funktion, um ein Handle für den Standard Heap des aufrufenden Prozesses zu erhalten, oder verwenden Sie das Handle für einen privaten Heap, der von der [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) -Funktion erstellt wurde. Dann wenden Sie die [**HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation) -Funktion mit dem Handle an.

Der LFH kann nicht für Heaps aktiviert werden, die mit **Heap \_ No \_ serialize** erstellt wurden, oder für Heaps, die mit einer festgelegten Größe erstellt wurden. Der LFH kann auch nicht aktiviert werden, wenn Sie die Heap-Debuggingtools in [Debuggingtools für Windows](/windows-hardware/drivers/debugger/) oder [Microsoft Application Verifier](https://www.microsoft.com/downloads/details.aspx?FamilyID=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18&displaylang=en)verwenden.

Nachdem die LFH für einen Heap aktiviert wurde, kann Sie nicht deaktiviert werden.

Anwendungen, die am meisten von der LFH profitieren, sind Multithreadanwendungen, die Arbeitsspeicher häufig belegen und eine Vielzahl von Zuordnungs Größen unter 16 KB verwenden. Nicht alle Anwendungen profitieren jedoch von der LFH. Um die Auswirkungen der Aktivierung von LFH in Ihrer Anwendung zu bewerten, verwenden Sie Leistungsprofil Erstellungs Daten.

 

 
