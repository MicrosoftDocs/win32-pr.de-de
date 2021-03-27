---
title: Informationen zur Prozess Speicherauslastung
description: Die getprocessmemoryinfo-Funktion nimmt ein Prozess handle als Eingabe an und füllt \_ die \_ Struktur der Prozess speicherzähler mit Informationen über die Speicher Statistik für den Prozess auf.
ms.assetid: 683c899e-a7e8-4440-8f13-2a713c1618bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133032b8cfb8a9af4ccea5661c9e0e0181ab4d93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856607"
---
# <a name="process-memory-usage-information"></a><span data-ttu-id="8bbc0-103">Informationen zur Prozess Speicherauslastung</span><span class="sxs-lookup"><span data-stu-id="8bbc0-103">Process Memory Usage Information</span></span>

<span data-ttu-id="8bbc0-104">Die [**getprocessmemoryinfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) -Funktion nimmt ein Prozess handle als Eingabe an und füllt die Struktur der [**Prozess \_ Speicher \_ Zähler**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters) mit Informationen über die Speicher Statistik für den Prozess auf.</span><span class="sxs-lookup"><span data-stu-id="8bbc0-104">The [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) function takes a process handle as input and fills a [**PROCESS\_MEMORY\_COUNTERS**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters) structure with information about the memory statistics for the process.</span></span> <span data-ttu-id="8bbc0-105">Der **CB** -Member erhält die Größe der Struktur.</span><span class="sxs-lookup"><span data-stu-id="8bbc0-105">The **cb** member receives the size of the structure.</span></span> <span data-ttu-id="8bbc0-106">Das **pagefehlercount** -Element empfängt die Anzahl der Seiten Fehler.</span><span class="sxs-lookup"><span data-stu-id="8bbc0-106">The **PageFaultCount** member receives the number of page faults.</span></span> <span data-ttu-id="8bbc0-107">Die verbleibenden Elemente erhalten die aktuelle und maximale Speicherauslastung in den folgenden Kategorien:</span><span class="sxs-lookup"><span data-stu-id="8bbc0-107">The remaining members receive the current and peak memory usage in the following categories:</span></span>

-   <span data-ttu-id="8bbc0-108">Arbeitssatz</span><span class="sxs-lookup"><span data-stu-id="8bbc0-108">working set</span></span>
-   <span data-ttu-id="8bbc0-109">Auslagerungs Pool</span><span class="sxs-lookup"><span data-stu-id="8bbc0-109">paged pool</span></span>
-   <span data-ttu-id="8bbc0-110">nicht Auslagerungs Pool</span><span class="sxs-lookup"><span data-stu-id="8bbc0-110">nonpaged pool</span></span>
-   <span data-ttu-id="8bbc0-111">Auslagerungs Datei</span><span class="sxs-lookup"><span data-stu-id="8bbc0-111">pagefile</span></span>

<span data-ttu-id="8bbc0-112">Das *Workingset* ist die Menge an Arbeitsspeicher, die dem Prozess Kontext zu einem bestimmten Zeitpunkt physisch zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8bbc0-112">The *working set* is the amount of memory physically mapped to the process context at a given time.</span></span> <span data-ttu-id="8bbc0-113">Der Arbeitsspeicher im Auslagerungs *Pool* ist der System Arbeitsspeicher, der in die Auslagerungs Datei auf dem Datenträger übertragen werden kann, wenn er nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8bbc0-113">Memory in the *paged pool* is system memory that can be transferred to the paging file on disk (paged) when it is not being used.</span></span> <span data-ttu-id="8bbc0-114">Der Arbeitsspeicher im nicht Auslagerungs *Pool* ist der System Arbeitsspeicher, der nicht auf den Datenträger ausgelagert werden kann, solange die entsprechenden Objekte zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="8bbc0-114">Memory in the *nonpaged pool* is system memory that cannot be paged to disk as long as the corresponding objects are allocated.</span></span> <span data-ttu-id="8bbc0-115">Die Verwendung der Auslagerungs *Datei* stellt dar, wie viel Arbeitsspeicher für den Prozess in der Auslagerungs Datei des Systems reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="8bbc0-115">The *pagefile* usage represents how much memory is set aside for the process in the system paging file.</span></span> <span data-ttu-id="8bbc0-116">Wenn die Speicherauslastung zu hoch ist, wird der ausgewählte Arbeitsspeicher vom virtuellen Speicher-Manager auf den Datenträger über die</span><span class="sxs-lookup"><span data-stu-id="8bbc0-116">When memory usage is too high, the virtual memory manager pages selected memory to disk.</span></span> <span data-ttu-id="8bbc0-117">Wenn ein Thread eine Seite benötigt, die sich nicht im Arbeitsspeicher befindet, lädt der Speicher-Manager ihn erneut aus der Auslagerungs Datei.</span><span class="sxs-lookup"><span data-stu-id="8bbc0-117">When a thread needs a page that is not in memory, the memory manager reloads it from the paging file.</span></span>

 

 




