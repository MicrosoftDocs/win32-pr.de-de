---
title: DOT
description: Gibt das Skalarprodukt zweier Vektoren zurück.
ms.assetid: ad24c06c-0b40-4dc5-a2b9-1d5438635ed8
keywords:
- dothlsl
topic_type:
- apiref
api_name:
- dot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6d05abf0d67628d1d77b362b028107e07b83457
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948997"
---
# <a name="dot"></a><span data-ttu-id="c1232-104">DOT</span><span class="sxs-lookup"><span data-stu-id="c1232-104">dot</span></span>

<span data-ttu-id="c1232-105">Gibt das Skalarprodukt zweier Vektoren zurück.</span><span class="sxs-lookup"><span data-stu-id="c1232-105">Returns the dot product of two vectors.</span></span>



| <span data-ttu-id="c1232-106">*ret* -Punkt (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="c1232-106">*ret* dot(*x*, *y*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="c1232-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1232-107">Parameters</span></span>



| <span data-ttu-id="c1232-108">Element</span><span class="sxs-lookup"><span data-stu-id="c1232-108">Item</span></span>                                                   | <span data-ttu-id="c1232-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1232-109">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="c1232-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="c1232-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="c1232-111">\[im \] ersten Vektor.</span><span class="sxs-lookup"><span data-stu-id="c1232-111">\[in\] The first vector.</span></span><br/>  |
| <span data-ttu-id="c1232-112"><span id="y"></span><span id="Y"></span>*Teenie*</span><span class="sxs-lookup"><span data-stu-id="c1232-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="c1232-113">\[im \] zweiten Vektor.</span><span class="sxs-lookup"><span data-stu-id="c1232-113">\[in\] The second vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="c1232-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1232-114">Return Value</span></span>

<span data-ttu-id="c1232-115">Das Punktprodukt des *x* -Parameters und des *y* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="c1232-115">The dot product of the *x* parameter and the *y* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="c1232-116">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="c1232-116">Type Description</span></span>



| <span data-ttu-id="c1232-117">Name</span><span class="sxs-lookup"><span data-stu-id="c1232-117">Name</span></span>  | [<span data-ttu-id="c1232-118">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="c1232-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="c1232-119">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="c1232-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="c1232-120">Size</span><span class="sxs-lookup"><span data-stu-id="c1232-120">Size</span></span>                            |
|-------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|---------------------------------|
| <span data-ttu-id="c1232-121">*x*</span><span class="sxs-lookup"><span data-stu-id="c1232-121">*x*</span></span>   | [<span data-ttu-id="c1232-122">**ve**</span><span class="sxs-lookup"><span data-stu-id="c1232-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="c1232-123">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c1232-123">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="c1232-124">any</span><span class="sxs-lookup"><span data-stu-id="c1232-124">any</span></span>                             |
| <span data-ttu-id="c1232-125">*y*</span><span class="sxs-lookup"><span data-stu-id="c1232-125">*y*</span></span>   | [<span data-ttu-id="c1232-126">**ve**</span><span class="sxs-lookup"><span data-stu-id="c1232-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="c1232-127">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c1232-127">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="c1232-128">gleiche Dimensionen wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="c1232-128">same dimensions(s) as input *x*</span></span> |
| <span data-ttu-id="c1232-129">*TZI*</span><span class="sxs-lookup"><span data-stu-id="c1232-129">*ret*</span></span> | [<span data-ttu-id="c1232-130">**Skalar**</span><span class="sxs-lookup"><span data-stu-id="c1232-130">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="c1232-131">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c1232-131">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="c1232-132">1</span><span class="sxs-lookup"><span data-stu-id="c1232-132">1</span></span>                               |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c1232-133">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="c1232-133">Minimum Shader Model</span></span>

<span data-ttu-id="c1232-134">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c1232-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c1232-135">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="c1232-135">Shader Model</span></span>                                                                       | <span data-ttu-id="c1232-136">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="c1232-136">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="c1232-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="c1232-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="c1232-138">ja</span><span class="sxs-lookup"><span data-stu-id="c1232-138">yes</span></span>       |
| [<span data-ttu-id="c1232-139">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c1232-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="c1232-140">ja</span><span class="sxs-lookup"><span data-stu-id="c1232-140">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c1232-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c1232-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1232-142">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="c1232-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

