---
title: exp
description: Gibt den Exponentialwert oder den Wert "base-e" des angegebenen-Werts zurück.
ms.assetid: 7a713251-af47-4f8d-b708-40309b80ba18
keywords:
- Exp HLSL
topic_type:
- apiref
api_name:
- exp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 699eb97ae0fd6bbdeba0da47693178d1e4c48e36
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727857"
---
# <a name="exp"></a><span data-ttu-id="01e74-104">exp</span><span class="sxs-lookup"><span data-stu-id="01e74-104">exp</span></span>

<span data-ttu-id="01e74-105">Gibt den Exponentialwert oder e<sup>x</sup>des angegebenen-Werts zurück.</span><span class="sxs-lookup"><span data-stu-id="01e74-105">Returns the base-e exponential, or e<sup>x</sup>, of the specified value.</span></span>



| <span data-ttu-id="01e74-106">*ret* -Exp (*x*)</span><span class="sxs-lookup"><span data-stu-id="01e74-106">*ret* exp(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="01e74-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="01e74-107">Parameters</span></span>



| <span data-ttu-id="01e74-108">Element</span><span class="sxs-lookup"><span data-stu-id="01e74-108">Item</span></span>                                                   | <span data-ttu-id="01e74-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01e74-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="01e74-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="01e74-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="01e74-111">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="01e74-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="01e74-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="01e74-112">Return Value</span></span>

<span data-ttu-id="01e74-113">Der Exponentialwert des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="01e74-113">The base-e exponential of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="01e74-114">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="01e74-114">Type Description</span></span>



| <span data-ttu-id="01e74-115">Name</span><span class="sxs-lookup"><span data-stu-id="01e74-115">Name</span></span>  | [<span data-ttu-id="01e74-116">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="01e74-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="01e74-117">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="01e74-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="01e74-118">Size</span><span class="sxs-lookup"><span data-stu-id="01e74-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="01e74-119">*x*</span><span class="sxs-lookup"><span data-stu-id="01e74-119">*x*</span></span>   | <span data-ttu-id="01e74-120">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="01e74-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="01e74-121">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="01e74-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="01e74-122">any</span><span class="sxs-lookup"><span data-stu-id="01e74-122">any</span></span>                            |
| <span data-ttu-id="01e74-123">*TZI*</span><span class="sxs-lookup"><span data-stu-id="01e74-123">*ret*</span></span> | <span data-ttu-id="01e74-124">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="01e74-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="01e74-125">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="01e74-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="01e74-126">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="01e74-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="01e74-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="01e74-127">Minimum Shader Model</span></span>

<span data-ttu-id="01e74-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="01e74-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="01e74-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="01e74-129">Shader Model</span></span>                                                                       | <span data-ttu-id="01e74-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="01e74-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="01e74-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="01e74-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="01e74-132">ja</span><span class="sxs-lookup"><span data-stu-id="01e74-132">yes</span></span>       |
| [<span data-ttu-id="01e74-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="01e74-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="01e74-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="01e74-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="01e74-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="01e74-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01e74-136">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="01e74-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

