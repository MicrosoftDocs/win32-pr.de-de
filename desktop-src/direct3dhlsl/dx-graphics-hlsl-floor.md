---
title: Floor (corecrt \_ Math. h)
description: Gibt die größte ganze Zahl zurück, die kleiner oder gleich dem angegebenen Wert ist.
ms.assetid: f7193425-2448-4ae6-99d5-bb5e1aa74111
keywords:
- bodenhlsl
topic_type:
- apiref
api_name:
- floor
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ecb46719d5361ec9f7c36b21d94793bc9a67ffe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982185"
---
# <a name="floor"></a><span data-ttu-id="134f7-104">floor</span><span class="sxs-lookup"><span data-stu-id="134f7-104">floor</span></span>

<span data-ttu-id="134f7-105">Gibt die größte ganze Zahl zurück, die kleiner oder gleich dem angegebenen Wert ist.</span><span class="sxs-lookup"><span data-stu-id="134f7-105">Returns the largest integer that is less than or equal to the specified value.</span></span>



| <span data-ttu-id="134f7-106">*ret* -Floor (*x*)</span><span class="sxs-lookup"><span data-stu-id="134f7-106">*ret* floor(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="134f7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="134f7-107">Parameters</span></span>



| <span data-ttu-id="134f7-108">Element</span><span class="sxs-lookup"><span data-stu-id="134f7-108">Item</span></span>                                                   | <span data-ttu-id="134f7-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="134f7-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="134f7-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="134f7-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="134f7-111">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="134f7-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="134f7-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="134f7-112">Return Value</span></span>

<span data-ttu-id="134f7-113">Der größte ganzzahlige Wert (zurückgegeben als Gleit kommatyp), der kleiner oder gleich dem *x* -Parameter ist.</span><span class="sxs-lookup"><span data-stu-id="134f7-113">The largest integer value (returned as a floating-point type) that is less than or equal to the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="134f7-114">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="134f7-114">Type Description</span></span>



| <span data-ttu-id="134f7-115">Name</span><span class="sxs-lookup"><span data-stu-id="134f7-115">Name</span></span>  | [<span data-ttu-id="134f7-116">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="134f7-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="134f7-117">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="134f7-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="134f7-118">Size</span><span class="sxs-lookup"><span data-stu-id="134f7-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="134f7-119">*x*</span><span class="sxs-lookup"><span data-stu-id="134f7-119">*x*</span></span>   | <span data-ttu-id="134f7-120">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="134f7-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="134f7-121">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="134f7-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="134f7-122">any</span><span class="sxs-lookup"><span data-stu-id="134f7-122">any</span></span>                            |
| <span data-ttu-id="134f7-123">*TZI*</span><span class="sxs-lookup"><span data-stu-id="134f7-123">*ret*</span></span> | <span data-ttu-id="134f7-124">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="134f7-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="134f7-125">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="134f7-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="134f7-126">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="134f7-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="134f7-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="134f7-127">Minimum Shader Model</span></span>

<span data-ttu-id="134f7-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="134f7-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="134f7-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="134f7-129">Shader Model</span></span>                                                                       | <span data-ttu-id="134f7-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="134f7-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="134f7-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="134f7-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="134f7-132">ja</span><span class="sxs-lookup"><span data-stu-id="134f7-132">yes</span></span>       |
| [<span data-ttu-id="134f7-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="134f7-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="134f7-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="134f7-134">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="134f7-135">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="134f7-135">Requirements</span></span>



| <span data-ttu-id="134f7-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="134f7-136">Requirement</span></span> | <span data-ttu-id="134f7-137">Wert</span><span class="sxs-lookup"><span data-stu-id="134f7-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="134f7-138">Header</span><span class="sxs-lookup"><span data-stu-id="134f7-138">Header</span></span><br/> | <dl> <span data-ttu-id="134f7-139"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="134f7-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="134f7-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="134f7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="134f7-141">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="134f7-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

