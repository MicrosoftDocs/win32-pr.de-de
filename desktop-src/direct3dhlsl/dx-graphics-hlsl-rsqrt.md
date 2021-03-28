---
title: rsqrt
description: Gibt die gegenseitige der Quadratwurzel des angegebenen-Werts zurück.
ms.assetid: 4e266e41-cde9-4a59-8937-98bfc63f3b5d
keywords:
- rsqrt HLSL
topic_type:
- apiref
api_name:
- rsqrt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56eb5f1cba8510e57a2c4b5622e10dc91666b6a6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993430"
---
# <a name="rsqrt"></a><span data-ttu-id="86f6b-104">rsqrt</span><span class="sxs-lookup"><span data-stu-id="86f6b-104">rsqrt</span></span>

<span data-ttu-id="86f6b-105">Gibt die gegenseitige der Quadratwurzel des angegebenen-Werts zurück.</span><span class="sxs-lookup"><span data-stu-id="86f6b-105">Returns the reciprocal of the square root of the specified value.</span></span>



| <span data-ttu-id="86f6b-106">*ret* rsqrt (*x*)</span><span class="sxs-lookup"><span data-stu-id="86f6b-106">*ret* rsqrt(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="86f6b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="86f6b-107">Parameters</span></span>



| <span data-ttu-id="86f6b-108">Element</span><span class="sxs-lookup"><span data-stu-id="86f6b-108">Item</span></span>                                                   | <span data-ttu-id="86f6b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86f6b-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="86f6b-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="86f6b-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="86f6b-111">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="86f6b-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="86f6b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86f6b-112">Return Value</span></span>

<span data-ttu-id="86f6b-113">Die gegenseitige der Quadratwurzel des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="86f6b-113">The reciprocal of the square root of the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="86f6b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86f6b-114">Remarks</span></span>

<span data-ttu-id="86f6b-115">Diese Funktion verwendet die folgende Formel: 1/ **sqrt**(*x*).</span><span class="sxs-lookup"><span data-stu-id="86f6b-115">This function uses the following formula: 1 / **sqrt**(*x*).</span></span>

## <a name="type-description"></a><span data-ttu-id="86f6b-116">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="86f6b-116">Type Description</span></span>



| <span data-ttu-id="86f6b-117">Name</span><span class="sxs-lookup"><span data-stu-id="86f6b-117">Name</span></span>  | [<span data-ttu-id="86f6b-118">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="86f6b-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="86f6b-119">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="86f6b-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="86f6b-120">Size</span><span class="sxs-lookup"><span data-stu-id="86f6b-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="86f6b-121">*x*</span><span class="sxs-lookup"><span data-stu-id="86f6b-121">*x*</span></span>   | <span data-ttu-id="86f6b-122">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="86f6b-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="86f6b-123">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="86f6b-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="86f6b-124">any</span><span class="sxs-lookup"><span data-stu-id="86f6b-124">any</span></span>                            |
| <span data-ttu-id="86f6b-125">*TZI*</span><span class="sxs-lookup"><span data-stu-id="86f6b-125">*ret*</span></span> | <span data-ttu-id="86f6b-126">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="86f6b-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="86f6b-127">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="86f6b-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="86f6b-128">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="86f6b-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="86f6b-129">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="86f6b-129">Minimum Shader Model</span></span>

<span data-ttu-id="86f6b-130">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="86f6b-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="86f6b-131">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="86f6b-131">Shader Model</span></span>                                                                       | <span data-ttu-id="86f6b-132">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="86f6b-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="86f6b-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="86f6b-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="86f6b-134">ja</span><span class="sxs-lookup"><span data-stu-id="86f6b-134">yes</span></span>                 |
| [<span data-ttu-id="86f6b-135">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="86f6b-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="86f6b-136">Ja ( \_ nur vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="86f6b-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="86f6b-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="86f6b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86f6b-138">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="86f6b-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

