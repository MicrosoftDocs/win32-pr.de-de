---
title: cosh
description: Gibt den hyperbolischen Kosinus des angegebenen-Werts zurück.
ms.assetid: ed68c461-de91-4ce4-a424-8ab28ee43f23
keywords:
- cosh HLSL
topic_type:
- apiref
api_name:
- cosh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3bd6cad2b79e849d8f20bbaf5baa6cfc7db0b702
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993583"
---
# <a name="cosh"></a><span data-ttu-id="e8ed7-104">cosh</span><span class="sxs-lookup"><span data-stu-id="e8ed7-104">cosh</span></span>

<span data-ttu-id="e8ed7-105">Gibt den hyperbolischen Kosinus des angegebenen-Werts zurück.</span><span class="sxs-lookup"><span data-stu-id="e8ed7-105">Returns the hyperbolic cosine of the specified value.</span></span>



| <span data-ttu-id="e8ed7-106">*ret* cosh (*x*)</span><span class="sxs-lookup"><span data-stu-id="e8ed7-106">*ret* cosh(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="e8ed7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8ed7-107">Parameters</span></span>



| <span data-ttu-id="e8ed7-108">Element</span><span class="sxs-lookup"><span data-stu-id="e8ed7-108">Item</span></span>                                                   | <span data-ttu-id="e8ed7-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8ed7-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="e8ed7-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="e8ed7-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="e8ed7-111">\[im \] angegebenen Wert im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="e8ed7-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="e8ed7-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8ed7-112">Return Value</span></span>

<span data-ttu-id="e8ed7-113">Der hyperbolische Kosinus des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="e8ed7-113">The hyperbolic cosine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="e8ed7-114">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="e8ed7-114">Type Description</span></span>



| <span data-ttu-id="e8ed7-115">Name</span><span class="sxs-lookup"><span data-stu-id="e8ed7-115">Name</span></span>  | [<span data-ttu-id="e8ed7-116">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="e8ed7-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="e8ed7-117">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="e8ed7-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="e8ed7-118">Size</span><span class="sxs-lookup"><span data-stu-id="e8ed7-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="e8ed7-119">*x*</span><span class="sxs-lookup"><span data-stu-id="e8ed7-119">*x*</span></span>   | <span data-ttu-id="e8ed7-120">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="e8ed7-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="e8ed7-121">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="e8ed7-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e8ed7-122">any</span><span class="sxs-lookup"><span data-stu-id="e8ed7-122">any</span></span>                            |
| <span data-ttu-id="e8ed7-123">*TZI*</span><span class="sxs-lookup"><span data-stu-id="e8ed7-123">*ret*</span></span> | <span data-ttu-id="e8ed7-124">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="e8ed7-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="e8ed7-125">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="e8ed7-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e8ed7-126">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="e8ed7-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e8ed7-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="e8ed7-127">Minimum Shader Model</span></span>

<span data-ttu-id="e8ed7-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e8ed7-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e8ed7-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="e8ed7-129">Shader Model</span></span>                                                                       | <span data-ttu-id="e8ed7-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="e8ed7-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="e8ed7-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="e8ed7-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="e8ed7-132">ja</span><span class="sxs-lookup"><span data-stu-id="e8ed7-132">yes</span></span>       |
| [<span data-ttu-id="e8ed7-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8ed7-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="e8ed7-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="e8ed7-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="e8ed7-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e8ed7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8ed7-136">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="e8ed7-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

