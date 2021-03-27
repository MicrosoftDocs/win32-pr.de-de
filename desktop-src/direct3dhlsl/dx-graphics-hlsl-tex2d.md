---
title: tex2D (HLSL-Referenz)
description: Stichproben eine 2D-Textur.
ms.assetid: 9f4cbca8-c3de-42ed-89d9-5e86e47d12e5
keywords:
- tex2D HLSL
topic_type:
- apiref
api_name:
- tex2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ac8edb3bc4bb84c2259e193abda90dc32ef385d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729521"
---
# <a name="tex2d-hlsl-reference"></a><span data-ttu-id="9351f-104">tex2D (HLSL-Referenz)</span><span class="sxs-lookup"><span data-stu-id="9351f-104">tex2D (HLSL reference)</span></span>

<span data-ttu-id="9351f-105">Stichproben eine 2D-Textur.</span><span class="sxs-lookup"><span data-stu-id="9351f-105">Samples a 2D texture.</span></span>



| <span data-ttu-id="9351f-106">Ret tex2D (s, t)</span><span class="sxs-lookup"><span data-stu-id="9351f-106">ret tex2D(s, t)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="9351f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9351f-107">Parameters</span></span>



| <span data-ttu-id="9351f-108">Element</span><span class="sxs-lookup"><span data-stu-id="9351f-108">Item</span></span>                                                   | <span data-ttu-id="9351f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9351f-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="9351f-110"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="9351f-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="9351f-111">\[im \] samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="9351f-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="9351f-112"><span id="t"></span><span id="T"></span>*Bund*</span><span class="sxs-lookup"><span data-stu-id="9351f-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="9351f-113">\[in \] der Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="9351f-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="9351f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9351f-114">Return Value</span></span>

<span data-ttu-id="9351f-115">Der Wert der Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="9351f-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="9351f-116">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="9351f-116">Type Description</span></span>



| <span data-ttu-id="9351f-117">Name</span><span class="sxs-lookup"><span data-stu-id="9351f-117">Name</span></span> | <span data-ttu-id="9351f-118">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="9351f-118">In/Out</span></span> | [<span data-ttu-id="9351f-119">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="9351f-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="9351f-120">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="9351f-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="9351f-121">Size</span><span class="sxs-lookup"><span data-stu-id="9351f-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="9351f-122">s</span><span class="sxs-lookup"><span data-stu-id="9351f-122">s</span></span>    | <span data-ttu-id="9351f-123">in</span><span class="sxs-lookup"><span data-stu-id="9351f-123">in</span></span>     | [<span data-ttu-id="9351f-124">**Objekt**</span><span class="sxs-lookup"><span data-stu-id="9351f-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="9351f-125">sampler2D</span><span class="sxs-lookup"><span data-stu-id="9351f-125">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="9351f-126">1</span><span class="sxs-lookup"><span data-stu-id="9351f-126">1</span></span>    |
| <span data-ttu-id="9351f-127">t</span><span class="sxs-lookup"><span data-stu-id="9351f-127">t</span></span>    | <span data-ttu-id="9351f-128">in</span><span class="sxs-lookup"><span data-stu-id="9351f-128">in</span></span>     | [<span data-ttu-id="9351f-129">**ve**</span><span class="sxs-lookup"><span data-stu-id="9351f-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="9351f-130">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="9351f-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9351f-131">2</span><span class="sxs-lookup"><span data-stu-id="9351f-131">2</span></span>    |
| <span data-ttu-id="9351f-132">TZI</span><span class="sxs-lookup"><span data-stu-id="9351f-132">ret</span></span>  | <span data-ttu-id="9351f-133">out</span><span class="sxs-lookup"><span data-stu-id="9351f-133">out</span></span>    | [<span data-ttu-id="9351f-134">**ve**</span><span class="sxs-lookup"><span data-stu-id="9351f-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="9351f-135">**float**</span><span class="sxs-lookup"><span data-stu-id="9351f-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9351f-136">4</span><span class="sxs-lookup"><span data-stu-id="9351f-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9351f-137">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="9351f-137">Minimum Shader Model</span></span>

<span data-ttu-id="9351f-138">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9351f-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9351f-139">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="9351f-139">Shader Model</span></span>                                              | <span data-ttu-id="9351f-140">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="9351f-140">Supported</span></span>                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9351f-141">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="9351f-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9351f-142">Ja (nur Pixel-Shader), aber Sie müssen beim Kompilieren die [Legacy Kompilierungs Option](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) verwenden.</span><span class="sxs-lookup"><span data-stu-id="9351f-142">yes (pixel shader only), but you must use the [legacy compile option](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) when compiling.</span></span> |
| [<span data-ttu-id="9351f-143">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9351f-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9351f-144">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="9351f-144">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="9351f-145">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9351f-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9351f-146">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="9351f-146">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="9351f-147">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9351f-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9351f-148">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="9351f-148">yes (pixel shader only)</span></span>                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="9351f-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9351f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9351f-150">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="9351f-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

