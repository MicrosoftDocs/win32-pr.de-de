---
title: "\"f\" (corecrt \\_ Math. h)"
description: Gibt den Gleit Komma Rest von x/y zurück.
ms.assetid: bb940548-c4c5-4109-a488-4ea7295c7213
keywords:
- f/a-HLSL
topic_type:
- apiref
api_name:
- fmod
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9dc4367e3aa80484098e88926567953fc8e9a90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354737"
---
# <a name="fmod"></a><span data-ttu-id="ebba3-104">fmod</span><span class="sxs-lookup"><span data-stu-id="ebba3-104">fmod</span></span>

<span data-ttu-id="ebba3-105">Gibt den Gleit Komma Rest von x/y zurück.</span><span class="sxs-lookup"><span data-stu-id="ebba3-105">Returns the floating-point remainder of x/y.</span></span>



| <span data-ttu-id="ebba3-106">*ret* f (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="ebba3-106">*ret* fmod(*x*, *y*)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="ebba3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebba3-107">Parameters</span></span>



| <span data-ttu-id="ebba3-108">Element</span><span class="sxs-lookup"><span data-stu-id="ebba3-108">Item</span></span>                                                   | <span data-ttu-id="ebba3-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ebba3-109">Description</span></span>                                    |
|--------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="ebba3-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="ebba3-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="ebba3-111">\[in \] der Gleit Komma-Dividende.</span><span class="sxs-lookup"><span data-stu-id="ebba3-111">\[in\] The floating-point dividend.</span></span><br/> |
| <span data-ttu-id="ebba3-112"><span id="y"></span><span id="Y"></span>*Teenie*</span><span class="sxs-lookup"><span data-stu-id="ebba3-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="ebba3-113">\[im Gleit \] Komma Trennzeichen.</span><span class="sxs-lookup"><span data-stu-id="ebba3-113">\[in\] The floating-point divisor.</span></span><br/>  |



 

## <a name="return-value"></a><span data-ttu-id="ebba3-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ebba3-114">Return Value</span></span>

<span data-ttu-id="ebba3-115">Der Gleit Komma Rest des *x* -Parameters, dividiert durch den *y* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="ebba3-115">The floating-point remainder of the *x* parameter divided by the *y* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebba3-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ebba3-116">Remarks</span></span>

<span data-ttu-id="ebba3-117">Der Gleit Komma Rest wird so berechnet, dass x = i \* y + f, wobei es sich um eine ganze Zahl handelt, f dasselbe Vorzeichen wie x hat und der absolute Wert von f kleiner ist als der absolute Wert von y.</span><span class="sxs-lookup"><span data-stu-id="ebba3-117">The floating-point remainder is calculated such that x = i \* y + f, where i is an integer, f has the same sign as x, and the absolute value of f is less than the absolute value of y.</span></span>

## <a name="type-description"></a><span data-ttu-id="ebba3-118">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="ebba3-118">Type Description</span></span>



| <span data-ttu-id="ebba3-119">Name</span><span class="sxs-lookup"><span data-stu-id="ebba3-119">Name</span></span>  | [<span data-ttu-id="ebba3-120">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="ebba3-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="ebba3-121">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="ebba3-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="ebba3-122">Size</span><span class="sxs-lookup"><span data-stu-id="ebba3-122">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="ebba3-123">*x*</span><span class="sxs-lookup"><span data-stu-id="ebba3-123">*x*</span></span>   | <span data-ttu-id="ebba3-124">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="ebba3-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="ebba3-125">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="ebba3-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ebba3-126">any</span><span class="sxs-lookup"><span data-stu-id="ebba3-126">any</span></span>                            |
| <span data-ttu-id="ebba3-127">*y*</span><span class="sxs-lookup"><span data-stu-id="ebba3-127">*y*</span></span>   | <span data-ttu-id="ebba3-128">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="ebba3-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="ebba3-129">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="ebba3-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ebba3-130">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="ebba3-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="ebba3-131">*TZI*</span><span class="sxs-lookup"><span data-stu-id="ebba3-131">*ret*</span></span> | <span data-ttu-id="ebba3-132">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="ebba3-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="ebba3-133">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="ebba3-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ebba3-134">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="ebba3-134">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ebba3-135">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="ebba3-135">Minimum Shader Model</span></span>

<span data-ttu-id="ebba3-136">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ebba3-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ebba3-137">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="ebba3-137">Shader Model</span></span>                                                                       | <span data-ttu-id="ebba3-138">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ebba3-138">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="ebba3-139">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="ebba3-139">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="ebba3-140">ja</span><span class="sxs-lookup"><span data-stu-id="ebba3-140">yes</span></span>       |
| [<span data-ttu-id="ebba3-141">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ebba3-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="ebba3-142">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ebba3-142">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="ebba3-143">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ebba3-143">Requirements</span></span>



| <span data-ttu-id="ebba3-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ebba3-144">Requirement</span></span> | <span data-ttu-id="ebba3-145">Wert</span><span class="sxs-lookup"><span data-stu-id="ebba3-145">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebba3-146">Header</span><span class="sxs-lookup"><span data-stu-id="ebba3-146">Header</span></span><br/> | <dl> <span data-ttu-id="ebba3-147"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebba3-147"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebba3-148">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ebba3-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebba3-149">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="ebba3-149">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

