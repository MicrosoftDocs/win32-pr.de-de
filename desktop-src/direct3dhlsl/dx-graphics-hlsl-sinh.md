---
title: sinh
description: Gibt den hyperbolischen Sinus des angegebenen-Werts zurück.
ms.assetid: 8a9e11a3-582f-4680-a5bd-ecde90560db3
keywords:
- sinh HLSL
topic_type:
- apiref
api_name:
- sinh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cbf6c5e04eb248c81782ba236010298ebb9564db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039465"
---
# <a name="sinh"></a><span data-ttu-id="da8bd-104">sinh</span><span class="sxs-lookup"><span data-stu-id="da8bd-104">sinh</span></span>

<span data-ttu-id="da8bd-105">Gibt den hyperbolischen Sinus des angegebenen-Werts zurück.</span><span class="sxs-lookup"><span data-stu-id="da8bd-105">Returns the hyperbolic sine of the specified value.</span></span>



| <span data-ttu-id="da8bd-106">*ret* sinh (*x*)</span><span class="sxs-lookup"><span data-stu-id="da8bd-106">*ret* sinh(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="da8bd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="da8bd-107">Parameters</span></span>



| <span data-ttu-id="da8bd-108">Element</span><span class="sxs-lookup"><span data-stu-id="da8bd-108">Item</span></span>                                                   | <span data-ttu-id="da8bd-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da8bd-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="da8bd-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="da8bd-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="da8bd-111">\[im \] angegebenen Wert im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="da8bd-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="da8bd-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da8bd-112">Return Value</span></span>

<span data-ttu-id="da8bd-113">Der hyperbolische Sinus des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="da8bd-113">The hyperbolic sine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="da8bd-114">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="da8bd-114">Type Description</span></span>



| <span data-ttu-id="da8bd-115">Name</span><span class="sxs-lookup"><span data-stu-id="da8bd-115">Name</span></span>  | [<span data-ttu-id="da8bd-116">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="da8bd-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="da8bd-117">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="da8bd-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="da8bd-118">Size</span><span class="sxs-lookup"><span data-stu-id="da8bd-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="da8bd-119">*x*</span><span class="sxs-lookup"><span data-stu-id="da8bd-119">*x*</span></span>   | <span data-ttu-id="da8bd-120">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="da8bd-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="da8bd-121">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="da8bd-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="da8bd-122">any</span><span class="sxs-lookup"><span data-stu-id="da8bd-122">any</span></span>                            |
| <span data-ttu-id="da8bd-123">*TZI*</span><span class="sxs-lookup"><span data-stu-id="da8bd-123">*ret*</span></span> | <span data-ttu-id="da8bd-124">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="da8bd-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="da8bd-125">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="da8bd-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="da8bd-126">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="da8bd-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="da8bd-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="da8bd-127">Minimum Shader Model</span></span>

<span data-ttu-id="da8bd-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="da8bd-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="da8bd-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="da8bd-129">Shader Model</span></span>                                                                       | <span data-ttu-id="da8bd-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="da8bd-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="da8bd-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="da8bd-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="da8bd-132">ja</span><span class="sxs-lookup"><span data-stu-id="da8bd-132">yes</span></span>                 |
| [<span data-ttu-id="da8bd-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="da8bd-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="da8bd-134">Ja ( \_ nur vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="da8bd-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="da8bd-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="da8bd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da8bd-136">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="da8bd-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

