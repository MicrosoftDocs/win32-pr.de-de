---
title: texcubebias
description: Stichprobe einer Cube-Textur nach dem Dateityp der MIP-Ebene nach t.w.
ms.assetid: dad27cff-6b10-45db-b70f-c4ad78c64e76
keywords:
- texcubebias HLSL
topic_type:
- apiref
api_name:
- texCUBEbias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0129c20db1da320e9cb85aacfc4490124be28f8a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101723"
---
# <a name="texcubebias"></a><span data-ttu-id="eb7ba-104">texcubebias</span><span class="sxs-lookup"><span data-stu-id="eb7ba-104">texCUBEbias</span></span>

<span data-ttu-id="eb7ba-105">Stichprobe einer Cube-Textur nach dem Dateityp der MIP-Ebene nach t.w.</span><span class="sxs-lookup"><span data-stu-id="eb7ba-105">Samples a cube texture after biasing the mip level by t.w.</span></span>



| <span data-ttu-id="eb7ba-106">Ret texcubebias (s, t)</span><span class="sxs-lookup"><span data-stu-id="eb7ba-106">ret texCUBEbias(s, t)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="eb7ba-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb7ba-107">Parameters</span></span>



| <span data-ttu-id="eb7ba-108">Element</span><span class="sxs-lookup"><span data-stu-id="eb7ba-108">Item</span></span>                                                   | <span data-ttu-id="eb7ba-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb7ba-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="eb7ba-110"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="eb7ba-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="eb7ba-111">\[im \] samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="eb7ba-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="eb7ba-112"><span id="t"></span><span id="T"></span>*Bund*</span><span class="sxs-lookup"><span data-stu-id="eb7ba-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="eb7ba-113">\[in \] der Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="eb7ba-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="eb7ba-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb7ba-114">Return Value</span></span>

<span data-ttu-id="eb7ba-115">Der Wert der Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="eb7ba-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="eb7ba-116">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="eb7ba-116">Type Description</span></span>



| <span data-ttu-id="eb7ba-117">Name</span><span class="sxs-lookup"><span data-stu-id="eb7ba-117">Name</span></span> | <span data-ttu-id="eb7ba-118">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="eb7ba-118">In/Out</span></span> | [<span data-ttu-id="eb7ba-119">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="eb7ba-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="eb7ba-120">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="eb7ba-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="eb7ba-121">Size</span><span class="sxs-lookup"><span data-stu-id="eb7ba-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="eb7ba-122">s</span><span class="sxs-lookup"><span data-stu-id="eb7ba-122">s</span></span>    | <span data-ttu-id="eb7ba-123">in</span><span class="sxs-lookup"><span data-stu-id="eb7ba-123">in</span></span>     | [<span data-ttu-id="eb7ba-124">**Objekt**</span><span class="sxs-lookup"><span data-stu-id="eb7ba-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="eb7ba-125">samplercube</span><span class="sxs-lookup"><span data-stu-id="eb7ba-125">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="eb7ba-126">1</span><span class="sxs-lookup"><span data-stu-id="eb7ba-126">1</span></span>    |
| <span data-ttu-id="eb7ba-127">t</span><span class="sxs-lookup"><span data-stu-id="eb7ba-127">t</span></span>    | <span data-ttu-id="eb7ba-128">in</span><span class="sxs-lookup"><span data-stu-id="eb7ba-128">in</span></span>     | [<span data-ttu-id="eb7ba-129">**ve**</span><span class="sxs-lookup"><span data-stu-id="eb7ba-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="eb7ba-130">**float**</span><span class="sxs-lookup"><span data-stu-id="eb7ba-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="eb7ba-131">4</span><span class="sxs-lookup"><span data-stu-id="eb7ba-131">4</span></span>    |
| <span data-ttu-id="eb7ba-132">TZI</span><span class="sxs-lookup"><span data-stu-id="eb7ba-132">ret</span></span>  | <span data-ttu-id="eb7ba-133">out</span><span class="sxs-lookup"><span data-stu-id="eb7ba-133">out</span></span>    | [<span data-ttu-id="eb7ba-134">**ve**</span><span class="sxs-lookup"><span data-stu-id="eb7ba-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="eb7ba-135">**float**</span><span class="sxs-lookup"><span data-stu-id="eb7ba-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="eb7ba-136">4</span><span class="sxs-lookup"><span data-stu-id="eb7ba-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="eb7ba-137">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="eb7ba-137">Minimum Shader Model</span></span>

<span data-ttu-id="eb7ba-138">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eb7ba-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="eb7ba-139">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="eb7ba-139">Shader Model</span></span>                                              | <span data-ttu-id="eb7ba-140">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="eb7ba-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="eb7ba-141">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="eb7ba-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="eb7ba-142">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="eb7ba-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="eb7ba-143">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eb7ba-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="eb7ba-144">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="eb7ba-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="eb7ba-145">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eb7ba-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="eb7ba-146">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="eb7ba-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="eb7ba-147">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eb7ba-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="eb7ba-148">Nein</span><span class="sxs-lookup"><span data-stu-id="eb7ba-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="eb7ba-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb7ba-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb7ba-150">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="eb7ba-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

