---
title: Apibuffer-Funktionen
description: Die apibuffer-Funktionen der Netzwerkverwaltung werden verwendet, um die von einer Anwendung verwendete Speicher Belegung mit Netzwerk Verwaltungsfunktionen zu verwalten.
ms.assetid: bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b316c6b2ee2d4095c15d5e859dd0069978c7ff91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341535"
---
# <a name="apibuffer-functions"></a><span data-ttu-id="76827-103">Apibuffer-Funktionen</span><span class="sxs-lookup"><span data-stu-id="76827-103">ApiBuffer Functions</span></span>

<span data-ttu-id="76827-104">Die apibuffer-Funktionen der Netzwerkverwaltung werden verwendet, um die von einer Anwendung verwendete Speicher Belegung mit Netzwerk Verwaltungsfunktionen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="76827-104">The network management ApiBuffer functions are used to manage memory allocation used by an application with network management functions.</span></span> <span data-ttu-id="76827-105">Im Allgemeinen sollten Sie jedoch für anderen von einer Anwendung verwendeten Arbeitsspeicher die [Speicherverwaltungsfunktionen](/windows/desktop/Memory/memory-management-functions) anstelle dieser apibuffer-Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="76827-105">However, in general, for other memory used by an application you should use the [memory management functions](/windows/desktop/Memory/memory-management-functions) instead of these ApiBuffer functions.</span></span>

<span data-ttu-id="76827-106">Die apibuffer-Funktionen sind nachfolgend aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="76827-106">The ApiBuffer functions are listed following.</span></span>



| <span data-ttu-id="76827-107">Funktion</span><span class="sxs-lookup"><span data-stu-id="76827-107">Function</span></span>                                                 | <span data-ttu-id="76827-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76827-108">Description</span></span>                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76827-109">**"Ntapibuffer" zuordnen**</span><span class="sxs-lookup"><span data-stu-id="76827-109">**NetApiBufferAllocate**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | <span data-ttu-id="76827-110">Belegt Speicher aus dem Heap.</span><span class="sxs-lookup"><span data-stu-id="76827-110">Allocates memory from the heap.</span></span> <span data-ttu-id="76827-111">Wenn Sie die Kompatibilität mit der Funktion " **nettapibufferfree** " benötigen, können Sie diese Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="76827-111">Call this function when you require compatibility with the **NetApiBufferFree** function.</span></span> |
| [<span data-ttu-id="76827-112">**"Nettapibufferfree"**</span><span class="sxs-lookup"><span data-stu-id="76827-112">**NetApiBufferFree**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | <span data-ttu-id="76827-113">Gibt Arbeitsspeicher frei, der von der Funktion " **nettapibufferbeleg;** " und anderen Netzwerk Verwaltungsfunktionen belegt wird</span><span class="sxs-lookup"><span data-stu-id="76827-113">Frees memory allocated by the **NetApiBufferAllocate** function and other network management functions.</span></span>                   |
| [<span data-ttu-id="76827-114">**"Nettapibufferrezuordnen"**</span><span class="sxs-lookup"><span data-stu-id="76827-114">**NetApiBufferReallocate**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | <span data-ttu-id="76827-115">Ändert die Größe eines Puffers, der durch einen Aufrufen der Funktion " **nettapibufferallo"** zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="76827-115">Changes the size of a buffer allocated by a call to the **NetApiBufferAllocate** function.</span></span>                                |
| [<span data-ttu-id="76827-116">**"Nettapibuffersize"**</span><span class="sxs-lookup"><span data-stu-id="76827-116">**NetApiBufferSize**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | <span data-ttu-id="76827-117">Gibt die Größe eines Puffers in Bytes zurück, der durch einen Aufrufen der Funktion " **nettapibufferallo"** zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="76827-117">Returns the size, in bytes, of a buffer allocated by a call to the **NetApiBufferAllocate** function.</span></span>                     |



 

<span data-ttu-id="76827-118">Für Remote fähige Funktionen, die Informationen an den Aufrufer zurückgeben, ordnet die RPC-Lauf Zeit Bibliothek den Puffer zu, der die Rückgabe Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="76827-118">For remotable functions that return information to the caller, the RPC run-time library allocates the buffer containing the return information.</span></span> <span data-ttu-id="76827-119">Wenn der Aufrufer die Verarbeitung der Informationen abgeschlossen hat, muss er die Funktion " [**nettapibufferfree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) " aufrufen, um den zugeordneten Puffer freizugeben.</span><span class="sxs-lookup"><span data-stu-id="76827-119">When the caller has finished processing the information, it must call the [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) function to free the allocated buffer.</span></span>

 

 