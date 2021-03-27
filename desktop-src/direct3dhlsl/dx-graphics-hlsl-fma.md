---
title: FMA (corecrt \_ Math. h)
description: Gibt die multiplizierte Multiplikation mit doppelter Genauigkeit von a \ b + c zurück.
ms.assetid: C4EF2552-7388-4CA8-B78F-6B2D4C8FC5F6
keywords:
- FMA HLSL
topic_type:
- apiref
api_name:
- fma
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 287f07881a00ca53a3f1fe702cf4d95b64bf14c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391887"
---
# <a name="fma"></a><span data-ttu-id="a1b46-104">fma</span><span class="sxs-lookup"><span data-stu-id="a1b46-104">fma</span></span>

<span data-ttu-id="a1b46-105">Gibt die multiplizierte Multiplikation mit doppelter Genauigkeit von a \* b + c zurück.</span><span class="sxs-lookup"><span data-stu-id="a1b46-105">Returns the double-precision fused multiply-addition of a \* b + c.</span></span>



| <span data-ttu-id="a1b46-106">*ret* FMA (Double *a*, *b*, *c*);</span><span class="sxs-lookup"><span data-stu-id="a1b46-106">*ret* fma(double *a*, *b*, *c*);</span></span> |
|----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="a1b46-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1b46-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1b46-108"><span id="a"></span><span id="A"></span>*ein*</span><span class="sxs-lookup"><span data-stu-id="a1b46-108"><span id="a"></span><span id="A"></span>*a*</span></span>
</dt> <dd>

<span data-ttu-id="a1b46-109">\[im \] ersten Wert in der multiplizierten Multiplikations Addition.</span><span class="sxs-lookup"><span data-stu-id="a1b46-109">\[in\] The first value in the fused multiply-addition.</span></span>

</dd> <dt>

<span data-ttu-id="a1b46-110"><span id="b"></span><span id="B"></span>*b*</span><span class="sxs-lookup"><span data-stu-id="a1b46-110"><span id="b"></span><span id="B"></span>*b*</span></span>
</dt> <dd>

<span data-ttu-id="a1b46-111">\[im \] zweiten Wert in der Addition multiplizieren multiplizieren.</span><span class="sxs-lookup"><span data-stu-id="a1b46-111">\[in\] The second value in the fused multiply-addition.</span></span>

</dd> <dt>

<span data-ttu-id="a1b46-112"><span id="c"></span><span id="C"></span>*scher*</span><span class="sxs-lookup"><span data-stu-id="a1b46-112"><span id="c"></span><span id="C"></span>*c*</span></span>
</dt> <dd>

<span data-ttu-id="a1b46-113">\[im \] dritten Wert in der Addition multiplizieren multiplizieren.</span><span class="sxs-lookup"><span data-stu-id="a1b46-113">\[in\] The third value in the fused multiply-addition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1b46-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1b46-114">Return Value</span></span>

<span data-ttu-id="a1b46-115">Die Multiplikation mit doppelter Genauigkeit multipliziert mit den Parametern *a* \* *b*  +  *c*.</span><span class="sxs-lookup"><span data-stu-id="a1b46-115">The double-precision fused multiply-addition of parameters *a* \* *b* + *c*.</span></span> <span data-ttu-id="a1b46-116">Der zurückgegebene Wert muss auf 0,5 Einheiten der geringsten Genauigkeit (ULP) genau sein.</span><span class="sxs-lookup"><span data-stu-id="a1b46-116">The returned value must be accurate to 0.5 units of least precision (ULP).</span></span>

## <a name="remarks"></a><span data-ttu-id="a1b46-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1b46-117">Remarks</span></span>

<span data-ttu-id="a1b46-118">Das systeminterne **FMA** -System muss Nane, INFs und denorms unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a1b46-118">The **fma** intrinsic must support NaNs, INFs, and Denorms.</span></span>

<span data-ttu-id="a1b46-119">Um die systeminterne Funktion " **FMA** " im Shader-Code zu verwenden, müssen Sie die [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) -Methode mit [**D3D11 \_ Feature \_ D3D11- \_ Optionen**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) aufrufen, um zu überprüfen, ob das Direct3D-Gerät die [**extendeddoublesshaderinstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) -Funktions Option</span><span class="sxs-lookup"><span data-stu-id="a1b46-119">To use the **fma** intrinsic in your shader code, call the [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) method with [**D3D11\_FEATURE\_D3D11\_OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) to verify that the Direct3D device supports the [**ExtendedDoublesShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) feature option.</span></span> <span data-ttu-id="a1b46-120">Die systeminterne **FMA** -Funktion erfordert einen WDDM 1,2-Anzeigetreiber, und alle WDDM 1,2-Anzeigetreiber müssen **FMA** unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a1b46-120">The **fma** intrinsic requires a WDDM 1.2 display driver, and all WDDM 1.2 display drivers must support **fma**.</span></span> <span data-ttu-id="a1b46-121">Wenn Ihre APP ein renderinggerät mit [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0 oder 11,1 erstellt und das Kompilierungs Ziel Shader-Modell 5 oder höher ist, kann der HLSL-Quellcode den systeminternen **FMA** -Code verwenden.</span><span class="sxs-lookup"><span data-stu-id="a1b46-121">If your app creates a rendering device with [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.0 or 11.1 and the compilation target is shader model 5 or later, the HLSL source code can use the **fma** intrinsic.</span></span>

### <a name="type-description"></a><span data-ttu-id="a1b46-122">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="a1b46-122">Type Description</span></span>



| <span data-ttu-id="a1b46-123">Name</span><span class="sxs-lookup"><span data-stu-id="a1b46-123">Name</span></span>  | [<span data-ttu-id="a1b46-124">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="a1b46-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="a1b46-125">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="a1b46-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="a1b46-126">Size</span><span class="sxs-lookup"><span data-stu-id="a1b46-126">Size</span></span>                         |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| <span data-ttu-id="a1b46-127">*ein*</span><span class="sxs-lookup"><span data-stu-id="a1b46-127">*a*</span></span>   | <span data-ttu-id="a1b46-128">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="a1b46-128">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="a1b46-129">**Maß**</span><span class="sxs-lookup"><span data-stu-id="a1b46-129">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="a1b46-130">any</span><span class="sxs-lookup"><span data-stu-id="a1b46-130">any</span></span>                          |
| <span data-ttu-id="a1b46-131">*b*</span><span class="sxs-lookup"><span data-stu-id="a1b46-131">*b*</span></span>   | <span data-ttu-id="a1b46-132">identisch mit Eingabe *a*</span><span class="sxs-lookup"><span data-stu-id="a1b46-132">same as input *a*</span></span>                                                                                              | [<span data-ttu-id="a1b46-133">**Maß**</span><span class="sxs-lookup"><span data-stu-id="a1b46-133">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="a1b46-134">gleiche Dimensionen wie Eingabe *a*</span><span class="sxs-lookup"><span data-stu-id="a1b46-134">same dimensions as input *a*</span></span> |
| <span data-ttu-id="a1b46-135">*c*</span><span class="sxs-lookup"><span data-stu-id="a1b46-135">*c*</span></span>   | <span data-ttu-id="a1b46-136">identisch mit Eingabe *a*</span><span class="sxs-lookup"><span data-stu-id="a1b46-136">same as input *a*</span></span>                                                                                              | [<span data-ttu-id="a1b46-137">**Maß**</span><span class="sxs-lookup"><span data-stu-id="a1b46-137">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="a1b46-138">gleiche Dimensionen wie Eingabe *a*</span><span class="sxs-lookup"><span data-stu-id="a1b46-138">same dimensions as input *a*</span></span> |
| <span data-ttu-id="a1b46-139">*TZI*</span><span class="sxs-lookup"><span data-stu-id="a1b46-139">*ret*</span></span> | <span data-ttu-id="a1b46-140">identisch mit Eingabe *a*</span><span class="sxs-lookup"><span data-stu-id="a1b46-140">same as input *a*</span></span>                                                                                              | [<span data-ttu-id="a1b46-141">**Maß**</span><span class="sxs-lookup"><span data-stu-id="a1b46-141">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="a1b46-142">gleiche Dimensionen wie Eingabe *a*</span><span class="sxs-lookup"><span data-stu-id="a1b46-142">same dimensions as input *a*</span></span> |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="a1b46-143">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="a1b46-143">Minimum Shader Model</span></span>

<span data-ttu-id="a1b46-144">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a1b46-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a1b46-145">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="a1b46-145">Shader Model</span></span>                                                | <span data-ttu-id="a1b46-146">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="a1b46-146">Supported</span></span> |
|-------------------------------------------------------------|-----------|
| [<span data-ttu-id="a1b46-147">Shadermodell 5 oder höher</span><span class="sxs-lookup"><span data-stu-id="a1b46-147">Shader model 5 or later</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="a1b46-148">ja</span><span class="sxs-lookup"><span data-stu-id="a1b46-148">yes</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="a1b46-149">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a1b46-149">Requirements</span></span>



| <span data-ttu-id="a1b46-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1b46-150">Requirement</span></span> | <span data-ttu-id="a1b46-151">Wert</span><span class="sxs-lookup"><span data-stu-id="a1b46-151">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1b46-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1b46-152">Minimum supported client</span></span><br/> | <span data-ttu-id="a1b46-153">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a1b46-153">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="a1b46-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1b46-154">Minimum supported server</span></span><br/> | <span data-ttu-id="a1b46-155">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a1b46-155">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="a1b46-156">Header</span><span class="sxs-lookup"><span data-stu-id="a1b46-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1b46-157"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1b46-157"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1b46-158">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a1b46-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1b46-159">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="a1b46-159">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

