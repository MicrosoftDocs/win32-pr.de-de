---
title: Min
description: Wählt den kleineren von x und y aus.
ms.assetid: 4e10cfc2-d680-4d7f-81b2-fa52024f902d
keywords:
- Min. HLSL
topic_type:
- apiref
api_name:
- min
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 129c5cb641c2d69b6c1365d8221663e264060532
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474100"
---
# <a name="min"></a><span data-ttu-id="4f789-104">Min</span><span class="sxs-lookup"><span data-stu-id="4f789-104">min</span></span>

<span data-ttu-id="4f789-105">Wählt den kleineren von x und y aus.</span><span class="sxs-lookup"><span data-stu-id="4f789-105">Selects the lesser of x and y.</span></span>



| <span data-ttu-id="4f789-106">Ret min (x, y)</span><span class="sxs-lookup"><span data-stu-id="4f789-106">ret min(x, y)</span></span> |
|---------------|



 

## <a name="parameters"></a><span data-ttu-id="4f789-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f789-107">Parameters</span></span>



| <span data-ttu-id="4f789-108">Element</span><span class="sxs-lookup"><span data-stu-id="4f789-108">Item</span></span>                                                   | <span data-ttu-id="4f789-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f789-109">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="4f789-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="4f789-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="4f789-111">\[im \] x-Eingabe Wert.</span><span class="sxs-lookup"><span data-stu-id="4f789-111">\[in\] The x input value.</span></span><br/> |
| <span data-ttu-id="4f789-112"><span id="y"></span><span id="Y"></span>*Teenie*</span><span class="sxs-lookup"><span data-stu-id="4f789-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="4f789-113">\[im \] y-Eingabe Wert.</span><span class="sxs-lookup"><span data-stu-id="4f789-113">\[in\] The y input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="4f789-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f789-114">Return Value</span></span>

<span data-ttu-id="4f789-115">Der *x* -oder *y* -Parameter, je nachdem, welcher Wert der kleinste Wert ist.</span><span class="sxs-lookup"><span data-stu-id="4f789-115">The *x* or *y* parameter, whichever is the smallest value.</span></span>


## <a name="remarks"></a><span data-ttu-id="4f789-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f789-116">Remarks</span></span>

<span data-ttu-id="4f789-117">Denormals werden wie folgt behandelt:</span><span class="sxs-lookup"><span data-stu-id="4f789-117">Denormals are handled as follows:</span></span>

| <span data-ttu-id="4f789-118">src0 Quelle1-></span><span class="sxs-lookup"><span data-stu-id="4f789-118">src0 src1-></span></span> | <span data-ttu-id="4f789-119">-inf</span><span class="sxs-lookup"><span data-stu-id="4f789-119">-inf</span></span> | <span data-ttu-id="4f789-120">F</span><span class="sxs-lookup"><span data-stu-id="4f789-120">F</span></span>             | <span data-ttu-id="4f789-121">+inf</span><span class="sxs-lookup"><span data-stu-id="4f789-121">+inf</span></span> | <span data-ttu-id="4f789-122">NAN</span><span class="sxs-lookup"><span data-stu-id="4f789-122">NAN</span></span>  |
|-------------|------|---------------|------|------|
| <span data-ttu-id="4f789-123">-inf</span><span class="sxs-lookup"><span data-stu-id="4f789-123">-inf</span></span>        | <span data-ttu-id="4f789-124">-inf</span><span class="sxs-lookup"><span data-stu-id="4f789-124">-inf</span></span> | <span data-ttu-id="4f789-125">-inf</span><span class="sxs-lookup"><span data-stu-id="4f789-125">-inf</span></span>          | <span data-ttu-id="4f789-126">-inf</span><span class="sxs-lookup"><span data-stu-id="4f789-126">-inf</span></span> | <span data-ttu-id="4f789-127">-inf</span><span class="sxs-lookup"><span data-stu-id="4f789-127">-inf</span></span> |
| <span data-ttu-id="4f789-128">F</span><span class="sxs-lookup"><span data-stu-id="4f789-128">F</span></span>           | <span data-ttu-id="4f789-129">-inf</span><span class="sxs-lookup"><span data-stu-id="4f789-129">-inf</span></span> | <span data-ttu-id="4f789-130">src0 oder Quelle1</span><span class="sxs-lookup"><span data-stu-id="4f789-130">src0 or src1</span></span>  | <span data-ttu-id="4f789-131">src0</span><span class="sxs-lookup"><span data-stu-id="4f789-131">src0</span></span> | <span data-ttu-id="4f789-132">src0</span><span class="sxs-lookup"><span data-stu-id="4f789-132">src0</span></span> |
| <span data-ttu-id="4f789-133">+inf</span><span class="sxs-lookup"><span data-stu-id="4f789-133">+inf</span></span>        | <span data-ttu-id="4f789-134">-inf</span><span class="sxs-lookup"><span data-stu-id="4f789-134">-inf</span></span> | <span data-ttu-id="4f789-135">src1</span><span class="sxs-lookup"><span data-stu-id="4f789-135">src1</span></span>          | <span data-ttu-id="4f789-136">+inf</span><span class="sxs-lookup"><span data-stu-id="4f789-136">+inf</span></span> | <span data-ttu-id="4f789-137">+inf</span><span class="sxs-lookup"><span data-stu-id="4f789-137">+inf</span></span> |
| <span data-ttu-id="4f789-138">NaN</span><span class="sxs-lookup"><span data-stu-id="4f789-138">NaN</span></span>         | <span data-ttu-id="4f789-139">-inf</span><span class="sxs-lookup"><span data-stu-id="4f789-139">-inf</span></span> | <span data-ttu-id="4f789-140">src1</span><span class="sxs-lookup"><span data-stu-id="4f789-140">src1</span></span>          | <span data-ttu-id="4f789-141">+inf</span><span class="sxs-lookup"><span data-stu-id="4f789-141">+inf</span></span> | <span data-ttu-id="4f789-142">NaN</span><span class="sxs-lookup"><span data-stu-id="4f789-142">NaN</span></span>  |

<span data-ttu-id="4f789-143">F bedeutet eine endliche reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="4f789-143">F means finite-real number.</span></span>


## <a name="type-description"></a><span data-ttu-id="4f789-144">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="4f789-144">Type Description</span></span>

| <span data-ttu-id="4f789-145">Name</span><span class="sxs-lookup"><span data-stu-id="4f789-145">Name</span></span> | <span data-ttu-id="4f789-146">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="4f789-146">In/Out</span></span>      | [<span data-ttu-id="4f789-147">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="4f789-147">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="4f789-148">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="4f789-148">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="4f789-149">Size</span><span class="sxs-lookup"><span data-stu-id="4f789-149">Size</span></span>                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="4f789-150">x</span><span class="sxs-lookup"><span data-stu-id="4f789-150">x</span></span>    | <span data-ttu-id="4f789-151">in</span><span class="sxs-lookup"><span data-stu-id="4f789-151">in</span></span>          | <span data-ttu-id="4f789-152">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="4f789-152">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="4f789-153">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4f789-153">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="4f789-154">any</span><span class="sxs-lookup"><span data-stu-id="4f789-154">any</span></span>                          |
| <span data-ttu-id="4f789-155">y</span><span class="sxs-lookup"><span data-stu-id="4f789-155">y</span></span>    | <span data-ttu-id="4f789-156">in</span><span class="sxs-lookup"><span data-stu-id="4f789-156">in</span></span>          | <span data-ttu-id="4f789-157">identisch mit Eingabe x</span><span class="sxs-lookup"><span data-stu-id="4f789-157">same as input x</span></span>                                                                                                | <span data-ttu-id="4f789-158">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4f789-158">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="4f789-159">gleiche Dimension (n) wie Eingabe x</span><span class="sxs-lookup"><span data-stu-id="4f789-159">same dimension(s) as input x</span></span> |
| <span data-ttu-id="4f789-160">TZI</span><span class="sxs-lookup"><span data-stu-id="4f789-160">ret</span></span>  | <span data-ttu-id="4f789-161">Rückgabetyp</span><span class="sxs-lookup"><span data-stu-id="4f789-161">return type</span></span> | <span data-ttu-id="4f789-162">identisch mit Eingabe x</span><span class="sxs-lookup"><span data-stu-id="4f789-162">same as input x</span></span>                                                                                                | <span data-ttu-id="4f789-163">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4f789-163">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="4f789-164">gleiche Dimension (n) wie Eingabe x</span><span class="sxs-lookup"><span data-stu-id="4f789-164">same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4f789-165">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="4f789-165">Minimum Shader Model</span></span>

<span data-ttu-id="4f789-166">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4f789-166">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4f789-167">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="4f789-167">Shader Model</span></span>                                                                       | <span data-ttu-id="4f789-168">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="4f789-168">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="4f789-169">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="4f789-169">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="4f789-170">ja</span><span class="sxs-lookup"><span data-stu-id="4f789-170">yes</span></span>                         |
| [<span data-ttu-id="4f789-171">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4f789-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="4f789-172">Ja (vs \_ 1 \_ 1 und PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="4f789-172">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="4f789-173">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4f789-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f789-174">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="4f789-174">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[<span data-ttu-id="4f789-175">**DirectX-Funktionsspezifikation**</span><span class="sxs-lookup"><span data-stu-id="4f789-175">**DirectX Functional Specification**</span></span>](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MIN)