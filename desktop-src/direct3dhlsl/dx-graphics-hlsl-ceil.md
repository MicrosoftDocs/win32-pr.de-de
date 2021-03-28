---
title: ceil (corecrt \_ Math. h)
description: Gibt den kleinsten ganzzahligen Wert zurück, der größer oder gleich dem angegebenen Wert ist.
ms.assetid: 9823f321-14c3-4b27-9a4b-7a885cece39b
keywords:
- ceil HLSL
topic_type:
- apiref
api_name:
- ceil
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec86db320119b7f162ed48a748c1d1ff4335b6f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995847"
---
# <a name="ceil"></a><span data-ttu-id="0bce7-104">ceil</span><span class="sxs-lookup"><span data-stu-id="0bce7-104">ceil</span></span>

<span data-ttu-id="0bce7-105">Gibt den kleinsten ganzzahligen Wert zurück, der größer oder gleich dem angegebenen Wert ist.</span><span class="sxs-lookup"><span data-stu-id="0bce7-105">Returns the smallest integer value that is greater than or equal to the specified value.</span></span>



| <span data-ttu-id="0bce7-106">*ret* ceil (*x*)</span><span class="sxs-lookup"><span data-stu-id="0bce7-106">*ret* ceil(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="0bce7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0bce7-107">Parameters</span></span>



| <span data-ttu-id="0bce7-108">Element</span><span class="sxs-lookup"><span data-stu-id="0bce7-108">Item</span></span>                                                   | <span data-ttu-id="0bce7-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0bce7-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="0bce7-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="0bce7-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="0bce7-111">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="0bce7-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="0bce7-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0bce7-112">Return Value</span></span>

<span data-ttu-id="0bce7-113">Der kleinste ganzzahlige Wert (zurückgegeben als Gleit kommatyp), der größer oder gleich dem *x* -Parameter ist.</span><span class="sxs-lookup"><span data-stu-id="0bce7-113">The smallest integer value (returned as a floating-point type) that is greater than or equal to the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="0bce7-114">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="0bce7-114">Type Description</span></span>



| <span data-ttu-id="0bce7-115">Name</span><span class="sxs-lookup"><span data-stu-id="0bce7-115">Name</span></span>  | [<span data-ttu-id="0bce7-116">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="0bce7-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="0bce7-117">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="0bce7-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="0bce7-118">Size</span><span class="sxs-lookup"><span data-stu-id="0bce7-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="0bce7-119">*x*</span><span class="sxs-lookup"><span data-stu-id="0bce7-119">*x*</span></span>   | <span data-ttu-id="0bce7-120">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="0bce7-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="0bce7-121">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="0bce7-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0bce7-122">any</span><span class="sxs-lookup"><span data-stu-id="0bce7-122">any</span></span>                            |
| <span data-ttu-id="0bce7-123">*TZI*</span><span class="sxs-lookup"><span data-stu-id="0bce7-123">*ret*</span></span> | <span data-ttu-id="0bce7-124">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="0bce7-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="0bce7-125">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="0bce7-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0bce7-126">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="0bce7-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0bce7-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="0bce7-127">Minimum Shader Model</span></span>

<span data-ttu-id="0bce7-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0bce7-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0bce7-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="0bce7-129">Shader Model</span></span>                                                                       | <span data-ttu-id="0bce7-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="0bce7-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="0bce7-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="0bce7-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="0bce7-132">ja</span><span class="sxs-lookup"><span data-stu-id="0bce7-132">yes</span></span>       |
| [<span data-ttu-id="0bce7-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bce7-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="0bce7-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="0bce7-134">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="0bce7-135">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0bce7-135">Requirements</span></span>



| <span data-ttu-id="0bce7-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0bce7-136">Requirement</span></span> | <span data-ttu-id="0bce7-137">Wert</span><span class="sxs-lookup"><span data-stu-id="0bce7-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bce7-138">Header</span><span class="sxs-lookup"><span data-stu-id="0bce7-138">Header</span></span><br/> | <dl> <span data-ttu-id="0bce7-139"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bce7-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bce7-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0bce7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bce7-141">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="0bce7-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

