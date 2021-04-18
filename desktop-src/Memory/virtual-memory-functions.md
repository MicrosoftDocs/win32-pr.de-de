---
description: Mit den Funktionen des virtuellen Arbeitsspeichers kann ein Prozess den Status von Seiten im virtuellen Adressraum bearbeiten oder ermitteln.
ms.assetid: 9488a854-1ef0-488f-b3d1-57c1acb82a88
title: Funktionen des virtuellen Arbeitsspeichers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c76866fd10dac01315622e8a4faef7bea436a61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347231"
---
# <a name="virtual-memory-functions"></a><span data-ttu-id="dcd22-103">Funktionen des virtuellen Arbeitsspeichers</span><span class="sxs-lookup"><span data-stu-id="dcd22-103">Virtual Memory Functions</span></span>

<span data-ttu-id="dcd22-104">Mit den Funktionen des virtuellen Arbeitsspeichers kann ein Prozess den Status von Seiten im virtuellen Adressraum bearbeiten oder ermitteln.</span><span class="sxs-lookup"><span data-stu-id="dcd22-104">The virtual memory functions enable a process to manipulate or determine the status of pages in its virtual address space.</span></span> <span data-ttu-id="dcd22-105">Sie können die folgenden Vorgänge ausführen:</span><span class="sxs-lookup"><span data-stu-id="dcd22-105">They can perform the following operations:</span></span>

-   <span data-ttu-id="dcd22-106">Reservieren Sie einen Bereich des virtuellen Adressraums eines Prozesses.</span><span class="sxs-lookup"><span data-stu-id="dcd22-106">Reserve a range of a process's virtual address space.</span></span> <span data-ttu-id="dcd22-107">Durch das Reservieren des Adressraums wird kein physischer Speicher zugeordnet, aber es wird verhindert, dass andere Zuordnungs Vorgänge den angegebenen Bereich verwenden.</span><span class="sxs-lookup"><span data-stu-id="dcd22-107">Reserving address space does not allocate any physical storage, but it prevents other allocation operations from using the specified range.</span></span> <span data-ttu-id="dcd22-108">Dies hat keine Auswirkung auf die virtuellen Adressräume anderer Prozesse.</span><span class="sxs-lookup"><span data-stu-id="dcd22-108">It does not affect the virtual address spaces of other processes.</span></span> <span data-ttu-id="dcd22-109">Das Reservieren von Seiten verhindert den unnötigen Verbrauch von physischem Speicher, während ein Prozess einen Bereich des Adressraums reservieren kann, in den eine dynamische Datenstruktur vergrößert werden kann.</span><span class="sxs-lookup"><span data-stu-id="dcd22-109">Reserving pages prevents needless consumption of physical storage, while enabling a process to reserve a range of its address space into which a dynamic data structure can grow.</span></span> <span data-ttu-id="dcd22-110">Der Prozess kann bei Bedarf physischen Speicher für diesen Speicherplatz zuweisen.</span><span class="sxs-lookup"><span data-stu-id="dcd22-110">The process can allocate physical storage for this space, as needed.</span></span>
-   <span data-ttu-id="dcd22-111">Commit für einen Bereich von reservierten Seiten im virtuellen Adressraum eines Prozesses, sodass physischer Speicher (entweder im RAM oder auf dem Datenträger) nur für den Zuweisungs Prozess zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="dcd22-111">Commit a range of reserved pages in a process's virtual address space so that physical storage (either in RAM or on disk) is accessible only to the allocating process.</span></span>
-   <span data-ttu-id="dcd22-112">Geben Sie Lese-/Schreibzugriff, schreibgeschützt oder keinen Zugriff für einen Bereich von zugegebenen Seiten an.</span><span class="sxs-lookup"><span data-stu-id="dcd22-112">Specify read/write, read-only, or no access for a range of committed pages.</span></span> <span data-ttu-id="dcd22-113">Dies unterscheidet sich von den Standard Zuordnungs Funktionen, die immer Seiten mit Lese-/Schreibzugriff zuordnen.</span><span class="sxs-lookup"><span data-stu-id="dcd22-113">This differs from the standard allocation functions that always allocate pages with read/write access.</span></span>
-   <span data-ttu-id="dcd22-114">Freigeben eines Bereichs von reservierten Seiten, sodass der Bereich der virtuellen Adressen für nachfolgende Zuordnungs Vorgänge durch den aufrufenden Prozess verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="dcd22-114">Free a range of reserved pages, making the range of virtual addresses available for subsequent allocation operations by the calling process.</span></span>
-   <span data-ttu-id="dcd22-115">Debuggen Sie einen Bereich von ausgeführtem Commit, um den physischen Speicher freizugeben und ihn für die nachfolgende Zuordnung durch jeden Prozess verfügbar zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="dcd22-115">Decommit a range of committed pages, releasing their physical storage and making it available for subsequent allocation by any process.</span></span>
-   <span data-ttu-id="dcd22-116">Sperren Sie eine oder mehrere Seiten mit zugesteuertem Speicher in den physischen Speicher (RAM), damit das System die Seiten nicht in die Auslagerungs Datei austauschen kann.</span><span class="sxs-lookup"><span data-stu-id="dcd22-116">Lock one or more pages of committed memory into physical memory (RAM) so that the system cannot swap the pages out to the paging file.</span></span>
-   <span data-ttu-id="dcd22-117">Abrufen von Informationen zu einem Bereich von Seiten im virtuellen Adressraum des aufrufenden Prozesses oder eines angegebenen Prozesses.</span><span class="sxs-lookup"><span data-stu-id="dcd22-117">Obtain information about a range of pages in the virtual address space of the calling process or a specified process.</span></span>
-   <span data-ttu-id="dcd22-118">Ändern des Zugriffs Schutzes für einen angegebenen Bereich von zugegebenen Seiten im virtuellen Adressraum des aufrufenden Prozesses oder eines angegebenen Prozesses.</span><span class="sxs-lookup"><span data-stu-id="dcd22-118">Change the access protection for a specified range of committed pages in the virtual address space of the calling process or a specified process.</span></span>

<span data-ttu-id="dcd22-119">Weitere Informationen finden Sie in den nachfolgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="dcd22-119">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="dcd22-120">Zuordnen des virtuellen Speichers</span><span class="sxs-lookup"><span data-stu-id="dcd22-120">Allocating Virtual Memory</span></span>](allocating-virtual-memory.md)
-   [<span data-ttu-id="dcd22-121">Vergleichen von Speicher Belegungs Methoden</span><span class="sxs-lookup"><span data-stu-id="dcd22-121">Comparing Memory Allocation Methods</span></span>](comparing-memory-allocation-methods.md)
-   [<span data-ttu-id="dcd22-122">Freigeben von virtuellem Speicher</span><span class="sxs-lookup"><span data-stu-id="dcd22-122">Freeing Virtual Memory</span></span>](freeing-virtual-memory.md)
-   [<span data-ttu-id="dcd22-123">Arbeiten mit Seiten</span><span class="sxs-lookup"><span data-stu-id="dcd22-123">Working With Pages</span></span>](working-with-pages.md)
-   [<span data-ttu-id="dcd22-124">Speicherverwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="dcd22-124">Memory Management Functions</span></span>](memory-management-functions.md)

 

 



