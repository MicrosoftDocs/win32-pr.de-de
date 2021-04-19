---
description: 'Computer mit mehreren Prozessoren sind in der Regel für eine von zwei Architekturen konzipiert: Non-Uniform Memory Access (NUMA) oder symmetrischen Multiprocessing (SMP).'
ms.assetid: 3c9186c8-a54d-4536-8237-bfff78cc7d11
title: Mehrere Prozessoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0093404a0df653a153823915f1ac72b5e41d50c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348006"
---
# <a name="multiple-processors"></a>Mehrere Prozessoren

Computer mit mehreren Prozessoren sind in der Regel für eine von zwei Architekturen konzipiert: Non-Uniform Memory Access (NUMA) oder symmetrischen Multiprocessing (SMP).

Bei einem NUMA-Computer ist jeder Prozessor näher an einigen Teilen des Speichers als andere, sodass der Speicherzugriff für einige Teile des Speichers schneller ist als bei anderen Teilen. Im NUMA-Modell versucht das System, Threads auf Prozessoren zu planen, die sich in der Nähe des verwendeten Speichers befinden. Weitere Informationen zu NUMA finden Sie [unter NUMA-Unterstützung](numa-support.md).

Auf einem SMP-Computer stellen zwei oder mehr identische Prozessoren oder Kerne eine Verbindung mit einem einzelnen gemeinsam genutzten Hauptspeicher her. Unter dem SMP-Modell kann jeder beliebige Thread jedem Prozessor zugewiesen werden. Daher ähnelt das Planen von Threads auf einem SMP-Computer dem Planen von Threads auf einem Computer mit einem einzelnen Prozessor. Allerdings verfügt der Planer über einen Pool von Prozessoren, sodass er die gleichzeitige Ausführung von Threads planen kann. Die Planung wird weiterhin durch die Thread Priorität bestimmt. Sie kann jedoch durch Festlegen der Thread Affinität und des idealen Thread-Prozessors beeinflusst werden, wie in diesem Thema erläutert.

## <a name="thread-affinity"></a>Thread Affinität

*Thread Affinität* erzwingt, dass ein Thread für eine bestimmte Teilmenge von Prozessoren ausgeführt wird. Das Festlegen der Thread Affinität sollte in der Regel vermieden werden, da Sie die Möglichkeit des Zeit Planungs Moduls beeinträchtigen kann, Threads über Prozessoren hinweg effektiv zu planen. Dies kann die Leistungssteigerungen verringern, die bei der parallelen Verarbeitung erzielt werden. Eine angemessene Verwendung der Thread Affinität ist das Testen der einzelnen Prozessoren.

Das System stellt eine Affinität mit einer Bitmaske dar, die als Prozessor Affinitäts Maske bezeichnet wird. Die Affinitäts Maske ist die Größe der maximalen Anzahl von Prozessoren im System, wobei Bits zum Identifizieren einer Teilmenge der Prozessoren festgelegt ist. Anfänglich bestimmt das System die Teilmenge der Prozessoren in der Maske.

Sie können die aktuelle Thread Affinität für alle Threads des Prozesses abrufen, indem Sie die [**getprocessaffinitymask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) -Funktion aufrufen. Verwenden Sie die Funktion [**setprocessaffinitymask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) , um die Thread Affinität für alle Threads des Prozesses anzugeben. Verwenden Sie die Funktion [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) , um die Thread Affinität für einen einzelnen Thread festzulegen. Die Thread Affinität muss eine Teilmenge der Prozess Affinität sein.

Auf Systemen mit mehr als 64 Prozessoren stellt die Affinitäts Maske anfänglich Prozessoren in einer einzelnen Prozessor Gruppe dar. Thread Affinität kann jedoch auf einen Prozessor in einer anderen Gruppe festgelegt werden, wodurch die Affinitäts Maske für den Prozess geändert wird. Weitere Informationen finden Sie unter [Prozessor Gruppen](processor-groups.md).

## <a name="thread-ideal-processor"></a>Thread idealer Prozessor

Wenn Sie einen *Thread idealen Prozessor* angeben, führt der Scheduler den Thread nach Möglichkeit auf dem angegebenen Prozessor aus. Verwenden Sie die [**setthreadidealprocessor**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessor) -Funktion, um einen bevorzugten Prozessor für einen Thread anzugeben. Dies garantiert nicht, dass der ideale Prozessor ausgewählt wird, stellt jedoch einen nützlichen Hinweis für den Scheduler bereit. Auf Systemen mit mehr als 64 Prozessoren können Sie die Funktion " [**setthreadidealprocessorex**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex) " verwenden, um einen bevorzugten Prozessor in einer bestimmten Prozessor Gruppe anzugeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[NUMA-Unterstützung](numa-support.md)
</dt> <dt>

[Prozessorgruppen](processor-groups.md)
</dt> </dl>

 

 
