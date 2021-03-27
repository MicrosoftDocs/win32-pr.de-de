---
title: log
description: Gibt den Logarithmus zur Basis-e des angegebenen-Werts zurück.
ms.assetid: 443e7aa7-7219-40ad-aafc-4bce09c8f596
keywords:
- Protokoll-HLSL
topic_type:
- apiref
api_name:
- log
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cdd08fe178925406145476b3250e8d256b263c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729161"
---
# <a name="log"></a><span data-ttu-id="4d8a8-104">log</span><span class="sxs-lookup"><span data-stu-id="4d8a8-104">log</span></span>

<span data-ttu-id="4d8a8-105">Gibt den Logarithmus zur Basis-e des angegebenen-Werts zurück.</span><span class="sxs-lookup"><span data-stu-id="4d8a8-105">Returns the base-e logarithm of the specified value.</span></span>



| <span data-ttu-id="4d8a8-106">*ret* -Protokoll (*x*)</span><span class="sxs-lookup"><span data-stu-id="4d8a8-106">*ret* log(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="4d8a8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d8a8-107">Parameters</span></span>



| <span data-ttu-id="4d8a8-108">Element</span><span class="sxs-lookup"><span data-stu-id="4d8a8-108">Item</span></span>                                                   | <span data-ttu-id="4d8a8-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d8a8-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="4d8a8-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="4d8a8-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="4d8a8-111">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="4d8a8-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="4d8a8-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d8a8-112">Return Value</span></span>

<span data-ttu-id="4d8a8-113">Der Logarithmus für die Basis-e des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="4d8a8-113">The base-e logarithm of the *x* parameter.</span></span> <span data-ttu-id="4d8a8-114">Wenn der *x* -Parameter negativ ist, gibt diese Funktion unbegrenzt zurück.</span><span class="sxs-lookup"><span data-stu-id="4d8a8-114">If the *x* parameter is negative, this function returns indefinite.</span></span> <span data-ttu-id="4d8a8-115">Wenn der *x* -Parameter 0 ist, gibt diese Funktion "-inf" zurück.</span><span class="sxs-lookup"><span data-stu-id="4d8a8-115">If the *x* parameter is 0, this function returns -INF.</span></span>

## <a name="type-description"></a><span data-ttu-id="4d8a8-116">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="4d8a8-116">Type Description</span></span>



| <span data-ttu-id="4d8a8-117">Name</span><span class="sxs-lookup"><span data-stu-id="4d8a8-117">Name</span></span>  | [<span data-ttu-id="4d8a8-118">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="4d8a8-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="4d8a8-119">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="4d8a8-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="4d8a8-120">Size</span><span class="sxs-lookup"><span data-stu-id="4d8a8-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="4d8a8-121">*x*</span><span class="sxs-lookup"><span data-stu-id="4d8a8-121">*x*</span></span>   | <span data-ttu-id="4d8a8-122">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="4d8a8-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="4d8a8-123">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="4d8a8-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4d8a8-124">any</span><span class="sxs-lookup"><span data-stu-id="4d8a8-124">any</span></span>                            |
| <span data-ttu-id="4d8a8-125">*TZI*</span><span class="sxs-lookup"><span data-stu-id="4d8a8-125">*ret*</span></span> | <span data-ttu-id="4d8a8-126">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="4d8a8-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="4d8a8-127">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="4d8a8-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4d8a8-128">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="4d8a8-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4d8a8-129">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="4d8a8-129">Minimum Shader Model</span></span>

<span data-ttu-id="4d8a8-130">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4d8a8-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4d8a8-131">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="4d8a8-131">Shader Model</span></span>                                                                       | <span data-ttu-id="4d8a8-132">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="4d8a8-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="4d8a8-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="4d8a8-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="4d8a8-134">ja</span><span class="sxs-lookup"><span data-stu-id="4d8a8-134">yes</span></span>                 |
| [<span data-ttu-id="4d8a8-135">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4d8a8-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="4d8a8-136">Ja ( \_ nur vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="4d8a8-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="4d8a8-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4d8a8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d8a8-138">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="4d8a8-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

