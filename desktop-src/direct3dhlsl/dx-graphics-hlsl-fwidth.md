---
title: Breite
description: Gibt den absoluten Wert der partiellen Ableitungen des angegebenen-Werts zurück.
ms.assetid: 7184c3b4-1720-4176-a494-7f73322a918e
keywords:
- Breite von HLSL
topic_type:
- apiref
api_name:
- fwidth
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf2d5a34e1f387aadb3b044ddd1264616a61109b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102046"
---
# <a name="fwidth"></a><span data-ttu-id="6a1e4-104">Breite</span><span class="sxs-lookup"><span data-stu-id="6a1e4-104">fwidth</span></span>

<span data-ttu-id="6a1e4-105">Gibt den absoluten Wert der partiellen Ableitungen des angegebenen-Werts zurück.</span><span class="sxs-lookup"><span data-stu-id="6a1e4-105">Returns the absolute value of the partial derivatives of the specified value.</span></span>



| <span data-ttu-id="6a1e4-106">*ret* -Breite (*x*)</span><span class="sxs-lookup"><span data-stu-id="6a1e4-106">*ret* fwidth(*x*)</span></span> |
|-------------------|



 

<span data-ttu-id="6a1e4-107">Diese Funktion berechnet Folgendes: [**ABS**](dx-graphics-hlsl-abs.md)([**DDX**](dx-graphics-hlsl-ddx.md)(*x*)) + [**ABS**](dx-graphics-hlsl-abs.md)([**ddY**](dx-graphics-hlsl-ddy.md)(*x*)).</span><span class="sxs-lookup"><span data-stu-id="6a1e4-107">This function computes the following: [**abs**](dx-graphics-hlsl-abs.md)([**ddx**](dx-graphics-hlsl-ddx.md)(*x*)) + [**abs**](dx-graphics-hlsl-abs.md)([**ddy**](dx-graphics-hlsl-ddy.md)(*x*)).</span></span>

<span data-ttu-id="6a1e4-108">Diese Funktion wird nur in Pixel-Shadern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6a1e4-108">This function is only supported in pixel shaders.</span></span>

## <a name="parameters"></a><span data-ttu-id="6a1e4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a1e4-109">Parameters</span></span>



| <span data-ttu-id="6a1e4-110">Element</span><span class="sxs-lookup"><span data-stu-id="6a1e4-110">Item</span></span>                                                   | <span data-ttu-id="6a1e4-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a1e4-111">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="6a1e4-112"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="6a1e4-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="6a1e4-113">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="6a1e4-113">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="6a1e4-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a1e4-114">Return Value</span></span>

<span data-ttu-id="6a1e4-115">Der absolute Wert der partiellen Ableitungen des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="6a1e4-115">The absolute value of the partial derivatives of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="6a1e4-116">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="6a1e4-116">Type Description</span></span>



| <span data-ttu-id="6a1e4-117">Name</span><span class="sxs-lookup"><span data-stu-id="6a1e4-117">Name</span></span>  | [<span data-ttu-id="6a1e4-118">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="6a1e4-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="6a1e4-119">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="6a1e4-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="6a1e4-120">Size</span><span class="sxs-lookup"><span data-stu-id="6a1e4-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="6a1e4-121">*x*</span><span class="sxs-lookup"><span data-stu-id="6a1e4-121">*x*</span></span>   | <span data-ttu-id="6a1e4-122">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="6a1e4-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="6a1e4-123">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="6a1e4-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6a1e4-124">any</span><span class="sxs-lookup"><span data-stu-id="6a1e4-124">any</span></span>                            |
| <span data-ttu-id="6a1e4-125">*TZI*</span><span class="sxs-lookup"><span data-stu-id="6a1e4-125">*ret*</span></span> | <span data-ttu-id="6a1e4-126">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="6a1e4-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="6a1e4-127">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="6a1e4-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6a1e4-128">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="6a1e4-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6a1e4-129">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="6a1e4-129">Minimum Shader Model</span></span>

<span data-ttu-id="6a1e4-130">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6a1e4-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6a1e4-131">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="6a1e4-131">Shader Model</span></span>                                                                       | <span data-ttu-id="6a1e4-132">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="6a1e4-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="6a1e4-133">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="6a1e4-133">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) and higher shader models</span></span> | <span data-ttu-id="6a1e4-134">ja</span><span class="sxs-lookup"><span data-stu-id="6a1e4-134">yes</span></span>                 |
| [<span data-ttu-id="6a1e4-135">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a1e4-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                          | <span data-ttu-id="6a1e4-136">Ja ( \_ nur PS 2 \_ x)</span><span class="sxs-lookup"><span data-stu-id="6a1e4-136">yes (ps\_2\_x only)</span></span> |
| [<span data-ttu-id="6a1e4-137">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a1e4-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="6a1e4-138">Nein</span><span class="sxs-lookup"><span data-stu-id="6a1e4-138">no</span></span>                  |



 

## <a name="see-also"></a><span data-ttu-id="6a1e4-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a1e4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a1e4-140">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="6a1e4-140">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

