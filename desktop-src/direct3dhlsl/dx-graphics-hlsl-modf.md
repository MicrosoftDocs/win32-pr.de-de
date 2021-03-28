---
title: modf (corecrt \_ Math. h)
description: Teilt den Wert x in Bruchteile und ganzzahlige Teile auf, von denen jedes dasselbe Vorzeichen wie x hat.
ms.assetid: 0cac1cf3-f0da-4b0a-ba30-4af5d65b04b2
keywords:
- modf HLSL
topic_type:
- apiref
api_name:
- modf
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5079549e70414f8237fd33a5e263dd8f17dcb9e3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961645"
---
# <a name="modf"></a><span data-ttu-id="c9969-104">modf</span><span class="sxs-lookup"><span data-stu-id="c9969-104">modf</span></span>

<span data-ttu-id="c9969-105">Teilt den Wert x in Bruchteile und ganzzahlige Teile auf, von denen jedes dasselbe Vorzeichen wie x hat.</span><span class="sxs-lookup"><span data-stu-id="c9969-105">Splits the value x into fractional and integer parts, each of which has the same sign as x.</span></span>



| <span data-ttu-id="c9969-106">Ret modf (x, out-IP)</span><span class="sxs-lookup"><span data-stu-id="c9969-106">ret modf(x, out ip)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="c9969-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9969-107">Parameters</span></span>



| <span data-ttu-id="c9969-108">Element</span><span class="sxs-lookup"><span data-stu-id="c9969-108">Item</span></span>                                                      | <span data-ttu-id="c9969-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c9969-109">Description</span></span>                                    |
|-----------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="c9969-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="c9969-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/>    | <span data-ttu-id="c9969-111">\[im \] x-Eingabe Wert.</span><span class="sxs-lookup"><span data-stu-id="c9969-111">\[in\] The x input value.</span></span><br/>           |
| <span data-ttu-id="c9969-112"><span id="ip"></span><span id="IP"></span>*-*</span><span class="sxs-lookup"><span data-stu-id="c9969-112"><span id="ip"></span><span id="IP"></span>*ip*</span></span><br/> | <span data-ttu-id="c9969-113">\[\]der ganzzahlige Teil von *x*.</span><span class="sxs-lookup"><span data-stu-id="c9969-113">\[out\] The integer portion of *x*.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="c9969-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9969-114">Return Value</span></span>

<span data-ttu-id="c9969-115">Der Teil mit Vorzeichen von x.</span><span class="sxs-lookup"><span data-stu-id="c9969-115">The signed-fractional portion of x.</span></span>

## <a name="type-description"></a><span data-ttu-id="c9969-116">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="c9969-116">Type Description</span></span>



| <span data-ttu-id="c9969-117">Name</span><span class="sxs-lookup"><span data-stu-id="c9969-117">Name</span></span> | <span data-ttu-id="c9969-118">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="c9969-118">In/Out</span></span> | [<span data-ttu-id="c9969-119">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="c9969-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="c9969-120">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="c9969-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="c9969-121">Size</span><span class="sxs-lookup"><span data-stu-id="c9969-121">Size</span></span>                         |
|------|--------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="c9969-122">x</span><span class="sxs-lookup"><span data-stu-id="c9969-122">x</span></span>    | <span data-ttu-id="c9969-123">in</span><span class="sxs-lookup"><span data-stu-id="c9969-123">in</span></span>     | <span data-ttu-id="c9969-124">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="c9969-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="c9969-125">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c9969-125">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="c9969-126">any</span><span class="sxs-lookup"><span data-stu-id="c9969-126">any</span></span>                          |
| <span data-ttu-id="c9969-127">ip</span><span class="sxs-lookup"><span data-stu-id="c9969-127">ip</span></span>   | <span data-ttu-id="c9969-128">out</span><span class="sxs-lookup"><span data-stu-id="c9969-128">out</span></span>    | <span data-ttu-id="c9969-129">identisch mit Eingabe x</span><span class="sxs-lookup"><span data-stu-id="c9969-129">same as input x</span></span>                                                                                                | <span data-ttu-id="c9969-130">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c9969-130">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="c9969-131">gleiche Dimension (n) wie Eingabe x</span><span class="sxs-lookup"><span data-stu-id="c9969-131">same dimension(s) as input x</span></span> |
| <span data-ttu-id="c9969-132">TZI</span><span class="sxs-lookup"><span data-stu-id="c9969-132">ret</span></span>  | <span data-ttu-id="c9969-133">out</span><span class="sxs-lookup"><span data-stu-id="c9969-133">out</span></span>    | <span data-ttu-id="c9969-134">identisch mit Eingabe x</span><span class="sxs-lookup"><span data-stu-id="c9969-134">same as input x</span></span>                                                                                                | <span data-ttu-id="c9969-135">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c9969-135">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="c9969-136">gleiche Dimension (n) wie Eingabe x</span><span class="sxs-lookup"><span data-stu-id="c9969-136">same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c9969-137">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="c9969-137">Minimum Shader Model</span></span>

<span data-ttu-id="c9969-138">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9969-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c9969-139">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="c9969-139">Shader Model</span></span>                                                                       | <span data-ttu-id="c9969-140">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="c9969-140">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="c9969-141">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="c9969-141">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="c9969-142">ja</span><span class="sxs-lookup"><span data-stu-id="c9969-142">yes</span></span>                 |
| [<span data-ttu-id="c9969-143">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c9969-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="c9969-144">Ja ( \_ nur vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="c9969-144">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="c9969-145">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c9969-145">Requirements</span></span>



| <span data-ttu-id="c9969-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9969-146">Requirement</span></span> | <span data-ttu-id="c9969-147">Wert</span><span class="sxs-lookup"><span data-stu-id="c9969-147">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9969-148">Header</span><span class="sxs-lookup"><span data-stu-id="c9969-148">Header</span></span><br/> | <dl> <span data-ttu-id="c9969-149"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9969-149"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9969-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c9969-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9969-151">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="c9969-151">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

