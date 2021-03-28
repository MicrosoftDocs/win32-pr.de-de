---
title: frexp (corecrt \_ Math. h)
description: Gibt die Mantisse und den Exponenten des angegebenen Gleit Komma Werts zurück.
ms.assetid: 9252feff-da85-4b3e-97db-1fcddd786695
keywords:
- frexp HLSL
topic_type:
- apiref
api_name:
- frexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bddbcbbf9e97aff739bb06a0f0d0ddac12134463
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961596"
---
# <a name="frexp"></a><span data-ttu-id="fcb72-104">frexp</span><span class="sxs-lookup"><span data-stu-id="fcb72-104">frexp</span></span>

<span data-ttu-id="fcb72-105">Gibt die Mantisse und den Exponenten des angegebenen Gleit Komma Werts zurück.</span><span class="sxs-lookup"><span data-stu-id="fcb72-105">Returns the mantissa and exponent of the specified floating-point value.</span></span>



| <span data-ttu-id="fcb72-106">*ret* frexp (*x*, *Exp*)</span><span class="sxs-lookup"><span data-stu-id="fcb72-106">*ret* frexp(*x*, *exp*)</span></span> |
|-------------------------|



 

<span data-ttu-id="fcb72-107">Der Rückgabewert ist die Mantisse, und der vom *Exp* -Parameter zurückgegebene Wert ist der Exponent.</span><span class="sxs-lookup"><span data-stu-id="fcb72-107">The return value is the mantissa, and the value returned by *exp* parameter is the exponent.</span></span>

## <a name="parameters"></a><span data-ttu-id="fcb72-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcb72-108">Parameters</span></span>



| <span data-ttu-id="fcb72-109">Element</span><span class="sxs-lookup"><span data-stu-id="fcb72-109">Item</span></span>                                                         | <span data-ttu-id="fcb72-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fcb72-110">Description</span></span>                                                                                                                                      |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcb72-111"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="fcb72-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="fcb72-112">\[im \] angegebenen Gleit Komma Wert.</span><span class="sxs-lookup"><span data-stu-id="fcb72-112">\[in\] The specified floating-point value.</span></span> <span data-ttu-id="fcb72-113">Wenn der *x* -Parameter 0 (null) ist, gibt diese Funktion für die Mantisse und den Exponenten 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="fcb72-113">If the *x* parameter is 0, this function returns 0 for both the mantissa and the exponent.</span></span><br/> |
| <span data-ttu-id="fcb72-114"><span id="exp"></span><span id="EXP"></span>*Exp*</span><span class="sxs-lookup"><span data-stu-id="fcb72-114"><span id="exp"></span><span id="EXP"></span>*exp*</span></span><br/> | <span data-ttu-id="fcb72-115">\[\]der zurückgegebene Exponent des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="fcb72-115">\[out\] The returned exponent of the *x* parameter.</span></span><br/>                                                                                   |



 

## <a name="return-value"></a><span data-ttu-id="fcb72-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fcb72-116">Return Value</span></span>

<span data-ttu-id="fcb72-117">Die Mantisse des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="fcb72-117">The mantissa of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="fcb72-118">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="fcb72-118">Type Description</span></span>



| <span data-ttu-id="fcb72-119">Name</span><span class="sxs-lookup"><span data-stu-id="fcb72-119">Name</span></span>  | [<span data-ttu-id="fcb72-120">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="fcb72-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="fcb72-121">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="fcb72-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="fcb72-122">Size</span><span class="sxs-lookup"><span data-stu-id="fcb72-122">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="fcb72-123">*x*</span><span class="sxs-lookup"><span data-stu-id="fcb72-123">*x*</span></span>   | <span data-ttu-id="fcb72-124">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="fcb72-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="fcb72-125">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="fcb72-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="fcb72-126">any</span><span class="sxs-lookup"><span data-stu-id="fcb72-126">any</span></span>                            |
| <span data-ttu-id="fcb72-127">*exp*</span><span class="sxs-lookup"><span data-stu-id="fcb72-127">*exp*</span></span> | <span data-ttu-id="fcb72-128">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="fcb72-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="fcb72-129">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="fcb72-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="fcb72-130">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="fcb72-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="fcb72-131">*TZI*</span><span class="sxs-lookup"><span data-stu-id="fcb72-131">*ret*</span></span> | <span data-ttu-id="fcb72-132">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="fcb72-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="fcb72-133">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="fcb72-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="fcb72-134">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="fcb72-134">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fcb72-135">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="fcb72-135">Minimum Shader Model</span></span>

<span data-ttu-id="fcb72-136">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fcb72-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fcb72-137">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="fcb72-137">Shader Model</span></span>                                                                       | <span data-ttu-id="fcb72-138">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="fcb72-138">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="fcb72-139">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="fcb72-139">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) and higher shader models</span></span> | <span data-ttu-id="fcb72-140">ja</span><span class="sxs-lookup"><span data-stu-id="fcb72-140">yes</span></span>                 |
| [<span data-ttu-id="fcb72-141">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fcb72-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                          | <span data-ttu-id="fcb72-142">Ja ( \_ nur PS 2 \_ x)</span><span class="sxs-lookup"><span data-stu-id="fcb72-142">yes (ps\_2\_x only)</span></span> |
| [<span data-ttu-id="fcb72-143">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fcb72-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="fcb72-144">nein</span><span class="sxs-lookup"><span data-stu-id="fcb72-144">no</span></span>                  |



 

## <a name="remarks"></a><span data-ttu-id="fcb72-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fcb72-145">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="fcb72-146">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="fcb72-146">Requirements</span></span>



| <span data-ttu-id="fcb72-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fcb72-147">Requirement</span></span> | <span data-ttu-id="fcb72-148">Wert</span><span class="sxs-lookup"><span data-stu-id="fcb72-148">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcb72-149">Header</span><span class="sxs-lookup"><span data-stu-id="fcb72-149">Header</span></span><br/> | <dl> <span data-ttu-id="fcb72-150"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcb72-150"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcb72-151">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fcb72-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcb72-152">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="fcb72-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

