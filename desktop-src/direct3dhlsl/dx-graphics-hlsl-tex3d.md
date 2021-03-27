---
title: tex3D (HLSL-Referenz)
description: Stichproben eine 3D-Textur.
ms.assetid: 713eec24-bdf5-456e-98da-30e2c9d7e808
keywords:
- tex3D HLSL
topic_type:
- apiref
api_name:
- tex3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3a071d00dedabdff02bae302c71aa8ecece4ba2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729520"
---
# <a name="tex3d-hlsl-reference"></a><span data-ttu-id="0f3a3-104">tex3D (HLSL-Referenz)</span><span class="sxs-lookup"><span data-stu-id="0f3a3-104">tex3D (HLSL reference)</span></span>

<span data-ttu-id="0f3a3-105">Stichproben eine 3D-Textur.</span><span class="sxs-lookup"><span data-stu-id="0f3a3-105">Samples a 3D texture.</span></span>



| <span data-ttu-id="0f3a3-106">Ret tex3D (s, t)</span><span class="sxs-lookup"><span data-stu-id="0f3a3-106">ret tex3D(s, t)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="0f3a3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f3a3-107">Parameters</span></span>



| <span data-ttu-id="0f3a3-108">Element</span><span class="sxs-lookup"><span data-stu-id="0f3a3-108">Item</span></span>                                                   | <span data-ttu-id="0f3a3-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f3a3-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="0f3a3-110"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="0f3a3-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="0f3a3-111">\[im \] samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="0f3a3-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="0f3a3-112"><span id="t"></span><span id="T"></span>*Bund*</span><span class="sxs-lookup"><span data-stu-id="0f3a3-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="0f3a3-113">\[in \] der Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="0f3a3-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="0f3a3-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f3a3-114">Return Value</span></span>

<span data-ttu-id="0f3a3-115">Der Wert der Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="0f3a3-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="0f3a3-116">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="0f3a3-116">Type Description</span></span>



| <span data-ttu-id="0f3a3-117">Name</span><span class="sxs-lookup"><span data-stu-id="0f3a3-117">Name</span></span> | <span data-ttu-id="0f3a3-118">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="0f3a3-118">In/Out</span></span> | [<span data-ttu-id="0f3a3-119">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="0f3a3-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="0f3a3-120">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="0f3a3-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="0f3a3-121">Size</span><span class="sxs-lookup"><span data-stu-id="0f3a3-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="0f3a3-122">s</span><span class="sxs-lookup"><span data-stu-id="0f3a3-122">s</span></span>    | <span data-ttu-id="0f3a3-123">in</span><span class="sxs-lookup"><span data-stu-id="0f3a3-123">in</span></span>     | [<span data-ttu-id="0f3a3-124">**Objekt**</span><span class="sxs-lookup"><span data-stu-id="0f3a3-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0f3a3-125">sampler3D</span><span class="sxs-lookup"><span data-stu-id="0f3a3-125">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="0f3a3-126">1</span><span class="sxs-lookup"><span data-stu-id="0f3a3-126">1</span></span>    |
| <span data-ttu-id="0f3a3-127">t</span><span class="sxs-lookup"><span data-stu-id="0f3a3-127">t</span></span>    | <span data-ttu-id="0f3a3-128">in</span><span class="sxs-lookup"><span data-stu-id="0f3a3-128">in</span></span>     | [<span data-ttu-id="0f3a3-129">**ve**</span><span class="sxs-lookup"><span data-stu-id="0f3a3-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0f3a3-130">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="0f3a3-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0f3a3-131">3</span><span class="sxs-lookup"><span data-stu-id="0f3a3-131">3</span></span>    |
| <span data-ttu-id="0f3a3-132">TZI</span><span class="sxs-lookup"><span data-stu-id="0f3a3-132">ret</span></span>  | <span data-ttu-id="0f3a3-133">out</span><span class="sxs-lookup"><span data-stu-id="0f3a3-133">out</span></span>    | [<span data-ttu-id="0f3a3-134">**ve**</span><span class="sxs-lookup"><span data-stu-id="0f3a3-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0f3a3-135">**float**</span><span class="sxs-lookup"><span data-stu-id="0f3a3-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0f3a3-136">4</span><span class="sxs-lookup"><span data-stu-id="0f3a3-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0f3a3-137">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="0f3a3-137">Minimum Shader Model</span></span>

<span data-ttu-id="0f3a3-138">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0f3a3-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0f3a3-139">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="0f3a3-139">Shader Model</span></span>                                              | <span data-ttu-id="0f3a3-140">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="0f3a3-140">Supported</span></span>                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f3a3-141">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="0f3a3-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0f3a3-142">Ja (nur Pixel-Shader), aber Sie müssen beim Kompilieren die [Legacy Kompilierungs Option](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) verwenden.</span><span class="sxs-lookup"><span data-stu-id="0f3a3-142">yes (pixel shader only), but you must use the [legacy compile option](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) when compiling.</span></span> |
| [<span data-ttu-id="0f3a3-143">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f3a3-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0f3a3-144">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="0f3a3-144">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="0f3a3-145">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f3a3-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0f3a3-146">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="0f3a3-146">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="0f3a3-147">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f3a3-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0f3a3-148">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="0f3a3-148">yes (pixel shader only)</span></span>                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="0f3a3-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0f3a3-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f3a3-150">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="0f3a3-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

