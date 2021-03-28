---
title: faceforward
description: Flippt die Oberfläche-normal (falls erforderlich) in eine Richtung vor i. Gibt das Ergebnis in n zurück.
ms.assetid: 6530a928-d221-49e4-ab68-6285c3db370f
keywords:
- faceforward HLSL
topic_type:
- apiref
api_name:
- faceforward
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c6a3f035ed4f0d16b500864f941bc4fe5413ff54
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101823"
---
# <a name="faceforward"></a><span data-ttu-id="94d2b-104">faceforward</span><span class="sxs-lookup"><span data-stu-id="94d2b-104">faceforward</span></span>

<span data-ttu-id="94d2b-105">Flippt die Oberfläche-normal (falls erforderlich) in eine Richtung vor i. Gibt das Ergebnis in n zurück.</span><span class="sxs-lookup"><span data-stu-id="94d2b-105">Flips the surface-normal (if needed) to face in a direction opposite to i; returns the result in n.</span></span>



| <span data-ttu-id="94d2b-106">*ret* faceforward (*n*, *i*, *ng*)</span><span class="sxs-lookup"><span data-stu-id="94d2b-106">*ret* faceforward(*n*, *i*, *ng*)</span></span> |
|-----------------------------------|



 

<span data-ttu-id="94d2b-107">Diese Funktion verwendet die folgende Formel:-*n*  Sign (Punkt (*i*, *ng*)).</span><span class="sxs-lookup"><span data-stu-id="94d2b-107">This function uses the following formula: -*n*  sign(dot(*i*, *ng*)).</span></span>

## <a name="parameters"></a><span data-ttu-id="94d2b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="94d2b-108">Parameters</span></span>



| <span data-ttu-id="94d2b-109">Element</span><span class="sxs-lookup"><span data-stu-id="94d2b-109">Item</span></span>                                                      | <span data-ttu-id="94d2b-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="94d2b-110">Description</span></span>                                                                                                     |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94d2b-111"><span id="n"></span><span id="N"></span>*Nr*</span><span class="sxs-lookup"><span data-stu-id="94d2b-111"><span id="n"></span><span id="N"></span>*n*</span></span><br/>    | <span data-ttu-id="94d2b-112">\[im \] resultierenden Gleit Komma Oberflächen-normal Vektor.</span><span class="sxs-lookup"><span data-stu-id="94d2b-112">\[in\] The resulting floating-point surface-normal vector.</span></span><br/>                                           |
| <span data-ttu-id="94d2b-113"><span id="i"></span><span id="I"></span>*Ich*</span><span class="sxs-lookup"><span data-stu-id="94d2b-113"><span id="i"></span><span id="I"></span>*i*</span></span><br/>    | <span data-ttu-id="94d2b-114">\[in \] einem Gleit Komma-Incident-Vektor, der von der Ansichts Position auf die Schattierungs Position zeigt.</span><span class="sxs-lookup"><span data-stu-id="94d2b-114">\[in\] A floating-point, incident vector that points from the view position to the shading position.</span></span><br/> |
| <span data-ttu-id="94d2b-115"><span id="ng"></span><span id="NG"></span>*1968*</span><span class="sxs-lookup"><span data-stu-id="94d2b-115"><span id="ng"></span><span id="NG"></span>*ng*</span></span><br/> | <span data-ttu-id="94d2b-116">\[in \] einem Gleit Komma Oberflächen-normal Vektor.</span><span class="sxs-lookup"><span data-stu-id="94d2b-116">\[in\] A floating-point surface-normal vector.</span></span><br/>                                                       |



 

## <a name="return-value"></a><span data-ttu-id="94d2b-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94d2b-117">Return Value</span></span>

<span data-ttu-id="94d2b-118">Ein Gleit Komma Wert, Oberflächen normaler Vektor, der der Ansichts Richtung entspricht.</span><span class="sxs-lookup"><span data-stu-id="94d2b-118">A floating-point, surface normal vector that is facing the view direction.</span></span>

## <a name="type-description"></a><span data-ttu-id="94d2b-119">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="94d2b-119">Type Description</span></span>



| <span data-ttu-id="94d2b-120">Name</span><span class="sxs-lookup"><span data-stu-id="94d2b-120">Name</span></span>  | [<span data-ttu-id="94d2b-121">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="94d2b-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="94d2b-122">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="94d2b-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="94d2b-123">Size</span><span class="sxs-lookup"><span data-stu-id="94d2b-123">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="94d2b-124">*n*</span><span class="sxs-lookup"><span data-stu-id="94d2b-124">*n*</span></span>   | [<span data-ttu-id="94d2b-125">**ve**</span><span class="sxs-lookup"><span data-stu-id="94d2b-125">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="94d2b-126">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="94d2b-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="94d2b-127">any</span><span class="sxs-lookup"><span data-stu-id="94d2b-127">any</span></span>                            |
| <span data-ttu-id="94d2b-128">*i*</span><span class="sxs-lookup"><span data-stu-id="94d2b-128">*i*</span></span>   | [<span data-ttu-id="94d2b-129">**ve**</span><span class="sxs-lookup"><span data-stu-id="94d2b-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="94d2b-130">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="94d2b-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="94d2b-131">gleiche Dimension (n) wie Eingabe *n*</span><span class="sxs-lookup"><span data-stu-id="94d2b-131">same dimension(s) as input *n*</span></span> |
| <span data-ttu-id="94d2b-132">*ng*</span><span class="sxs-lookup"><span data-stu-id="94d2b-132">*ng*</span></span>  | [<span data-ttu-id="94d2b-133">**ve**</span><span class="sxs-lookup"><span data-stu-id="94d2b-133">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="94d2b-134">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="94d2b-134">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="94d2b-135">gleiche Dimensionen wie Eingabe *n*</span><span class="sxs-lookup"><span data-stu-id="94d2b-135">same dimensions as input *n*</span></span>   |
| <span data-ttu-id="94d2b-136">*TZI*</span><span class="sxs-lookup"><span data-stu-id="94d2b-136">*ret*</span></span> | [<span data-ttu-id="94d2b-137">**ve**</span><span class="sxs-lookup"><span data-stu-id="94d2b-137">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="94d2b-138">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="94d2b-138">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="94d2b-139">gleiche Dimensionen wie Eingabe *n*</span><span class="sxs-lookup"><span data-stu-id="94d2b-139">same dimensions as input *n*</span></span>   |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="94d2b-140">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="94d2b-140">Minimum Shader Model</span></span>

<span data-ttu-id="94d2b-141">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="94d2b-141">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="94d2b-142">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="94d2b-142">Shader Model</span></span>                                                                       | <span data-ttu-id="94d2b-143">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="94d2b-143">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="94d2b-144">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="94d2b-144">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="94d2b-145">ja</span><span class="sxs-lookup"><span data-stu-id="94d2b-145">yes</span></span>                   |
| [<span data-ttu-id="94d2b-146">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="94d2b-146">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="94d2b-147">vs \_ 1 \_ 1 und PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="94d2b-147">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="94d2b-148">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="94d2b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94d2b-149">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="94d2b-149">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

