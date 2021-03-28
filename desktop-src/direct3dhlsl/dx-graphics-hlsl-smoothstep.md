---
title: smoothstep
description: Gibt eine Smooth Hermite-interpolung zwischen 0 und 1 zurück, wenn x im Bereich \ min, Max \ liegt.
ms.assetid: 6a879d82-f5ab-4e9b-bc9c-8988cbe6aa82
keywords:
- smoothstep HLSL
topic_type:
- apiref
api_name:
- smoothstep
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64e828b52a4d4517e53ba1f1aaf0f687255ad02b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976672"
---
# <a name="smoothstep"></a><span data-ttu-id="34a4f-104">smoothstep</span><span class="sxs-lookup"><span data-stu-id="34a4f-104">smoothstep</span></span>

<span data-ttu-id="34a4f-105">Gibt eine Smooth Hermite Interpolations zwischen 0 und 1 zurück, wenn *x* im Bereich \[ *Min*, *Max* liegt \] .</span><span class="sxs-lookup"><span data-stu-id="34a4f-105">Returns a smooth Hermite interpolation between 0 and 1, if *x* is in the range \[*min*, *max*\].</span></span>



| <span data-ttu-id="34a4f-106">*ret* -glättstep (*Min*, *Max*, *x*)</span><span class="sxs-lookup"><span data-stu-id="34a4f-106">*ret* smoothstep(*min*, *max*, *x*)</span></span> |
|-------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="34a4f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="34a4f-107">Parameters</span></span>



| <span data-ttu-id="34a4f-108">Element</span><span class="sxs-lookup"><span data-stu-id="34a4f-108">Item</span></span>                                                         | <span data-ttu-id="34a4f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34a4f-109">Description</span></span>                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="34a4f-110"><span id="min"></span><span id="MIN"></span>*man*</span><span class="sxs-lookup"><span data-stu-id="34a4f-110"><span id="min"></span><span id="MIN"></span>*min*</span></span><br/> | <span data-ttu-id="34a4f-111">\[im \] Minimal Bereich des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="34a4f-111">\[in\] The minimum range of the *x* parameter.</span></span><br/> |
| <span data-ttu-id="34a4f-112"><span id="max"></span><span id="MAX"></span>*Max*</span><span class="sxs-lookup"><span data-stu-id="34a4f-112"><span id="max"></span><span id="MAX"></span>*max*</span></span><br/> | <span data-ttu-id="34a4f-113">\[im \] maximalen Bereich des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="34a4f-113">\[in\] The maximum range of the *x* parameter.</span></span><br/> |
| <span data-ttu-id="34a4f-114"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="34a4f-114"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="34a4f-115">\[im \] angegebenen Wert, der interpoliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="34a4f-115">\[in\] The specified value to be interpolated.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="34a4f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="34a4f-116">Return Value</span></span>

<span data-ttu-id="34a4f-117">Gibt 0 zurück, wenn *x* kleiner als *Min* ist. 1, wenn *x* größer als der *Maximale* Wert ist. andernfalls ein Wert zwischen 0 und 1, wenn *x* im Bereich \[ *Min*, Max liegt  \] .</span><span class="sxs-lookup"><span data-stu-id="34a4f-117">Returns 0 if *x* is less than *min*; 1 if *x* is greater than *max*; otherwise, a value between 0 and 1 if *x* is in the range \[*min*, *max*\].</span></span>

## <a name="remarks"></a><span data-ttu-id="34a4f-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34a4f-118">Remarks</span></span>

<span data-ttu-id="34a4f-119">Verwenden Sie die systeminterne Funktion " **smoothstep** HLSL", um einen reibungslosen Übergang zwischen zwei Werten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="34a4f-119">Use the **smoothstep** HLSL intrinsic function to create a smooth transition between two values.</span></span> <span data-ttu-id="34a4f-120">Beispielsweise können Sie diese Funktion verwenden, um zwei Farben reibungslos zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="34a4f-120">For example, you can use this function to blend two colors smoothly.</span></span>

## <a name="type-description"></a><span data-ttu-id="34a4f-121">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="34a4f-121">Type Description</span></span>



| <span data-ttu-id="34a4f-122">Name</span><span class="sxs-lookup"><span data-stu-id="34a4f-122">Name</span></span>  | [<span data-ttu-id="34a4f-123">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="34a4f-123">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="34a4f-124">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="34a4f-124">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="34a4f-125">Size</span><span class="sxs-lookup"><span data-stu-id="34a4f-125">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="34a4f-126">*x*</span><span class="sxs-lookup"><span data-stu-id="34a4f-126">*x*</span></span>   | <span data-ttu-id="34a4f-127">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="34a4f-127">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="34a4f-128">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="34a4f-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="34a4f-129">any</span><span class="sxs-lookup"><span data-stu-id="34a4f-129">any</span></span>                            |
| <span data-ttu-id="34a4f-130">*min*</span><span class="sxs-lookup"><span data-stu-id="34a4f-130">*min*</span></span> | <span data-ttu-id="34a4f-131">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="34a4f-131">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="34a4f-132">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="34a4f-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="34a4f-133">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="34a4f-133">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="34a4f-134">*max*</span><span class="sxs-lookup"><span data-stu-id="34a4f-134">*max*</span></span> | <span data-ttu-id="34a4f-135">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="34a4f-135">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="34a4f-136">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="34a4f-136">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="34a4f-137">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="34a4f-137">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="34a4f-138">*TZI*</span><span class="sxs-lookup"><span data-stu-id="34a4f-138">*ret*</span></span> | <span data-ttu-id="34a4f-139">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="34a4f-139">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="34a4f-140">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="34a4f-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="34a4f-141">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="34a4f-141">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="34a4f-142">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="34a4f-142">Minimum Shader Model</span></span>

<span data-ttu-id="34a4f-143">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="34a4f-143">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="34a4f-144">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="34a4f-144">Shader Model</span></span>                                                                       | <span data-ttu-id="34a4f-145">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="34a4f-145">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="34a4f-146">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="34a4f-146">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="34a4f-147">ja</span><span class="sxs-lookup"><span data-stu-id="34a4f-147">yes</span></span>                 |
| [<span data-ttu-id="34a4f-148">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="34a4f-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="34a4f-149">Ja ( \_ nur vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="34a4f-149">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="34a4f-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="34a4f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34a4f-151">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="34a4f-151">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

