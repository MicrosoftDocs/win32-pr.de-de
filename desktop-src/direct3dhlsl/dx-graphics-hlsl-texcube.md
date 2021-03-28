---
title: Texcube (HLSL-Referenz)
description: Abtastungen einer Cube-Textur.
ms.assetid: 77943eb9-86e8-4ae4-8975-8f925e084ce4
keywords:
- Texcube HLSL
topic_type:
- apiref
api_name:
- texCUBE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 524ed44028372eeabf176c30da8b3a31a8ee7988
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039122"
---
# <a name="texcube-hlsl-reference"></a><span data-ttu-id="06bfb-104">Texcube (HLSL-Referenz)</span><span class="sxs-lookup"><span data-stu-id="06bfb-104">texCUBE (HLSL reference)</span></span>

<span data-ttu-id="06bfb-105">Abtastungen einer Cube-Textur.</span><span class="sxs-lookup"><span data-stu-id="06bfb-105">Samples a cube texture.</span></span>



| <span data-ttu-id="06bfb-106">Ret Texcube (s, t)</span><span class="sxs-lookup"><span data-stu-id="06bfb-106">ret texCUBE(s, t)</span></span> |
|-------------------|



 

## <a name="parameters"></a><span data-ttu-id="06bfb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="06bfb-107">Parameters</span></span>



| <span data-ttu-id="06bfb-108">Element</span><span class="sxs-lookup"><span data-stu-id="06bfb-108">Item</span></span>                                                   | <span data-ttu-id="06bfb-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06bfb-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="06bfb-110"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="06bfb-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="06bfb-111">\[im \] samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="06bfb-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="06bfb-112"><span id="t"></span><span id="T"></span>*Bund*</span><span class="sxs-lookup"><span data-stu-id="06bfb-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="06bfb-113">\[in \] der Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="06bfb-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="06bfb-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06bfb-114">Return Value</span></span>

<span data-ttu-id="06bfb-115">Der Wert der Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="06bfb-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="06bfb-116">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="06bfb-116">Type Description</span></span>



| <span data-ttu-id="06bfb-117">Name</span><span class="sxs-lookup"><span data-stu-id="06bfb-117">Name</span></span> | <span data-ttu-id="06bfb-118">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="06bfb-118">In/Out</span></span> | [<span data-ttu-id="06bfb-119">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="06bfb-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="06bfb-120">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="06bfb-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="06bfb-121">Size</span><span class="sxs-lookup"><span data-stu-id="06bfb-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="06bfb-122">s</span><span class="sxs-lookup"><span data-stu-id="06bfb-122">s</span></span>    | <span data-ttu-id="06bfb-123">in</span><span class="sxs-lookup"><span data-stu-id="06bfb-123">in</span></span>     | [<span data-ttu-id="06bfb-124">**Objekt**</span><span class="sxs-lookup"><span data-stu-id="06bfb-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="06bfb-125">samplercube</span><span class="sxs-lookup"><span data-stu-id="06bfb-125">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="06bfb-126">1</span><span class="sxs-lookup"><span data-stu-id="06bfb-126">1</span></span>    |
| <span data-ttu-id="06bfb-127">t</span><span class="sxs-lookup"><span data-stu-id="06bfb-127">t</span></span>    | <span data-ttu-id="06bfb-128">in</span><span class="sxs-lookup"><span data-stu-id="06bfb-128">in</span></span>     | [<span data-ttu-id="06bfb-129">**ve**</span><span class="sxs-lookup"><span data-stu-id="06bfb-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="06bfb-130">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="06bfb-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="06bfb-131">3</span><span class="sxs-lookup"><span data-stu-id="06bfb-131">3</span></span>    |
| <span data-ttu-id="06bfb-132">TZI</span><span class="sxs-lookup"><span data-stu-id="06bfb-132">ret</span></span>  | <span data-ttu-id="06bfb-133">out</span><span class="sxs-lookup"><span data-stu-id="06bfb-133">out</span></span>    | [<span data-ttu-id="06bfb-134">**ve**</span><span class="sxs-lookup"><span data-stu-id="06bfb-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="06bfb-135">**float**</span><span class="sxs-lookup"><span data-stu-id="06bfb-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="06bfb-136">4</span><span class="sxs-lookup"><span data-stu-id="06bfb-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="06bfb-137">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="06bfb-137">Minimum Shader Model</span></span>

<span data-ttu-id="06bfb-138">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="06bfb-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="06bfb-139">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="06bfb-139">Shader Model</span></span>                                              | <span data-ttu-id="06bfb-140">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="06bfb-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="06bfb-141">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="06bfb-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="06bfb-142">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="06bfb-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="06bfb-143">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="06bfb-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="06bfb-144">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="06bfb-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="06bfb-145">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="06bfb-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="06bfb-146">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="06bfb-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="06bfb-147">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="06bfb-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="06bfb-148">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="06bfb-148">yes (pixel shader only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="06bfb-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="06bfb-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06bfb-150">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="06bfb-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

