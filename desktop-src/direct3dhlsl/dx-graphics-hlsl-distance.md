---
title: distance
description: Gibt einen skalaren Abstand zwischen zwei Vektoren zurück.
ms.assetid: dda8dc39-fd72-4e92-bf9d-e700db0ede9e
keywords:
- entfernunghlsl
topic_type:
- apiref
api_name:
- distance
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0f3a64778666ac8f7de16b91eed202e36e90ed1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315585"
---
# <a name="distance"></a><span data-ttu-id="6c988-104">distance</span><span class="sxs-lookup"><span data-stu-id="6c988-104">distance</span></span>

<span data-ttu-id="6c988-105">Gibt einen skalaren Abstand zwischen zwei Vektoren zurück.</span><span class="sxs-lookup"><span data-stu-id="6c988-105">Returns a distance scalar between two vectors.</span></span>



| <span data-ttu-id="6c988-106">*ret* -Distanz (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="6c988-106">*ret* distance(*x*, *y*)</span></span> |
|--------------------------|



 

## <a name="parameters"></a><span data-ttu-id="6c988-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c988-107">Parameters</span></span>



| <span data-ttu-id="6c988-108">Element</span><span class="sxs-lookup"><span data-stu-id="6c988-108">Item</span></span>                                                   | <span data-ttu-id="6c988-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6c988-109">Description</span></span>                                                    |
|--------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="6c988-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="6c988-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="6c988-111">\[im \] ersten zu vergleichenden Gleit Komma Vektor.</span><span class="sxs-lookup"><span data-stu-id="6c988-111">\[in\] The first floating-point vector to compare.</span></span><br/>  |
| <span data-ttu-id="6c988-112"><span id="y"></span><span id="Y"></span>*Teenie*</span><span class="sxs-lookup"><span data-stu-id="6c988-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="6c988-113">\[im \] zweiten zu vergleichenden Gleit Komma Vektor.</span><span class="sxs-lookup"><span data-stu-id="6c988-113">\[in\] The second floating-point vector to compare.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="6c988-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c988-114">Return Value</span></span>

<span data-ttu-id="6c988-115">Ein Gleit Komma-Skalarwert, der den Abstand zwischen dem *x* -Parameter und dem *y* -Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="6c988-115">A floating-point, scalar value that represents the distance between the *x* parameter and the *y* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="6c988-116">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="6c988-116">Type Description</span></span>



| <span data-ttu-id="6c988-117">Name</span><span class="sxs-lookup"><span data-stu-id="6c988-117">Name</span></span>  | [<span data-ttu-id="6c988-118">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="6c988-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="6c988-119">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="6c988-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="6c988-120">Size</span><span class="sxs-lookup"><span data-stu-id="6c988-120">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="6c988-121">*x*</span><span class="sxs-lookup"><span data-stu-id="6c988-121">*x*</span></span>   | [<span data-ttu-id="6c988-122">**ve**</span><span class="sxs-lookup"><span data-stu-id="6c988-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="6c988-123">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="6c988-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6c988-124">any</span><span class="sxs-lookup"><span data-stu-id="6c988-124">any</span></span>                            |
| <span data-ttu-id="6c988-125">*y*</span><span class="sxs-lookup"><span data-stu-id="6c988-125">*y*</span></span>   | [<span data-ttu-id="6c988-126">**ve**</span><span class="sxs-lookup"><span data-stu-id="6c988-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="6c988-127">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="6c988-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6c988-128">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="6c988-128">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="6c988-129">*TZI*</span><span class="sxs-lookup"><span data-stu-id="6c988-129">*ret*</span></span> | [<span data-ttu-id="6c988-130">**Skalar**</span><span class="sxs-lookup"><span data-stu-id="6c988-130">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="6c988-131">**float**</span><span class="sxs-lookup"><span data-stu-id="6c988-131">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6c988-132">1</span><span class="sxs-lookup"><span data-stu-id="6c988-132">1</span></span>                              |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6c988-133">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="6c988-133">Minimum Shader Model</span></span>

<span data-ttu-id="6c988-134">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6c988-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6c988-135">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="6c988-135">Shader Model</span></span>                                                                       | <span data-ttu-id="6c988-136">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="6c988-136">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="6c988-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="6c988-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="6c988-138">ja</span><span class="sxs-lookup"><span data-stu-id="6c988-138">yes</span></span>       |
| [<span data-ttu-id="6c988-139">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6c988-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="6c988-140">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="6c988-140">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="6c988-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6c988-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c988-142">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="6c988-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

