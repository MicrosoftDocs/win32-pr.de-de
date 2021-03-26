---
title: SinCos
description: Gibt den Sinus und Kosinus von x zurück.
ms.assetid: 2ef9e84e-4539-47f5-9966-d8e02ca15d36
keywords:
- SinCos HLSL
topic_type:
- apiref
api_name:
- sincos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8391c2fcecc939db1d7044fe56fbd281fe3e79fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993542"
---
# <a name="sincos"></a><span data-ttu-id="45ed1-104">SinCos</span><span class="sxs-lookup"><span data-stu-id="45ed1-104">sincos</span></span>

<span data-ttu-id="45ed1-105">Gibt den Sinus und Kosinus von x zurück.</span><span class="sxs-lookup"><span data-stu-id="45ed1-105">Returns the sine and cosine of x.</span></span>



| <span data-ttu-id="45ed1-106">SinCos (*x*, out *s*, out *c*)</span><span class="sxs-lookup"><span data-stu-id="45ed1-106">sincos(*x*, out *s*, out *c*)</span></span> |
|-------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="45ed1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="45ed1-107">Parameters</span></span>



| <span data-ttu-id="45ed1-108">Element</span><span class="sxs-lookup"><span data-stu-id="45ed1-108">Item</span></span>                                                   | <span data-ttu-id="45ed1-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45ed1-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="45ed1-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="45ed1-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="45ed1-111">\[im \] angegebenen Wert im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="45ed1-111">\[in\] The specified value, in radians.</span></span><br/> |
| <span data-ttu-id="45ed1-112"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="45ed1-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="45ed1-113">\[Out \] gibt den Sinus von x zurück.</span><span class="sxs-lookup"><span data-stu-id="45ed1-113">\[out\] Returns the sine of x.</span></span><br/>          |
| <span data-ttu-id="45ed1-114"><span id="c"></span><span id="C"></span>*scher*</span><span class="sxs-lookup"><span data-stu-id="45ed1-114"><span id="c"></span><span id="C"></span>*c*</span></span><br/> | <span data-ttu-id="45ed1-115">\[Out \] gibt den Kosinus von x zurück.</span><span class="sxs-lookup"><span data-stu-id="45ed1-115">\[out\] Returns the cosine of x.</span></span><br/>        |



 

## <a name="return-value"></a><span data-ttu-id="45ed1-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="45ed1-116">Return Value</span></span>

<span data-ttu-id="45ed1-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="45ed1-117">None.</span></span>

## <a name="type-description"></a><span data-ttu-id="45ed1-118">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="45ed1-118">Type Description</span></span>



| <span data-ttu-id="45ed1-119">Name</span><span class="sxs-lookup"><span data-stu-id="45ed1-119">Name</span></span> | [<span data-ttu-id="45ed1-120">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="45ed1-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="45ed1-121">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="45ed1-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="45ed1-122">Size</span><span class="sxs-lookup"><span data-stu-id="45ed1-122">Size</span></span>                           |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="45ed1-123">*x*</span><span class="sxs-lookup"><span data-stu-id="45ed1-123">*x*</span></span>  | <span data-ttu-id="45ed1-124">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="45ed1-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="45ed1-125">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="45ed1-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="45ed1-126">any</span><span class="sxs-lookup"><span data-stu-id="45ed1-126">any</span></span>                            |
| <span data-ttu-id="45ed1-127">*s*</span><span class="sxs-lookup"><span data-stu-id="45ed1-127">*s*</span></span>  | <span data-ttu-id="45ed1-128">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="45ed1-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="45ed1-129">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="45ed1-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="45ed1-130">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="45ed1-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="45ed1-131">c</span><span class="sxs-lookup"><span data-stu-id="45ed1-131">c</span></span>    | <span data-ttu-id="45ed1-132">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="45ed1-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="45ed1-133">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="45ed1-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="45ed1-134">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="45ed1-134">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="45ed1-135">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="45ed1-135">Minimum Shader Model</span></span>

<span data-ttu-id="45ed1-136">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="45ed1-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="45ed1-137">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="45ed1-137">Shader Model</span></span>                                                                       | <span data-ttu-id="45ed1-138">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="45ed1-138">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="45ed1-139">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="45ed1-139">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="45ed1-140">ja</span><span class="sxs-lookup"><span data-stu-id="45ed1-140">yes</span></span>                 |
| [<span data-ttu-id="45ed1-141">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="45ed1-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="45ed1-142">Ja ( \_ nur vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="45ed1-142">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="45ed1-143">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="45ed1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45ed1-144">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="45ed1-144">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

