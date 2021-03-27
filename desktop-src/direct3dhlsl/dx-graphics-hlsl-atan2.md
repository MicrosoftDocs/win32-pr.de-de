---
title: atan2 (corecrt \_ Math. h)
description: Gibt den Arkus Tangens von zwei Werten (x, y) zurück.
ms.assetid: e7b53751-f321-4390-8f8f-ec1fa3aaa798
keywords:
- atan2 HLSL
topic_type:
- apiref
api_name:
- atan2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52fbc6574d0fc0d53a165ae7da87c2627a295be4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219504"
---
# <a name="atan2"></a><span data-ttu-id="d34fe-104">atan2</span><span class="sxs-lookup"><span data-stu-id="d34fe-104">atan2</span></span>

<span data-ttu-id="d34fe-105">Gibt den Arkus Tangens von zwei Werten (x, y) zurück.</span><span class="sxs-lookup"><span data-stu-id="d34fe-105">Returns the arctangent of two values (x,y).</span></span>



| <span data-ttu-id="d34fe-106">*ret* atan2 (*y*, *x*)</span><span class="sxs-lookup"><span data-stu-id="d34fe-106">*ret* atan2(*y*, *x*)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="d34fe-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d34fe-107">Parameters</span></span>



| <span data-ttu-id="d34fe-108">Element</span><span class="sxs-lookup"><span data-stu-id="d34fe-108">Item</span></span>                                                   | <span data-ttu-id="d34fe-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d34fe-109">Description</span></span>                    |
|--------------------------------------------------------|--------------------------------|
| <span data-ttu-id="d34fe-110"><span id="y"></span><span id="Y"></span>*Teenie*</span><span class="sxs-lookup"><span data-stu-id="d34fe-110"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="d34fe-111">\[im \] y-Wert.</span><span class="sxs-lookup"><span data-stu-id="d34fe-111">\[in\] The y value.</span></span><br/> |
| <span data-ttu-id="d34fe-112"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="d34fe-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="d34fe-113">\[im \] x-Wert.</span><span class="sxs-lookup"><span data-stu-id="d34fe-113">\[in\] The x value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d34fe-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d34fe-114">Return Value</span></span>

<span data-ttu-id="d34fe-115">Der Arkus Tangens von (y, x).</span><span class="sxs-lookup"><span data-stu-id="d34fe-115">The arctangent of (y,x).</span></span>

## <a name="remarks"></a><span data-ttu-id="d34fe-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d34fe-116">Remarks</span></span>

<span data-ttu-id="d34fe-117">Die Vorzeichen der *x* -und *y* -Parameter werden verwendet, um den Quadranten der Rückgabewerte innerhalb des Bereichs von bis Adressierung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="d34fe-117">The signs of the *x* and *y* parameters are used to determine the quadrant of the return values within the range of -π to π.</span></span> <span data-ttu-id="d34fe-118">Die intrinsische Funktion **atan2** HLSL ist für jeden anderen Punkt als den Ursprung klar definiert, auch wenn *y* gleich 0 und *x* nicht gleich 0 ist.</span><span class="sxs-lookup"><span data-stu-id="d34fe-118">The **atan2** HLSL intrinsic function is well-defined for every point other than the origin, even if *y* equals 0 and *x* does not equal 0.</span></span>

## <a name="type-description"></a><span data-ttu-id="d34fe-119">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="d34fe-119">Type Description</span></span>



| <span data-ttu-id="d34fe-120">Name</span><span class="sxs-lookup"><span data-stu-id="d34fe-120">Name</span></span>  | [<span data-ttu-id="d34fe-121">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="d34fe-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="d34fe-122">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="d34fe-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d34fe-123">Size</span><span class="sxs-lookup"><span data-stu-id="d34fe-123">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="d34fe-124">*y*</span><span class="sxs-lookup"><span data-stu-id="d34fe-124">*y*</span></span>   | <span data-ttu-id="d34fe-125">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="d34fe-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="d34fe-126">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="d34fe-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d34fe-127">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="d34fe-127">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="d34fe-128">*x*</span><span class="sxs-lookup"><span data-stu-id="d34fe-128">*x*</span></span>   | <span data-ttu-id="d34fe-129">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="d34fe-129">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="d34fe-130">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="d34fe-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d34fe-131">any</span><span class="sxs-lookup"><span data-stu-id="d34fe-131">any</span></span>                            |
| <span data-ttu-id="d34fe-132">*TZI*</span><span class="sxs-lookup"><span data-stu-id="d34fe-132">*ret*</span></span> | <span data-ttu-id="d34fe-133">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="d34fe-133">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="d34fe-134">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="d34fe-134">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d34fe-135">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="d34fe-135">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d34fe-136">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="d34fe-136">Minimum Shader Model</span></span>

<span data-ttu-id="d34fe-137">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d34fe-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d34fe-138">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="d34fe-138">Shader Model</span></span>                                                                       | <span data-ttu-id="d34fe-139">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="d34fe-139">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="d34fe-140">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="d34fe-140">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="d34fe-141">ja</span><span class="sxs-lookup"><span data-stu-id="d34fe-141">yes</span></span>       |
| [<span data-ttu-id="d34fe-142">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d34fe-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="d34fe-143">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d34fe-143">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="d34fe-144">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d34fe-144">Requirements</span></span>



| <span data-ttu-id="d34fe-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d34fe-145">Requirement</span></span> | <span data-ttu-id="d34fe-146">Wert</span><span class="sxs-lookup"><span data-stu-id="d34fe-146">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d34fe-147">Header</span><span class="sxs-lookup"><span data-stu-id="d34fe-147">Header</span></span><br/> | <dl> <span data-ttu-id="d34fe-148"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d34fe-148"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d34fe-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d34fe-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d34fe-150">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d34fe-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

