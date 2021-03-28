---
title: tex2Dproj
description: Abtastungen einer 2D-Textur mithilfe einer projektives Teilung; die Textur Koordinate wird durch t. w dividiert, bevor die Suche stattfindet.
ms.assetid: c6b79360-3737-4b74-bdf3-6d46323e8e54
keywords:
- tex2Dproj HLSL
topic_type:
- apiref
api_name:
- tex2Dproj
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 365401e4e4eca8703207ffb5c7676748f4a06d30
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516865"
---
# <a name="tex2dproj"></a><span data-ttu-id="02beb-104">tex2Dproj</span><span class="sxs-lookup"><span data-stu-id="02beb-104">tex2Dproj</span></span>

<span data-ttu-id="02beb-105">Abtastungen einer 2D-Textur mithilfe einer projektives Teilung; die Textur Koordinate wird durch t. w dividiert, bevor die Suche stattfindet.</span><span class="sxs-lookup"><span data-stu-id="02beb-105">Samples a 2D texture using a projective divide; the texture coordinate is divided by t.w before the lookup takes place.</span></span>



| <span data-ttu-id="02beb-106">Ret tex2Dproj (s, t)</span><span class="sxs-lookup"><span data-stu-id="02beb-106">ret tex2Dproj(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="02beb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="02beb-107">Parameters</span></span>



| <span data-ttu-id="02beb-108">Element</span><span class="sxs-lookup"><span data-stu-id="02beb-108">Item</span></span>                                                   | <span data-ttu-id="02beb-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02beb-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="02beb-110"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="02beb-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="02beb-111">\[im \] samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="02beb-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="02beb-112"><span id="t"></span><span id="T"></span>*Bund*</span><span class="sxs-lookup"><span data-stu-id="02beb-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="02beb-113">\[in \] der Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="02beb-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="02beb-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02beb-114">Return Value</span></span>

<span data-ttu-id="02beb-115">Der Wert der Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="02beb-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="02beb-116">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="02beb-116">Type Description</span></span>



| <span data-ttu-id="02beb-117">Name</span><span class="sxs-lookup"><span data-stu-id="02beb-117">Name</span></span> | <span data-ttu-id="02beb-118">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="02beb-118">In/Out</span></span> | [<span data-ttu-id="02beb-119">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="02beb-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="02beb-120">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="02beb-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="02beb-121">Size</span><span class="sxs-lookup"><span data-stu-id="02beb-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="02beb-122">s</span><span class="sxs-lookup"><span data-stu-id="02beb-122">s</span></span>    | <span data-ttu-id="02beb-123">in</span><span class="sxs-lookup"><span data-stu-id="02beb-123">in</span></span>     | [<span data-ttu-id="02beb-124">**Objekt**</span><span class="sxs-lookup"><span data-stu-id="02beb-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="02beb-125">sampler2D</span><span class="sxs-lookup"><span data-stu-id="02beb-125">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="02beb-126">1</span><span class="sxs-lookup"><span data-stu-id="02beb-126">1</span></span>    |
| <span data-ttu-id="02beb-127">t</span><span class="sxs-lookup"><span data-stu-id="02beb-127">t</span></span>    | <span data-ttu-id="02beb-128">in</span><span class="sxs-lookup"><span data-stu-id="02beb-128">in</span></span>     | [<span data-ttu-id="02beb-129">**ve**</span><span class="sxs-lookup"><span data-stu-id="02beb-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="02beb-130">**float**</span><span class="sxs-lookup"><span data-stu-id="02beb-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="02beb-131">4</span><span class="sxs-lookup"><span data-stu-id="02beb-131">4</span></span>    |
| <span data-ttu-id="02beb-132">TZI</span><span class="sxs-lookup"><span data-stu-id="02beb-132">ret</span></span>  | <span data-ttu-id="02beb-133">out</span><span class="sxs-lookup"><span data-stu-id="02beb-133">out</span></span>    | [<span data-ttu-id="02beb-134">**ve**</span><span class="sxs-lookup"><span data-stu-id="02beb-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="02beb-135">**float**</span><span class="sxs-lookup"><span data-stu-id="02beb-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="02beb-136">4</span><span class="sxs-lookup"><span data-stu-id="02beb-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="02beb-137">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="02beb-137">Minimum Shader Model</span></span>

<span data-ttu-id="02beb-138">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="02beb-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="02beb-139">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="02beb-139">Shader Model</span></span>                                              | <span data-ttu-id="02beb-140">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="02beb-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="02beb-141">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="02beb-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="02beb-142">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="02beb-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="02beb-143">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="02beb-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="02beb-144">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="02beb-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="02beb-145">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="02beb-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="02beb-146">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="02beb-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="02beb-147">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="02beb-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="02beb-148">Nein</span><span class="sxs-lookup"><span data-stu-id="02beb-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="02beb-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02beb-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02beb-150">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="02beb-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

