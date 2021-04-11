---
description: Das Workingset eines Programms ist eine Sammlung von Seiten im virtuellen Adressraum, auf die vor kurzem verwiesen wurde.
ms.assetid: 6017ef59-d2e9-4245-a406-8965024dbb35
title: Arbeits Satz verarbeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 900b5d8a19c756a9087a9b2c006259857691dc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216011"
---
# <a name="process-working-set"></a><span data-ttu-id="390c7-103">Arbeits Satz verarbeiten</span><span class="sxs-lookup"><span data-stu-id="390c7-103">Process Working Set</span></span>

<span data-ttu-id="390c7-104">Das *Workingset* eines Programms ist eine Sammlung von Seiten im virtuellen Adressraum, auf die vor kurzem verwiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="390c7-104">The *working set* of a program is a collection of those pages in its virtual address space that have been recently referenced.</span></span> <span data-ttu-id="390c7-105">Sie enthält sowohl freigegebene als auch private Daten.</span><span class="sxs-lookup"><span data-stu-id="390c7-105">It includes both shared and private data.</span></span> <span data-ttu-id="390c7-106">Die freigegebenen Daten enthalten Seiten, die alle von der Anwendung ausgeführten Anweisungen enthalten, einschließlich der in ihren DLLs und der System-DLLs.</span><span class="sxs-lookup"><span data-stu-id="390c7-106">The shared data includes pages that contain all instructions your application executes, including those in your DLLs and the system DLLs.</span></span> <span data-ttu-id="390c7-107">Wenn die Workingsetgröße zunimmt, steigt der Arbeitsspeicher Bedarf.</span><span class="sxs-lookup"><span data-stu-id="390c7-107">As the working set size increases, memory demand increases.</span></span>

<span data-ttu-id="390c7-108">Einem Prozess sind minimale Workingsetgröße und maximale Workingsetgröße zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="390c7-108">A process has an associated minimum working set size and maximum working set size.</span></span> <span data-ttu-id="390c7-109">Jedes Mal, wenn Sie " [**forateprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)" aufrufen, wird die minimale Workingsetgröße für den Prozess reserviert.</span><span class="sxs-lookup"><span data-stu-id="390c7-109">Each time you call [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), it reserves the minimum working set size for the process.</span></span> <span data-ttu-id="390c7-110">Der virtuelle Speicher-Manager versucht, genügend Arbeitsspeicher für den minimalen Workingset beizubehalten, wenn der Prozess aktiv ist, behält jedoch die maximale Größe bei.</span><span class="sxs-lookup"><span data-stu-id="390c7-110">The virtual memory manager attempts to keep enough memory for the minimum working set resident when the process is active, but keeps no more than the maximum size.</span></span>

<span data-ttu-id="390c7-111">Um die angeforderten minimalen und maximalen Größen der Workingsets für die Anwendung zu erhalten, müssen Sie die [**GetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-getprocessworkingsetsize) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="390c7-111">To get the requested minimum and maximum sizes of the working set for your application, call the [**GetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-getprocessworkingsetsize) function.</span></span>

<span data-ttu-id="390c7-112">Das System legt die standardmäßigen workingsetgrößen fest.</span><span class="sxs-lookup"><span data-stu-id="390c7-112">The system sets the default working set sizes.</span></span> <span data-ttu-id="390c7-113">Sie können die workingsetgrößen auch mithilfe der [**SetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-setprocessworkingsetsize) -Funktion ändern.</span><span class="sxs-lookup"><span data-stu-id="390c7-113">You can also modify the working set sizes using the [**SetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-setprocessworkingsetsize) function.</span></span> <span data-ttu-id="390c7-114">Das Festlegen dieser Werte ist keine Garantie dafür, dass der Arbeitsspeicher reserviert oder Residenten ist.</span><span class="sxs-lookup"><span data-stu-id="390c7-114">Setting these values is not a guarantee that the memory will be reserved or resident.</span></span> <span data-ttu-id="390c7-115">Achten Sie darauf, eine zu große minimale oder maximale Workingsetgröße anzufordern, da dadurch die Systemleistung beeinträchtigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="390c7-115">Be careful about requesting too large a minimum or maximum working set size, because doing so can degrade system performance.</span></span>

<span data-ttu-id="390c7-116">Verwenden Sie die [**getprocessmemoryinfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) -Funktion, um die aktuelle oder maximale Größe des Workingsets für den Prozess zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="390c7-116">To obtain the current or peak size of the working set for your process, use the [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="390c7-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="390c7-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="390c7-118">[Informationen zur Speicherleistung](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="390c7-118">[Memory Performance Information](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="390c7-119">Arbeitssatz</span><span class="sxs-lookup"><span data-stu-id="390c7-119">Working Set</span></span>](../memory/working-set.md)
</dt> </dl>

 

 
