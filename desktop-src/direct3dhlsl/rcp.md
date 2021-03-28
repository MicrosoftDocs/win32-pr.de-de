---
title: rcp
description: Berechnet eine schnelle, ungefähre und pro Komponente.
ms.assetid: c8d451e4-717e-45b3-a0fe-da55feb8f443
keywords:
- RCP HLSL
topic_type:
- apiref
api_name:
- rcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a857c897def08f31e18ef19466daa2b4584740a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728193"
---
# <a name="rcp"></a><span data-ttu-id="7f425-104">rcp</span><span class="sxs-lookup"><span data-stu-id="7f425-104">rcp</span></span>

<span data-ttu-id="7f425-105">Berechnet eine schnelle, ungefähre und pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="7f425-105">Calculates a fast, approximate, per-component reciprocal.</span></span>



| <span data-ttu-id="7f425-106">*ret* RCP (*x*)</span><span class="sxs-lookup"><span data-stu-id="7f425-106">*ret* rcp(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="7f425-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f425-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f425-108"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="7f425-108"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="7f425-109">\[im \] Eingabe Wert.</span><span class="sxs-lookup"><span data-stu-id="7f425-109">\[in\] The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f425-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f425-110">Return Value</span></span>

<span data-ttu-id="7f425-111">Die gegenseitige des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="7f425-111">The reciprocal of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="7f425-112">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="7f425-112">Type Description</span></span>



| <span data-ttu-id="7f425-113">Name</span><span class="sxs-lookup"><span data-stu-id="7f425-113">Name</span></span>  | [<span data-ttu-id="7f425-114">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="7f425-114">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="7f425-115">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="7f425-115">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                      | <span data-ttu-id="7f425-116">Size</span><span class="sxs-lookup"><span data-stu-id="7f425-116">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="7f425-117">*x*</span><span class="sxs-lookup"><span data-stu-id="7f425-117">*x*</span></span>   | <span data-ttu-id="7f425-118">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="7f425-118">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="7f425-119">[**float**](/windows/desktop/WinProg/windows-data-types) oder [ **Double**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="7f425-119">[**float**](/windows/desktop/WinProg/windows-data-types) or [**double**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="7f425-120">any</span><span class="sxs-lookup"><span data-stu-id="7f425-120">any</span></span>                            |
| <span data-ttu-id="7f425-121">*TZI*</span><span class="sxs-lookup"><span data-stu-id="7f425-121">*ret*</span></span> | <span data-ttu-id="7f425-122">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="7f425-122">same as input *x*</span></span>                                                                                              | <span data-ttu-id="7f425-123">[**float**](/windows/desktop/WinProg/windows-data-types) oder [ **Double**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="7f425-123">[**float**](/windows/desktop/WinProg/windows-data-types) or [**double**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="7f425-124">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="7f425-124">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7f425-125">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="7f425-125">Minimum Shader Model</span></span>

<span data-ttu-id="7f425-126">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7f425-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7f425-127">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="7f425-127">Shader Model</span></span>                                                                | <span data-ttu-id="7f425-128">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="7f425-128">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="7f425-129">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="7f425-129">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="7f425-130">ja</span><span class="sxs-lookup"><span data-stu-id="7f425-130">yes</span></span>       |



 

<span data-ttu-id="7f425-131">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="7f425-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="7f425-132">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="7f425-132">Vertex</span></span> | <span data-ttu-id="7f425-133">Hülle</span><span class="sxs-lookup"><span data-stu-id="7f425-133">Hull</span></span> | <span data-ttu-id="7f425-134">Domain</span><span class="sxs-lookup"><span data-stu-id="7f425-134">Domain</span></span> | <span data-ttu-id="7f425-135">Geometrie</span><span class="sxs-lookup"><span data-stu-id="7f425-135">Geometry</span></span> | <span data-ttu-id="7f425-136">Pixel</span><span class="sxs-lookup"><span data-stu-id="7f425-136">Pixel</span></span> | <span data-ttu-id="7f425-137">Compute</span><span class="sxs-lookup"><span data-stu-id="7f425-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7f425-138">x</span><span class="sxs-lookup"><span data-stu-id="7f425-138">x</span></span>      | <span data-ttu-id="7f425-139">x</span><span class="sxs-lookup"><span data-stu-id="7f425-139">x</span></span>    | <span data-ttu-id="7f425-140">x</span><span class="sxs-lookup"><span data-stu-id="7f425-140">x</span></span>      | <span data-ttu-id="7f425-141">x</span><span class="sxs-lookup"><span data-stu-id="7f425-141">x</span></span>        | <span data-ttu-id="7f425-142">x</span><span class="sxs-lookup"><span data-stu-id="7f425-142">x</span></span>     | <span data-ttu-id="7f425-143">x</span><span class="sxs-lookup"><span data-stu-id="7f425-143">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7f425-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7f425-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f425-145">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="7f425-145">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="7f425-146">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="7f425-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 