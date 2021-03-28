---
title: asin
description: Gibt den Arkus Sinus des angegebenen-Werts zurück.
ms.assetid: 49559cb2-3305-4c97-8071-1589bcca3a75
keywords:
- ASIN HLSL
topic_type:
- apiref
api_name:
- asin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2f64865cb3172037f6630dc422a69aa4d135b1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039546"
---
# <a name="asin"></a><span data-ttu-id="16383-104">asin</span><span class="sxs-lookup"><span data-stu-id="16383-104">asin</span></span>

<span data-ttu-id="16383-105">Gibt den Arkus Sinus des angegebenen-Werts zurück.</span><span class="sxs-lookup"><span data-stu-id="16383-105">Returns the arcsine of the specified value.</span></span>



| <span data-ttu-id="16383-106">*ret* ASIN (*x*)</span><span class="sxs-lookup"><span data-stu-id="16383-106">*ret* asin(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="16383-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="16383-107">Parameters</span></span>



| <span data-ttu-id="16383-108">Element</span><span class="sxs-lookup"><span data-stu-id="16383-108">Item</span></span>                                                   | <span data-ttu-id="16383-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16383-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="16383-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="16383-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="16383-111">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="16383-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="16383-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="16383-112">Return Value</span></span>

<span data-ttu-id="16383-113">Der Arkus Sinus des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="16383-113">The arcsine of the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="16383-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16383-114">Remarks</span></span>

<span data-ttu-id="16383-115">Jede Komponente des *x* -Parameters muss innerhalb des Bereichs von--/2 bis 1 liegen/2.</span><span class="sxs-lookup"><span data-stu-id="16383-115">Each component of the *x* parameter should be within the range of -π/2 to π/2.</span></span>

## <a name="type-description"></a><span data-ttu-id="16383-116">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="16383-116">Type Description</span></span>



| <span data-ttu-id="16383-117">Name</span><span class="sxs-lookup"><span data-stu-id="16383-117">Name</span></span>  | [<span data-ttu-id="16383-118">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="16383-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="16383-119">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="16383-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="16383-120">Size</span><span class="sxs-lookup"><span data-stu-id="16383-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="16383-121">*x*</span><span class="sxs-lookup"><span data-stu-id="16383-121">*x*</span></span>   | <span data-ttu-id="16383-122">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="16383-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="16383-123">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="16383-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="16383-124">any</span><span class="sxs-lookup"><span data-stu-id="16383-124">any</span></span>                            |
| <span data-ttu-id="16383-125">*TZI*</span><span class="sxs-lookup"><span data-stu-id="16383-125">*ret*</span></span> | <span data-ttu-id="16383-126">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="16383-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="16383-127">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="16383-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="16383-128">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="16383-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="16383-129">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="16383-129">Minimum Shader Model</span></span>

<span data-ttu-id="16383-130">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="16383-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="16383-131">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="16383-131">Shader Model</span></span>                                                                       | <span data-ttu-id="16383-132">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="16383-132">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="16383-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="16383-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="16383-134">ja</span><span class="sxs-lookup"><span data-stu-id="16383-134">yes</span></span>       |
| [<span data-ttu-id="16383-135">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16383-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="16383-136">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="16383-136">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="16383-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="16383-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16383-138">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="16383-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

