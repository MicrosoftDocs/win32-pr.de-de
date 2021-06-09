---
title: SV_GroupID
description: Indizes für die Threadgruppe, in der ein Compute-Shader ausgeführt wird.
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
ms.openlocfilehash: ab94cef0a9a33f23947e11b93a5487c65eee3890
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827039"
---
# <a name="sv_groupid"></a><span data-ttu-id="19895-104">SV \_ GroupID</span><span class="sxs-lookup"><span data-stu-id="19895-104">SV\_GroupID</span></span>

<span data-ttu-id="19895-105">Indizes für die Threadgruppe, in der ein Compute-Shader ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="19895-105">Indices for which thread group a compute shader is executing in.</span></span> <span data-ttu-id="19895-106">Die Indizes gelten für die gesamte Gruppe und nicht für einen einzelnen Thread.</span><span class="sxs-lookup"><span data-stu-id="19895-106">The indices are to the whole group and not an individual thread.</span></span> <span data-ttu-id="19895-107">Mögliche Werte variieren in dem Bereich, der als Parameter an [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="19895-107">Possible values vary across the range passed as parameters to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch).</span></span> <span data-ttu-id="19895-108">Beispielsweise führt der Aufruf von Dispatch(2,1,1) zu möglichen Werten von 0,0,0 und 1,0,0.</span><span class="sxs-lookup"><span data-stu-id="19895-108">For example calling Dispatch(2,1,1) results in possible values of 0,0,0 and 1,0,0.</span></span>

<span data-ttu-id="19895-109">Definiert den Gruppenoffset innerhalb eines [**Dispatchaufrufs**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) pro Dimension des Dispatchaufrufs.</span><span class="sxs-lookup"><span data-stu-id="19895-109">Defines the group offset within a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) call, per dimension of the dispatch call.</span></span>

## <a name="type"></a><span data-ttu-id="19895-110">Typ</span><span class="sxs-lookup"><span data-stu-id="19895-110">Type</span></span>



| <span data-ttu-id="19895-111">Typ</span><span class="sxs-lookup"><span data-stu-id="19895-111">Type</span></span>      |
|-------|
| <span data-ttu-id="19895-112">uint3</span><span class="sxs-lookup"><span data-stu-id="19895-112">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="19895-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="19895-113">Remarks</span></span>

<span data-ttu-id="19895-114">Dieser Systemwert ist optional.</span><span class="sxs-lookup"><span data-stu-id="19895-114">This system value is optional.</span></span>

<span data-ttu-id="19895-115">Die folgende Abbildung zeigt die Beziehung zwischen den Parametern, die an [**Dispatch,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)Dispatch(5,3,2) übergeben werden, den im [attribut numthreads angegebenen](sm5-attributes-numthreads.md) Werten, numthreads(10,8,3) und Werten, die an den Compute-Shader für die threadbezogenen Systemwerte übergeben werden ([SV \_ GroupIndex](sv-groupindex.md),[SV \_ DispatchThreadID](sv-dispatchthreadid.md),[SV \_ GroupThreadID](sv-groupthreadid.md), SV \_ GroupID).</span><span class="sxs-lookup"><span data-stu-id="19895-115">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),SV\_GroupID).</span></span>

![Abbildung der Beziehung zwischen Dispatch, Threadgruppen und Threads](images/threadgroupids.png)

<span data-ttu-id="19895-117">Diese Funktion wird in den folgenden Shadertypen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="19895-117">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="19895-118">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="19895-118">Vertex</span></span> | <span data-ttu-id="19895-119">Rumpf</span><span class="sxs-lookup"><span data-stu-id="19895-119">Hull</span></span> | <span data-ttu-id="19895-120">Domain</span><span class="sxs-lookup"><span data-stu-id="19895-120">Domain</span></span> | <span data-ttu-id="19895-121">Geometrie</span><span class="sxs-lookup"><span data-stu-id="19895-121">Geometry</span></span> | <span data-ttu-id="19895-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="19895-122">Pixel</span></span> | <span data-ttu-id="19895-123">Compute</span><span class="sxs-lookup"><span data-stu-id="19895-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="19895-124">x</span><span class="sxs-lookup"><span data-stu-id="19895-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="19895-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19895-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19895-126">Semantik</span><span class="sxs-lookup"><span data-stu-id="19895-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="19895-127">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="19895-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
