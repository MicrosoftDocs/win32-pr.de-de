---
title: tex3Dproj
description: Stichproben eine 3D-Textur mithilfe einer projektives Teilung; die Textur Koordinate wird durch t. w dividiert, bevor die Suche stattfindet.
ms.assetid: c7062ef0-3169-4cbe-b47b-4efc80944963
keywords:
- tex3Dproj HLSL
topic_type:
- apiref
api_name:
- tex3Dproj
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 519477b7dba4f746dc1720a08c2ce581ab7b7205
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517030"
---
# <a name="tex3dproj"></a><span data-ttu-id="d0ea8-104">tex3Dproj</span><span class="sxs-lookup"><span data-stu-id="d0ea8-104">tex3Dproj</span></span>

<span data-ttu-id="d0ea8-105">Stichproben eine 3D-Textur mithilfe einer projektives Teilung; die Textur Koordinate wird durch t. w dividiert, bevor die Suche stattfindet.</span><span class="sxs-lookup"><span data-stu-id="d0ea8-105">Samples a 3D texture using a projective divide; the texture coordinate is divided by t.w before the lookup takes place.</span></span>



| <span data-ttu-id="d0ea8-106">Ret tex3Dproj (s, t)</span><span class="sxs-lookup"><span data-stu-id="d0ea8-106">ret tex3Dproj(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="d0ea8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0ea8-107">Parameters</span></span>



| <span data-ttu-id="d0ea8-108">Element</span><span class="sxs-lookup"><span data-stu-id="d0ea8-108">Item</span></span>                                                   | <span data-ttu-id="d0ea8-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0ea8-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="d0ea8-110"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="d0ea8-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="d0ea8-111">\[im \] samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="d0ea8-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="d0ea8-112"><span id="t"></span><span id="T"></span>*Bund*</span><span class="sxs-lookup"><span data-stu-id="d0ea8-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="d0ea8-113">\[in \] der Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="d0ea8-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d0ea8-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d0ea8-114">Return Value</span></span>

<span data-ttu-id="d0ea8-115">Der Wert der Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="d0ea8-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="d0ea8-116">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="d0ea8-116">Type Description</span></span>



| <span data-ttu-id="d0ea8-117">Name</span><span class="sxs-lookup"><span data-stu-id="d0ea8-117">Name</span></span> | <span data-ttu-id="d0ea8-118">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="d0ea8-118">In/Out</span></span> | [<span data-ttu-id="d0ea8-119">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="d0ea8-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="d0ea8-120">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="d0ea8-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d0ea8-121">Size</span><span class="sxs-lookup"><span data-stu-id="d0ea8-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="d0ea8-122">s</span><span class="sxs-lookup"><span data-stu-id="d0ea8-122">s</span></span>    | <span data-ttu-id="d0ea8-123">in</span><span class="sxs-lookup"><span data-stu-id="d0ea8-123">in</span></span>     | [<span data-ttu-id="d0ea8-124">**Objekt**</span><span class="sxs-lookup"><span data-stu-id="d0ea8-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d0ea8-125">sampler3D</span><span class="sxs-lookup"><span data-stu-id="d0ea8-125">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="d0ea8-126">1</span><span class="sxs-lookup"><span data-stu-id="d0ea8-126">1</span></span>    |
| <span data-ttu-id="d0ea8-127">t</span><span class="sxs-lookup"><span data-stu-id="d0ea8-127">t</span></span>    | <span data-ttu-id="d0ea8-128">in</span><span class="sxs-lookup"><span data-stu-id="d0ea8-128">in</span></span>     | [<span data-ttu-id="d0ea8-129">**ve**</span><span class="sxs-lookup"><span data-stu-id="d0ea8-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d0ea8-130">**float**</span><span class="sxs-lookup"><span data-stu-id="d0ea8-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d0ea8-131">4</span><span class="sxs-lookup"><span data-stu-id="d0ea8-131">4</span></span>    |
| <span data-ttu-id="d0ea8-132">TZI</span><span class="sxs-lookup"><span data-stu-id="d0ea8-132">ret</span></span>  | <span data-ttu-id="d0ea8-133">out</span><span class="sxs-lookup"><span data-stu-id="d0ea8-133">out</span></span>    | [<span data-ttu-id="d0ea8-134">**ve**</span><span class="sxs-lookup"><span data-stu-id="d0ea8-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d0ea8-135">**float**</span><span class="sxs-lookup"><span data-stu-id="d0ea8-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d0ea8-136">4</span><span class="sxs-lookup"><span data-stu-id="d0ea8-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d0ea8-137">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="d0ea8-137">Minimum Shader Model</span></span>

<span data-ttu-id="d0ea8-138">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d0ea8-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d0ea8-139">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="d0ea8-139">Shader Model</span></span>                                              | <span data-ttu-id="d0ea8-140">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="d0ea8-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="d0ea8-141">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="d0ea8-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d0ea8-142">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="d0ea8-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="d0ea8-143">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d0ea8-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d0ea8-144">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="d0ea8-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="d0ea8-145">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d0ea8-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d0ea8-146">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="d0ea8-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="d0ea8-147">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d0ea8-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d0ea8-148">Nein</span><span class="sxs-lookup"><span data-stu-id="d0ea8-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="d0ea8-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0ea8-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0ea8-150">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d0ea8-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

