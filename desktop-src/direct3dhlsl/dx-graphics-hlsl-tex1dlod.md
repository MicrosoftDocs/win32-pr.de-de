---
title: tex1Dlod
description: Stichproben eine 1D-Textur mit Mipmaps. Die Mipmap-LOD wird in t.w. angegeben.
ms.assetid: f1700ee6-2f79-4b8b-ad34-30561f319356
keywords:
- tex1Dlod HLSL
topic_type:
- apiref
api_name:
- tex1Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ca6379448290d027bba8a8b62f80cac39c84f25
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729160"
---
# <a name="tex1dlod"></a><span data-ttu-id="8f7ed-105">tex1Dlod</span><span class="sxs-lookup"><span data-stu-id="8f7ed-105">tex1Dlod</span></span>

<span data-ttu-id="8f7ed-106">Stichproben eine 1D-Textur mit Mipmaps.</span><span class="sxs-lookup"><span data-stu-id="8f7ed-106">Samples a 1D texture with mipmaps.</span></span> <span data-ttu-id="8f7ed-107">Die Mipmap-LOD wird in t.w. angegeben.</span><span class="sxs-lookup"><span data-stu-id="8f7ed-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="8f7ed-108">Ret tex1Dlod (s, t)</span><span class="sxs-lookup"><span data-stu-id="8f7ed-108">ret tex1Dlod(s, t)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="8f7ed-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f7ed-109">Parameters</span></span>



| <span data-ttu-id="8f7ed-110">Element</span><span class="sxs-lookup"><span data-stu-id="8f7ed-110">Item</span></span>                                                   | <span data-ttu-id="8f7ed-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f7ed-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="8f7ed-112"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="8f7ed-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="8f7ed-113">\[im \] samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="8f7ed-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="8f7ed-114"><span id="t"></span><span id="T"></span>*Bund*</span><span class="sxs-lookup"><span data-stu-id="8f7ed-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="8f7ed-115">\[in \] der Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="8f7ed-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="8f7ed-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f7ed-116">Return Value</span></span>

<span data-ttu-id="8f7ed-117">Der Wert der Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="8f7ed-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="8f7ed-118">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="8f7ed-118">Type Description</span></span>



| <span data-ttu-id="8f7ed-119">Name</span><span class="sxs-lookup"><span data-stu-id="8f7ed-119">Name</span></span> | <span data-ttu-id="8f7ed-120">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="8f7ed-120">In/Out</span></span> | [<span data-ttu-id="8f7ed-121">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="8f7ed-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="8f7ed-122">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="8f7ed-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="8f7ed-123">Size</span><span class="sxs-lookup"><span data-stu-id="8f7ed-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="8f7ed-124">s</span><span class="sxs-lookup"><span data-stu-id="8f7ed-124">s</span></span>    | <span data-ttu-id="8f7ed-125">in</span><span class="sxs-lookup"><span data-stu-id="8f7ed-125">in</span></span>     | [<span data-ttu-id="8f7ed-126">**Objekt**</span><span class="sxs-lookup"><span data-stu-id="8f7ed-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8f7ed-127">sampler1D</span><span class="sxs-lookup"><span data-stu-id="8f7ed-127">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="8f7ed-128">1</span><span class="sxs-lookup"><span data-stu-id="8f7ed-128">1</span></span>    |
| <span data-ttu-id="8f7ed-129">t</span><span class="sxs-lookup"><span data-stu-id="8f7ed-129">t</span></span>    | <span data-ttu-id="8f7ed-130">in</span><span class="sxs-lookup"><span data-stu-id="8f7ed-130">in</span></span>     | [<span data-ttu-id="8f7ed-131">**ve**</span><span class="sxs-lookup"><span data-stu-id="8f7ed-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8f7ed-132">**float**</span><span class="sxs-lookup"><span data-stu-id="8f7ed-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8f7ed-133">4</span><span class="sxs-lookup"><span data-stu-id="8f7ed-133">4</span></span>    |
| <span data-ttu-id="8f7ed-134">TZI</span><span class="sxs-lookup"><span data-stu-id="8f7ed-134">ret</span></span>  | <span data-ttu-id="8f7ed-135">out</span><span class="sxs-lookup"><span data-stu-id="8f7ed-135">out</span></span>    | [<span data-ttu-id="8f7ed-136">**ve**</span><span class="sxs-lookup"><span data-stu-id="8f7ed-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8f7ed-137">**float**</span><span class="sxs-lookup"><span data-stu-id="8f7ed-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8f7ed-138">4</span><span class="sxs-lookup"><span data-stu-id="8f7ed-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8f7ed-139">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="8f7ed-139">Minimum Shader Model</span></span>

<span data-ttu-id="8f7ed-140">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8f7ed-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8f7ed-141">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="8f7ed-141">Shader Model</span></span>                                              | <span data-ttu-id="8f7ed-142">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="8f7ed-142">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="8f7ed-143">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="8f7ed-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8f7ed-144">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="8f7ed-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="8f7ed-145">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8f7ed-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8f7ed-146">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="8f7ed-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="8f7ed-147">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8f7ed-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8f7ed-148">nein</span><span class="sxs-lookup"><span data-stu-id="8f7ed-148">no</span></span>                      |
| [<span data-ttu-id="8f7ed-149">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8f7ed-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8f7ed-150">Nein</span><span class="sxs-lookup"><span data-stu-id="8f7ed-150">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="8f7ed-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f7ed-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f7ed-152">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="8f7ed-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

