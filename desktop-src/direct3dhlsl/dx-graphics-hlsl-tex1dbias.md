---
title: tex1Dbias
description: Abtastungen einer 1D-Textur nach dem Dateityp der MIP-Ebene nach t.w.
ms.assetid: 2619ae23-e4b2-4699-b2ac-5ee711f9569a
keywords:
- tex1Dbias HLSL
topic_type:
- apiref
api_name:
- tex1Dbias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0328b9328a1406177fa26bd566c0fbf7d384db63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101819"
---
# <a name="tex1dbias"></a><span data-ttu-id="6ad37-104">tex1Dbias</span><span class="sxs-lookup"><span data-stu-id="6ad37-104">tex1Dbias</span></span>

<span data-ttu-id="6ad37-105">Abtastungen einer 1D-Textur nach dem Dateityp der MIP-Ebene nach t.w.</span><span class="sxs-lookup"><span data-stu-id="6ad37-105">Samples a 1D texture after biasing the mip level by t.w.</span></span>



| <span data-ttu-id="6ad37-106">Ret tex1Dbias (s, t)</span><span class="sxs-lookup"><span data-stu-id="6ad37-106">ret tex1Dbias(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="6ad37-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ad37-107">Parameters</span></span>



| <span data-ttu-id="6ad37-108">Element</span><span class="sxs-lookup"><span data-stu-id="6ad37-108">Item</span></span>                                                   | <span data-ttu-id="6ad37-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ad37-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="6ad37-110"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="6ad37-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="6ad37-111">\[im \] samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="6ad37-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="6ad37-112"><span id="t"></span><span id="T"></span>*Bund*</span><span class="sxs-lookup"><span data-stu-id="6ad37-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="6ad37-113">\[in \] der Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="6ad37-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="6ad37-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ad37-114">Return Value</span></span>

<span data-ttu-id="6ad37-115">Der Wert der Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="6ad37-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="6ad37-116">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="6ad37-116">Type Description</span></span>



| <span data-ttu-id="6ad37-117">Name</span><span class="sxs-lookup"><span data-stu-id="6ad37-117">Name</span></span> | <span data-ttu-id="6ad37-118">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="6ad37-118">In/Out</span></span> | [<span data-ttu-id="6ad37-119">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="6ad37-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="6ad37-120">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="6ad37-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="6ad37-121">Size</span><span class="sxs-lookup"><span data-stu-id="6ad37-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="6ad37-122">s</span><span class="sxs-lookup"><span data-stu-id="6ad37-122">s</span></span>    | <span data-ttu-id="6ad37-123">in</span><span class="sxs-lookup"><span data-stu-id="6ad37-123">in</span></span>     | [<span data-ttu-id="6ad37-124">**Objekt**</span><span class="sxs-lookup"><span data-stu-id="6ad37-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="6ad37-125">sampler1D</span><span class="sxs-lookup"><span data-stu-id="6ad37-125">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="6ad37-126">1</span><span class="sxs-lookup"><span data-stu-id="6ad37-126">1</span></span>    |
| <span data-ttu-id="6ad37-127">t</span><span class="sxs-lookup"><span data-stu-id="6ad37-127">t</span></span>    | <span data-ttu-id="6ad37-128">in</span><span class="sxs-lookup"><span data-stu-id="6ad37-128">in</span></span>     | [<span data-ttu-id="6ad37-129">**ve**</span><span class="sxs-lookup"><span data-stu-id="6ad37-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="6ad37-130">**float**</span><span class="sxs-lookup"><span data-stu-id="6ad37-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6ad37-131">4</span><span class="sxs-lookup"><span data-stu-id="6ad37-131">4</span></span>    |
| <span data-ttu-id="6ad37-132">TZI</span><span class="sxs-lookup"><span data-stu-id="6ad37-132">ret</span></span>  | <span data-ttu-id="6ad37-133">out</span><span class="sxs-lookup"><span data-stu-id="6ad37-133">out</span></span>    | [<span data-ttu-id="6ad37-134">**ve**</span><span class="sxs-lookup"><span data-stu-id="6ad37-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="6ad37-135">**float**</span><span class="sxs-lookup"><span data-stu-id="6ad37-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6ad37-136">4</span><span class="sxs-lookup"><span data-stu-id="6ad37-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6ad37-137">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="6ad37-137">Minimum Shader Model</span></span>

<span data-ttu-id="6ad37-138">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6ad37-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6ad37-139">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="6ad37-139">Shader Model</span></span>                                              | <span data-ttu-id="6ad37-140">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="6ad37-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="6ad37-141">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="6ad37-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6ad37-142">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="6ad37-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="6ad37-143">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6ad37-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6ad37-144">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="6ad37-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="6ad37-145">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6ad37-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6ad37-146">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="6ad37-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="6ad37-147">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6ad37-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6ad37-148">Nein</span><span class="sxs-lookup"><span data-stu-id="6ad37-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="6ad37-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ad37-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ad37-150">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="6ad37-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

