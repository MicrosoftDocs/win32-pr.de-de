---
title: SV_GroupIndex
description: Der \ 0034; vereinfacht \ 0034; der Index eines Compute-Shader-Threads innerhalb einer Thread Gruppe, der den mehrdimensionalen SV \_ groupthreadid in einen 1D-Wert umwandelt. SV \_ groupIndex variiert zwischen 0 und (numthreadsx \ numthreadsy \ numthreadsz) \ 8211; 1.
ms.assetid: e793be10-7c83-478c-859a-4b0a2c537570
keywords:
- SV_GroupIndex HLSL
topic_type:
- apiref
api_name:
- SV_GroupIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 952a94378a0570d5bb7bc4f08959074bc8a4da4d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728177"
---
# <a name="sv_groupindex"></a><span data-ttu-id="54f3d-105">SV \_ groupIndex</span><span class="sxs-lookup"><span data-stu-id="54f3d-105">SV\_GroupIndex</span></span>

<span data-ttu-id="54f3d-106">Der "vereinfachte" Index eines Compute-Shader-Threads innerhalb einer Thread Gruppe, der den mehrdimensionalen SV \_ groupthreadid in einen 1D-Wert umwandelt.</span><span class="sxs-lookup"><span data-stu-id="54f3d-106">The "flattened" index of a compute shader thread within a thread group, which turns the multi-dimensional SV\_GroupThreadID into a 1D value.</span></span> <span data-ttu-id="54f3d-107">SV \_ groupIndex variiert zwischen 0 und (numthreadsx \* \* numthreadsz) – 1.</span><span class="sxs-lookup"><span data-stu-id="54f3d-107">SV\_GroupIndex varies from 0 to (numthreadsX \* numthreadsY \* numThreadsZ) – 1.</span></span>

## <a name="type"></a><span data-ttu-id="54f3d-108">Typ</span><span class="sxs-lookup"><span data-stu-id="54f3d-108">Type</span></span>



| <span data-ttu-id="54f3d-109">Typ</span><span class="sxs-lookup"><span data-stu-id="54f3d-109">Type</span></span> |
|------|
| <span data-ttu-id="54f3d-110">uint</span><span class="sxs-lookup"><span data-stu-id="54f3d-110">uint</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="54f3d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54f3d-111">Remarks</span></span>


```
SV_GroupIndex = SV_GroupThreadID.z*dimx*dimy + 
                      SV_GroupThreadID.y*dimx + 
                      SV_GroupThreadID.x
```



<span data-ttu-id="54f3d-112">Dabei sind "dimx" und "dimy" die Dimensionen, die im [numThreads](sm5-attributes-numthreads.md) -Attribut für den Einstiegspunkt angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="54f3d-112">where dimx and dimy are the dimensions specified in the [numthreads](sm5-attributes-numthreads.md) attribute for the entry point.</span></span>

<span data-ttu-id="54f3d-113">Dieser System Wert ist optional.</span><span class="sxs-lookup"><span data-stu-id="54f3d-113">This system value is optional.</span></span> <span data-ttu-id="54f3d-114">Durch die Verwendung wird jedoch sichergestellt, dass ein Thread nur in den zugewiesenen Speicherbereich in der groupshared-Variablen schreibt.</span><span class="sxs-lookup"><span data-stu-id="54f3d-114">However, its use ensures that a thread only writes to its assigned region of memory in the groupshared variable.</span></span>

<span data-ttu-id="54f3d-115">Die folgende Abbildung zeigt die Beziehung zwischen den Parametern, die an Verknüpfung id3d11devicecontext aus übermittelt werden [**::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch (5, 3, 2), die im [numThreads](sm5-attributes-numthreads.md) -Attribut angegebenen Werte, numThreads (10, 8, 3) und Werte, die an den Compute-Shader für die Thread bezogenen System Werte (SV \_ groupIndex,[SV \_ dispatchthreadid](sv-dispatchthreadid.md),[SV \_ groupthreadid](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)) weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="54f3d-115">The following illustration shows the relationship between the parameters passed to [**ID3D11DeviceContext::Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values (SV\_GroupIndex,[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![Darstellung der Beziehung zwischen Dispatch, Thread Gruppen und Threads](images/threadgroupids.png)

<span data-ttu-id="54f3d-117">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="54f3d-117">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="54f3d-118">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="54f3d-118">Vertex</span></span> | <span data-ttu-id="54f3d-119">Hülle</span><span class="sxs-lookup"><span data-stu-id="54f3d-119">Hull</span></span> | <span data-ttu-id="54f3d-120">Domain</span><span class="sxs-lookup"><span data-stu-id="54f3d-120">Domain</span></span> | <span data-ttu-id="54f3d-121">Geometrie</span><span class="sxs-lookup"><span data-stu-id="54f3d-121">Geometry</span></span> | <span data-ttu-id="54f3d-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="54f3d-122">Pixel</span></span> | <span data-ttu-id="54f3d-123">Compute</span><span class="sxs-lookup"><span data-stu-id="54f3d-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="54f3d-124">x</span><span class="sxs-lookup"><span data-stu-id="54f3d-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="54f3d-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="54f3d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54f3d-126">Semantik</span><span class="sxs-lookup"><span data-stu-id="54f3d-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="54f3d-127">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="54f3d-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 