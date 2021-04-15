---
title: texcubeproj
description: Stichproben einer Cube-Textur mithilfe einer projektives Teilung die Textur Koordinate wird durch t. w dividiert, bevor die Suche stattfindet.
ms.assetid: 86bdd1c3-0a8d-4d09-b70d-1ebcee32c866
keywords:
- texcubeproj HLSL
topic_type:
- apiref
api_name:
- texCUBEproj
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d23a9b85034c1591cfe695759b29612a3674d436
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474085"
---
# <a name="texcubeproj"></a><span data-ttu-id="7103a-104">texcubeproj</span><span class="sxs-lookup"><span data-stu-id="7103a-104">texCUBEproj</span></span>

<span data-ttu-id="7103a-105">Stichproben einer Cube-Textur mithilfe einer projektives Teilung die Textur Koordinate wird durch t. w dividiert, bevor die Suche stattfindet.</span><span class="sxs-lookup"><span data-stu-id="7103a-105">Samples a cube texture using a projective divide; the texture coordinate is divided by t.w before the lookup takes place.</span></span>



| <span data-ttu-id="7103a-106">Ret texcubeproj (s, t)</span><span class="sxs-lookup"><span data-stu-id="7103a-106">ret texCUBEproj(s, t)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="7103a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7103a-107">Parameters</span></span>



| <span data-ttu-id="7103a-108">Element</span><span class="sxs-lookup"><span data-stu-id="7103a-108">Item</span></span>                                                   | <span data-ttu-id="7103a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7103a-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="7103a-110"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="7103a-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="7103a-111">\[im \] samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="7103a-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="7103a-112"><span id="t"></span><span id="T"></span>*Bund*</span><span class="sxs-lookup"><span data-stu-id="7103a-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="7103a-113">\[in \] der Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="7103a-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="7103a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7103a-114">Return Value</span></span>

<span data-ttu-id="7103a-115">Der Wert der Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="7103a-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="7103a-116">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="7103a-116">Type Description</span></span>



| <span data-ttu-id="7103a-117">Name</span><span class="sxs-lookup"><span data-stu-id="7103a-117">Name</span></span> | <span data-ttu-id="7103a-118">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="7103a-118">In/Out</span></span> | [<span data-ttu-id="7103a-119">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="7103a-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="7103a-120">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="7103a-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="7103a-121">Size</span><span class="sxs-lookup"><span data-stu-id="7103a-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="7103a-122">s</span><span class="sxs-lookup"><span data-stu-id="7103a-122">s</span></span>    | <span data-ttu-id="7103a-123">in</span><span class="sxs-lookup"><span data-stu-id="7103a-123">in</span></span>     | [<span data-ttu-id="7103a-124">**Objekt**</span><span class="sxs-lookup"><span data-stu-id="7103a-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="7103a-125">samplercube</span><span class="sxs-lookup"><span data-stu-id="7103a-125">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="7103a-126">1</span><span class="sxs-lookup"><span data-stu-id="7103a-126">1</span></span>    |
| <span data-ttu-id="7103a-127">t</span><span class="sxs-lookup"><span data-stu-id="7103a-127">t</span></span>    | <span data-ttu-id="7103a-128">in</span><span class="sxs-lookup"><span data-stu-id="7103a-128">in</span></span>     | [<span data-ttu-id="7103a-129">**ve**</span><span class="sxs-lookup"><span data-stu-id="7103a-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="7103a-130">**float**</span><span class="sxs-lookup"><span data-stu-id="7103a-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7103a-131">4</span><span class="sxs-lookup"><span data-stu-id="7103a-131">4</span></span>    |
| <span data-ttu-id="7103a-132">TZI</span><span class="sxs-lookup"><span data-stu-id="7103a-132">ret</span></span>  | <span data-ttu-id="7103a-133">out</span><span class="sxs-lookup"><span data-stu-id="7103a-133">out</span></span>    | [<span data-ttu-id="7103a-134">**ve**</span><span class="sxs-lookup"><span data-stu-id="7103a-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="7103a-135">**float**</span><span class="sxs-lookup"><span data-stu-id="7103a-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7103a-136">4</span><span class="sxs-lookup"><span data-stu-id="7103a-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7103a-137">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="7103a-137">Minimum Shader Model</span></span>

<span data-ttu-id="7103a-138">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7103a-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7103a-139">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="7103a-139">Shader Model</span></span>                                              | <span data-ttu-id="7103a-140">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="7103a-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="7103a-141">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="7103a-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7103a-142">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="7103a-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="7103a-143">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7103a-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7103a-144">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="7103a-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="7103a-145">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7103a-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7103a-146">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="7103a-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="7103a-147">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7103a-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7103a-148">Nein</span><span class="sxs-lookup"><span data-stu-id="7103a-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="7103a-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7103a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7103a-150">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="7103a-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

