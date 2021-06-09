---
title: SV_GroupThreadID
description: Indizes, für die ein einzelner Thread innerhalb einer Threadgruppe einen Compute-Shader ausführt.
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
ms.openlocfilehash: d399008f1a9314ceb1fd4b1499b51340b499600b
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827029"
---
# <a name="sv_groupthreadid"></a><span data-ttu-id="4de5f-104">SV \_ GroupThreadID</span><span class="sxs-lookup"><span data-stu-id="4de5f-104">SV\_GroupThreadID</span></span>

<span data-ttu-id="4de5f-105">Indizes, für die ein einzelner Thread innerhalb einer Threadgruppe einen Compute-Shader ausführt.</span><span class="sxs-lookup"><span data-stu-id="4de5f-105">Indices for which an individual thread within a thread group a compute shader is executing in.</span></span> <span data-ttu-id="4de5f-106">SV \_ GroupThreadID variiert je nach Bereich, der für den Compute-Shader im [numthreads-Attribut](sm5-attributes-numthreads.md) angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4de5f-106">SV\_GroupThreadID varies across the range specified for the compute shader in the [numthreads](sm5-attributes-numthreads.md) attribute.</span></span> <span data-ttu-id="4de5f-107">Wenn beispielsweise numthreads(3,2,1) als mögliche Werte für den SV \_ GroupThreadID-Eingabewert angegeben wurde, weist dieser Wertebereich (0-2,0-1,0) auf.</span><span class="sxs-lookup"><span data-stu-id="4de5f-107">For example if numthreads(3,2,1) was specified possible values for the SV\_GroupThreadID input value have this range of values (0-2,0-1,0).</span></span>

## <a name="type"></a><span data-ttu-id="4de5f-108">Typ</span><span class="sxs-lookup"><span data-stu-id="4de5f-108">Type</span></span>



| <span data-ttu-id="4de5f-109">Typ</span><span class="sxs-lookup"><span data-stu-id="4de5f-109">Type</span></span>      |
|-------|
| <span data-ttu-id="4de5f-110">uint3</span><span class="sxs-lookup"><span data-stu-id="4de5f-110">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4de5f-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4de5f-111">Remarks</span></span>

<span data-ttu-id="4de5f-112">Dieser Systemwert ist optional und liegt immer innerhalb der Grenzen der Werte, die an das [numthreads-Attribut](sm5-attributes-numthreads.md) übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="4de5f-112">This system value is optional, and is always within the bounds of the values passed into the [numthreads](sm5-attributes-numthreads.md) attribute.</span></span>

<span data-ttu-id="4de5f-113">Die folgende Abbildung zeigt die Beziehung zwischen den Parametern, die an [**Dispatch,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)Dispatch(5,3,2) übergeben werden, den im [attribut numthreads angegebenen](sm5-attributes-numthreads.md) Werten, numthreads(10,8,3) und Werten, die an den Compute-Shader für die threadbezogenen Systemwerte übergeben werden ([SV \_ GroupIndex](sv-groupindex.md),[SV \_ DispatchThreadID](sv-dispatchthreadid.md), SV \_ GroupThreadID,[SV \_ GroupID](sv-groupid.md)).</span><span class="sxs-lookup"><span data-stu-id="4de5f-113">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),SV\_GroupThreadID,[SV\_GroupID](sv-groupid.md)).</span></span>

![Abbildung der Beziehung zwischen Dispatch, Threadgruppen und Threads](images/threadgroupids.png)

<span data-ttu-id="4de5f-115">Diese Funktion wird in den folgenden Shadertypen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="4de5f-115">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="4de5f-116">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="4de5f-116">Vertex</span></span> | <span data-ttu-id="4de5f-117">Rumpf</span><span class="sxs-lookup"><span data-stu-id="4de5f-117">Hull</span></span> | <span data-ttu-id="4de5f-118">Domain</span><span class="sxs-lookup"><span data-stu-id="4de5f-118">Domain</span></span> | <span data-ttu-id="4de5f-119">Geometrie</span><span class="sxs-lookup"><span data-stu-id="4de5f-119">Geometry</span></span> | <span data-ttu-id="4de5f-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="4de5f-120">Pixel</span></span> | <span data-ttu-id="4de5f-121">Compute</span><span class="sxs-lookup"><span data-stu-id="4de5f-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="4de5f-122">x</span><span class="sxs-lookup"><span data-stu-id="4de5f-122">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4de5f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4de5f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4de5f-124">Semantik</span><span class="sxs-lookup"><span data-stu-id="4de5f-124">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="4de5f-125">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="4de5f-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
