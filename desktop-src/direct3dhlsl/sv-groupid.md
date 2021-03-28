---
title: SV_GroupID
description: Indizes für die Thread Gruppe, in der ein Compute-Shader ausgeführt wird.
ms.assetid: 1b90ca74-a2b6-4a5f-aa4a-1ec879360593
keywords:
- SV_GroupID HLSL
topic_type:
- apiref
api_name:
- SV_GroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2588474a4c6f2cfc6d616cdb70940277389fd1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101787"
---
# <a name="sv_groupid"></a><span data-ttu-id="82721-104">SV \_ GroupID</span><span class="sxs-lookup"><span data-stu-id="82721-104">SV\_GroupID</span></span>

<span data-ttu-id="82721-105">Indizes für die Thread Gruppe, in der ein Compute-Shader ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="82721-105">Indices for which thread group a compute shader is executing in.</span></span> <span data-ttu-id="82721-106">Die Indizes gelten für die gesamte Gruppe und nicht für einen einzelnen Thread.</span><span class="sxs-lookup"><span data-stu-id="82721-106">The indices are to the whole group and not an individual thread.</span></span> <span data-ttu-id="82721-107">Mögliche Werte variieren in dem Bereich, der als Parameter an [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)weitergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="82721-107">Possible values vary across the range passed as parameters to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch).</span></span> <span data-ttu-id="82721-108">Der Aufruf von Dispatch (2, 1, 1) führt beispielsweise zu möglichen Werten von 0, 0, 0 und 1, 0, 0.</span><span class="sxs-lookup"><span data-stu-id="82721-108">For example calling Dispatch(2,1,1) results in possible values of 0,0,0 and 1,0,0.</span></span>

<span data-ttu-id="82721-109">Definiert den Gruppen Offset in einem [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) -Befehl pro Dimension des dispatchaufrufes.</span><span class="sxs-lookup"><span data-stu-id="82721-109">Defines the group offset within a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) call, per dimension of the dispatch call.</span></span>

## <a name="type"></a><span data-ttu-id="82721-110">Typ</span><span class="sxs-lookup"><span data-stu-id="82721-110">Type</span></span>



|       |
|-------|
| <span data-ttu-id="82721-111">Typ</span><span class="sxs-lookup"><span data-stu-id="82721-111">Type</span></span>  |
| <span data-ttu-id="82721-112">uint3</span><span class="sxs-lookup"><span data-stu-id="82721-112">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="82721-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82721-113">Remarks</span></span>

<span data-ttu-id="82721-114">Dieser System Wert ist optional.</span><span class="sxs-lookup"><span data-stu-id="82721-114">This system value is optional.</span></span>

<span data-ttu-id="82721-115">Die folgende Abbildung zeigt die Beziehung zwischen den Parametern, die an [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)weitergeleitet werden. Dispatch (5, 3, 2), die im [numThreads](sm5-attributes-numthreads.md) -Attribut angegebenen Werte, numThreads (10, 8, 3) und Werte, die an den Compute-Shader für die Thread bezogenen System Werte ([SV \_ groupIndex](sv-groupindex.md),[SV \_ dispatchthreadid](sv-dispatchthreadid.md),[SV \_ groupthreadid](sv-groupthreadid.md), SV \_ GroupID) weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="82721-115">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),SV\_GroupID).</span></span>

![Darstellung der Beziehung zwischen Dispatch, Thread Gruppen und Threads](images/threadgroupids.png)

<span data-ttu-id="82721-117">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="82721-117">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="82721-118">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="82721-118">Vertex</span></span> | <span data-ttu-id="82721-119">Hülle</span><span class="sxs-lookup"><span data-stu-id="82721-119">Hull</span></span> | <span data-ttu-id="82721-120">Domain</span><span class="sxs-lookup"><span data-stu-id="82721-120">Domain</span></span> | <span data-ttu-id="82721-121">Geometrie</span><span class="sxs-lookup"><span data-stu-id="82721-121">Geometry</span></span> | <span data-ttu-id="82721-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="82721-122">Pixel</span></span> | <span data-ttu-id="82721-123">Compute</span><span class="sxs-lookup"><span data-stu-id="82721-123">Compute</span></span> |
|        |      |        |          |       | <span data-ttu-id="82721-124">x</span><span class="sxs-lookup"><span data-stu-id="82721-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="82721-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="82721-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82721-126">Semantik</span><span class="sxs-lookup"><span data-stu-id="82721-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="82721-127">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="82721-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 