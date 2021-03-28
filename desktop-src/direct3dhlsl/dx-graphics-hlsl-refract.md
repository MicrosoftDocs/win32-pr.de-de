---
title: Löschen
description: Gibt einen rückbrechungs Vektor mithilfe eines eintretende Strahl, eines Oberflächen normalen und eines abbrechungs Indexes zurück.
ms.assetid: 9f9467d7-dd9b-472a-bbdc-752394d382c6
keywords:
- HLSL Abbrechen
topic_type:
- apiref
api_name:
- refract
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e499d078a020ade1ff9ff2566c3fd15b2a820d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993567"
---
# <a name="refract"></a><span data-ttu-id="ddf4f-104">Löschen</span><span class="sxs-lookup"><span data-stu-id="ddf4f-104">refract</span></span>

<span data-ttu-id="ddf4f-105">Gibt einen rückbrechungs Vektor mithilfe eines eintretende Strahl, eines Oberflächen normalen und eines abbrechungs Indexes zurück.</span><span class="sxs-lookup"><span data-stu-id="ddf4f-105">Returns a refraction vector using an entering ray, a surface normal, and a refraction index.</span></span>



| <span data-ttu-id="ddf4f-106">*ret* Refract (*i*, *n*,?)</span><span class="sxs-lookup"><span data-stu-id="ddf4f-106">*ret* refract(*i*, *n*, ?)</span></span> |
|----------------------------|



 

## <a name="parameters"></a><span data-ttu-id="ddf4f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ddf4f-107">Parameters</span></span>



| <span data-ttu-id="ddf4f-108">Element</span><span class="sxs-lookup"><span data-stu-id="ddf4f-108">Item</span></span>                                                   | <span data-ttu-id="ddf4f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ddf4f-109">Description</span></span>                                                  |
|--------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="ddf4f-110"><span id="i"></span><span id="I"></span>*Ich*</span><span class="sxs-lookup"><span data-stu-id="ddf4f-110"><span id="i"></span><span id="I"></span>*i*</span></span><br/> | <span data-ttu-id="ddf4f-111">\[in \] einem Gleit Komma-Richtungsvektor.</span><span class="sxs-lookup"><span data-stu-id="ddf4f-111">\[in\] A floating-point, ray direction vector.</span></span><br/>    |
| <span data-ttu-id="ddf4f-112"><span id="n"></span><span id="N"></span>*Nr*</span><span class="sxs-lookup"><span data-stu-id="ddf4f-112"><span id="n"></span><span id="N"></span>*n*</span></span><br/> | <span data-ttu-id="ddf4f-113">\[in \] einem Gleit Komma-, Oberflächen normalen Vektor.</span><span class="sxs-lookup"><span data-stu-id="ddf4f-113">\[in\] A floating-point, surface normal vector.</span></span><br/>   |
| <span data-ttu-id="ddf4f-114">*?*</span><span class="sxs-lookup"><span data-stu-id="ddf4f-114">*?*</span></span><br/>                                         | <span data-ttu-id="ddf4f-115">\[brechen Sie in \] einem Gleit Komma den Index Skalarwert ab.</span><span class="sxs-lookup"><span data-stu-id="ddf4f-115">\[in\] A floating-point, refraction index scalar.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="ddf4f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ddf4f-116">Return Value</span></span>

<span data-ttu-id="ddf4f-117">Ein Gleit Komma Trennzeichen.</span><span class="sxs-lookup"><span data-stu-id="ddf4f-117">A floating-point, refraction vector.</span></span> <span data-ttu-id="ddf4f-118">Wenn der Winkel zwischen dem eingaberay i und dem Oberflächen normalen n zu groß für einen bestimmten abbrechungs Index ist, ist der Rückgabewert (0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="ddf4f-118">If the angle between the entering ray i and the surface normal n is too great for a given refraction index ?, the return value is (0,0,0).</span></span>

## <a name="type-description"></a><span data-ttu-id="ddf4f-119">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="ddf4f-119">Type Description</span></span>



| <span data-ttu-id="ddf4f-120">Name</span><span class="sxs-lookup"><span data-stu-id="ddf4f-120">Name</span></span>              | [<span data-ttu-id="ddf4f-121">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="ddf4f-122">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="ddf4f-123">Size</span><span class="sxs-lookup"><span data-stu-id="ddf4f-123">Size</span></span>                           |
|-------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="ddf4f-124">*i*</span><span class="sxs-lookup"><span data-stu-id="ddf4f-124">*i*</span></span>               | [<span data-ttu-id="ddf4f-125">**ve**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-125">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ddf4f-126">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ddf4f-127">any</span><span class="sxs-lookup"><span data-stu-id="ddf4f-127">any</span></span>                            |
| <span data-ttu-id="ddf4f-128">*n*</span><span class="sxs-lookup"><span data-stu-id="ddf4f-128">*n*</span></span>               | [<span data-ttu-id="ddf4f-129">**ve**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ddf4f-130">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ddf4f-131">gleiche Dimension (n) wie Eingabe *i*</span><span class="sxs-lookup"><span data-stu-id="ddf4f-131">same dimension(s) as input *i*</span></span> |
| <span data-ttu-id="ddf4f-132">?</span><span class="sxs-lookup"><span data-stu-id="ddf4f-132">?</span></span>                 | [<span data-ttu-id="ddf4f-133">**Skalar**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-133">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ddf4f-134">**float**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-134">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ddf4f-135">1</span><span class="sxs-lookup"><span data-stu-id="ddf4f-135">1</span></span>                              |
| <span data-ttu-id="ddf4f-136">Brechungs Vektor</span><span class="sxs-lookup"><span data-stu-id="ddf4f-136">refraction vector</span></span> | [<span data-ttu-id="ddf4f-137">**ve**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-137">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ddf4f-138">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-138">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ddf4f-139">gleiche Dimension (n) wie Eingabe *i*</span><span class="sxs-lookup"><span data-stu-id="ddf4f-139">same dimension(s) as input *i*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ddf4f-140">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="ddf4f-140">Minimum Shader Model</span></span>

<span data-ttu-id="ddf4f-141">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ddf4f-141">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ddf4f-142">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="ddf4f-142">Shader Model</span></span>                                                                       | <span data-ttu-id="ddf4f-143">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ddf4f-143">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="ddf4f-144">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="ddf4f-144">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="ddf4f-145">ja</span><span class="sxs-lookup"><span data-stu-id="ddf4f-145">yes</span></span>                 |
| [<span data-ttu-id="ddf4f-146">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ddf4f-146">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="ddf4f-147">Ja ( \_ nur vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="ddf4f-147">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="ddf4f-148">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ddf4f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddf4f-149">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="ddf4f-149">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

