---
title: SV_DispatchThreadID
description: Indizes für die kombinierte Thread- und Threadgruppe, in der ein Compute-Shader ausgeführt wird.
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
ms.openlocfilehash: 8e2713aaa50206660f7672688a43e644873b1c13
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827059"
---
# <a name="sv_dispatchthreadid"></a><span data-ttu-id="969de-104">SV \_ DispatchThreadID</span><span class="sxs-lookup"><span data-stu-id="969de-104">SV\_DispatchThreadID</span></span>

<span data-ttu-id="969de-105">Indizes für die kombinierte Thread- und Threadgruppe, in der ein Compute-Shader ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="969de-105">Indices for which combined thread and thread group a compute shader is executing in.</span></span> <span data-ttu-id="969de-106">SV \_ DispatchThreadID ist die Summe aus SV \_ GroupID \* numthreads und GroupThreadID.</span><span class="sxs-lookup"><span data-stu-id="969de-106">SV\_DispatchThreadID is the sum of SV\_GroupID \* numthreads and GroupThreadID.</span></span> <span data-ttu-id="969de-107">Sie variiert über den unter [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) und [numthreads angegebenen](sm5-attributes-numthreads.md)Bereich.</span><span class="sxs-lookup"><span data-stu-id="969de-107">It varies across the range specified in [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) and [numthreads](sm5-attributes-numthreads.md).</span></span> <span data-ttu-id="969de-108">Wenn z. B. Dispatch(2,2,2) für einen Compute-Shader mit numthreads(3,3,3) SV \_ DispatchThreadID aufgerufen wird, hat für jede Dimension einen Bereich von 0,.5.</span><span class="sxs-lookup"><span data-stu-id="969de-108">For example if Dispatch(2,2,2) is called on a compute shader with numthreads(3,3,3) SV\_DispatchThreadID will have a range of 0..5 for each dimension.</span></span>

## <a name="type"></a><span data-ttu-id="969de-109">Typ</span><span class="sxs-lookup"><span data-stu-id="969de-109">Type</span></span>



| <span data-ttu-id="969de-110">Typ</span><span class="sxs-lookup"><span data-stu-id="969de-110">Type</span></span>      |
|-------|
| <span data-ttu-id="969de-111">uint3</span><span class="sxs-lookup"><span data-stu-id="969de-111">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="969de-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="969de-112">Remarks</span></span>

<span data-ttu-id="969de-113">Dieser Systemwert ist optional.</span><span class="sxs-lookup"><span data-stu-id="969de-113">This system value is optional.</span></span>

<span data-ttu-id="969de-114">Die folgende Abbildung zeigt die Beziehung zwischen den parametern, die an [**Dispatch,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)Dispatch(5,3,2) übergeben werden, den im [numthreads-Attribut angegebenen](sm5-attributes-numthreads.md) Werten, numthreads(10,8,3) und Werten, die an den Compute-Shader für die threadbezogenen Systemwerte übergeben werden ([SV \_ GroupIndex](sv-groupindex.md), SV \_ DispatchThreadID,[SV \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)).</span><span class="sxs-lookup"><span data-stu-id="969de-114">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),SV\_DispatchThreadID,[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![Abbildung der Beziehung zwischen Dispatch, Threadgruppen und Threads](images/threadgroupids.png)

<span data-ttu-id="969de-116">Diese Funktion wird in den folgenden Shadertypen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="969de-116">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="969de-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="969de-117">Vertex</span></span> | <span data-ttu-id="969de-118">Rumpf</span><span class="sxs-lookup"><span data-stu-id="969de-118">Hull</span></span> | <span data-ttu-id="969de-119">Domain</span><span class="sxs-lookup"><span data-stu-id="969de-119">Domain</span></span> | <span data-ttu-id="969de-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="969de-120">Geometry</span></span> | <span data-ttu-id="969de-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="969de-121">Pixel</span></span> | <span data-ttu-id="969de-122">Compute</span><span class="sxs-lookup"><span data-stu-id="969de-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="969de-123">x</span><span class="sxs-lookup"><span data-stu-id="969de-123">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="969de-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="969de-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="969de-125">Semantik</span><span class="sxs-lookup"><span data-stu-id="969de-125">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="969de-126">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="969de-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
