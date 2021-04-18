---
title: Speicher Belegung in com
description: .
ms.assetid: b3c318d2-1273-430e-8aca-5bd5c95c138e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62227f78287f184b019eee3e498ec8a25f25a03c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338461"
---
# <a name="memory-allocation-in-com"></a><span data-ttu-id="faf85-103">Speicher Belegung in com</span><span class="sxs-lookup"><span data-stu-id="faf85-103">Memory Allocation in COM</span></span>

<span data-ttu-id="faf85-104">Manchmal ordnet eine Methode einen Speicherpuffer auf dem Heap zu und gibt die Adresse des Puffers an den Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="faf85-104">Sometimes a method allocates a memory buffer on the heap and returns the address of the buffer to the caller.</span></span> <span data-ttu-id="faf85-105">COM definiert ein Funktions Paar zum Zuordnen und Freigeben von Arbeitsspeicher auf dem Heap.</span><span class="sxs-lookup"><span data-stu-id="faf85-105">COM defines a pair of functions for allocating and freeing memory on the heap.</span></span>

-   <span data-ttu-id="faf85-106">Die [**cotaskmembelegc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) -Funktion weist einen Speicherblock zu.</span><span class="sxs-lookup"><span data-stu-id="faf85-106">The [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) function allocates a block of memory.</span></span>
-   <span data-ttu-id="faf85-107">Die [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) -Funktion gibt einen Speicherblock frei, der mit [**cotaskmembelegc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc)zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="faf85-107">The [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) function frees a block of memory that was allocated with [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc).</span></span>

<span data-ttu-id="faf85-108">Wir haben ein Beispiel für dieses Muster im [Dialogfeld "Öffnen" angezeigt](example--the-open-dialog-box.md):</span><span class="sxs-lookup"><span data-stu-id="faf85-108">We saw an example of this pattern in the [Open dialog box example](example--the-open-dialog-box.md):</span></span>


```C++
PWSTR pszFilePath;
hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
if (SUCCEEDED(hr))
{
    // ...
    CoTaskMemFree(pszFilePath);
}
```



<span data-ttu-id="faf85-109">Die [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) -Methode ordnet Speicher für eine Zeichenfolge zu.</span><span class="sxs-lookup"><span data-stu-id="faf85-109">The [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) method allocates memory for a string.</span></span> <span data-ttu-id="faf85-110">Intern wird von der-Methode [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) aufgerufen, um die Zeichenfolge zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="faf85-110">Internally, the method calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate the string.</span></span> <span data-ttu-id="faf85-111">Wenn die-Methode zurückgegeben wird, verweist *pszfilepath* auf den Speicherort des neuen Puffers.</span><span class="sxs-lookup"><span data-stu-id="faf85-111">When the method returns, *pszFilePath* points to the memory location of the new buffer.</span></span> <span data-ttu-id="faf85-112">Der Aufrufer ist für das Aufrufen von [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) zuständig, um den Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="faf85-112">The caller is responsible for calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory.</span></span>

<span data-ttu-id="faf85-113">Warum definiert com seine eigenen Speicher Belegungs Funktionen?</span><span class="sxs-lookup"><span data-stu-id="faf85-113">Why does COM define its own memory allocation functions?</span></span> <span data-ttu-id="faf85-114">Ein Grund ist, eine Abstraktions Ebene über die Heap Zuweisung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="faf85-114">One reason is to provide an abstraction layer over the heap allocator.</span></span> <span data-ttu-id="faf85-115">Andernfalls können einige Methoden **malloc** aufrufen, während andere als **New** bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="faf85-115">Otherwise, some methods might call **malloc** while others called **new**.</span></span> <span data-ttu-id="faf85-116">Dann müsste Ihr Programm in einigen Fällen **kostenlos** anrufen und in anderen Fällen **Löschen** , und die Nachverfolgung des gesamten Programms würde schnell unmöglich werden.</span><span class="sxs-lookup"><span data-stu-id="faf85-116">Then your program would need to call **free** in some cases and **delete** in others, and keeping track of it all would quickly become impossible.</span></span> <span data-ttu-id="faf85-117">Die com-Zuordnungs Funktionen erstellen einen einheitlichen Ansatz.</span><span class="sxs-lookup"><span data-stu-id="faf85-117">The COM allocation functions create a uniform approach.</span></span>

<span data-ttu-id="faf85-118">Ein weiterer Aspekt ist die Tatsache, dass com ein *binärer* Standard ist, sodass er nicht an eine bestimmte Programmiersprache gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="faf85-118">Another consideration is the fact that COM is a *binary* standard, so it is not tied to a particular programming language.</span></span> <span data-ttu-id="faf85-119">Daher kann com nicht auf eine sprachspezifische Form der Speicher Belegung zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="faf85-119">Therefore, COM cannot rely on any language-specific form of memory allocation.</span></span>

## <a name="next"></a><span data-ttu-id="faf85-120">Nächste</span><span class="sxs-lookup"><span data-stu-id="faf85-120">Next</span></span>

[<span data-ttu-id="faf85-121">COM-Codierungs Methoden</span><span class="sxs-lookup"><span data-stu-id="faf85-121">COM Coding Practices</span></span>](com-coding-practices.md)

 

 