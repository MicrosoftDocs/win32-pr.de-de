---
title: tex1D (HLSL-Referenz)
description: Stichproben eine 1D-Textur.
ms.assetid: 587be0fd-af12-4bf0-862b-84988435e90e
keywords:
- tex1D HLSL
topic_type:
- apiref
api_name:
- tex1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dec5cc8a35b18c35076f99443ad3c1166fcf410
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728201"
---
# <a name="tex1d-hlsl-reference"></a><span data-ttu-id="994f2-104">tex1D (HLSL-Referenz)</span><span class="sxs-lookup"><span data-stu-id="994f2-104">tex1D (HLSL reference)</span></span>

<span data-ttu-id="994f2-105">Stichproben eine 1D-Textur.</span><span class="sxs-lookup"><span data-stu-id="994f2-105">Samples a 1D texture.</span></span>



| <span data-ttu-id="994f2-106">Ret tex1D (s, t)</span><span class="sxs-lookup"><span data-stu-id="994f2-106">ret tex1D(s, t)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="994f2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="994f2-107">Parameters</span></span>



| <span data-ttu-id="994f2-108">Element</span><span class="sxs-lookup"><span data-stu-id="994f2-108">Item</span></span>                                                   | <span data-ttu-id="994f2-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="994f2-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="994f2-110"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="994f2-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="994f2-111">\[im \] samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="994f2-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="994f2-112"><span id="t"></span><span id="T"></span>*Bund*</span><span class="sxs-lookup"><span data-stu-id="994f2-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="994f2-113">\[in \] der Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="994f2-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="994f2-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="994f2-114">Return Value</span></span>

<span data-ttu-id="994f2-115">Der Wert der Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="994f2-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="994f2-116">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="994f2-116">Type Description</span></span>



| <span data-ttu-id="994f2-117">Name</span><span class="sxs-lookup"><span data-stu-id="994f2-117">Name</span></span> | <span data-ttu-id="994f2-118">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="994f2-118">In/Out</span></span> | [<span data-ttu-id="994f2-119">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="994f2-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="994f2-120">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="994f2-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="994f2-121">Size</span><span class="sxs-lookup"><span data-stu-id="994f2-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="994f2-122">s</span><span class="sxs-lookup"><span data-stu-id="994f2-122">s</span></span>    | <span data-ttu-id="994f2-123">in</span><span class="sxs-lookup"><span data-stu-id="994f2-123">in</span></span>     | [<span data-ttu-id="994f2-124">**Objekt**</span><span class="sxs-lookup"><span data-stu-id="994f2-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="994f2-125">sampler1D</span><span class="sxs-lookup"><span data-stu-id="994f2-125">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="994f2-126">1</span><span class="sxs-lookup"><span data-stu-id="994f2-126">1</span></span>    |
| <span data-ttu-id="994f2-127">t</span><span class="sxs-lookup"><span data-stu-id="994f2-127">t</span></span>    | <span data-ttu-id="994f2-128">in</span><span class="sxs-lookup"><span data-stu-id="994f2-128">in</span></span>     | [<span data-ttu-id="994f2-129">**Skalar**</span><span class="sxs-lookup"><span data-stu-id="994f2-129">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="994f2-130">**float**</span><span class="sxs-lookup"><span data-stu-id="994f2-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="994f2-131">1</span><span class="sxs-lookup"><span data-stu-id="994f2-131">1</span></span>    |
| <span data-ttu-id="994f2-132">TZI</span><span class="sxs-lookup"><span data-stu-id="994f2-132">ret</span></span>  | <span data-ttu-id="994f2-133">out</span><span class="sxs-lookup"><span data-stu-id="994f2-133">out</span></span>    | [<span data-ttu-id="994f2-134">**ve**</span><span class="sxs-lookup"><span data-stu-id="994f2-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="994f2-135">**float**</span><span class="sxs-lookup"><span data-stu-id="994f2-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="994f2-136">4</span><span class="sxs-lookup"><span data-stu-id="994f2-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="994f2-137">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="994f2-137">Minimum Shader Model</span></span>

<span data-ttu-id="994f2-138">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="994f2-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="994f2-139">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="994f2-139">Shader Model</span></span>                                              | <span data-ttu-id="994f2-140">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="994f2-140">Supported</span></span>                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="994f2-141">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="994f2-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="994f2-142">Ja (nur Pixel-Shader), aber Sie müssen beim Kompilieren die [Legacy Kompilierungs Option](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) verwenden.</span><span class="sxs-lookup"><span data-stu-id="994f2-142">yes (pixel shader only), but you must use the [legacy compile option](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) when compiling.</span></span> |
| [<span data-ttu-id="994f2-143">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="994f2-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="994f2-144">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="994f2-144">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="994f2-145">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="994f2-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="994f2-146">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="994f2-146">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="994f2-147">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="994f2-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="994f2-148">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="994f2-148">yes (pixel shader only)</span></span>                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="994f2-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="994f2-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="994f2-150">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="994f2-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

