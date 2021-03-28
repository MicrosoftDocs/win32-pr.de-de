---
title: tex1Dproj
description: Stichproben eine 1D-Textur mithilfe einer projektives Teilung. die Textur Koordinate wird durch t. w dividiert, bevor die Suche stattfindet.
ms.assetid: 7cfe996d-3967-40da-b0e7-e03938478594
keywords:
- tex1Dproj HLSL
topic_type:
- apiref
api_name:
- tex1Dproj
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34fc1c019ab5479fe8a23446c94073e19ca68de7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976784"
---
# <a name="tex1dproj"></a><span data-ttu-id="ccb6c-104">tex1Dproj</span><span class="sxs-lookup"><span data-stu-id="ccb6c-104">tex1Dproj</span></span>

<span data-ttu-id="ccb6c-105">Stichproben eine 1D-Textur mithilfe einer projektives Teilung. die Textur Koordinate wird durch t. w dividiert, bevor die Suche stattfindet.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-105">Samples a 1D texture using a projective divide; the texture coordinate is divided by t.w before the lookup takes place.</span></span>



| <span data-ttu-id="ccb6c-106">Ret tex1Dproj (s, t)</span><span class="sxs-lookup"><span data-stu-id="ccb6c-106">ret tex1Dproj(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="ccb6c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ccb6c-107">Parameters</span></span>



| <span data-ttu-id="ccb6c-108">Element</span><span class="sxs-lookup"><span data-stu-id="ccb6c-108">Item</span></span>                                                   | <span data-ttu-id="ccb6c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ccb6c-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="ccb6c-110"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="ccb6c-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="ccb6c-111">\[im \] samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="ccb6c-112"><span id="t"></span><span id="T"></span>*Bund*</span><span class="sxs-lookup"><span data-stu-id="ccb6c-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="ccb6c-113">\[in \] der Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="ccb6c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ccb6c-114">Return Value</span></span>

<span data-ttu-id="ccb6c-115">Der Wert der Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="ccb6c-116">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="ccb6c-116">Type Description</span></span>



| <span data-ttu-id="ccb6c-117">Name</span><span class="sxs-lookup"><span data-stu-id="ccb6c-117">Name</span></span> | <span data-ttu-id="ccb6c-118">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="ccb6c-118">In/Out</span></span> | [<span data-ttu-id="ccb6c-119">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="ccb6c-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="ccb6c-120">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="ccb6c-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="ccb6c-121">Size</span><span class="sxs-lookup"><span data-stu-id="ccb6c-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="ccb6c-122">s</span><span class="sxs-lookup"><span data-stu-id="ccb6c-122">s</span></span>    | <span data-ttu-id="ccb6c-123">in</span><span class="sxs-lookup"><span data-stu-id="ccb6c-123">in</span></span>     | [<span data-ttu-id="ccb6c-124">**Objekt**</span><span class="sxs-lookup"><span data-stu-id="ccb6c-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ccb6c-125">sampler1D</span><span class="sxs-lookup"><span data-stu-id="ccb6c-125">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="ccb6c-126">1</span><span class="sxs-lookup"><span data-stu-id="ccb6c-126">1</span></span>    |
| <span data-ttu-id="ccb6c-127">t</span><span class="sxs-lookup"><span data-stu-id="ccb6c-127">t</span></span>    | <span data-ttu-id="ccb6c-128">in</span><span class="sxs-lookup"><span data-stu-id="ccb6c-128">in</span></span>     | [<span data-ttu-id="ccb6c-129">**ve**</span><span class="sxs-lookup"><span data-stu-id="ccb6c-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ccb6c-130">**float**</span><span class="sxs-lookup"><span data-stu-id="ccb6c-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ccb6c-131">4</span><span class="sxs-lookup"><span data-stu-id="ccb6c-131">4</span></span>    |
| <span data-ttu-id="ccb6c-132">TZI</span><span class="sxs-lookup"><span data-stu-id="ccb6c-132">ret</span></span>  | <span data-ttu-id="ccb6c-133">out</span><span class="sxs-lookup"><span data-stu-id="ccb6c-133">out</span></span>    | [<span data-ttu-id="ccb6c-134">**ve**</span><span class="sxs-lookup"><span data-stu-id="ccb6c-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ccb6c-135">**float**</span><span class="sxs-lookup"><span data-stu-id="ccb6c-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ccb6c-136">4</span><span class="sxs-lookup"><span data-stu-id="ccb6c-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ccb6c-137">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="ccb6c-137">Minimum Shader Model</span></span>

<span data-ttu-id="ccb6c-138">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ccb6c-139">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="ccb6c-139">Shader Model</span></span>                                              | <span data-ttu-id="ccb6c-140">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ccb6c-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="ccb6c-141">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="ccb6c-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ccb6c-142">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="ccb6c-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="ccb6c-143">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ccb6c-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ccb6c-144">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="ccb6c-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="ccb6c-145">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ccb6c-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ccb6c-146">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="ccb6c-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="ccb6c-147">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ccb6c-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ccb6c-148">Nein</span><span class="sxs-lookup"><span data-stu-id="ccb6c-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="ccb6c-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ccb6c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccb6c-150">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="ccb6c-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

