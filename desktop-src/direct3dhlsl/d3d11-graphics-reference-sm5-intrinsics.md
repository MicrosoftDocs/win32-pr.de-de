---
title: Intrinsische Funktionen von Shader Model 5
description: Shadermodell 5 implementiert die intrinsischen Funktionen aus Shader Model 4 und niedriger (Weitere Informationen finden Sie unter intrinsische Funktionen (DirectX HLSL), eine umfassende Liste der unterstützten Funktionen) sowie die folgenden neuen Funktionen.
ms.assetid: 6f91fb40-d6d0-459f-adf7-cff263d7d346
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0cd5976526f75b676a853ef7480d4e81e0e00a91
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389515"
---
# <a name="shader-model-5-intrinsic-functions"></a><span data-ttu-id="4a11a-103">Intrinsische Funktionen von Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="4a11a-103">Shader Model 5 Intrinsic Functions</span></span>

<span data-ttu-id="4a11a-104">Shader Model 5 implementiert die intrinsischen Funktionen aus Shader Model 4 und niedriger (Weitere Informationen finden Sie unter [**intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) , eine umfassende Liste der unterstützten Funktionen) sowie die folgenden neuen Funktionen:</span><span class="sxs-lookup"><span data-stu-id="4a11a-104">Shader Model 5 implements the intrinsic functions from Shader Model 4 and below (see [**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) for a complete list of supported functions), as well as the following new functions:</span></span>

-   [<span data-ttu-id="4a11a-105">**Allmemorybarrier**</span><span class="sxs-lookup"><span data-stu-id="4a11a-105">**AllMemoryBarrier**</span></span>](allmemorybarrier.md)
-   [<span data-ttu-id="4a11a-106">**Allmemorybarrierwithgroupsync**</span><span class="sxs-lookup"><span data-stu-id="4a11a-106">**AllMemoryBarrierWithGroupSync**</span></span>](allmemorybarrierwithgroupsync.md)
-   [<span data-ttu-id="4a11a-107">**AsDouble**</span><span class="sxs-lookup"><span data-stu-id="4a11a-107">**asdouble**</span></span>](asdouble.md)
-   [<span data-ttu-id="4a11a-108">**asuint**</span><span class="sxs-lookup"><span data-stu-id="4a11a-108">**asuint**</span></span>](asuint.md)
-   [<span data-ttu-id="4a11a-109">**countbits**</span><span class="sxs-lookup"><span data-stu-id="4a11a-109">**countbits**</span></span>](countbits.md)
-   [<span data-ttu-id="4a11a-110">**DDX \_ grob**</span><span class="sxs-lookup"><span data-stu-id="4a11a-110">**ddx\_coarse**</span></span>](ddx-coarse.md)
-   [<span data-ttu-id="4a11a-111">**\_grobe grobe**</span><span class="sxs-lookup"><span data-stu-id="4a11a-111">**ddy\_coarse**</span></span>](ddy-coarse.md)
-   [<span data-ttu-id="4a11a-112">**Devicememorybarrier**</span><span class="sxs-lookup"><span data-stu-id="4a11a-112">**DeviceMemoryBarrier**</span></span>](devicememorybarrier.md)
-   [<span data-ttu-id="4a11a-113">**Devicememorybarrierwithgroupsync**</span><span class="sxs-lookup"><span data-stu-id="4a11a-113">**DeviceMemoryBarrierWithGroupSync**</span></span>](devicememorybarrierwithgroupsync.md)
-   [<span data-ttu-id="4a11a-114">**Evaluateattributeatcentroid**</span><span class="sxs-lookup"><span data-stu-id="4a11a-114">**EvaluateAttributeAtCentroid**</span></span>](evaluateattributeatcentroid.md)
-   [<span data-ttu-id="4a11a-115">**Evaluateattributeatsample**</span><span class="sxs-lookup"><span data-stu-id="4a11a-115">**EvaluateAttributeAtSample**</span></span>](evaluateattributeatsample.md)
-   [<span data-ttu-id="4a11a-116">**f16tof32**</span><span class="sxs-lookup"><span data-stu-id="4a11a-116">**f16tof32**</span></span>](f16tof32.md)
-   [<span data-ttu-id="4a11a-117">**f32tof16**</span><span class="sxs-lookup"><span data-stu-id="4a11a-117">**f32tof16**</span></span>](f32tof16.md)
-   [<span data-ttu-id="4a11a-118">**firstbithigh**</span><span class="sxs-lookup"><span data-stu-id="4a11a-118">**firstbithigh**</span></span>](firstbithigh.md)
-   [<span data-ttu-id="4a11a-119">**firstbitlow**</span><span class="sxs-lookup"><span data-stu-id="4a11a-119">**firstbitlow**</span></span>](firstbitlow.md)
-   [<span data-ttu-id="4a11a-120">**FMA**</span><span class="sxs-lookup"><span data-stu-id="4a11a-120">**fma**</span></span>](dx-graphics-hlsl-fma.md)
-   [<span data-ttu-id="4a11a-121">**Groupmemorybarrier**</span><span class="sxs-lookup"><span data-stu-id="4a11a-121">**GroupMemoryBarrier**</span></span>](groupmemorybarrier.md)
-   [<span data-ttu-id="4a11a-122">**Groupmemorybarrierwithgroupsync**</span><span class="sxs-lookup"><span data-stu-id="4a11a-122">**GroupMemoryBarrierWithGroupSync**</span></span>](groupmemorybarrierwithgroupsync.md)
-   [<span data-ttu-id="4a11a-123">**Interlockedadd**</span><span class="sxs-lookup"><span data-stu-id="4a11a-123">**InterlockedAdd**</span></span>](interlockedadd.md)
-   [<span data-ttu-id="4a11a-124">**Interlockedand**</span><span class="sxs-lookup"><span data-stu-id="4a11a-124">**InterlockedAnd**</span></span>](interlockedand.md)
-   [<span data-ttu-id="4a11a-125">**InterlockedCompareExchange**</span><span class="sxs-lookup"><span data-stu-id="4a11a-125">**InterlockedCompareExchange**</span></span>](interlockedcompareexchange.md)
-   [<span data-ttu-id="4a11a-126">**Interlockedcomparestore**</span><span class="sxs-lookup"><span data-stu-id="4a11a-126">**InterlockedCompareStore**</span></span>](interlockedcomparestore.md)
-   [<span data-ttu-id="4a11a-127">**InterlockedExchange**</span><span class="sxs-lookup"><span data-stu-id="4a11a-127">**InterlockedExchange**</span></span>](interlockedexchange.md)
-   [<span data-ttu-id="4a11a-128">**Interlockedmax**</span><span class="sxs-lookup"><span data-stu-id="4a11a-128">**InterlockedMax**</span></span>](interlockedmax.md)
-   [<span data-ttu-id="4a11a-129">**Interlockedmin**</span><span class="sxs-lookup"><span data-stu-id="4a11a-129">**InterlockedMin**</span></span>](interlockedmin.md)
-   [<span data-ttu-id="4a11a-130">**Interlockedor**</span><span class="sxs-lookup"><span data-stu-id="4a11a-130">**InterlockedOr**</span></span>](interlockedor.md)
-   [<span data-ttu-id="4a11a-131">**Interlockedxor**</span><span class="sxs-lookup"><span data-stu-id="4a11a-131">**InterlockedXor**</span></span>](interlockedxor.md)
-   [<span data-ttu-id="4a11a-132">**msad4**</span><span class="sxs-lookup"><span data-stu-id="4a11a-132">**msad4**</span></span>](dx-graphics-hlsl-msad4.md)
-   [<span data-ttu-id="4a11a-133">**Process2DQuadTessFactorsAvg**</span><span class="sxs-lookup"><span data-stu-id="4a11a-133">**Process2DQuadTessFactorsAvg**</span></span>](process2dquadtessfactorsavg.md)
-   [<span data-ttu-id="4a11a-134">**Process2DQuadTessFactorsMax**</span><span class="sxs-lookup"><span data-stu-id="4a11a-134">**Process2DQuadTessFactorsMax**</span></span>](process2dquadtessfactorsmax.md)
-   [<span data-ttu-id="4a11a-135">**Process2DQuadTessFactorsMin**</span><span class="sxs-lookup"><span data-stu-id="4a11a-135">**Process2DQuadTessFactorsMin**</span></span>](process2dquadtessfactorsmin.md)
-   [<span data-ttu-id="4a11a-136">**Processisolinetess Factors**</span><span class="sxs-lookup"><span data-stu-id="4a11a-136">**ProcessIsolineTessFactors**</span></span>](processisolinetessfactors.md)
-   [<span data-ttu-id="4a11a-137">**Processquadtess Factor-savg**</span><span class="sxs-lookup"><span data-stu-id="4a11a-137">**ProcessQuadTessFactorsAvg**</span></span>](processquadtessfactorsavg.md)
-   [<span data-ttu-id="4a11a-138">**Processquadtfaktorialsmax**</span><span class="sxs-lookup"><span data-stu-id="4a11a-138">**ProcessQuadTessFactorsMax**</span></span>](processquadtessfactorsmax.md)
-   [<span data-ttu-id="4a11a-139">**Processquadtess Factor Smin**</span><span class="sxs-lookup"><span data-stu-id="4a11a-139">**ProcessQuadTessFactorsMin**</span></span>](processquadtessfactorsmin.md)
-   [<span data-ttu-id="4a11a-140">**Processtritesfactor**</span><span class="sxs-lookup"><span data-stu-id="4a11a-140">**ProcessTriTessFactorsAvg**</span></span>](processtritessfactorsavg.md)
-   [<span data-ttu-id="4a11a-141">**Processtritesfactorismax**</span><span class="sxs-lookup"><span data-stu-id="4a11a-141">**ProcessTriTessFactorsMax**</span></span>](processtritessfactorsmax.md)
-   [<span data-ttu-id="4a11a-142">**Processtritesfactor Smin**</span><span class="sxs-lookup"><span data-stu-id="4a11a-142">**ProcessTriTessFactorsMin**</span></span>](processtritessfactorsmin.md)
-   [<span data-ttu-id="4a11a-143">**rcp**</span><span class="sxs-lookup"><span data-stu-id="4a11a-143">**rcp**</span></span>](rcp.md)
-   [<span data-ttu-id="4a11a-144">**reversebits**</span><span class="sxs-lookup"><span data-stu-id="4a11a-144">**reversebits**</span></span>](reversebits.md)

## <a name="related-topics"></a><span data-ttu-id="4a11a-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4a11a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a11a-146">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="4a11a-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




