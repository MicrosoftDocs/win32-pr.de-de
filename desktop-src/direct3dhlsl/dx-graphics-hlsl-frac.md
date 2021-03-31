---
title: Frac
description: Gibt den Bruchteil (oder Dezimalwert) von x zurück. ein Wert größer oder gleich 0 und kleiner als 1.
ms.assetid: 4e85390f-2b1a-402b-b932-09b80097f7e6
keywords:
- Frac HLSL
topic_type:
- apiref
api_name:
- frac
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 468bddc34f22f9bb5f34871102678e1765148b11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474109"
---
# <a name="frac"></a><span data-ttu-id="d00cb-104">Frac</span><span class="sxs-lookup"><span data-stu-id="d00cb-104">frac</span></span>

<span data-ttu-id="d00cb-105">Gibt den Bruchteil (oder Dezimalwert) von x zurück. ein Wert größer oder gleich 0 und kleiner als 1.</span><span class="sxs-lookup"><span data-stu-id="d00cb-105">Returns the fractional (or decimal) part of x; which is greater than or equal to 0 and less than 1.</span></span>

<span data-ttu-id="d00cb-106">Siehe auch [trunc](./dx-graphics-hlsl-trunc.md).</span><span class="sxs-lookup"><span data-stu-id="d00cb-106">Also see [trunc](./dx-graphics-hlsl-trunc.md).</span></span>

| <span data-ttu-id="d00cb-107">*ret* -Frac (*x*)</span><span class="sxs-lookup"><span data-stu-id="d00cb-107">*ret* frac(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="d00cb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d00cb-108">Parameters</span></span>



| <span data-ttu-id="d00cb-109">Element</span><span class="sxs-lookup"><span data-stu-id="d00cb-109">Item</span></span>                                                   | <span data-ttu-id="d00cb-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d00cb-110">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="d00cb-111"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="d00cb-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="d00cb-112">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="d00cb-112">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d00cb-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d00cb-113">Return Value</span></span>

<span data-ttu-id="d00cb-114">Der Bruch Teil des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="d00cb-114">The fractional part of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="d00cb-115">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="d00cb-115">Type Description</span></span>



| <span data-ttu-id="d00cb-116">Name</span><span class="sxs-lookup"><span data-stu-id="d00cb-116">Name</span></span>  | [<span data-ttu-id="d00cb-117">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="d00cb-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="d00cb-118">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="d00cb-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d00cb-119">Size</span><span class="sxs-lookup"><span data-stu-id="d00cb-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="d00cb-120">*x*</span><span class="sxs-lookup"><span data-stu-id="d00cb-120">*x*</span></span>   | <span data-ttu-id="d00cb-121">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="d00cb-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="d00cb-122">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="d00cb-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d00cb-123">any</span><span class="sxs-lookup"><span data-stu-id="d00cb-123">any</span></span>                            |
| <span data-ttu-id="d00cb-124">*TZI*</span><span class="sxs-lookup"><span data-stu-id="d00cb-124">*ret*</span></span> | <span data-ttu-id="d00cb-125">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="d00cb-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="d00cb-126">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="d00cb-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d00cb-127">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="d00cb-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d00cb-128">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="d00cb-128">Minimum Shader Model</span></span>

<span data-ttu-id="d00cb-129">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d00cb-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d00cb-130">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="d00cb-130">Shader Model</span></span>                                                                       | <span data-ttu-id="d00cb-131">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="d00cb-131">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="d00cb-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="d00cb-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="d00cb-133">ja</span><span class="sxs-lookup"><span data-stu-id="d00cb-133">yes</span></span>       |
| [<span data-ttu-id="d00cb-134">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d00cb-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="d00cb-135">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d00cb-135">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="d00cb-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d00cb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d00cb-137">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d00cb-137">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

