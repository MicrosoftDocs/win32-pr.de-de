---
title: Round (corecrt \_ Math. h)
description: Rundet den angegebenen Wert auf die nächste ganze Zahl.
ms.assetid: 258ce717-dca1-4ed2-ad98-1ecfdb58f939
keywords:
- runhlsl
topic_type:
- apiref
api_name:
- round
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f00bf845dfe16a92729b523fba62f6fd6dcde2b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961644"
---
# <a name="round"></a><span data-ttu-id="061f8-104">round</span><span class="sxs-lookup"><span data-stu-id="061f8-104">round</span></span>

<span data-ttu-id="061f8-105">Rundet den angegebenen Wert auf die nächste ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="061f8-105">Rounds the specified value to the nearest integer.</span></span> <span data-ttu-id="061f8-106">Die Hälfte der Fälle wird auch auf die nächstgelegene gerundet.</span><span class="sxs-lookup"><span data-stu-id="061f8-106">Halfway cases are rounded to the nearest even.</span></span>



| <span data-ttu-id="061f8-107">*ret* -Runde (*x*)</span><span class="sxs-lookup"><span data-stu-id="061f8-107">*ret* round(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="061f8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="061f8-108">Parameters</span></span>



| <span data-ttu-id="061f8-109">Element</span><span class="sxs-lookup"><span data-stu-id="061f8-109">Item</span></span>                                                   | <span data-ttu-id="061f8-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="061f8-110">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="061f8-111"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="061f8-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="061f8-112">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="061f8-112">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="061f8-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="061f8-113">Return Value</span></span>

<span data-ttu-id="061f8-114">Der *x* -Parameter, gerundet auf die nächste ganze Zahl innerhalb eines Gleit Komma Typs.</span><span class="sxs-lookup"><span data-stu-id="061f8-114">The *x* parameter, rounded to the nearest integer within a floating-point type.</span></span>

## <a name="type-description"></a><span data-ttu-id="061f8-115">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="061f8-115">Type Description</span></span>



| <span data-ttu-id="061f8-116">Name</span><span class="sxs-lookup"><span data-stu-id="061f8-116">Name</span></span>  | [<span data-ttu-id="061f8-117">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="061f8-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="061f8-118">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="061f8-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="061f8-119">Size</span><span class="sxs-lookup"><span data-stu-id="061f8-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="061f8-120">*x*</span><span class="sxs-lookup"><span data-stu-id="061f8-120">*x*</span></span>   | <span data-ttu-id="061f8-121">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="061f8-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="061f8-122">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="061f8-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="061f8-123">any</span><span class="sxs-lookup"><span data-stu-id="061f8-123">any</span></span>                            |
| <span data-ttu-id="061f8-124">*TZI*</span><span class="sxs-lookup"><span data-stu-id="061f8-124">*ret*</span></span> | <span data-ttu-id="061f8-125">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="061f8-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="061f8-126">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="061f8-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="061f8-127">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="061f8-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="061f8-128">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="061f8-128">Minimum Shader Model</span></span>

<span data-ttu-id="061f8-129">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="061f8-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="061f8-130">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="061f8-130">Shader Model</span></span>                                                                       | <span data-ttu-id="061f8-131">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="061f8-131">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="061f8-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="061f8-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="061f8-133">ja</span><span class="sxs-lookup"><span data-stu-id="061f8-133">yes</span></span>                 |
| [<span data-ttu-id="061f8-134">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="061f8-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="061f8-135">Ja ( \_ nur vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="061f8-135">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="061f8-136">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="061f8-136">Requirements</span></span>



| <span data-ttu-id="061f8-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="061f8-137">Requirement</span></span> | <span data-ttu-id="061f8-138">Wert</span><span class="sxs-lookup"><span data-stu-id="061f8-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="061f8-139">Header</span><span class="sxs-lookup"><span data-stu-id="061f8-139">Header</span></span><br/> | <dl> <span data-ttu-id="061f8-140"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="061f8-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="061f8-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="061f8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="061f8-142">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="061f8-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

