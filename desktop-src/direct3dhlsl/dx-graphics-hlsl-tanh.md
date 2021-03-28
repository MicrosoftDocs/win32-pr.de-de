---
title: tanh
description: Gibt den hyperbolischen Tangens des angegebenen-Werts zurück.
ms.assetid: e2d27aa0-5e03-4f2f-a29c-884711710c8d
keywords:
- tanh HLSL
topic_type:
- apiref
api_name:
- tanh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c5312aaac6d6f164e940f99183e61688b393fbd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039186"
---
# <a name="tanh"></a><span data-ttu-id="7dec6-104">tanh</span><span class="sxs-lookup"><span data-stu-id="7dec6-104">tanh</span></span>

<span data-ttu-id="7dec6-105">Gibt den hyperbolischen Tangens des angegebenen-Werts zurück.</span><span class="sxs-lookup"><span data-stu-id="7dec6-105">Returns the hyperbolic tangent of the specified value.</span></span>



| <span data-ttu-id="7dec6-106">*ret* -tanh (*x*)</span><span class="sxs-lookup"><span data-stu-id="7dec6-106">*ret* tanh(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="7dec6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7dec6-107">Parameters</span></span>



| <span data-ttu-id="7dec6-108">Element</span><span class="sxs-lookup"><span data-stu-id="7dec6-108">Item</span></span>                                                   | <span data-ttu-id="7dec6-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7dec6-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="7dec6-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="7dec6-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="7dec6-111">\[im \] angegebenen Wert im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="7dec6-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="7dec6-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7dec6-112">Return Value</span></span>

<span data-ttu-id="7dec6-113">Der hyperbolische Tangens des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="7dec6-113">The hyperbolic tangent of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="7dec6-114">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="7dec6-114">Type Description</span></span>



| <span data-ttu-id="7dec6-115">Name</span><span class="sxs-lookup"><span data-stu-id="7dec6-115">Name</span></span>  | [<span data-ttu-id="7dec6-116">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="7dec6-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="7dec6-117">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="7dec6-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="7dec6-118">Size</span><span class="sxs-lookup"><span data-stu-id="7dec6-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="7dec6-119">*x*</span><span class="sxs-lookup"><span data-stu-id="7dec6-119">*x*</span></span>   | <span data-ttu-id="7dec6-120">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="7dec6-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="7dec6-121">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="7dec6-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7dec6-122">any</span><span class="sxs-lookup"><span data-stu-id="7dec6-122">any</span></span>                            |
| <span data-ttu-id="7dec6-123">*TZI*</span><span class="sxs-lookup"><span data-stu-id="7dec6-123">*ret*</span></span> | <span data-ttu-id="7dec6-124">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="7dec6-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="7dec6-125">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="7dec6-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7dec6-126">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="7dec6-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7dec6-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="7dec6-127">Minimum Shader Model</span></span>

<span data-ttu-id="7dec6-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7dec6-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7dec6-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="7dec6-129">Shader Model</span></span>                                                                       | <span data-ttu-id="7dec6-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="7dec6-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="7dec6-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="7dec6-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="7dec6-132">ja</span><span class="sxs-lookup"><span data-stu-id="7dec6-132">yes</span></span>                 |
| [<span data-ttu-id="7dec6-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7dec6-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="7dec6-134">Ja ( \_ nur vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="7dec6-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="7dec6-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7dec6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dec6-136">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="7dec6-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

