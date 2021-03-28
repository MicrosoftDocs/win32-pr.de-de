---
title: übergreifende
description: Gibt das Kreuz Produkt von zwei Gleit Komma-3D-Vektoren zurück.
ms.assetid: 5f1832af-6bc5-49a7-956a-fd762f674f5f
keywords:
- Kreuz HLSL
topic_type:
- apiref
api_name:
- cross
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91959bf415c3e56edf370942de268523bf998743
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993582"
---
# <a name="cross"></a><span data-ttu-id="1a39a-104">übergreifende</span><span class="sxs-lookup"><span data-stu-id="1a39a-104">cross</span></span>

<span data-ttu-id="1a39a-105">Gibt das Kreuz Produkt von zwei Gleit Komma-3D-Vektoren zurück.</span><span class="sxs-lookup"><span data-stu-id="1a39a-105">Returns the cross product of two floating-point, 3D vectors.</span></span>



| <span data-ttu-id="1a39a-106">*ret* Kreuz (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="1a39a-106">*ret* cross(*x*, *y*)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="1a39a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a39a-107">Parameters</span></span>



| <span data-ttu-id="1a39a-108">Element</span><span class="sxs-lookup"><span data-stu-id="1a39a-108">Item</span></span>                                                   | <span data-ttu-id="1a39a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a39a-109">Description</span></span>                                             |
|--------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="1a39a-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="1a39a-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="1a39a-111">\[im \] ersten Gleit Komma-3D-Vektor.</span><span class="sxs-lookup"><span data-stu-id="1a39a-111">\[in\] The first floating-point, 3D vector.</span></span><br/>  |
| <span data-ttu-id="1a39a-112"><span id="y"></span><span id="Y"></span>*Teenie*</span><span class="sxs-lookup"><span data-stu-id="1a39a-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="1a39a-113">\[im \] zweiten Gleit Komma-3D-Vektor.</span><span class="sxs-lookup"><span data-stu-id="1a39a-113">\[in\] The second floating-point, 3D vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="1a39a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a39a-114">Return Value</span></span>

<span data-ttu-id="1a39a-115">Das Kreuz Produkt des *x* -Parameters und des *y* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="1a39a-115">The cross product of the *x* parameter and the *y* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="1a39a-116">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="1a39a-116">Type Description</span></span>



| <span data-ttu-id="1a39a-117">Name</span><span class="sxs-lookup"><span data-stu-id="1a39a-117">Name</span></span>  | [<span data-ttu-id="1a39a-118">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="1a39a-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="1a39a-119">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="1a39a-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="1a39a-120">Size</span><span class="sxs-lookup"><span data-stu-id="1a39a-120">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="1a39a-121">*x*</span><span class="sxs-lookup"><span data-stu-id="1a39a-121">*x*</span></span>   | [<span data-ttu-id="1a39a-122">**ve**</span><span class="sxs-lookup"><span data-stu-id="1a39a-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="1a39a-123">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="1a39a-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1a39a-124">3</span><span class="sxs-lookup"><span data-stu-id="1a39a-124">3</span></span>    |
| <span data-ttu-id="1a39a-125">*y*</span><span class="sxs-lookup"><span data-stu-id="1a39a-125">*y*</span></span>   | [<span data-ttu-id="1a39a-126">**ve**</span><span class="sxs-lookup"><span data-stu-id="1a39a-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="1a39a-127">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="1a39a-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1a39a-128">3</span><span class="sxs-lookup"><span data-stu-id="1a39a-128">3</span></span>    |
| <span data-ttu-id="1a39a-129">*TZI*</span><span class="sxs-lookup"><span data-stu-id="1a39a-129">*ret*</span></span> | [<span data-ttu-id="1a39a-130">**ve**</span><span class="sxs-lookup"><span data-stu-id="1a39a-130">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="1a39a-131">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="1a39a-131">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1a39a-132">3</span><span class="sxs-lookup"><span data-stu-id="1a39a-132">3</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1a39a-133">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="1a39a-133">Minimum Shader Model</span></span>

<span data-ttu-id="1a39a-134">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1a39a-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1a39a-135">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="1a39a-135">Shader Model</span></span>                                                                       | <span data-ttu-id="1a39a-136">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="1a39a-136">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="1a39a-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="1a39a-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="1a39a-138">ja</span><span class="sxs-lookup"><span data-stu-id="1a39a-138">yes</span></span>                   |
| [<span data-ttu-id="1a39a-139">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1a39a-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="1a39a-140">vs \_ 1 \_ 1 und PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="1a39a-140">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="1a39a-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1a39a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a39a-142">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="1a39a-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

