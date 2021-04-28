---
title: Speicherbelegung in COM
description: Speicherbelegung in COM
ms.assetid: b3c318d2-1273-430e-8aca-5bd5c95c138e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82cb9913da55fab82f699ac05dae3998f7582224
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103888"
---
# <a name="memory-allocation-in-com"></a><span data-ttu-id="c6dd9-103">Speicherbelegung in COM</span><span class="sxs-lookup"><span data-stu-id="c6dd9-103">Memory Allocation in COM</span></span>

<span data-ttu-id="c6dd9-104">Manchmal ordnet eine Methode einen Speicherpuffer auf dem Heap zu und gibt die Adresse des Puffers an den Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="c6dd9-104">Sometimes a method allocates a memory buffer on the heap and returns the address of the buffer to the caller.</span></span> <span data-ttu-id="c6dd9-105">COM definiert ein Paar von Funktionen zum Zuordnen und Freigeben von Arbeitsspeicher auf dem Heap.</span><span class="sxs-lookup"><span data-stu-id="c6dd9-105">COM defines a pair of functions for allocating and freeing memory on the heap.</span></span>

-   <span data-ttu-id="c6dd9-106">Die [**CoTaskMemAlloc-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) weist einen Speicherblock zu.</span><span class="sxs-lookup"><span data-stu-id="c6dd9-106">The [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) function allocates a block of memory.</span></span>
-   <span data-ttu-id="c6dd9-107">Die [**CoTaskMemFree-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) gibt einen Speicherblock frei, der mit [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc)belegt wurde.</span><span class="sxs-lookup"><span data-stu-id="c6dd9-107">The [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) function frees a block of memory that was allocated with [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc).</span></span>

<span data-ttu-id="c6dd9-108">Wir haben ein Beispiel für dieses Muster im Beispiel für das [Dialogfeld Öffnen](example--the-open-dialog-box.md)gesehen:</span><span class="sxs-lookup"><span data-stu-id="c6dd9-108">We saw an example of this pattern in the [Open dialog box example](example--the-open-dialog-box.md):</span></span>


```C++
PWSTR pszFilePath;
hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
if (SUCCEEDED(hr))
{
    // ...
    CoTaskMemFree(pszFilePath);
}
```



<span data-ttu-id="c6dd9-109">Die [**GetDisplayName-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) belegt Arbeitsspeicher für eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c6dd9-109">The [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) method allocates memory for a string.</span></span> <span data-ttu-id="c6dd9-110">Intern ruft die Methode [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) auf, um die Zeichenfolge zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="c6dd9-110">Internally, the method calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate the string.</span></span> <span data-ttu-id="c6dd9-111">Wenn die Methode zurückgegeben wird, zeigt *pszFilePath* auf den Speicherort des neuen Puffers.</span><span class="sxs-lookup"><span data-stu-id="c6dd9-111">When the method returns, *pszFilePath* points to the memory location of the new buffer.</span></span> <span data-ttu-id="c6dd9-112">Der Aufrufer ist für den Aufruf [**von CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) verantwortlich, um den Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="c6dd9-112">The caller is responsible for calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory.</span></span>

<span data-ttu-id="c6dd9-113">Warum definiert COM eigene Speicherbelegungsfunktionen?</span><span class="sxs-lookup"><span data-stu-id="c6dd9-113">Why does COM define its own memory allocation functions?</span></span> <span data-ttu-id="c6dd9-114">Ein Grund dafür ist die Bereitstellung einer Abstraktionsschicht über der Heapzuweisung.</span><span class="sxs-lookup"><span data-stu-id="c6dd9-114">One reason is to provide an abstraction layer over the heap allocator.</span></span> <span data-ttu-id="c6dd9-115">Andernfalls können einige Methoden **malloc** aufrufen, während andere **neue** aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="c6dd9-115">Otherwise, some methods might call **malloc** while others called **new**.</span></span> <span data-ttu-id="c6dd9-116">Dann müsste Ihr Programm in einigen Fällen **"free"** aufrufen und in anderen **löschen,** und es wäre schnell unmöglich, alles nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="c6dd9-116">Then your program would need to call **free** in some cases and **delete** in others, and keeping track of it all would quickly become impossible.</span></span> <span data-ttu-id="c6dd9-117">Die COM-Zuordnungsfunktionen erstellen einen einheitlichen Ansatz.</span><span class="sxs-lookup"><span data-stu-id="c6dd9-117">The COM allocation functions create a uniform approach.</span></span>

<span data-ttu-id="c6dd9-118">Ein weiterer Aspekt ist die Tatsache, dass COM ein *binärer* Standard ist und daher nicht an eine bestimmte Programmiersprache gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="c6dd9-118">Another consideration is the fact that COM is a *binary* standard, so it is not tied to a particular programming language.</span></span> <span data-ttu-id="c6dd9-119">Aus diesem Grund kann COM sich nicht auf eine sprachspezifische Form der Speicherbelegung verlassen.</span><span class="sxs-lookup"><span data-stu-id="c6dd9-119">Therefore, COM cannot rely on any language-specific form of memory allocation.</span></span>

## <a name="next"></a><span data-ttu-id="c6dd9-120">Nächste</span><span class="sxs-lookup"><span data-stu-id="c6dd9-120">Next</span></span>

[<span data-ttu-id="c6dd9-121">COM-Codierungsmethoden</span><span class="sxs-lookup"><span data-stu-id="c6dd9-121">COM Coding Practices</span></span>](com-coding-practices.md)

 

 
