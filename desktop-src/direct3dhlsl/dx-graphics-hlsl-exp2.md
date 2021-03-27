---
title: exp2 (corecrt \_ Math. h)
description: Gibt den Exponentialwert 2 oder den 2X-Wert des angegebenen-Werts zurück.
ms.assetid: 68b0057c-864d-440b-84f6-781d5fa3b019
keywords:
- exp2 HLSL
topic_type:
- apiref
api_name:
- exp2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63aaf5ee7c29da49ca2e7b21d80af6967721058d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982186"
---
# <a name="exp2"></a><span data-ttu-id="e5bc4-104">exp2</span><span class="sxs-lookup"><span data-stu-id="e5bc4-104">exp2</span></span>

<span data-ttu-id="e5bc4-105">Gibt den Exponentialwert 2 oder 2<sup>x</sup>des angegebenen-Werts zurück.</span><span class="sxs-lookup"><span data-stu-id="e5bc4-105">Returns the base 2 exponential, or 2<sup>x</sup>, of the specified value.</span></span>



| <span data-ttu-id="e5bc4-106">*ret* exp2 (*x*)</span><span class="sxs-lookup"><span data-stu-id="e5bc4-106">*ret* exp2(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="e5bc4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5bc4-107">Parameters</span></span>



| <span data-ttu-id="e5bc4-108">Element</span><span class="sxs-lookup"><span data-stu-id="e5bc4-108">Item</span></span>                                                   | <span data-ttu-id="e5bc4-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5bc4-109">Description</span></span>                                           |
|--------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="e5bc4-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="e5bc4-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="e5bc4-111">\[im \] angegebenen Gleit Komma Wert.</span><span class="sxs-lookup"><span data-stu-id="e5bc4-111">\[in\] The specified floating-point value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="e5bc4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e5bc4-112">Return Value</span></span>

<span data-ttu-id="e5bc4-113">Die exponentialbasis 2 des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="e5bc4-113">The base 2 exponential of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="e5bc4-114">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="e5bc4-114">Type Description</span></span>



| <span data-ttu-id="e5bc4-115">Name</span><span class="sxs-lookup"><span data-stu-id="e5bc4-115">Name</span></span>  | [<span data-ttu-id="e5bc4-116">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="e5bc4-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="e5bc4-117">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="e5bc4-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="e5bc4-118">Size</span><span class="sxs-lookup"><span data-stu-id="e5bc4-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="e5bc4-119">*x*</span><span class="sxs-lookup"><span data-stu-id="e5bc4-119">*x*</span></span>   | <span data-ttu-id="e5bc4-120">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="e5bc4-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="e5bc4-121">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="e5bc4-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e5bc4-122">any</span><span class="sxs-lookup"><span data-stu-id="e5bc4-122">any</span></span>                            |
| <span data-ttu-id="e5bc4-123">*TZI*</span><span class="sxs-lookup"><span data-stu-id="e5bc4-123">*ret*</span></span> | <span data-ttu-id="e5bc4-124">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="e5bc4-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="e5bc4-125">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="e5bc4-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e5bc4-126">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="e5bc4-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e5bc4-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="e5bc4-127">Minimum Shader Model</span></span>

<span data-ttu-id="e5bc4-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e5bc4-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e5bc4-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="e5bc4-129">Shader Model</span></span>                                                                       | <span data-ttu-id="e5bc4-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="e5bc4-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="e5bc4-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="e5bc4-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="e5bc4-132">ja</span><span class="sxs-lookup"><span data-stu-id="e5bc4-132">yes</span></span>       |
| [<span data-ttu-id="e5bc4-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e5bc4-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="e5bc4-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="e5bc4-134">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="e5bc4-135">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e5bc4-135">Requirements</span></span>



| <span data-ttu-id="e5bc4-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5bc4-136">Requirement</span></span> | <span data-ttu-id="e5bc4-137">Wert</span><span class="sxs-lookup"><span data-stu-id="e5bc4-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5bc4-138">Header</span><span class="sxs-lookup"><span data-stu-id="e5bc4-138">Header</span></span><br/> | <dl> <span data-ttu-id="e5bc4-139"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5bc4-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5bc4-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e5bc4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5bc4-141">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="e5bc4-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

