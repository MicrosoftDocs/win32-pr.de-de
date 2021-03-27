---
title: DDX
description: Gibt die partielle Ableitung des angegebenen-Werts in Bezug auf die x-Koordinate des Bildschirm Raums zurück.
ms.assetid: a21c2d2a-7c62-4dc6-8521-273690be1104
keywords:
- DDX HLSL
topic_type:
- apiref
api_name:
- ddx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc82f41e8968ccfadaf5d87a8058d332f04ce3a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390509"
---
# <a name="ddx"></a><span data-ttu-id="5a3d5-104">DDX</span><span class="sxs-lookup"><span data-stu-id="5a3d5-104">ddx</span></span>

<span data-ttu-id="5a3d5-105">Gibt die partielle Ableitung des angegebenen-Werts in Bezug auf die x-Koordinate des Bildschirm Raums zurück.</span><span class="sxs-lookup"><span data-stu-id="5a3d5-105">Returns the partial derivative of the specified value with respect to the screen-space x-coordinate.</span></span>



| <span data-ttu-id="5a3d5-106">*ret* DDX (*x*)</span><span class="sxs-lookup"><span data-stu-id="5a3d5-106">*ret* ddx(*x*)</span></span> |
|----------------|



 

<span data-ttu-id="5a3d5-107">Diese Funktion berechnet die partielle Ableitung in Bezug auf die x-Koordinate des Bildschirm Raums.</span><span class="sxs-lookup"><span data-stu-id="5a3d5-107">This function computes the partial derivative with respect to the screen-space x-coordinate.</span></span> <span data-ttu-id="5a3d5-108">Um die partielle Ableitung in Bezug auf die y-Koordinate des Bildschirm Raums zu berechnen, verwenden Sie die Funktion [**ddY**](dx-graphics-hlsl-ddy.md) .</span><span class="sxs-lookup"><span data-stu-id="5a3d5-108">To compute the partial derivative with respect to the screen-space y-coordinate, use the [**ddy**](dx-graphics-hlsl-ddy.md) function.</span></span>

<span data-ttu-id="5a3d5-109">Diese Funktion wird nur in Pixel-Shadern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5a3d5-109">This function is only supported in pixel shaders.</span></span>

## <a name="parameters"></a><span data-ttu-id="5a3d5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a3d5-110">Parameters</span></span>



| <span data-ttu-id="5a3d5-111">Element</span><span class="sxs-lookup"><span data-stu-id="5a3d5-111">Item</span></span>                                                   | <span data-ttu-id="5a3d5-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a3d5-112">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="5a3d5-113"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="5a3d5-113"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="5a3d5-114">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="5a3d5-114">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="5a3d5-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a3d5-115">Return Value</span></span>

<span data-ttu-id="5a3d5-116">Die partielle Ableitung des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="5a3d5-116">The partial derivative of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="5a3d5-117">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="5a3d5-117">Type Description</span></span>



| <span data-ttu-id="5a3d5-118">Name</span><span class="sxs-lookup"><span data-stu-id="5a3d5-118">Name</span></span>  | [<span data-ttu-id="5a3d5-119">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="5a3d5-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="5a3d5-120">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="5a3d5-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="5a3d5-121">Size</span><span class="sxs-lookup"><span data-stu-id="5a3d5-121">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="5a3d5-122">*x*</span><span class="sxs-lookup"><span data-stu-id="5a3d5-122">*x*</span></span>   | <span data-ttu-id="5a3d5-123">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="5a3d5-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="5a3d5-124">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="5a3d5-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5a3d5-125">any</span><span class="sxs-lookup"><span data-stu-id="5a3d5-125">any</span></span>                            |
| <span data-ttu-id="5a3d5-126">*TZI*</span><span class="sxs-lookup"><span data-stu-id="5a3d5-126">*ret*</span></span> | <span data-ttu-id="5a3d5-127">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="5a3d5-127">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="5a3d5-128">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="5a3d5-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5a3d5-129">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="5a3d5-129">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5a3d5-130">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="5a3d5-130">Minimum Shader Model</span></span>

<span data-ttu-id="5a3d5-131">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5a3d5-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5a3d5-132">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="5a3d5-132">Shader Model</span></span>                                                                | <span data-ttu-id="5a3d5-133">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="5a3d5-133">Supported</span></span>                                 |
|-----------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="5a3d5-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="5a3d5-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="5a3d5-135">ja</span><span class="sxs-lookup"><span data-stu-id="5a3d5-135">yes</span></span>                                       |
| [<span data-ttu-id="5a3d5-136">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="5a3d5-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                                  | <span data-ttu-id="5a3d5-137">ja</span><span class="sxs-lookup"><span data-stu-id="5a3d5-137">yes</span></span>                                       |
| [<span data-ttu-id="5a3d5-138">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a3d5-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)                   | <span data-ttu-id="5a3d5-139">ja</span><span class="sxs-lookup"><span data-stu-id="5a3d5-139">yes</span></span>                                       |
| [<span data-ttu-id="5a3d5-140">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a3d5-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                   | <span data-ttu-id="5a3d5-141">ja in PS \_ 2 \_ x; wird in PS 2 0 nicht unterstützt \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5a3d5-141">yes in ps\_2\_x; unsupported in ps\_2\_0.</span></span> |
| [<span data-ttu-id="5a3d5-142">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a3d5-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                   | <span data-ttu-id="5a3d5-143">nein</span><span class="sxs-lookup"><span data-stu-id="5a3d5-143">no</span></span>                                        |



 

<span data-ttu-id="5a3d5-144">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="5a3d5-144">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="5a3d5-145">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="5a3d5-145">Vertex</span></span> | <span data-ttu-id="5a3d5-146">Hülle</span><span class="sxs-lookup"><span data-stu-id="5a3d5-146">Hull</span></span> | <span data-ttu-id="5a3d5-147">Domain</span><span class="sxs-lookup"><span data-stu-id="5a3d5-147">Domain</span></span> | <span data-ttu-id="5a3d5-148">Geometrie</span><span class="sxs-lookup"><span data-stu-id="5a3d5-148">Geometry</span></span> | <span data-ttu-id="5a3d5-149">Pixel</span><span class="sxs-lookup"><span data-stu-id="5a3d5-149">Pixel</span></span> | <span data-ttu-id="5a3d5-150">Compute</span><span class="sxs-lookup"><span data-stu-id="5a3d5-150">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="5a3d5-151">x</span><span class="sxs-lookup"><span data-stu-id="5a3d5-151">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="5a3d5-152">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5a3d5-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a3d5-153">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="5a3d5-153">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

