---
title: SV_DispatchThreadID
description: Indizes, für die der kombinierte Thread und die Thread Gruppe, in der ein Compute-Shader ausgeführt wird.
ms.assetid: bad697f6-26d9-47cd-93e5-127621a161e8
keywords:
- SV_DispatchThreadID HLSL
topic_type:
- apiref
api_name:
- SV_DispatchThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d55fcf7e291c561ecb51dd32dfac135c563974c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549872"
---
# <a name="sv_dispatchthreadid"></a><span data-ttu-id="13f0c-104">SV \_ dispatchthreadid</span><span class="sxs-lookup"><span data-stu-id="13f0c-104">SV\_DispatchThreadID</span></span>

<span data-ttu-id="13f0c-105">Indizes, für die der kombinierte Thread und die Thread Gruppe, in der ein Compute-Shader ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="13f0c-105">Indices for which combined thread and thread group a compute shader is executing in.</span></span> <span data-ttu-id="13f0c-106">SV \_ dispatchthreadid ist die Summe von SV \_ GroupID \* numThreads und groupthreadid.</span><span class="sxs-lookup"><span data-stu-id="13f0c-106">SV\_DispatchThreadID is the sum of SV\_GroupID \* numthreads and GroupThreadID.</span></span> <span data-ttu-id="13f0c-107">Sie variiert in dem Bereich, der in [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) und [numThreads](sm5-attributes-numthreads.md)angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="13f0c-107">It varies across the range specified in [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) and [numthreads](sm5-attributes-numthreads.md).</span></span> <span data-ttu-id="13f0c-108">Wenn z. b. Dispatch (2, 2, 2) auf einem Compute-Shader mit numThreads (3, 3, 3) aufgerufen wird, weist SV \_ dispatchthreadid einen Bereich von 0.. 5 für jede Dimension auf.</span><span class="sxs-lookup"><span data-stu-id="13f0c-108">For example if Dispatch(2,2,2) is called on a compute shader with numthreads(3,3,3) SV\_DispatchThreadID will have a range of 0..5 for each dimension.</span></span>

## <a name="type"></a><span data-ttu-id="13f0c-109">Typ</span><span class="sxs-lookup"><span data-stu-id="13f0c-109">Type</span></span>



|       |
|-------|
| <span data-ttu-id="13f0c-110">Typ</span><span class="sxs-lookup"><span data-stu-id="13f0c-110">Type</span></span>  |
| <span data-ttu-id="13f0c-111">uint3</span><span class="sxs-lookup"><span data-stu-id="13f0c-111">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="13f0c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13f0c-112">Remarks</span></span>

<span data-ttu-id="13f0c-113">Dieser System Wert ist optional.</span><span class="sxs-lookup"><span data-stu-id="13f0c-113">This system value is optional.</span></span>

<span data-ttu-id="13f0c-114">Die folgende Abbildung zeigt die Beziehung zwischen den Parametern, die an [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)weitergeleitet werden. Dispatch (5, 3, 2), die im [numThreads](sm5-attributes-numthreads.md) -Attribut angegebenen Werte, numThreads (10, 8, 3) und Werte, die an den Compute-Shader für die Thread bezogenen System Werte ([SV \_ groupIndex](sv-groupindex.md), SV \_ dispatchthreadid,[SV \_ groupthreadid](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)) weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="13f0c-114">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),SV\_DispatchThreadID,[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![Darstellung der Beziehung zwischen Dispatch, Thread Gruppen und Threads](images/threadgroupids.png)

<span data-ttu-id="13f0c-116">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="13f0c-116">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="13f0c-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="13f0c-117">Vertex</span></span> | <span data-ttu-id="13f0c-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="13f0c-118">Hull</span></span> | <span data-ttu-id="13f0c-119">Domain</span><span class="sxs-lookup"><span data-stu-id="13f0c-119">Domain</span></span> | <span data-ttu-id="13f0c-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="13f0c-120">Geometry</span></span> | <span data-ttu-id="13f0c-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="13f0c-121">Pixel</span></span> | <span data-ttu-id="13f0c-122">Compute</span><span class="sxs-lookup"><span data-stu-id="13f0c-122">Compute</span></span> |
|        |      |        |          |       | <span data-ttu-id="13f0c-123">x</span><span class="sxs-lookup"><span data-stu-id="13f0c-123">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="13f0c-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="13f0c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13f0c-125">Semantik</span><span class="sxs-lookup"><span data-stu-id="13f0c-125">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="13f0c-126">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="13f0c-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 