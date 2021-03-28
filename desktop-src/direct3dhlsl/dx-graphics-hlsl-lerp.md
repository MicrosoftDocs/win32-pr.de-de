---
title: Lerp
description: Führt eine lineare interpolung aus.
ms.assetid: e369f182-b5bd-4b7f-aa77-9cfe11033bc4
keywords:
- Lerp HLSL
topic_type:
- apiref
api_name:
- lerp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c7a5251aaf410d7224b87b9ee9a8f0e8a0c947e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993431"
---
# <a name="lerp"></a><span data-ttu-id="22a42-104">Lerp</span><span class="sxs-lookup"><span data-stu-id="22a42-104">lerp</span></span>

<span data-ttu-id="22a42-105">Führt eine lineare interpolung aus.</span><span class="sxs-lookup"><span data-stu-id="22a42-105">Performs a linear interpolation.</span></span>



| <span data-ttu-id="22a42-106">*ret* Lerp (*x*, *y*, *s*)</span><span class="sxs-lookup"><span data-stu-id="22a42-106">*ret* lerp(*x*, *y*, *s*)</span></span> |
|---------------------------|



 

## <a name="parameters"></a><span data-ttu-id="22a42-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="22a42-107">Parameters</span></span>



| <span data-ttu-id="22a42-108">Element</span><span class="sxs-lookup"><span data-stu-id="22a42-108">Item</span></span>                                                   | <span data-ttu-id="22a42-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22a42-109">Description</span></span>                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22a42-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="22a42-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="22a42-111">\[im \] ersten Gleit Komma Wert.</span><span class="sxs-lookup"><span data-stu-id="22a42-111">\[in\] The first-floating point value.</span></span><br/>                                                     |
| <span data-ttu-id="22a42-112"><span id="y"></span><span id="Y"></span>*Teenie*</span><span class="sxs-lookup"><span data-stu-id="22a42-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="22a42-113">\[im \] zweiten Gleit Komma Wert.</span><span class="sxs-lookup"><span data-stu-id="22a42-113">\[in\] The second-floating point value.</span></span><br/>                                                    |
| <span data-ttu-id="22a42-114"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="22a42-114"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="22a42-115">\[in \] einem Wert, der linear zwischen dem *x* -Parameter und dem *y* -Parameter interpoliert.</span><span class="sxs-lookup"><span data-stu-id="22a42-115">\[in\] A value that linearly interpolates between the *x* parameter and the *y* parameter.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="22a42-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22a42-116">Return Value</span></span>

<span data-ttu-id="22a42-117">Das Ergebnis der linearen interpolung.</span><span class="sxs-lookup"><span data-stu-id="22a42-117">The result of the linear interpolation.</span></span>

## <a name="type-description"></a><span data-ttu-id="22a42-118">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="22a42-118">Type Description</span></span>



| <span data-ttu-id="22a42-119">Name</span><span class="sxs-lookup"><span data-stu-id="22a42-119">Name</span></span>  | [<span data-ttu-id="22a42-120">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="22a42-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="22a42-121">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="22a42-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="22a42-122">Size</span><span class="sxs-lookup"><span data-stu-id="22a42-122">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="22a42-123">*x*</span><span class="sxs-lookup"><span data-stu-id="22a42-123">*x*</span></span>   | <span data-ttu-id="22a42-124">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="22a42-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="22a42-125">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="22a42-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="22a42-126">any</span><span class="sxs-lookup"><span data-stu-id="22a42-126">any</span></span>                            |
| <span data-ttu-id="22a42-127">*y*</span><span class="sxs-lookup"><span data-stu-id="22a42-127">*y*</span></span>   | <span data-ttu-id="22a42-128">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="22a42-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="22a42-129">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="22a42-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="22a42-130">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="22a42-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="22a42-131">*s*</span><span class="sxs-lookup"><span data-stu-id="22a42-131">*s*</span></span>   | <span data-ttu-id="22a42-132">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="22a42-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="22a42-133">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="22a42-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="22a42-134">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="22a42-134">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="22a42-135">*TZI*</span><span class="sxs-lookup"><span data-stu-id="22a42-135">*ret*</span></span> | <span data-ttu-id="22a42-136">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="22a42-136">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="22a42-137">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="22a42-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="22a42-138">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="22a42-138">same dimension(s) as input *x*</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="22a42-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22a42-139">Remarks</span></span>

<span data-ttu-id="22a42-140">Die lineare interpolung basiert auf der folgenden Formel: x \* (1-s) + y \* s, die gleichwertig als x + s (y-x) geschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="22a42-140">Linear interpolation is based on the following formula: x\*(1-s) + y\*s which can equivalently be written as x + s(y-x).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="22a42-141">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="22a42-141">Minimum Shader Model</span></span>

<span data-ttu-id="22a42-142">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="22a42-142">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="22a42-143">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="22a42-143">Shader Model</span></span>                                                                       | <span data-ttu-id="22a42-144">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="22a42-144">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="22a42-145">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="22a42-145">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="22a42-146">ja</span><span class="sxs-lookup"><span data-stu-id="22a42-146">yes</span></span>                         |
| [<span data-ttu-id="22a42-147">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="22a42-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="22a42-148">Ja (vs \_ 1 \_ 1 und PS \_ 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="22a42-148">yes (vs\_1\_1 and ps\_1\_1)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="22a42-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="22a42-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22a42-150">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="22a42-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

