---
title: pow
description: Gibt den angegebenen Wert in der angegebenen Potenz zurück.
ms.assetid: 1d64452c-81c7-4ef5-a332-13e0263c2cd1
keywords:
- Pow HLSL
topic_type:
- apiref
api_name:
- pow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f190c374b6c0ac42d41862eb918f0c0482b6d785
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474093"
---
# <a name="pow"></a><span data-ttu-id="b0c13-104">pow</span><span class="sxs-lookup"><span data-stu-id="b0c13-104">pow</span></span>

<span data-ttu-id="b0c13-105">Gibt den angegebenen Wert in der angegebenen Potenz zurück.</span><span class="sxs-lookup"><span data-stu-id="b0c13-105">Returns the specified value raised to the specified power.</span></span>



| <span data-ttu-id="b0c13-106">*ret* Pow (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="b0c13-106">*ret* pow(*x*, *y*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="b0c13-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0c13-107">Parameters</span></span>



| <span data-ttu-id="b0c13-108">Element</span><span class="sxs-lookup"><span data-stu-id="b0c13-108">Item</span></span>                                                   | <span data-ttu-id="b0c13-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b0c13-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="b0c13-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="b0c13-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="b0c13-111">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="b0c13-111">\[in\] The specified value.</span></span><br/> |
| <span data-ttu-id="b0c13-112"><span id="y"></span><span id="Y"></span>*Teenie*</span><span class="sxs-lookup"><span data-stu-id="b0c13-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="b0c13-113">\[in \] der angegebenen Potenz.</span><span class="sxs-lookup"><span data-stu-id="b0c13-113">\[in\] The specified power.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b0c13-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0c13-114">Return Value</span></span>

<span data-ttu-id="b0c13-115">Der *x* -Parameter, der für den *y* -Parameter ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="b0c13-115">The *x* parameter raised to the power of the *y* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0c13-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0c13-116">Remarks</span></span>

<span data-ttu-id="b0c13-117">Die intrinsische Funktion " **Pow** HLSL" berechnet *x*<sup>y</sup>.</span><span class="sxs-lookup"><span data-stu-id="b0c13-117">The **pow** HLSL intrinsic function calculates *x*<sup>y</sup>.</span></span>



| <span data-ttu-id="b0c13-118">X</span><span class="sxs-lookup"><span data-stu-id="b0c13-118">X</span></span>      | <span data-ttu-id="b0c13-119">Y</span><span class="sxs-lookup"><span data-stu-id="b0c13-119">Y</span></span>      | <span data-ttu-id="b0c13-120">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="b0c13-120">Result</span></span>                                                                      |
|--------|--------|-----------------------------------------------------------------------------|
| <span data-ttu-id="b0c13-121">< 0</span><span class="sxs-lookup"><span data-stu-id="b0c13-121">< 0</span></span> | <span data-ttu-id="b0c13-122">any</span><span class="sxs-lookup"><span data-stu-id="b0c13-122">any</span></span>    | <span data-ttu-id="b0c13-123">NAN</span><span class="sxs-lookup"><span data-stu-id="b0c13-123">NAN</span></span>                                                                         |
| <span data-ttu-id="b0c13-124">> 0</span><span class="sxs-lookup"><span data-stu-id="b0c13-124">> 0</span></span> | <span data-ttu-id="b0c13-125">= = 0</span><span class="sxs-lookup"><span data-stu-id="b0c13-125">== 0</span></span>   | <span data-ttu-id="b0c13-126">1</span><span class="sxs-lookup"><span data-stu-id="b0c13-126">1</span></span>                                                                           |
| <span data-ttu-id="b0c13-127">= = 0</span><span class="sxs-lookup"><span data-stu-id="b0c13-127">== 0</span></span>   | <span data-ttu-id="b0c13-128">> 0</span><span class="sxs-lookup"><span data-stu-id="b0c13-128">> 0</span></span> | <span data-ttu-id="b0c13-129">0</span><span class="sxs-lookup"><span data-stu-id="b0c13-129">0</span></span>                                                                           |
| <span data-ttu-id="b0c13-130">= = 0</span><span class="sxs-lookup"><span data-stu-id="b0c13-130">== 0</span></span>   | <span data-ttu-id="b0c13-131">< 0</span><span class="sxs-lookup"><span data-stu-id="b0c13-131">< 0</span></span> | <span data-ttu-id="b0c13-132">INF</span><span class="sxs-lookup"><span data-stu-id="b0c13-132">inf</span></span>                                                                         |
| <span data-ttu-id="b0c13-133">> 0</span><span class="sxs-lookup"><span data-stu-id="b0c13-133">> 0</span></span> | <span data-ttu-id="b0c13-134">< 0</span><span class="sxs-lookup"><span data-stu-id="b0c13-134">< 0</span></span> | <span data-ttu-id="b0c13-135">1/X<sup>-Y</sup></span><span class="sxs-lookup"><span data-stu-id="b0c13-135">1/X<sup>-Y</sup></span></span>                                                            |
| <span data-ttu-id="b0c13-136">= = 0</span><span class="sxs-lookup"><span data-stu-id="b0c13-136">== 0</span></span>   | <span data-ttu-id="b0c13-137">= = 0</span><span class="sxs-lookup"><span data-stu-id="b0c13-137">== 0</span></span>   | <span data-ttu-id="b0c13-138">Hängt vom jeweiligen Grafikprozessor ab.</span><span class="sxs-lookup"><span data-stu-id="b0c13-138">Depends on the particular graphics processor</span></span><br/> <span data-ttu-id="b0c13-139">0, oder 1 oder NaN</span><span class="sxs-lookup"><span data-stu-id="b0c13-139">0, or 1, or NAN</span></span><br/> |



 

## <a name="type-description"></a><span data-ttu-id="b0c13-140">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="b0c13-140">Type Description</span></span>



| <span data-ttu-id="b0c13-141">Name</span><span class="sxs-lookup"><span data-stu-id="b0c13-141">Name</span></span>  | [<span data-ttu-id="b0c13-142">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="b0c13-142">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="b0c13-143">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="b0c13-143">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="b0c13-144">Size</span><span class="sxs-lookup"><span data-stu-id="b0c13-144">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="b0c13-145">*x*</span><span class="sxs-lookup"><span data-stu-id="b0c13-145">*x*</span></span>   | <span data-ttu-id="b0c13-146">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="b0c13-146">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="b0c13-147">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="b0c13-147">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b0c13-148">any</span><span class="sxs-lookup"><span data-stu-id="b0c13-148">any</span></span>                            |
| <span data-ttu-id="b0c13-149">*y*</span><span class="sxs-lookup"><span data-stu-id="b0c13-149">*y*</span></span>   | <span data-ttu-id="b0c13-150">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="b0c13-150">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="b0c13-151">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="b0c13-151">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b0c13-152">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="b0c13-152">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="b0c13-153">*TZI*</span><span class="sxs-lookup"><span data-stu-id="b0c13-153">*ret*</span></span> | <span data-ttu-id="b0c13-154">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="b0c13-154">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="b0c13-155">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="b0c13-155">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b0c13-156">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="b0c13-156">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b0c13-157">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="b0c13-157">Minimum Shader Model</span></span>

<span data-ttu-id="b0c13-158">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b0c13-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b0c13-159">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="b0c13-159">Shader Model</span></span>                                                                       | <span data-ttu-id="b0c13-160">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="b0c13-160">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="b0c13-161">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="b0c13-161">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="b0c13-162">ja</span><span class="sxs-lookup"><span data-stu-id="b0c13-162">yes</span></span>                 |
| [<span data-ttu-id="b0c13-163">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b0c13-163">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="b0c13-164">Ja ( \_ nur vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="b0c13-164">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="b0c13-165">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b0c13-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0c13-166">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b0c13-166">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

