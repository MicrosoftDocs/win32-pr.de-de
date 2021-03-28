---
title: texcubelod
description: Stichproben eine cubetextur mit Mipmaps. Die Mipmap-LOD wird in t.w. angegeben.
ms.assetid: fa7b236d-2c52-42bd-9123-919541f9e675
keywords:
- texcubelod HLSL
topic_type:
- apiref
api_name:
- texCUBElod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72635211263085f03b87c2e013ea57d1b6a21464
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976840"
---
# <a name="texcubelod"></a><span data-ttu-id="c611b-105">texcubelod</span><span class="sxs-lookup"><span data-stu-id="c611b-105">texCUBElod</span></span>

<span data-ttu-id="c611b-106">Stichproben eine cubetextur mit Mipmaps.</span><span class="sxs-lookup"><span data-stu-id="c611b-106">Samples a cube texture with mipmaps.</span></span> <span data-ttu-id="c611b-107">Die Mipmap-LOD wird in t.w. angegeben.</span><span class="sxs-lookup"><span data-stu-id="c611b-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="c611b-108">Ret texcubelod (s, t)</span><span class="sxs-lookup"><span data-stu-id="c611b-108">ret texCUBElod(s, t)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="c611b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c611b-109">Parameters</span></span>



| <span data-ttu-id="c611b-110">Element</span><span class="sxs-lookup"><span data-stu-id="c611b-110">Item</span></span>                                                   | <span data-ttu-id="c611b-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c611b-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="c611b-112"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="c611b-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="c611b-113">\[im \] samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="c611b-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="c611b-114"><span id="t"></span><span id="T"></span>*Bund*</span><span class="sxs-lookup"><span data-stu-id="c611b-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="c611b-115">\[in \] der Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="c611b-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="c611b-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c611b-116">Return Value</span></span>

<span data-ttu-id="c611b-117">Der Wert der Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="c611b-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="c611b-118">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="c611b-118">Type Description</span></span>



| <span data-ttu-id="c611b-119">Name</span><span class="sxs-lookup"><span data-stu-id="c611b-119">Name</span></span> | <span data-ttu-id="c611b-120">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="c611b-120">In/Out</span></span> | [<span data-ttu-id="c611b-121">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="c611b-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="c611b-122">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="c611b-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="c611b-123">Size</span><span class="sxs-lookup"><span data-stu-id="c611b-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="c611b-124">s</span><span class="sxs-lookup"><span data-stu-id="c611b-124">s</span></span>    | <span data-ttu-id="c611b-125">in</span><span class="sxs-lookup"><span data-stu-id="c611b-125">in</span></span>     | [<span data-ttu-id="c611b-126">**Objekt**</span><span class="sxs-lookup"><span data-stu-id="c611b-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="c611b-127">samplercube</span><span class="sxs-lookup"><span data-stu-id="c611b-127">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="c611b-128">1</span><span class="sxs-lookup"><span data-stu-id="c611b-128">1</span></span>    |
| <span data-ttu-id="c611b-129">t</span><span class="sxs-lookup"><span data-stu-id="c611b-129">t</span></span>    | <span data-ttu-id="c611b-130">in</span><span class="sxs-lookup"><span data-stu-id="c611b-130">in</span></span>     | [<span data-ttu-id="c611b-131">**ve**</span><span class="sxs-lookup"><span data-stu-id="c611b-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="c611b-132">**float**</span><span class="sxs-lookup"><span data-stu-id="c611b-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c611b-133">4</span><span class="sxs-lookup"><span data-stu-id="c611b-133">4</span></span>    |
| <span data-ttu-id="c611b-134">TZI</span><span class="sxs-lookup"><span data-stu-id="c611b-134">ret</span></span>  | <span data-ttu-id="c611b-135">out</span><span class="sxs-lookup"><span data-stu-id="c611b-135">out</span></span>    | [<span data-ttu-id="c611b-136">**ve**</span><span class="sxs-lookup"><span data-stu-id="c611b-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="c611b-137">**float**</span><span class="sxs-lookup"><span data-stu-id="c611b-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c611b-138">4</span><span class="sxs-lookup"><span data-stu-id="c611b-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c611b-139">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="c611b-139">Minimum Shader Model</span></span>

<span data-ttu-id="c611b-140">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c611b-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c611b-141">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="c611b-141">Shader Model</span></span>                                              | <span data-ttu-id="c611b-142">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="c611b-142">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="c611b-143">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="c611b-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c611b-144">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="c611b-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="c611b-145">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c611b-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c611b-146">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="c611b-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="c611b-147">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c611b-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c611b-148">nein</span><span class="sxs-lookup"><span data-stu-id="c611b-148">no</span></span>                      |
| [<span data-ttu-id="c611b-149">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c611b-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c611b-150">Nein</span><span class="sxs-lookup"><span data-stu-id="c611b-150">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="c611b-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c611b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c611b-152">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="c611b-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

