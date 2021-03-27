---
title: max
description: Wählt den größeren von x und y aus.
ms.assetid: 08e17a0c-6d44-49ea-b613-bd262534522c
keywords:
- Max. HLSL
topic_type:
- apiref
api_name:
- max
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a40ccb32bb2c2fcd7ca7342b9d7d4d143688102
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390756"
---
# <a name="max"></a><span data-ttu-id="64add-104">max</span><span class="sxs-lookup"><span data-stu-id="64add-104">max</span></span>

<span data-ttu-id="64add-105">Wählt den größeren von x und y aus.</span><span class="sxs-lookup"><span data-stu-id="64add-105">Selects the greater of x and y.</span></span>



| <span data-ttu-id="64add-106">Ret Max (x, y)</span><span class="sxs-lookup"><span data-stu-id="64add-106">ret max(x, y)</span></span> |
|---------------|



 

## <a name="parameters"></a><span data-ttu-id="64add-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="64add-107">Parameters</span></span>



| <span data-ttu-id="64add-108">Element</span><span class="sxs-lookup"><span data-stu-id="64add-108">Item</span></span>                                                   | <span data-ttu-id="64add-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64add-109">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="64add-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="64add-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="64add-111">\[im \] x-Eingabe Wert.</span><span class="sxs-lookup"><span data-stu-id="64add-111">\[in\] The x input value.</span></span><br/> |
| <span data-ttu-id="64add-112"><span id="y"></span><span id="Y"></span>*Teenie*</span><span class="sxs-lookup"><span data-stu-id="64add-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="64add-113">\[im \] y-Eingabe Wert.</span><span class="sxs-lookup"><span data-stu-id="64add-113">\[in\] The y input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="64add-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64add-114">Return Value</span></span>

<span data-ttu-id="64add-115">Der *x* -oder *y* -Parameter, je nachdem, welcher Wert der größte Wert ist.</span><span class="sxs-lookup"><span data-stu-id="64add-115">The *x* or *y* parameter, whichever is the largest value.</span></span>


## <a name="remarks"></a><span data-ttu-id="64add-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64add-116">Remarks</span></span>

<span data-ttu-id="64add-117">Denormals werden wie folgt behandelt:</span><span class="sxs-lookup"><span data-stu-id="64add-117">Denormals are handled as follows:</span></span>

| <span data-ttu-id="64add-118">src0 Quelle1-></span><span class="sxs-lookup"><span data-stu-id="64add-118">src0 src1-></span></span> | <span data-ttu-id="64add-119">-inf</span><span class="sxs-lookup"><span data-stu-id="64add-119">-inf</span></span> | <span data-ttu-id="64add-120">F</span><span class="sxs-lookup"><span data-stu-id="64add-120">F</span></span>             | <span data-ttu-id="64add-121">+inf</span><span class="sxs-lookup"><span data-stu-id="64add-121">+inf</span></span> | <span data-ttu-id="64add-122">NAN</span><span class="sxs-lookup"><span data-stu-id="64add-122">NAN</span></span>  |
|-------------|------|---------------|------|------|
| <span data-ttu-id="64add-123">-inf</span><span class="sxs-lookup"><span data-stu-id="64add-123">-inf</span></span>        | <span data-ttu-id="64add-124">-inf</span><span class="sxs-lookup"><span data-stu-id="64add-124">-inf</span></span> | <span data-ttu-id="64add-125">src1</span><span class="sxs-lookup"><span data-stu-id="64add-125">src1</span></span>          | <span data-ttu-id="64add-126">+inf</span><span class="sxs-lookup"><span data-stu-id="64add-126">+inf</span></span> | <span data-ttu-id="64add-127">-inf</span><span class="sxs-lookup"><span data-stu-id="64add-127">-inf</span></span> |
| <span data-ttu-id="64add-128">F</span><span class="sxs-lookup"><span data-stu-id="64add-128">F</span></span>           | <span data-ttu-id="64add-129">src0</span><span class="sxs-lookup"><span data-stu-id="64add-129">src0</span></span> | <span data-ttu-id="64add-130">src0 oder Quelle1</span><span class="sxs-lookup"><span data-stu-id="64add-130">src0 or src1</span></span>  | <span data-ttu-id="64add-131">+inf</span><span class="sxs-lookup"><span data-stu-id="64add-131">+inf</span></span> | <span data-ttu-id="64add-132">src0</span><span class="sxs-lookup"><span data-stu-id="64add-132">src0</span></span> |
| <span data-ttu-id="64add-133">+inf</span><span class="sxs-lookup"><span data-stu-id="64add-133">+inf</span></span>        | <span data-ttu-id="64add-134">+inf</span><span class="sxs-lookup"><span data-stu-id="64add-134">+inf</span></span> | <span data-ttu-id="64add-135">+inf</span><span class="sxs-lookup"><span data-stu-id="64add-135">+inf</span></span>          | <span data-ttu-id="64add-136">+inf</span><span class="sxs-lookup"><span data-stu-id="64add-136">+inf</span></span> | <span data-ttu-id="64add-137">+inf</span><span class="sxs-lookup"><span data-stu-id="64add-137">+inf</span></span> |
| <span data-ttu-id="64add-138">NaN</span><span class="sxs-lookup"><span data-stu-id="64add-138">NaN</span></span>         | <span data-ttu-id="64add-139">-inf</span><span class="sxs-lookup"><span data-stu-id="64add-139">-inf</span></span> | <span data-ttu-id="64add-140">src1</span><span class="sxs-lookup"><span data-stu-id="64add-140">src1</span></span>          | <span data-ttu-id="64add-141">+inf</span><span class="sxs-lookup"><span data-stu-id="64add-141">+inf</span></span> | <span data-ttu-id="64add-142">NaN</span><span class="sxs-lookup"><span data-stu-id="64add-142">NaN</span></span>  |

<span data-ttu-id="64add-143">F bedeutet eine endliche reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="64add-143">F means finite-real number.</span></span>


## <a name="type-description"></a><span data-ttu-id="64add-144">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="64add-144">Type Description</span></span>

| <span data-ttu-id="64add-145">Name</span><span class="sxs-lookup"><span data-stu-id="64add-145">Name</span></span> | <span data-ttu-id="64add-146">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="64add-146">In/Out</span></span>      | [<span data-ttu-id="64add-147">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="64add-147">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="64add-148">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="64add-148">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="64add-149">Size</span><span class="sxs-lookup"><span data-stu-id="64add-149">Size</span></span>                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="64add-150">x</span><span class="sxs-lookup"><span data-stu-id="64add-150">x</span></span>    | <span data-ttu-id="64add-151">in</span><span class="sxs-lookup"><span data-stu-id="64add-151">in</span></span>          | <span data-ttu-id="64add-152">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="64add-152">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="64add-153">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="64add-153">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="64add-154">any</span><span class="sxs-lookup"><span data-stu-id="64add-154">any</span></span>                          |
| <span data-ttu-id="64add-155">y</span><span class="sxs-lookup"><span data-stu-id="64add-155">y</span></span>    | <span data-ttu-id="64add-156">in</span><span class="sxs-lookup"><span data-stu-id="64add-156">in</span></span>          | <span data-ttu-id="64add-157">identisch mit Eingabe x</span><span class="sxs-lookup"><span data-stu-id="64add-157">same as input x</span></span>                                                                                                | <span data-ttu-id="64add-158">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="64add-158">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="64add-159">gleiche Dimension (n) wie Eingabe x</span><span class="sxs-lookup"><span data-stu-id="64add-159">same dimension(s) as input x</span></span> |
| <span data-ttu-id="64add-160">TZI</span><span class="sxs-lookup"><span data-stu-id="64add-160">ret</span></span>  | <span data-ttu-id="64add-161">Rückgabetyp</span><span class="sxs-lookup"><span data-stu-id="64add-161">return type</span></span> | <span data-ttu-id="64add-162">identisch mit Eingabe x</span><span class="sxs-lookup"><span data-stu-id="64add-162">same as input x</span></span>                                                                                                | <span data-ttu-id="64add-163">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="64add-163">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="64add-164">gleiche Dimension (n) wie Eingabe x</span><span class="sxs-lookup"><span data-stu-id="64add-164">same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="64add-165">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="64add-165">Minimum Shader Model</span></span>

<span data-ttu-id="64add-166">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="64add-166">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="64add-167">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="64add-167">Shader Model</span></span>                                                                       | <span data-ttu-id="64add-168">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="64add-168">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="64add-169">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="64add-169">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="64add-170">ja</span><span class="sxs-lookup"><span data-stu-id="64add-170">yes</span></span>                         |
| [<span data-ttu-id="64add-171">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="64add-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="64add-172">Ja (vs \_ 1 \_ 1 und PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="64add-172">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="64add-173">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="64add-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64add-174">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="64add-174">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[<span data-ttu-id="64add-175">**DirectX-Funktionsspezifikation**</span><span class="sxs-lookup"><span data-stu-id="64add-175">**DirectX Functional Specification**</span></span>](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MAX) 
</dt> </dl>
 
