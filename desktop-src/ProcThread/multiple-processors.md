---
description: 'Computer mit mehreren Prozessoren sind in der Regel für eine von zwei Architekturen konzipiert: numa (Non-Uniform Memory Access) oder Symmetric Multiprocessing (SMP).'
ms.assetid: 3c9186c8-a54d-4536-8237-bfff78cc7d11
title: Mehrere Prozessoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d28b381faaceb5a171ddcf33c0705fee144f98952c4d473c0db8c7d99050deb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032410"
---
# <a name="multiple-processors"></a>Mehrere Prozessoren

Computer mit mehreren Prozessoren sind in der Regel für eine von zwei Architekturen konzipiert: numa (Non-Uniform Memory Access) oder Symmetric Multiprocessing (SMP).

Auf einem NUMA-Computer ist jeder Prozessor näher an einigen Teilen des Arbeitsspeichers als andere, sodass der Speicherzugriff für einige Teile des Arbeitsspeichers schneller ist als für andere Teile. Unter dem NUMA-Modell versucht das System, Threads auf Prozessoren zu planen, die sich in der Nähe des verwendeten Arbeitsspeichers befinden. Weitere Informationen zu NUMA finden Sie unter [NUMA-Unterstützung.](numa-support.md)

Auf einem SMP-Computer stellen zwei oder mehr identische Prozessoren oder Kerne eine Verbindung mit einem einzelnen gemeinsam genutzten Hauptspeicher her. Unter dem SMP-Modell kann jeder Thread jedem Prozessor zugewiesen werden. Daher ähnelt das Planen von Threads auf einem SMP-Computer dem Planen von Threads auf einem Computer mit einem einzelnen Prozessor. Der Scheduler verfügt jedoch über einen Pool von Prozessoren, sodass threads gleichzeitig ausgeführt werden können. Die Zeitplanung wird weiterhin durch die Threadpriorität bestimmt, kann aber durch Festlegen der Threadaffinität und des idealen Threadprozessors beeinflusst werden, wie in diesem Thema erläutert.

## <a name="thread-affinity"></a>Threadaffinität

*Threadaffinität* erzwingt die Ausführung eines Threads auf einer bestimmten Teilmenge von Prozessoren. Das Festlegen der Threadaffinität sollte im Allgemeinen vermieden werden, da sie die Fähigkeit des Planers beeinträchtigen kann, Threads prozessorübergreifend effektiv zu planen. Dies kann die Leistungssteigerungen verringern, die durch die parallele Verarbeitung erzielt werden. Eine geeignete Verwendung der Threadaffinität besteht darin, jeden Prozessor zu testen.

Das System stellt die Affinität mit einer Bitmaske dar, die als Prozessoraffinitätsmaske bezeichnet wird. Die Affinitätsmaske ist die Größe der maximalen Anzahl von Prozessoren im System, wobei Bits festgelegt sind, um eine Teilmenge von Prozessoren zu identifizieren. Zunächst bestimmt das System die Teilmenge der Prozessoren in der Maske.

Sie können die aktuelle Threadaffinität für alle Threads des Prozesses abrufen, indem Sie die [**GetProcessAffinityMask-Funktion**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) aufrufen. Verwenden Sie die [**SetProcessAffinityMask-Funktion,**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) um threadaffinität für alle Threads des Prozesses anzugeben. Verwenden Sie die [**Funktion SetThreadAffinityMask,**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) um die Threadaffinität für einen einzelnen Thread festzulegen. Die Threadaffinität muss eine Teilmenge der Prozessaffinität sein.

Auf Systemen mit mehr als 64 Prozessoren stellt die Affinitätsmaske zunächst Prozessoren in einer einzelnen Prozessorgruppe dar. Die Threadaffinität kann jedoch auf einen Prozessor in einer anderen Gruppe festgelegt werden, wodurch die Affinitätsmaske für den Prozess verändert wird. Weitere Informationen finden Sie unter [Prozessorgruppen.](processor-groups.md)

## <a name="thread-ideal-processor"></a>Idealer Threadprozessor

Wenn Sie einen *idealen Threadprozessor* angeben, führt der Scheduler den Thread nach Möglichkeit auf dem angegebenen Prozessor aus. Verwenden Sie die [**SetThreadIdealProcessor-Funktion,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessor) um einen bevorzugten Prozessor für einen Thread anzugeben. Dies garantiert nicht, dass der ideale Prozessor ausgewählt wird, stellt aber einen nützlichen Hinweis für den Planer bereit. Auf Systemen mit mehr als 64 Prozessoren können Sie die [**SetThreadIdealProcessorEx-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex) verwenden, um einen bevorzugten Prozessor in einer bestimmten Prozessorgruppe anzugeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[NUMA-Unterstützung](numa-support.md)
</dt> <dt>

[Prozessorgruppen](processor-groups.md)
</dt> </dl>

 

 
