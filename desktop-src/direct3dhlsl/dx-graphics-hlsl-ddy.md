---
title: tziger
description: Gibt die partielle Ableitung des angegebenen-Werts in Bezug auf die y-Koordinate des Bildschirm Raums zurück.
ms.assetid: 1c88804f-a13f-4714-a3ef-466307afbc1b
keywords:
- ddY HLSL
topic_type:
- apiref
api_name:
- ddy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d27e48a6d9ae237e4e58d1fd30afbac3b2b40d3d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390508"
---
# <a name="ddy"></a><span data-ttu-id="bde53-104">tziger</span><span class="sxs-lookup"><span data-stu-id="bde53-104">ddy</span></span>

<span data-ttu-id="bde53-105">Gibt die partielle Ableitung des angegebenen-Werts in Bezug auf die y-Koordinate des Bildschirm Raums zurück.</span><span class="sxs-lookup"><span data-stu-id="bde53-105">Returns the partial derivative of the specified value with respect to the screen-space y-coordinate.</span></span>



| <span data-ttu-id="bde53-106">*ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="bde53-106">*ret* ddy(*x*)</span></span> |
|----------------|



 

<span data-ttu-id="bde53-107">Diese Funktion berechnet die partielle Ableitung in Bezug auf die y-Koordinate für den Bildschirmbereich.</span><span class="sxs-lookup"><span data-stu-id="bde53-107">This function computes the partial derivative with respect to the screen-space y-coordinate.</span></span> <span data-ttu-id="bde53-108">Verwenden Sie die [**DDX**](dx-graphics-hlsl-ddx.md) -Funktion, um die partielle Ableitung in Bezug auf die x-Koordinate des Bildschirm Raums zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="bde53-108">To compute the partial derivative with respect to the screen-space x-coordinate, use the [**ddx**](dx-graphics-hlsl-ddx.md) function.</span></span>

<span data-ttu-id="bde53-109">Diese Funktion wird nur in Pixel-Shadern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bde53-109">This function is only supported in pixel shaders.</span></span>

## <a name="parameters"></a><span data-ttu-id="bde53-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bde53-110">Parameters</span></span>



| <span data-ttu-id="bde53-111">Element</span><span class="sxs-lookup"><span data-stu-id="bde53-111">Item</span></span>                                                   | <span data-ttu-id="bde53-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bde53-112">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="bde53-113"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="bde53-113"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="bde53-114">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="bde53-114">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="bde53-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bde53-115">Return Value</span></span>

<span data-ttu-id="bde53-116">Die partielle Ableitung des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="bde53-116">The partial derivative of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="bde53-117">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="bde53-117">Type Description</span></span>



| <span data-ttu-id="bde53-118">Name</span><span class="sxs-lookup"><span data-stu-id="bde53-118">Name</span></span>  | [<span data-ttu-id="bde53-119">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="bde53-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="bde53-120">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="bde53-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="bde53-121">Size</span><span class="sxs-lookup"><span data-stu-id="bde53-121">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="bde53-122">*x*</span><span class="sxs-lookup"><span data-stu-id="bde53-122">*x*</span></span>   | <span data-ttu-id="bde53-123">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="bde53-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="bde53-124">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="bde53-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bde53-125">any</span><span class="sxs-lookup"><span data-stu-id="bde53-125">any</span></span>                            |
| <span data-ttu-id="bde53-126">*TZI*</span><span class="sxs-lookup"><span data-stu-id="bde53-126">*ret*</span></span> | <span data-ttu-id="bde53-127">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="bde53-127">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="bde53-128">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="bde53-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bde53-129">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="bde53-129">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bde53-130">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="bde53-130">Minimum Shader Model</span></span>

<span data-ttu-id="bde53-131">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bde53-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bde53-132">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="bde53-132">Shader Model</span></span>                                                                | <span data-ttu-id="bde53-133">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="bde53-133">Supported</span></span>                                 |
|-----------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="bde53-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="bde53-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="bde53-135">ja</span><span class="sxs-lookup"><span data-stu-id="bde53-135">yes</span></span>                                       |
| [<span data-ttu-id="bde53-136">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="bde53-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                                  | <span data-ttu-id="bde53-137">ja</span><span class="sxs-lookup"><span data-stu-id="bde53-137">yes</span></span>                                       |
| [<span data-ttu-id="bde53-138">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bde53-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)                   | <span data-ttu-id="bde53-139">ja</span><span class="sxs-lookup"><span data-stu-id="bde53-139">yes</span></span>                                       |
| [<span data-ttu-id="bde53-140">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bde53-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                   | <span data-ttu-id="bde53-141">ja in PS \_ 2 \_ x; wird in PS 2 0 nicht unterstützt \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="bde53-141">yes in ps\_2\_x; unsupported in ps\_2\_0.</span></span> |
| [<span data-ttu-id="bde53-142">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bde53-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                   | <span data-ttu-id="bde53-143">nein</span><span class="sxs-lookup"><span data-stu-id="bde53-143">no</span></span>                                        |



 

<span data-ttu-id="bde53-144">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="bde53-144">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="bde53-145">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="bde53-145">Vertex</span></span> | <span data-ttu-id="bde53-146">Hülle</span><span class="sxs-lookup"><span data-stu-id="bde53-146">Hull</span></span> | <span data-ttu-id="bde53-147">Domain</span><span class="sxs-lookup"><span data-stu-id="bde53-147">Domain</span></span> | <span data-ttu-id="bde53-148">Geometrie</span><span class="sxs-lookup"><span data-stu-id="bde53-148">Geometry</span></span> | <span data-ttu-id="bde53-149">Pixel</span><span class="sxs-lookup"><span data-stu-id="bde53-149">Pixel</span></span> | <span data-ttu-id="bde53-150">Compute</span><span class="sxs-lookup"><span data-stu-id="bde53-150">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="bde53-151">x</span><span class="sxs-lookup"><span data-stu-id="bde53-151">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="bde53-152">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bde53-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bde53-153">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="bde53-153">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

