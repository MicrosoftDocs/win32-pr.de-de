---
title: gezündet
description: Gibt einen Beleuchtungs Koeffizient-Vektor zurück.
ms.assetid: 6ae116df-41b7-42f1-96cb-da480a7c1bab
keywords:
- Lit HLSL
topic_type:
- apiref
api_name:
- lit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dbf6f1e53218355ba1ee9ccf58dac6176007218
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858264"
---
# <a name="lit"></a><span data-ttu-id="4d1b2-104">gezündet</span><span class="sxs-lookup"><span data-stu-id="4d1b2-104">lit</span></span>

<span data-ttu-id="4d1b2-105">Gibt einen Beleuchtungs Koeffizient-Vektor zurück.</span><span class="sxs-lookup"><span data-stu-id="4d1b2-105">Returns a lighting coefficient vector.</span></span>



| <span data-ttu-id="4d1b2-106">*ret* beleuchtet (*n \_ Punkt \_ l*, *n \_ Punkt \_ h*, *m*)</span><span class="sxs-lookup"><span data-stu-id="4d1b2-106">*ret* lit(*n\_dot\_l*, *n\_dot\_h*, *m*)</span></span> |
|------------------------------------------|



 

<span data-ttu-id="4d1b2-107">Diese Funktion gibt einen Beleuchtungs Koeffizienten (Ambient, diffuse, Glanz, 1) zurück, wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="4d1b2-107">This function returns a lighting coefficient vector (ambient, diffuse, specular, 1) where:</span></span>

-   <span data-ttu-id="4d1b2-108">Ambient = 1</span><span class="sxs-lookup"><span data-stu-id="4d1b2-108">ambient = 1</span></span>
-   <span data-ttu-id="4d1b2-109">diffuses = n l < 0?</span><span class="sxs-lookup"><span data-stu-id="4d1b2-109">diffuse = n · l < 0 ?</span></span> <span data-ttu-id="4d1b2-110">0: n int</span><span class="sxs-lookup"><span data-stu-id="4d1b2-110">0 : n · l</span></span>
-   <span data-ttu-id="4d1b2-111">Glanz = n l < 0 \| \| n = h < 0?</span><span class="sxs-lookup"><span data-stu-id="4d1b2-111">specular = n · l < 0 \|\| n · h < 0 ?</span></span> <span data-ttu-id="4d1b2-112">0: (n = h) ^ m</span><span class="sxs-lookup"><span data-stu-id="4d1b2-112">0 : (n · h) ^ m</span></span>

<span data-ttu-id="4d1b2-113">Wenn der Vektor n der normale Vektor ist, ist l die Richtung zu hell und h ist der halbvektor.</span><span class="sxs-lookup"><span data-stu-id="4d1b2-113">Where the vector n is the normal vector, l is the direction to light and h is the half vector.</span></span>

## <a name="parameters"></a><span data-ttu-id="4d1b2-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d1b2-114">Parameters</span></span>



| <span data-ttu-id="4d1b2-115">Element</span><span class="sxs-lookup"><span data-stu-id="4d1b2-115">Item</span></span>                                                                       | <span data-ttu-id="4d1b2-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d1b2-116">Description</span></span>                                                                              |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d1b2-117"><span id="n_dot_l"></span><span id="N_DOT_L"></span>*n \_ Punkt \_ l*</span><span class="sxs-lookup"><span data-stu-id="4d1b2-117"><span id="n_dot_l"></span><span id="N_DOT_L"></span>*n\_dot\_l*</span></span><br/> | <span data-ttu-id="4d1b2-118">\[im \] Punktprodukt der normalisierten Oberflächen normal und der Licht Vektor.</span><span class="sxs-lookup"><span data-stu-id="4d1b2-118">\[in\] The dot product of the normalized surface normal and the light vector.</span></span><br/> |
| <span data-ttu-id="4d1b2-119"><span id="n_dot_h"></span><span id="N_DOT_H"></span>*n \_ Punkt \_ h*</span><span class="sxs-lookup"><span data-stu-id="4d1b2-119"><span id="n_dot_h"></span><span id="N_DOT_H"></span>*n\_dot\_h*</span></span><br/> | <span data-ttu-id="4d1b2-120">\[im \] Punktprodukt des halb Winkel Vektors und der Oberflächen normalen.</span><span class="sxs-lookup"><span data-stu-id="4d1b2-120">\[in\] The dot product of the half-angle vector and the surface normal.</span></span><br/>       |
| <span data-ttu-id="4d1b2-121"><span id="m"></span><span id="M"></span>*800*</span><span class="sxs-lookup"><span data-stu-id="4d1b2-121"><span id="m"></span><span id="M"></span>*m*</span></span><br/>                     | <span data-ttu-id="4d1b2-122">\[in \] einem Glanz Exponenten.</span><span class="sxs-lookup"><span data-stu-id="4d1b2-122">\[in\] A specular exponent.</span></span><br/>                                                   |



 

## <a name="return-value"></a><span data-ttu-id="4d1b2-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d1b2-123">Return Value</span></span>

<span data-ttu-id="4d1b2-124">Der Beleuchtungs Koeffizient-Vektor.</span><span class="sxs-lookup"><span data-stu-id="4d1b2-124">The lighting coefficient vector.</span></span>

## <a name="type-description"></a><span data-ttu-id="4d1b2-125">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="4d1b2-125">Type Description</span></span>



| <span data-ttu-id="4d1b2-126">Name</span><span class="sxs-lookup"><span data-stu-id="4d1b2-126">Name</span></span>        | [<span data-ttu-id="4d1b2-127">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="4d1b2-127">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="4d1b2-128">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="4d1b2-128">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="4d1b2-129">Size</span><span class="sxs-lookup"><span data-stu-id="4d1b2-129">Size</span></span> |
|-------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="4d1b2-130">*n \_ Punkt \_ l*</span><span class="sxs-lookup"><span data-stu-id="4d1b2-130">*n\_dot\_l*</span></span> | [<span data-ttu-id="4d1b2-131">**Skalar**</span><span class="sxs-lookup"><span data-stu-id="4d1b2-131">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="4d1b2-132">**float**</span><span class="sxs-lookup"><span data-stu-id="4d1b2-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4d1b2-133">1</span><span class="sxs-lookup"><span data-stu-id="4d1b2-133">1</span></span>    |
| <span data-ttu-id="4d1b2-134">*n \_ Punkt \_ h*</span><span class="sxs-lookup"><span data-stu-id="4d1b2-134">*n\_dot\_h*</span></span> | [<span data-ttu-id="4d1b2-135">**Skalar**</span><span class="sxs-lookup"><span data-stu-id="4d1b2-135">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="4d1b2-136">**float**</span><span class="sxs-lookup"><span data-stu-id="4d1b2-136">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4d1b2-137">1</span><span class="sxs-lookup"><span data-stu-id="4d1b2-137">1</span></span>    |
| <span data-ttu-id="4d1b2-138">*m*</span><span class="sxs-lookup"><span data-stu-id="4d1b2-138">*m*</span></span>         | [<span data-ttu-id="4d1b2-139">**Skalar**</span><span class="sxs-lookup"><span data-stu-id="4d1b2-139">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="4d1b2-140">**float**</span><span class="sxs-lookup"><span data-stu-id="4d1b2-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4d1b2-141">1</span><span class="sxs-lookup"><span data-stu-id="4d1b2-141">1</span></span>    |
| <span data-ttu-id="4d1b2-142">*TZI*</span><span class="sxs-lookup"><span data-stu-id="4d1b2-142">*ret*</span></span>       | [<span data-ttu-id="4d1b2-143">**ve**</span><span class="sxs-lookup"><span data-stu-id="4d1b2-143">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="4d1b2-144">**float**</span><span class="sxs-lookup"><span data-stu-id="4d1b2-144">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4d1b2-145">4</span><span class="sxs-lookup"><span data-stu-id="4d1b2-145">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4d1b2-146">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="4d1b2-146">Minimum Shader Model</span></span>

<span data-ttu-id="4d1b2-147">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4d1b2-147">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4d1b2-148">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="4d1b2-148">Shader Model</span></span>                                                                       | <span data-ttu-id="4d1b2-149">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="4d1b2-149">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="4d1b2-150">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="4d1b2-150">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="4d1b2-151">ja</span><span class="sxs-lookup"><span data-stu-id="4d1b2-151">yes</span></span>                 |
| [<span data-ttu-id="4d1b2-152">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4d1b2-152">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="4d1b2-153">Ja ( \_ nur vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="4d1b2-153">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="4d1b2-154">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4d1b2-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d1b2-155">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="4d1b2-155">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

