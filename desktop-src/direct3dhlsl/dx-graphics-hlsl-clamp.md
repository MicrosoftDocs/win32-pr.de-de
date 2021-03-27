---
title: gekl
description: Bindet den angegebenen Wert in den angegebenen minimalen und maximalen Bereich.
ms.assetid: bcfafcec-3f9c-4b65-950c-da34184d5cdb
keywords:
- HLSL-Klammer
topic_type:
- apiref
api_name:
- clamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5d6b0a3e83c0b1a5e511aba96df03b828b90c11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729544"
---
# <a name="clamp"></a><span data-ttu-id="464ab-104">gekl</span><span class="sxs-lookup"><span data-stu-id="464ab-104">clamp</span></span>

<span data-ttu-id="464ab-105">Bindet den angegebenen Wert in den angegebenen minimalen und maximalen Bereich.</span><span class="sxs-lookup"><span data-stu-id="464ab-105">Clamps the specified value to the specified minimum and maximum range.</span></span>



| <span data-ttu-id="464ab-106">*ret* -Klammer (*x*, *Min*, *Max*)</span><span class="sxs-lookup"><span data-stu-id="464ab-106">*ret* clamp(*x*, *min*, *max*)</span></span> |
|--------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="464ab-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="464ab-107">Parameters</span></span>



| <span data-ttu-id="464ab-108">Element</span><span class="sxs-lookup"><span data-stu-id="464ab-108">Item</span></span>                                                         | <span data-ttu-id="464ab-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="464ab-109">Description</span></span>                                    |
|--------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="464ab-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="464ab-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="464ab-111">\[in \] einem Wert, der fixiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="464ab-111">\[in\] A value to clamp.</span></span><br/>            |
| <span data-ttu-id="464ab-112"><span id="min"></span><span id="MIN"></span>*man*</span><span class="sxs-lookup"><span data-stu-id="464ab-112"><span id="min"></span><span id="MIN"></span>*min*</span></span><br/> | <span data-ttu-id="464ab-113">\[im \] angegebenen minimalen Bereich.</span><span class="sxs-lookup"><span data-stu-id="464ab-113">\[in\] The specified minimum range.</span></span><br/> |
| <span data-ttu-id="464ab-114"><span id="max"></span><span id="MAX"></span>*Max*</span><span class="sxs-lookup"><span data-stu-id="464ab-114"><span id="max"></span><span id="MAX"></span>*max*</span></span><br/> | <span data-ttu-id="464ab-115">\[im \] angegebenen maximalen Bereich.</span><span class="sxs-lookup"><span data-stu-id="464ab-115">\[in\] The specified maximum range.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="464ab-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="464ab-116">Return Value</span></span>

<span data-ttu-id="464ab-117">Der gebundene Wert für den *x* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="464ab-117">The clamped value for the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="464ab-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="464ab-118">Remarks</span></span>

<span data-ttu-id="464ab-119">Bei Werten von-INF oder INF verhält sich die Klammer wie erwartet.</span><span class="sxs-lookup"><span data-stu-id="464ab-119">For values of -INF or INF, clamp will behave as expected.</span></span> <span data-ttu-id="464ab-120">Bei Werten von Nan sind die Ergebnisse jedoch nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="464ab-120">However for values of NaN, the results are undefined.</span></span>

## <a name="type-description"></a><span data-ttu-id="464ab-121">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="464ab-121">Type Description</span></span>



| <span data-ttu-id="464ab-122">Name</span><span class="sxs-lookup"><span data-stu-id="464ab-122">Name</span></span>  | [<span data-ttu-id="464ab-123">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="464ab-123">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="464ab-124">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="464ab-124">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="464ab-125">Size</span><span class="sxs-lookup"><span data-stu-id="464ab-125">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="464ab-126">*x*</span><span class="sxs-lookup"><span data-stu-id="464ab-126">*x*</span></span>   | <span data-ttu-id="464ab-127">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="464ab-127">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="464ab-128">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="464ab-128">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="464ab-129">any</span><span class="sxs-lookup"><span data-stu-id="464ab-129">any</span></span>                            |
| <span data-ttu-id="464ab-130">*min*</span><span class="sxs-lookup"><span data-stu-id="464ab-130">*min*</span></span> | <span data-ttu-id="464ab-131">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="464ab-131">same as input *x*</span></span>                                                                                              | <span data-ttu-id="464ab-132">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="464ab-132">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="464ab-133">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="464ab-133">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="464ab-134">*max*</span><span class="sxs-lookup"><span data-stu-id="464ab-134">*max*</span></span> | <span data-ttu-id="464ab-135">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="464ab-135">same as input *x*</span></span>                                                                                              | <span data-ttu-id="464ab-136">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="464ab-136">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="464ab-137">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="464ab-137">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="464ab-138">*TZI*</span><span class="sxs-lookup"><span data-stu-id="464ab-138">*ret*</span></span> | <span data-ttu-id="464ab-139">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="464ab-139">same as input *x*</span></span>                                                                                              | <span data-ttu-id="464ab-140">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="464ab-140">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="464ab-141">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="464ab-141">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="464ab-142">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="464ab-142">Minimum Shader Model</span></span>

<span data-ttu-id="464ab-143">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="464ab-143">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="464ab-144">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="464ab-144">Shader Model</span></span>                                                                       | <span data-ttu-id="464ab-145">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="464ab-145">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="464ab-146">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="464ab-146">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="464ab-147">ja</span><span class="sxs-lookup"><span data-stu-id="464ab-147">yes</span></span>                   |
| [<span data-ttu-id="464ab-148">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="464ab-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="464ab-149">vs \_ 1 \_ 1 und PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="464ab-149">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="464ab-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="464ab-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="464ab-151">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="464ab-151">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

