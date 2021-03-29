---
title: tex3Dlod
description: Stichproben eine 3D-Textur mit Mipmaps. Die Mipmap-LOD wird in t.w. angegeben.
ms.assetid: 9bdd8fa1-8c02-4765-8f4d-61ceb532354e
keywords:
- tex3Dlod HLSL
topic_type:
- apiref
api_name:
- tex3Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bc25af449f7f32e94d4ca344bf5ef3a4d09b376c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976665"
---
# <a name="tex3dlod"></a><span data-ttu-id="fd857-105">tex3Dlod</span><span class="sxs-lookup"><span data-stu-id="fd857-105">tex3Dlod</span></span>

<span data-ttu-id="fd857-106">Stichproben eine 3D-Textur mit Mipmaps.</span><span class="sxs-lookup"><span data-stu-id="fd857-106">Samples a 3D texture with mipmaps.</span></span> <span data-ttu-id="fd857-107">Die Mipmap-LOD wird in t.w. angegeben.</span><span class="sxs-lookup"><span data-stu-id="fd857-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="fd857-108">Ret tex3Dlod (s, t)</span><span class="sxs-lookup"><span data-stu-id="fd857-108">ret tex3Dlod(s, t)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="fd857-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd857-109">Parameters</span></span>



| <span data-ttu-id="fd857-110">Element</span><span class="sxs-lookup"><span data-stu-id="fd857-110">Item</span></span>                                                   | <span data-ttu-id="fd857-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd857-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="fd857-112"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="fd857-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="fd857-113">\[im \] samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="fd857-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="fd857-114"><span id="t"></span><span id="T"></span>*Bund*</span><span class="sxs-lookup"><span data-stu-id="fd857-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="fd857-115">\[in \] der Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="fd857-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="fd857-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd857-116">Return Value</span></span>

<span data-ttu-id="fd857-117">Der Wert der Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="fd857-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="fd857-118">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="fd857-118">Type Description</span></span>



| <span data-ttu-id="fd857-119">Name</span><span class="sxs-lookup"><span data-stu-id="fd857-119">Name</span></span> | <span data-ttu-id="fd857-120">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="fd857-120">In/Out</span></span> | [<span data-ttu-id="fd857-121">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="fd857-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="fd857-122">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="fd857-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="fd857-123">Size</span><span class="sxs-lookup"><span data-stu-id="fd857-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="fd857-124">s</span><span class="sxs-lookup"><span data-stu-id="fd857-124">s</span></span>    | <span data-ttu-id="fd857-125">in</span><span class="sxs-lookup"><span data-stu-id="fd857-125">in</span></span>     | [<span data-ttu-id="fd857-126">**Objekt**</span><span class="sxs-lookup"><span data-stu-id="fd857-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="fd857-127">sampler3D</span><span class="sxs-lookup"><span data-stu-id="fd857-127">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="fd857-128">1</span><span class="sxs-lookup"><span data-stu-id="fd857-128">1</span></span>    |
| <span data-ttu-id="fd857-129">t</span><span class="sxs-lookup"><span data-stu-id="fd857-129">t</span></span>    | <span data-ttu-id="fd857-130">in</span><span class="sxs-lookup"><span data-stu-id="fd857-130">in</span></span>     | [<span data-ttu-id="fd857-131">**ve**</span><span class="sxs-lookup"><span data-stu-id="fd857-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="fd857-132">**float**</span><span class="sxs-lookup"><span data-stu-id="fd857-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="fd857-133">4</span><span class="sxs-lookup"><span data-stu-id="fd857-133">4</span></span>    |
| <span data-ttu-id="fd857-134">TZI</span><span class="sxs-lookup"><span data-stu-id="fd857-134">ret</span></span>  | <span data-ttu-id="fd857-135">out</span><span class="sxs-lookup"><span data-stu-id="fd857-135">out</span></span>    | [<span data-ttu-id="fd857-136">**ve**</span><span class="sxs-lookup"><span data-stu-id="fd857-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="fd857-137">**float**</span><span class="sxs-lookup"><span data-stu-id="fd857-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="fd857-138">4</span><span class="sxs-lookup"><span data-stu-id="fd857-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fd857-139">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="fd857-139">Minimum Shader Model</span></span>

<span data-ttu-id="fd857-140">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fd857-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fd857-141">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="fd857-141">Shader Model</span></span>                                              | <span data-ttu-id="fd857-142">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="fd857-142">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="fd857-143">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="fd857-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fd857-144">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="fd857-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="fd857-145">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fd857-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fd857-146">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="fd857-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="fd857-147">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fd857-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fd857-148">nein</span><span class="sxs-lookup"><span data-stu-id="fd857-148">no</span></span>                      |
| [<span data-ttu-id="fd857-149">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fd857-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fd857-150">Nein</span><span class="sxs-lookup"><span data-stu-id="fd857-150">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="fd857-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd857-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd857-152">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="fd857-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

