---
title: SV_GroupThreadID
description: Indizes, für die ein einzelner Thread in einer Thread Gruppe, in der ein Compute-Shader ausgeführt wird, ausgeführt wird.
ms.assetid: be944592-c4ea-43c9-88bc-98a9a190a437
keywords:
- SV_GroupThreadID HLSL
topic_type:
- apiref
api_name:
- SV_GroupThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d4d35766bdbdc2d69c98983a85f336ab784d24d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316268"
---
# <a name="sv_groupthreadid"></a><span data-ttu-id="d5d0a-104">SV \_ groupthreadid</span><span class="sxs-lookup"><span data-stu-id="d5d0a-104">SV\_GroupThreadID</span></span>

<span data-ttu-id="d5d0a-105">Indizes, für die ein einzelner Thread in einer Thread Gruppe, in der ein Compute-Shader ausgeführt wird, ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5d0a-105">Indices for which an individual thread within a thread group a compute shader is executing in.</span></span> <span data-ttu-id="d5d0a-106">SV \_ groupthreadid variiert in dem Bereich, der für den Compute-Shader im [numThreads](sm5-attributes-numthreads.md) -Attribut angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d5d0a-106">SV\_GroupThreadID varies across the range specified for the compute shader in the [numthreads](sm5-attributes-numthreads.md) attribute.</span></span> <span data-ttu-id="d5d0a-107">Wenn z. b. numThreads (3, 2, 1) angegeben wurden, haben die Werte für den \_ Eingabe Wert SV groupthreadid diesen Wertebereich (0-2, 0-1, 0).</span><span class="sxs-lookup"><span data-stu-id="d5d0a-107">For example if numthreads(3,2,1) was specified possible values for the SV\_GroupThreadID input value have this range of values (0-2,0-1,0).</span></span>

## <a name="type"></a><span data-ttu-id="d5d0a-108">Typ</span><span class="sxs-lookup"><span data-stu-id="d5d0a-108">Type</span></span>



|       |
|-------|
| <span data-ttu-id="d5d0a-109">Typ</span><span class="sxs-lookup"><span data-stu-id="d5d0a-109">Type</span></span>  |
| <span data-ttu-id="d5d0a-110">uint3</span><span class="sxs-lookup"><span data-stu-id="d5d0a-110">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d5d0a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5d0a-111">Remarks</span></span>

<span data-ttu-id="d5d0a-112">Dieser System Wert ist optional und liegt immer innerhalb der Grenzen der Werte, die an das [numThreads](sm5-attributes-numthreads.md) -Attribut übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="d5d0a-112">This system value is optional, and is always within the bounds of the values passed into the [numthreads](sm5-attributes-numthreads.md) attribute.</span></span>

<span data-ttu-id="d5d0a-113">Die folgende Abbildung zeigt die Beziehung zwischen den Parametern, die an [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)weitergeleitet werden. Dispatch (5, 3, 2), die im [numThreads](sm5-attributes-numthreads.md) -Attribut angegebenen Werte, numThreads (10, 8, 3) und Werte, die an den Compute-Shader für die Thread bezogenen System Werte ([SV \_ groupIndex](sv-groupindex.md),[SV \_ dispatchthreadid](sv-dispatchthreadid.md), SV \_ groupthreadid,[SV \_ GroupID](sv-groupid.md)) weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d5d0a-113">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),SV\_GroupThreadID,[SV\_GroupID](sv-groupid.md)).</span></span>

![Darstellung der Beziehung zwischen Dispatch, Thread Gruppen und Threads](images/threadgroupids.png)

<span data-ttu-id="d5d0a-115">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="d5d0a-115">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d5d0a-116">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="d5d0a-116">Vertex</span></span> | <span data-ttu-id="d5d0a-117">Hülle</span><span class="sxs-lookup"><span data-stu-id="d5d0a-117">Hull</span></span> | <span data-ttu-id="d5d0a-118">Domain</span><span class="sxs-lookup"><span data-stu-id="d5d0a-118">Domain</span></span> | <span data-ttu-id="d5d0a-119">Geometrie</span><span class="sxs-lookup"><span data-stu-id="d5d0a-119">Geometry</span></span> | <span data-ttu-id="d5d0a-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="d5d0a-120">Pixel</span></span> | <span data-ttu-id="d5d0a-121">Compute</span><span class="sxs-lookup"><span data-stu-id="d5d0a-121">Compute</span></span> |
|        |      |        |          |       | <span data-ttu-id="d5d0a-122">x</span><span class="sxs-lookup"><span data-stu-id="d5d0a-122">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d5d0a-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d5d0a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5d0a-124">Semantik</span><span class="sxs-lookup"><span data-stu-id="d5d0a-124">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="d5d0a-125">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="d5d0a-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 