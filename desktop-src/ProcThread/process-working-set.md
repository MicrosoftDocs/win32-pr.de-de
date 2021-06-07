---
description: Der Arbeitssatz eines Programms ist eine Auflistung der Seiten im virtuellen Adressraum, auf die kürzlich verwiesen wurde.
ms.assetid: 6017ef59-d2e9-4245-a406-8965024dbb35
title: Prozessarbeitssatz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaded3d0b5f8c6ad552cc728c68ad0407391c343
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549902"
---
# <a name="process-working-set"></a><span data-ttu-id="02126-103">Prozessarbeitssatz</span><span class="sxs-lookup"><span data-stu-id="02126-103">Process Working Set</span></span>

<span data-ttu-id="02126-104">Der *Arbeitssatz eines* Programms ist eine Auflistung der Seiten im virtuellen Adressraum, auf die kürzlich verwiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="02126-104">The *working set* of a program is a collection of those pages in its virtual address space that have been recently referenced.</span></span> <span data-ttu-id="02126-105">Sie umfasst sowohl freigegebene als auch private Daten.</span><span class="sxs-lookup"><span data-stu-id="02126-105">It includes both shared and private data.</span></span> <span data-ttu-id="02126-106">Die freigegebenen Daten enthalten Seiten, die alle Anweisungen enthalten, die Ihre Anwendung ausgeführt, einschließlich der Anweisungen in Ihren DLLs und den System-DLLs.</span><span class="sxs-lookup"><span data-stu-id="02126-106">The shared data includes pages that contain all instructions your application executes, including those in your DLLs and the system DLLs.</span></span> <span data-ttu-id="02126-107">Wenn die Arbeitssatzgröße zunimmt, steigt der Arbeitsspeicherbedarf.</span><span class="sxs-lookup"><span data-stu-id="02126-107">As the working set size increases, memory demand increases.</span></span>

<span data-ttu-id="02126-108">Einem Prozess sind eine minimale Arbeitssatzgröße und eine maximale Arbeitssatzgröße zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="02126-108">A process has an associated minimum working set size and maximum working set size.</span></span> <span data-ttu-id="02126-109">Jedes Mal, wenn [**Sie CreateProcess aufrufen,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)wird die minimale Arbeitssatzgröße für den Prozess reserviert.</span><span class="sxs-lookup"><span data-stu-id="02126-109">Each time you call [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), it reserves the minimum working set size for the process.</span></span> <span data-ttu-id="02126-110">Der Virtuelle Arbeitsspeicher-Manager versucht, genügend Arbeitsspeicher für den minimalen Arbeitssatz zu behalten, der sich befindet, wenn der Prozess aktiv ist, behält jedoch nicht mehr als die maximale Größe bei.</span><span class="sxs-lookup"><span data-stu-id="02126-110">The virtual memory manager attempts to keep enough memory for the minimum working set resident when the process is active, but keeps no more than the maximum size.</span></span>

<span data-ttu-id="02126-111">Rufen Sie die [**GetProcessWorkingSetSize-Funktion**](/windows/desktop/api/memoryapi/nf-memoryapi-getprocessworkingsetsize) auf, um die angeforderten Mindest- und Höchstgrößen des Arbeitssets für Ihre Anwendung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="02126-111">To get the requested minimum and maximum sizes of the working set for your application, call the [**GetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-getprocessworkingsetsize) function.</span></span>

<span data-ttu-id="02126-112">Das System legt die Standardarbeitssatzgrößen fest.</span><span class="sxs-lookup"><span data-stu-id="02126-112">The system sets the default working set sizes.</span></span> <span data-ttu-id="02126-113">Sie können die Arbeitssatzgrößen auch mithilfe der [**SetProcessWorkingSetSize-Funktion**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize) ändern.</span><span class="sxs-lookup"><span data-stu-id="02126-113">You can also modify the working set sizes using the [**SetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize) function.</span></span> <span data-ttu-id="02126-114">Das Festlegen dieser Werte ist keine Garantie dafür, dass der Arbeitsspeicher reserviert oder resident ist.</span><span class="sxs-lookup"><span data-stu-id="02126-114">Setting these values is not a guarantee that the memory will be reserved or resident.</span></span> <span data-ttu-id="02126-115">Seien Sie vorsichtig, wenn Sie eine zu große minimale oder maximale Arbeitssatzgröße anfordern, da dies die Systemleistung beeinträchtigen kann.</span><span class="sxs-lookup"><span data-stu-id="02126-115">Be careful about requesting too large a minimum or maximum working set size, because doing so can degrade system performance.</span></span>

<span data-ttu-id="02126-116">Verwenden Sie die [**GetProcessMemoryInfo-Funktion,**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) um die aktuelle oder Spitzengröße des Arbeitssets für Ihren Prozess zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="02126-116">To obtain the current or peak size of the working set for your process, use the [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02126-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="02126-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="02126-118">[Arbeitsspeicherleistungsinformationen](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="02126-118">[Memory Performance Information](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="02126-119">Arbeitssatz</span><span class="sxs-lookup"><span data-stu-id="02126-119">Working Set</span></span>](../memory/working-set.md)
</dt> </dl>

 

 
