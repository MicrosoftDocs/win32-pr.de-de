---
title: tan
description: Gibt den Tangens des angegebenen-Werts zurück.
ms.assetid: ca03b184-9e1a-4152-9292-f8af38aa9423
keywords:
- Tan HLSL
topic_type:
- apiref
api_name:
- tan
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf9451a2bf1a5759470e87343f1b4a15583b470a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728208"
---
# <a name="tan"></a><span data-ttu-id="fd961-104">tan</span><span class="sxs-lookup"><span data-stu-id="fd961-104">tan</span></span>

<span data-ttu-id="fd961-105">Gibt den Tangens des angegebenen-Werts zurück.</span><span class="sxs-lookup"><span data-stu-id="fd961-105">Returns the tangent of the specified value.</span></span>



| <span data-ttu-id="fd961-106">*ret* Tan (*x*)</span><span class="sxs-lookup"><span data-stu-id="fd961-106">*ret* tan(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="fd961-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd961-107">Parameters</span></span>



| <span data-ttu-id="fd961-108">Element</span><span class="sxs-lookup"><span data-stu-id="fd961-108">Item</span></span>                                                   | <span data-ttu-id="fd961-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd961-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="fd961-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="fd961-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="fd961-111">\[im \] angegebenen Wert im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="fd961-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="fd961-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd961-112">Return Value</span></span>

<span data-ttu-id="fd961-113">Der Tangens des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="fd961-113">The tangent of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="fd961-114">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="fd961-114">Type Description</span></span>



| <span data-ttu-id="fd961-115">Name</span><span class="sxs-lookup"><span data-stu-id="fd961-115">Name</span></span>  | [<span data-ttu-id="fd961-116">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="fd961-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="fd961-117">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="fd961-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="fd961-118">Size</span><span class="sxs-lookup"><span data-stu-id="fd961-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="fd961-119">*x*</span><span class="sxs-lookup"><span data-stu-id="fd961-119">*x*</span></span>   | <span data-ttu-id="fd961-120">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="fd961-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="fd961-121">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="fd961-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="fd961-122">any</span><span class="sxs-lookup"><span data-stu-id="fd961-122">any</span></span>                            |
| <span data-ttu-id="fd961-123">*TZI*</span><span class="sxs-lookup"><span data-stu-id="fd961-123">*ret*</span></span> | <span data-ttu-id="fd961-124">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="fd961-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="fd961-125">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="fd961-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="fd961-126">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="fd961-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fd961-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="fd961-127">Minimum Shader Model</span></span>

<span data-ttu-id="fd961-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fd961-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fd961-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="fd961-129">Shader Model</span></span>                                                                       | <span data-ttu-id="fd961-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="fd961-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="fd961-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="fd961-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="fd961-132">ja</span><span class="sxs-lookup"><span data-stu-id="fd961-132">yes</span></span>                 |
| [<span data-ttu-id="fd961-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fd961-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="fd961-134">Ja ( \_ nur vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="fd961-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="fd961-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fd961-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd961-136">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="fd961-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

