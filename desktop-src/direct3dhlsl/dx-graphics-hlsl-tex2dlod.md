---
title: tex2Dlod
description: Stichproben eine 2D-Textur mit Mipmaps. Die Mipmap-LOD wird in t.w. angegeben.
ms.assetid: 689eff39-f6ac-4c25-8b92-ca68707ae8ad
keywords:
- tex2Dlod HLSL
topic_type:
- apiref
api_name:
- tex2Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f63a922fe86dc10d984369a1a872f84089b4db34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976648"
---
# <a name="tex2dlod"></a><span data-ttu-id="198c8-105">tex2Dlod</span><span class="sxs-lookup"><span data-stu-id="198c8-105">tex2Dlod</span></span>

<span data-ttu-id="198c8-106">Stichproben eine 2D-Textur mit Mipmaps.</span><span class="sxs-lookup"><span data-stu-id="198c8-106">Samples a 2D texture with mipmaps.</span></span> <span data-ttu-id="198c8-107">Die Mipmap-LOD wird in t.w. angegeben.</span><span class="sxs-lookup"><span data-stu-id="198c8-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="198c8-108">Ret tex2Dlod (s, t)</span><span class="sxs-lookup"><span data-stu-id="198c8-108">ret tex2Dlod(s, t)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="198c8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="198c8-109">Parameters</span></span>



| <span data-ttu-id="198c8-110">Element</span><span class="sxs-lookup"><span data-stu-id="198c8-110">Item</span></span>                                                   | <span data-ttu-id="198c8-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="198c8-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="198c8-112"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="198c8-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="198c8-113">\[im \] samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="198c8-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="198c8-114"><span id="t"></span><span id="T"></span>*Bund*</span><span class="sxs-lookup"><span data-stu-id="198c8-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="198c8-115">\[in \] der Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="198c8-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="198c8-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="198c8-116">Return Value</span></span>

<span data-ttu-id="198c8-117">Der Wert der Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="198c8-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="198c8-118">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="198c8-118">Type Description</span></span>



| <span data-ttu-id="198c8-119">Name</span><span class="sxs-lookup"><span data-stu-id="198c8-119">Name</span></span> | <span data-ttu-id="198c8-120">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="198c8-120">In/Out</span></span> | [<span data-ttu-id="198c8-121">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="198c8-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="198c8-122">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="198c8-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="198c8-123">Size</span><span class="sxs-lookup"><span data-stu-id="198c8-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="198c8-124">s</span><span class="sxs-lookup"><span data-stu-id="198c8-124">s</span></span>    | <span data-ttu-id="198c8-125">in</span><span class="sxs-lookup"><span data-stu-id="198c8-125">in</span></span>     | [<span data-ttu-id="198c8-126">**Objekt**</span><span class="sxs-lookup"><span data-stu-id="198c8-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="198c8-127">sampler2D</span><span class="sxs-lookup"><span data-stu-id="198c8-127">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="198c8-128">1</span><span class="sxs-lookup"><span data-stu-id="198c8-128">1</span></span>    |
| <span data-ttu-id="198c8-129">t</span><span class="sxs-lookup"><span data-stu-id="198c8-129">t</span></span>    | <span data-ttu-id="198c8-130">in</span><span class="sxs-lookup"><span data-stu-id="198c8-130">in</span></span>     | [<span data-ttu-id="198c8-131">**ve**</span><span class="sxs-lookup"><span data-stu-id="198c8-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="198c8-132">**float**</span><span class="sxs-lookup"><span data-stu-id="198c8-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="198c8-133">4</span><span class="sxs-lookup"><span data-stu-id="198c8-133">4</span></span>    |
| <span data-ttu-id="198c8-134">TZI</span><span class="sxs-lookup"><span data-stu-id="198c8-134">ret</span></span>  | <span data-ttu-id="198c8-135">out</span><span class="sxs-lookup"><span data-stu-id="198c8-135">out</span></span>    | [<span data-ttu-id="198c8-136">**ve**</span><span class="sxs-lookup"><span data-stu-id="198c8-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="198c8-137">**float**</span><span class="sxs-lookup"><span data-stu-id="198c8-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="198c8-138">4</span><span class="sxs-lookup"><span data-stu-id="198c8-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="198c8-139">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="198c8-139">Minimum Shader Model</span></span>

<span data-ttu-id="198c8-140">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="198c8-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="198c8-141">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="198c8-141">Shader Model</span></span>                                                                       | <span data-ttu-id="198c8-142">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="198c8-142">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="198c8-143">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="198c8-143">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) and higher shader models</span></span> | <span data-ttu-id="198c8-144">ja</span><span class="sxs-lookup"><span data-stu-id="198c8-144">yes</span></span>       |
| [<span data-ttu-id="198c8-145">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="198c8-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                          | <span data-ttu-id="198c8-146">nein</span><span class="sxs-lookup"><span data-stu-id="198c8-146">no</span></span>        |
| [<span data-ttu-id="198c8-147">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="198c8-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="198c8-148">nein</span><span class="sxs-lookup"><span data-stu-id="198c8-148">no</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="198c8-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="198c8-149">Remarks</span></span>

<span data-ttu-id="198c8-150">Ab Direct3D 10 können Sie die neue HLSL-Syntax verwenden, um auf Texturen und andere Ressourcen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="198c8-150">Starting with Direct3D 10, you can use new HLSL syntax to access textures and other resources.</span></span> <span data-ttu-id="198c8-151">Sie können systemeigene Textur Suchfunktionen, wie z. b. **tex2Dlod**, durch einen stärker objektorientierten Stil ersetzen.</span><span class="sxs-lookup"><span data-stu-id="198c8-151">You can replace intrinsic-style texture lookup functions, such as **tex2Dlod**, with a more object-oriented style.</span></span> <span data-ttu-id="198c8-152">In diesem objektorientierten Stil sind Texturen von Samplern entkoppelt und verfügen über Methoden zum Laden und Sampling.</span><span class="sxs-lookup"><span data-stu-id="198c8-152">In this object-oriented style, textures are decoupled from samplers and have methods for loading and sampling.</span></span>

<span data-ttu-id="198c8-153">Beispiel für eine 2D-Textur, anstatt **tex2Dlod** wie in diesem Code zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="198c8-153">To sample a 2D texture, instead of using **tex2Dlod** as in this code:</span></span>


```
sampler S;
...
color = tex2Dlod(S, Location);
```



<span data-ttu-id="198c8-154">Verwenden Sie die [samplelevel](dx-graphics-hlsl-to-samplelevel.md) -Methode eines [**Textur Objekts**](dx-graphics-hlsl-to-type.md) wie in diesem Code:</span><span class="sxs-lookup"><span data-stu-id="198c8-154">Use the [SampleLevel](dx-graphics-hlsl-to-samplelevel.md) method of a [**Texture Object**](dx-graphics-hlsl-to-type.md) as in this code:</span></span>


```
Texture2D MyTexture;
SamplerState MySampler;
...
color = MyTexture.SampleLevel(MySampler, Location, LOD);
```



<span data-ttu-id="198c8-155">Um die Funktionen für die Textur Suche im systeminternen Stil, wie z. b. **tex2Dlod**, mit [Shader Model 4](dx-graphics-hlsl-sm4.md) und höher zu verwenden, verwenden Sie [**D3DCOMPILE \_ enable abwärts \_ \_ Compatibility**](d3dcompile-constants.md) to compile.</span><span class="sxs-lookup"><span data-stu-id="198c8-155">To use the intrinsic-style texture lookup functions, such as **tex2Dlod**, with [shader model 4](dx-graphics-hlsl-sm4.md) and higher, use [**D3DCOMPILE\_ENABLE\_BACKWARDS\_COMPATIBILITY**](d3dcompile-constants.md) to compile.</span></span> <span data-ttu-id="198c8-156">Wenn Sie jedoch Shader Model 4 und höher (auch [ \* \_ 4 \_ 0 \_ Ebene \_ 9 \_ \* ](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)) mit neueren, objektorientierten Stil Code als Ziel haben möchten, migrieren Sie zur neueren HLSL-Syntax.</span><span class="sxs-lookup"><span data-stu-id="198c8-156">However, if you want to target shader model 4 and higher (even [\*\_4\_0\_level\_9\_\*](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)) with newer object-oriented style code, migrate to the newer HLSL syntax.</span></span>

## <a name="see-also"></a><span data-ttu-id="198c8-157">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="198c8-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="198c8-158">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="198c8-158">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

