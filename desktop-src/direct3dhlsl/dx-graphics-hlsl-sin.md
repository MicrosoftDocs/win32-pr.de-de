---
title: sin
description: Gibt den Sinus des angegebenen-Werts zurück.
ms.assetid: e1c3ead8-73dd-4798-8553-1a42dbaefe8e
keywords:
- Sin HLSL
topic_type:
- apiref
api_name:
- sin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d48332d35052a893dcb348a70e4d464a6bbfe0c9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390861"
---
# <a name="sin"></a><span data-ttu-id="02105-104">sin</span><span class="sxs-lookup"><span data-stu-id="02105-104">sin</span></span>

<span data-ttu-id="02105-105">Gibt den Sinus des angegebenen-Werts zurück.</span><span class="sxs-lookup"><span data-stu-id="02105-105">Returns the sine of the specified value.</span></span>



| <span data-ttu-id="02105-106">*ret* Sin (*x*)</span><span class="sxs-lookup"><span data-stu-id="02105-106">*ret* sin(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="02105-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="02105-107">Parameters</span></span>



| <span data-ttu-id="02105-108">Element</span><span class="sxs-lookup"><span data-stu-id="02105-108">Item</span></span>                                                   | <span data-ttu-id="02105-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02105-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="02105-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="02105-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="02105-111">\[im \] angegebenen Wert im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="02105-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="02105-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02105-112">Return Value</span></span>

<span data-ttu-id="02105-113">Der Sinus des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="02105-113">The sine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="02105-114">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="02105-114">Type Description</span></span>



| <span data-ttu-id="02105-115">Name</span><span class="sxs-lookup"><span data-stu-id="02105-115">Name</span></span>  | [<span data-ttu-id="02105-116">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="02105-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="02105-117">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="02105-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="02105-118">Size</span><span class="sxs-lookup"><span data-stu-id="02105-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="02105-119">*x*</span><span class="sxs-lookup"><span data-stu-id="02105-119">*x*</span></span>   | <span data-ttu-id="02105-120">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="02105-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="02105-121">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="02105-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="02105-122">any</span><span class="sxs-lookup"><span data-stu-id="02105-122">any</span></span>                            |
| <span data-ttu-id="02105-123">*TZI*</span><span class="sxs-lookup"><span data-stu-id="02105-123">*ret*</span></span> | <span data-ttu-id="02105-124">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="02105-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="02105-125">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="02105-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="02105-126">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="02105-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="02105-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="02105-127">Minimum Shader Model</span></span>

<span data-ttu-id="02105-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="02105-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="02105-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="02105-129">Shader Model</span></span>                                                                       | <span data-ttu-id="02105-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="02105-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="02105-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="02105-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="02105-132">ja</span><span class="sxs-lookup"><span data-stu-id="02105-132">yes</span></span>                 |
| [<span data-ttu-id="02105-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="02105-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="02105-134">Ja ( \_ nur vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="02105-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="02105-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="02105-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02105-136">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="02105-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

