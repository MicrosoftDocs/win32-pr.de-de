---
title: Schritt
description: Vergleicht zwei Werte, wobei 0 oder 1 zurückgegeben wird, je nachdem, welcher Wert größer ist.
ms.assetid: 1c1c4ec4-ae97-42ce-99af-71903e0b5edf
keywords:
- Schritt HLSL
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f9c800e8d8c6f78386139f822f118163f3b431f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729528"
---
# <a name="step"></a><span data-ttu-id="ab8cf-104">Schritt</span><span class="sxs-lookup"><span data-stu-id="ab8cf-104">step</span></span>

<span data-ttu-id="ab8cf-105">Vergleicht zwei Werte, wobei 0 oder 1 zurückgegeben wird, je nachdem, welcher Wert größer ist.</span><span class="sxs-lookup"><span data-stu-id="ab8cf-105">Compares two values, returning 0 or 1 based on which value is greater.</span></span>



| <span data-ttu-id="ab8cf-106">*ret* -Schritt (*y*, *x*)</span><span class="sxs-lookup"><span data-stu-id="ab8cf-106">*ret* step(*y*, *x*)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="ab8cf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab8cf-107">Parameters</span></span>



| <span data-ttu-id="ab8cf-108">Element</span><span class="sxs-lookup"><span data-stu-id="ab8cf-108">Item</span></span>                                                   | <span data-ttu-id="ab8cf-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab8cf-109">Description</span></span>                                                   |
|--------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="ab8cf-110"><span id="y"></span><span id="Y"></span>*Teenie*</span><span class="sxs-lookup"><span data-stu-id="ab8cf-110"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="ab8cf-111">\[\]der erste zu vergleichende Gleit Komma Wert.</span><span class="sxs-lookup"><span data-stu-id="ab8cf-111">\[in\] The first floating-point value to compare.</span></span><br/>  |
| <span data-ttu-id="ab8cf-112"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="ab8cf-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="ab8cf-113">\[im \] zweiten zu vergleichenden Gleit Komma Wert.</span><span class="sxs-lookup"><span data-stu-id="ab8cf-113">\[in\] The second floating-point value to compare.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="ab8cf-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab8cf-114">Return Value</span></span>

<span data-ttu-id="ab8cf-115">1, wenn der *x* -Parameter größer oder gleich dem *y* -Parameter ist. andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="ab8cf-115">1 if the *x* parameter is greater than or equal to the *y* parameter; otherwise, 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab8cf-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab8cf-116">Remarks</span></span>

<span data-ttu-id="ab8cf-117">Diese Funktion verwendet die folgende Formel: (*x*  >=  *y*)?</span><span class="sxs-lookup"><span data-stu-id="ab8cf-117">This function uses the following formula: (*x* >= *y*) ?</span></span> <span data-ttu-id="ab8cf-118">1:0.</span><span class="sxs-lookup"><span data-stu-id="ab8cf-118">1 : 0.</span></span> <span data-ttu-id="ab8cf-119">Die-Funktion gibt entweder 0 oder 1 zurück, je nachdem, ob der *x* -Parameter größer als der *y* -Parameter ist.</span><span class="sxs-lookup"><span data-stu-id="ab8cf-119">The function returns either 0 or 1 depending on whether the *x* parameter is greater than the *y* parameter.</span></span> <span data-ttu-id="ab8cf-120">Verwenden Sie die systeminterne Funktion " [**smoothstep**](dx-graphics-hlsl-smoothstep.md) HLSL", um eine reibungslose interpolsierung zwischen 0 und 1 zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="ab8cf-120">To compute a smooth interpolation between 0 and 1, use the [**smoothstep**](dx-graphics-hlsl-smoothstep.md) HLSL intrinsic function.</span></span>

## <a name="type-description"></a><span data-ttu-id="ab8cf-121">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="ab8cf-121">Type Description</span></span>



| <span data-ttu-id="ab8cf-122">Name</span><span class="sxs-lookup"><span data-stu-id="ab8cf-122">Name</span></span>  | [<span data-ttu-id="ab8cf-123">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="ab8cf-123">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="ab8cf-124">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="ab8cf-124">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="ab8cf-125">Size</span><span class="sxs-lookup"><span data-stu-id="ab8cf-125">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="ab8cf-126">*y*</span><span class="sxs-lookup"><span data-stu-id="ab8cf-126">*y*</span></span>   | <span data-ttu-id="ab8cf-127">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="ab8cf-127">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="ab8cf-128">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="ab8cf-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ab8cf-129">any</span><span class="sxs-lookup"><span data-stu-id="ab8cf-129">any</span></span>                            |
| <span data-ttu-id="ab8cf-130">*x*</span><span class="sxs-lookup"><span data-stu-id="ab8cf-130">*x*</span></span>   | <span data-ttu-id="ab8cf-131">identisch mit der Eingabe *y*</span><span class="sxs-lookup"><span data-stu-id="ab8cf-131">same as input *y*</span></span>                                                                                              | [<span data-ttu-id="ab8cf-132">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="ab8cf-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ab8cf-133">gleiche Dimension (n) wie Eingabe *y*</span><span class="sxs-lookup"><span data-stu-id="ab8cf-133">same dimension(s) as input *y*</span></span> |
| <span data-ttu-id="ab8cf-134">*TZI*</span><span class="sxs-lookup"><span data-stu-id="ab8cf-134">*ret*</span></span> | <span data-ttu-id="ab8cf-135">identisch mit der Eingabe *y*</span><span class="sxs-lookup"><span data-stu-id="ab8cf-135">same as input *y*</span></span>                                                                                              | [<span data-ttu-id="ab8cf-136">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="ab8cf-136">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ab8cf-137">gleiche Dimension (n) wie Eingabe *y*</span><span class="sxs-lookup"><span data-stu-id="ab8cf-137">same dimension(s) as input *y*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ab8cf-138">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="ab8cf-138">Minimum Shader Model</span></span>

<span data-ttu-id="ab8cf-139">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ab8cf-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ab8cf-140">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="ab8cf-140">Shader Model</span></span>                                                                       | <span data-ttu-id="ab8cf-141">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ab8cf-141">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="ab8cf-142">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="ab8cf-142">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="ab8cf-143">ja</span><span class="sxs-lookup"><span data-stu-id="ab8cf-143">yes</span></span>                         |
| [<span data-ttu-id="ab8cf-144">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ab8cf-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="ab8cf-145">Ja (vs \_ 1 \_ 1 und PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="ab8cf-145">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="ab8cf-146">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ab8cf-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab8cf-147">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="ab8cf-147">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

