---
title: LDE XP (corecrt \_ Math. h)
description: Gibt das Ergebnis der Multiplikation des angegebenen Werts mit zwei Werten zurück, die auf die Potenz des angegebenen Exponenten zurückzuführen sind.
ms.assetid: 6d6fee96-f952-4058-a1ac-3abb98dbd540
keywords:
- LDE XP HLSL
topic_type:
- apiref
api_name:
- ldexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 731cb5cbf933ea3f8754a7d70b9ef0b7a54e783b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870139"
---
# <a name="ldexp"></a><span data-ttu-id="0bc04-104">ldexp</span><span class="sxs-lookup"><span data-stu-id="0bc04-104">ldexp</span></span>

<span data-ttu-id="0bc04-105">Gibt das Ergebnis der Multiplikation des angegebenen Werts mit zwei Werten zurück, die auf die Potenz des angegebenen Exponenten zurückzuführen sind.</span><span class="sxs-lookup"><span data-stu-id="0bc04-105">Returns the result of multiplying the specified value by two, raised to the power of the specified exponent.</span></span>



| <span data-ttu-id="0bc04-106">*ret* LDE XP (*x*, *Exp*)</span><span class="sxs-lookup"><span data-stu-id="0bc04-106">*ret* ldexp(*x*, *exp*)</span></span> |
|-------------------------|



 

<span data-ttu-id="0bc04-107">Diese Funktion verwendet die folgende Formel: *x* \* 2 <sup>Exp</sup></span><span class="sxs-lookup"><span data-stu-id="0bc04-107">This function uses the following formula: *x* \* 2<sup>exp</sup></span></span>

## <a name="parameters"></a><span data-ttu-id="0bc04-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0bc04-108">Parameters</span></span>



| <span data-ttu-id="0bc04-109">Element</span><span class="sxs-lookup"><span data-stu-id="0bc04-109">Item</span></span>                                                         | <span data-ttu-id="0bc04-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0bc04-110">Description</span></span>                               |
|--------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="0bc04-111"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="0bc04-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="0bc04-112">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="0bc04-112">\[in\] The specified value.</span></span><br/>    |
| <span data-ttu-id="0bc04-113"><span id="exp"></span><span id="EXP"></span>*Exp*</span><span class="sxs-lookup"><span data-stu-id="0bc04-113"><span id="exp"></span><span id="EXP"></span>*exp*</span></span><br/> | <span data-ttu-id="0bc04-114">\[im \] angegebenen Exponenten.</span><span class="sxs-lookup"><span data-stu-id="0bc04-114">\[in\] The specified exponent.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="0bc04-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0bc04-115">Return Value</span></span>

<span data-ttu-id="0bc04-116">Das Ergebnis der Multiplikation des *x* -Parameters mit zwei Werten, die durch den *Exp* -Parameter ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="0bc04-116">The result of multiplying the *x* parameter by two, raised to the power of the *exp* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="0bc04-117">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="0bc04-117">Type Description</span></span>



| <span data-ttu-id="0bc04-118">Name</span><span class="sxs-lookup"><span data-stu-id="0bc04-118">Name</span></span>  | [<span data-ttu-id="0bc04-119">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="0bc04-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="0bc04-120">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="0bc04-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="0bc04-121">Size</span><span class="sxs-lookup"><span data-stu-id="0bc04-121">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="0bc04-122">*x*</span><span class="sxs-lookup"><span data-stu-id="0bc04-122">*x*</span></span>   | <span data-ttu-id="0bc04-123">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="0bc04-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="0bc04-124">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="0bc04-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0bc04-125">any</span><span class="sxs-lookup"><span data-stu-id="0bc04-125">any</span></span>                            |
| <span data-ttu-id="0bc04-126">*exp*</span><span class="sxs-lookup"><span data-stu-id="0bc04-126">*exp*</span></span> | <span data-ttu-id="0bc04-127">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="0bc04-127">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="0bc04-128">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="0bc04-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0bc04-129">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="0bc04-129">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="0bc04-130">*TZI*</span><span class="sxs-lookup"><span data-stu-id="0bc04-130">*ret*</span></span> | <span data-ttu-id="0bc04-131">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="0bc04-131">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="0bc04-132">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="0bc04-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0bc04-133">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="0bc04-133">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0bc04-134">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="0bc04-134">Minimum Shader Model</span></span>

<span data-ttu-id="0bc04-135">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0bc04-135">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0bc04-136">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="0bc04-136">Shader Model</span></span>                                                                       | <span data-ttu-id="0bc04-137">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="0bc04-137">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="0bc04-138">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="0bc04-138">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="0bc04-139">ja</span><span class="sxs-lookup"><span data-stu-id="0bc04-139">yes</span></span>                 |
| [<span data-ttu-id="0bc04-140">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bc04-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="0bc04-141">Ja ( \_ nur vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="0bc04-141">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="0bc04-142">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0bc04-142">Requirements</span></span>



| <span data-ttu-id="0bc04-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0bc04-143">Requirement</span></span> | <span data-ttu-id="0bc04-144">Wert</span><span class="sxs-lookup"><span data-stu-id="0bc04-144">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bc04-145">Header</span><span class="sxs-lookup"><span data-stu-id="0bc04-145">Header</span></span><br/> | <dl> <span data-ttu-id="0bc04-146"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bc04-146"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bc04-147">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0bc04-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bc04-148">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="0bc04-148">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

