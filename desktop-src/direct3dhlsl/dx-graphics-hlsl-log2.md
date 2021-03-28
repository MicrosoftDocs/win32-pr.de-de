---
title: log2 (corecrt \_ Math. h)
description: Gibt den Logarithmus zur Basis 2 des angegebenen-Werts zurück.
ms.assetid: 0bc75697-92c0-4de5-89bd-2ce824baa03e
keywords:
- log2 HLSL
topic_type:
- apiref
api_name:
- log2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81692071b7886fa3e3096d785bccf80c7eff937a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961748"
---
# <a name="log2"></a><span data-ttu-id="e0175-104">log2</span><span class="sxs-lookup"><span data-stu-id="e0175-104">log2</span></span>

<span data-ttu-id="e0175-105">Gibt den Logarithmus zur Basis 2 des angegebenen-Werts zurück.</span><span class="sxs-lookup"><span data-stu-id="e0175-105">Returns the base-2 logarithm of the specified value.</span></span>



| <span data-ttu-id="e0175-106">*ret* log2 (*x*)</span><span class="sxs-lookup"><span data-stu-id="e0175-106">*ret* log2(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="e0175-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0175-107">Parameters</span></span>



| <span data-ttu-id="e0175-108">Element</span><span class="sxs-lookup"><span data-stu-id="e0175-108">Item</span></span>                                                   | <span data-ttu-id="e0175-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0175-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="e0175-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="e0175-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="e0175-111">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="e0175-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="e0175-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0175-112">Return Value</span></span>

<span data-ttu-id="e0175-113">Der Logarithmus zur Basis 2 des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="e0175-113">The base-2 logarithm of the *x* parameter.</span></span> <span data-ttu-id="e0175-114">Wenn der *x* -Parameter negativ ist, gibt diese Funktion unbegrenzt zurück.</span><span class="sxs-lookup"><span data-stu-id="e0175-114">If the *x* parameter is negative, this function returns indefinite.</span></span> <span data-ttu-id="e0175-115">Wenn der *x* -Parameter 0 (null) ist, gibt diese Funktion + INF zurück.</span><span class="sxs-lookup"><span data-stu-id="e0175-115">If the *x* parameter is 0, this function returns +INF.</span></span>

## <a name="type-description"></a><span data-ttu-id="e0175-116">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="e0175-116">Type Description</span></span>



| <span data-ttu-id="e0175-117">Name</span><span class="sxs-lookup"><span data-stu-id="e0175-117">Name</span></span>  | [<span data-ttu-id="e0175-118">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="e0175-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="e0175-119">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="e0175-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="e0175-120">Size</span><span class="sxs-lookup"><span data-stu-id="e0175-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="e0175-121">*x*</span><span class="sxs-lookup"><span data-stu-id="e0175-121">*x*</span></span>   | <span data-ttu-id="e0175-122">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="e0175-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="e0175-123">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="e0175-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e0175-124">any</span><span class="sxs-lookup"><span data-stu-id="e0175-124">any</span></span>                            |
| <span data-ttu-id="e0175-125">*TZI*</span><span class="sxs-lookup"><span data-stu-id="e0175-125">*ret*</span></span> | <span data-ttu-id="e0175-126">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="e0175-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="e0175-127">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="e0175-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e0175-128">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="e0175-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e0175-129">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="e0175-129">Minimum Shader Model</span></span>

<span data-ttu-id="e0175-130">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e0175-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e0175-131">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="e0175-131">Shader Model</span></span>                                                                       | <span data-ttu-id="e0175-132">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="e0175-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="e0175-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="e0175-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="e0175-134">ja</span><span class="sxs-lookup"><span data-stu-id="e0175-134">yes</span></span>                 |
| [<span data-ttu-id="e0175-135">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e0175-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="e0175-136">Ja ( \_ nur vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="e0175-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="e0175-137">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e0175-137">Requirements</span></span>



| <span data-ttu-id="e0175-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0175-138">Requirement</span></span> | <span data-ttu-id="e0175-139">Wert</span><span class="sxs-lookup"><span data-stu-id="e0175-139">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0175-140">Header</span><span class="sxs-lookup"><span data-stu-id="e0175-140">Header</span></span><br/> | <dl> <span data-ttu-id="e0175-141"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0175-141"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0175-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e0175-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0175-143">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="e0175-143">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

