---
title: numThreads
description: Definiert die Anzahl der Threads, die in einer einzelnen Thread Gruppe ausgeführt werden sollen, wenn ein Compute-Shader versendet wird (siehe Verknüpfung id3d11devicecontext aus Dispatch).
ms.assetid: ec6b751c-d81c-4221-ae80-166d2a3707fe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: abcca751b58bc88ba984ac5c2210a563591d592e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390953"
---
# <a name="numthreads"></a><span data-ttu-id="bc34e-103">numThreads</span><span class="sxs-lookup"><span data-stu-id="bc34e-103">numthreads</span></span>

<span data-ttu-id="bc34e-104">Definiert die Anzahl der Threads, die in einer einzelnen Thread Gruppe ausgeführt werden sollen, wenn ein Compute-Shader versendet wird (siehe [**Verknüpfung id3d11devicecontext aus::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)).</span><span class="sxs-lookup"><span data-stu-id="bc34e-104">Defines the number of threads to be executed in a single thread group when a compute shader is dispatched (see [**ID3D11DeviceContext::Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)).</span></span>


```
numthreads(X, Y, Z)    
```



<span data-ttu-id="bc34e-105">Der X-, y-und Z-Wert geben die Größe der Thread Gruppe in einer bestimmten Richtung an, und der Gesamtwert von x \* Y \* Z gibt die Anzahl der Threads in der Gruppe an.</span><span class="sxs-lookup"><span data-stu-id="bc34e-105">The X, Y and Z values indicate the size of the thread group in a particular direction and the total of X\*Y\*Z gives the number of threads in the group.</span></span> <span data-ttu-id="bc34e-106">Durch die Möglichkeit, die Größe der Thread Gruppe über drei Dimensionen hinweg anzugeben, können auf einzelne Threads auf eine Weise zugegriffen werden, die logisch 2D-und 3D-Datenstrukturen ist.</span><span class="sxs-lookup"><span data-stu-id="bc34e-106">The ability to specify the size of the thread group across three dimensions allows individual threads to be accessed in a manner that logically 2D and 3D data structures.</span></span>

<span data-ttu-id="bc34e-107">Wenn z. b. ein Compute-Shader eine 4 x 4-Matrix Addition durchführt, können numThreads auf numThreads (4, 4, 1) festgelegt werden, und die Indizierung in den einzelnen Threads würde automatisch den Matrix Einträgen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="bc34e-107">For example, if a compute shader is doing 4x4 matrix addition then numthreads could be set to numthreads(4,4,1) and the indexing in the individual threads would automatically match the matrix entries.</span></span> <span data-ttu-id="bc34e-108">Der COMPUTE-Shader kann auch eine Thread Gruppe mit der gleichen Anzahl von Threads (16) mit numThreads (16, 1, 1) deklarieren, müsste jedoch den aktuellen Matrix Eintrag basierend auf der aktuellen Thread Nummer berechnen.</span><span class="sxs-lookup"><span data-stu-id="bc34e-108">The compute shader could also declare a thread group with the same number of threads (16) using numthreads(16,1,1), however it would then have to calculate the current matrix entry based on the current thread number.</span></span>

<span data-ttu-id="bc34e-109">Die zulässigen Parameterwerte für **numThreads** sind von der COMPUTE-Shader-Version abhängig.</span><span class="sxs-lookup"><span data-stu-id="bc34e-109">The allowable parameter values for **numthreads** depends on the compute shader version.</span></span>



| <span data-ttu-id="bc34e-110">Compute-Shader</span><span class="sxs-lookup"><span data-stu-id="bc34e-110">Compute Shader</span></span> | <span data-ttu-id="bc34e-111">Maximum Z</span><span class="sxs-lookup"><span data-stu-id="bc34e-111">Maximum Z</span></span> | <span data-ttu-id="bc34e-112">Maximale Threads (X \* Y \* Z)</span><span class="sxs-lookup"><span data-stu-id="bc34e-112">Maximum Threads (X\*Y\*Z)</span></span> |
|----------------|-----------|---------------------------|
| <span data-ttu-id="bc34e-113">CS \_ 4 \_ x</span><span class="sxs-lookup"><span data-stu-id="bc34e-113">cs\_4\_x</span></span>       | <span data-ttu-id="bc34e-114">1</span><span class="sxs-lookup"><span data-stu-id="bc34e-114">1</span></span>         | <span data-ttu-id="bc34e-115">768</span><span class="sxs-lookup"><span data-stu-id="bc34e-115">768</span></span>                       |
| <span data-ttu-id="bc34e-116">CS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bc34e-116">cs\_5\_0</span></span>       | <span data-ttu-id="bc34e-117">64</span><span class="sxs-lookup"><span data-stu-id="bc34e-117">64</span></span>        | <span data-ttu-id="bc34e-118">1024</span><span class="sxs-lookup"><span data-stu-id="bc34e-118">1024</span></span>                      |



 

<span data-ttu-id="bc34e-119">Die folgende Abbildung zeigt die Beziehung zwischen den Parametern, die an Verknüpfung id3d11devicecontext aus übermittelt werden [**::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch (5, 3, 2), die im numThreads-Attribut angegebenen Werte, numThreads (10, 8, 3) und Werte, die an den Compute-Shader für die Thread bezogenen System Werte ([SV \_ groupIndex](sv-groupindex.md),[SV \_ dispatchthreadid](sv-dispatchthreadid.md),[SV \_ groupthreadid](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)) weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bc34e-119">The following illustration shows the relationship between the parameters passed to [**ID3D11DeviceContext::Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the numthreads attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![Darstellung der Beziehung zwischen Dispatch, Thread Gruppen und Threads](images/threadgroupids.png)

<span data-ttu-id="bc34e-121">Dieses Attribut wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="bc34e-121">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="bc34e-122">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="bc34e-122">Vertex</span></span> | <span data-ttu-id="bc34e-123">Hülle</span><span class="sxs-lookup"><span data-stu-id="bc34e-123">Hull</span></span> | <span data-ttu-id="bc34e-124">Domain</span><span class="sxs-lookup"><span data-stu-id="bc34e-124">Domain</span></span> | <span data-ttu-id="bc34e-125">Geometrie</span><span class="sxs-lookup"><span data-stu-id="bc34e-125">Geometry</span></span> | <span data-ttu-id="bc34e-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="bc34e-126">Pixel</span></span> | <span data-ttu-id="bc34e-127">Compute</span><span class="sxs-lookup"><span data-stu-id="bc34e-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="bc34e-128">x</span><span class="sxs-lookup"><span data-stu-id="bc34e-128">x</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="bc34e-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bc34e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc34e-130">Shader Model 5-Attribute</span><span class="sxs-lookup"><span data-stu-id="bc34e-130">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="bc34e-131">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="bc34e-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 