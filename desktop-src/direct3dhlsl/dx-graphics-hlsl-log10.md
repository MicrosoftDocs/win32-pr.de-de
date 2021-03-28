---
title: LOG10
description: Gibt den Logarithmus zur Basis 10 des angegebenen-Werts zurück.
ms.assetid: a94f8438-8153-4a31-bde3-98831edf99e5
keywords:
- LOG10 HLSL
topic_type:
- apiref
api_name:
- log10
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d226dcc33da1aee6d55e21c6d97febc23577503
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315980"
---
# <a name="log10"></a><span data-ttu-id="c453c-104">LOG10</span><span class="sxs-lookup"><span data-stu-id="c453c-104">log10</span></span>

<span data-ttu-id="c453c-105">Gibt den Logarithmus zur Basis 10 des angegebenen-Werts zurück.</span><span class="sxs-lookup"><span data-stu-id="c453c-105">Returns the base-10 logarithm of the specified value.</span></span>



| <span data-ttu-id="c453c-106">*ret* log10 (*x*)</span><span class="sxs-lookup"><span data-stu-id="c453c-106">*ret* log10(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="c453c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c453c-107">Parameters</span></span>



| <span data-ttu-id="c453c-108">Element</span><span class="sxs-lookup"><span data-stu-id="c453c-108">Item</span></span>                                                   | <span data-ttu-id="c453c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c453c-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="c453c-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="c453c-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="c453c-111">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="c453c-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="c453c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c453c-112">Return Value</span></span>

<span data-ttu-id="c453c-113">Der Logarithmus zur Basis 10 des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="c453c-113">The base-10 logarithm of the *x* parameter.</span></span> <span data-ttu-id="c453c-114">Wenn der *x* -Parameter negativ ist, gibt diese Funktion unbegrenzt zurück.</span><span class="sxs-lookup"><span data-stu-id="c453c-114">If the *x* parameter is negative, this function returns indefinite.</span></span> <span data-ttu-id="c453c-115">Wenn das *x* 0 ist, gibt diese Funktion "-inf" zurück.</span><span class="sxs-lookup"><span data-stu-id="c453c-115">If the *x* is 0, this function returns -INF.</span></span>

## <a name="type-description"></a><span data-ttu-id="c453c-116">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="c453c-116">Type Description</span></span>



| <span data-ttu-id="c453c-117">Name</span><span class="sxs-lookup"><span data-stu-id="c453c-117">Name</span></span>  | [<span data-ttu-id="c453c-118">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="c453c-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="c453c-119">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="c453c-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="c453c-120">Size</span><span class="sxs-lookup"><span data-stu-id="c453c-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="c453c-121">*x*</span><span class="sxs-lookup"><span data-stu-id="c453c-121">*x*</span></span>   | <span data-ttu-id="c453c-122">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="c453c-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="c453c-123">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="c453c-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c453c-124">any</span><span class="sxs-lookup"><span data-stu-id="c453c-124">any</span></span>                            |
| <span data-ttu-id="c453c-125">*TZI*</span><span class="sxs-lookup"><span data-stu-id="c453c-125">*ret*</span></span> | <span data-ttu-id="c453c-126">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="c453c-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="c453c-127">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="c453c-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c453c-128">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="c453c-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c453c-129">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="c453c-129">Minimum Shader Model</span></span>

<span data-ttu-id="c453c-130">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c453c-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c453c-131">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="c453c-131">Shader Model</span></span>                                                                       | <span data-ttu-id="c453c-132">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="c453c-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="c453c-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="c453c-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="c453c-134">ja</span><span class="sxs-lookup"><span data-stu-id="c453c-134">yes</span></span>                 |
| [<span data-ttu-id="c453c-135">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c453c-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="c453c-136">Ja ( \_ nur vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="c453c-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="c453c-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c453c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c453c-138">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="c453c-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

