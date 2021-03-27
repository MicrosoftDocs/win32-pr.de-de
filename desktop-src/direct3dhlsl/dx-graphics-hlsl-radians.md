---
title: Bogenmaß
description: Konvertiert den angegebenen Wert von Grad in Bogenmaß.
ms.assetid: 6fc6b1f8-b686-49ba-93ea-2b2470b3fc72
keywords:
- HLSL HLSL
topic_type:
- apiref
api_name:
- radians
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 029c0ffe2838cdcc997e47cae4e0adafede4411d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390959"
---
# <a name="radians"></a><span data-ttu-id="1c065-104">Bogenmaß</span><span class="sxs-lookup"><span data-stu-id="1c065-104">radians</span></span>

<span data-ttu-id="1c065-105">Konvertiert den angegebenen Wert von Grad in Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="1c065-105">Converts the specified value from degrees to radians.</span></span>



| <span data-ttu-id="1c065-106">*ret* -Bogenmaße (*x*)</span><span class="sxs-lookup"><span data-stu-id="1c065-106">*ret* radians(*x*)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="1c065-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c065-107">Parameters</span></span>



| <span data-ttu-id="1c065-108">Element</span><span class="sxs-lookup"><span data-stu-id="1c065-108">Item</span></span>                                                   | <span data-ttu-id="1c065-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1c065-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="1c065-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="1c065-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="1c065-111">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="1c065-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="1c065-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c065-112">Return Value</span></span>

<span data-ttu-id="1c065-113">Der *x* -Parameter, der von Grad in Bogenmaß konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1c065-113">The *x* parameter converted from degrees to radians.</span></span>

## <a name="type-description"></a><span data-ttu-id="1c065-114">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="1c065-114">Type Description</span></span>



| <span data-ttu-id="1c065-115">Name</span><span class="sxs-lookup"><span data-stu-id="1c065-115">Name</span></span>  | [<span data-ttu-id="1c065-116">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="1c065-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="1c065-117">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="1c065-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="1c065-118">Size</span><span class="sxs-lookup"><span data-stu-id="1c065-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="1c065-119">*x*</span><span class="sxs-lookup"><span data-stu-id="1c065-119">*x*</span></span>   | <span data-ttu-id="1c065-120">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="1c065-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="1c065-121">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="1c065-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1c065-122">any</span><span class="sxs-lookup"><span data-stu-id="1c065-122">any</span></span>                            |
| <span data-ttu-id="1c065-123">*TZI*</span><span class="sxs-lookup"><span data-stu-id="1c065-123">*ret*</span></span> | <span data-ttu-id="1c065-124">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="1c065-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="1c065-125">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="1c065-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1c065-126">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="1c065-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1c065-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="1c065-127">Minimum Shader Model</span></span>

<span data-ttu-id="1c065-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1c065-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1c065-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="1c065-129">Shader Model</span></span>                                                                       | <span data-ttu-id="1c065-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="1c065-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="1c065-131">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="1c065-131">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="1c065-132">ja</span><span class="sxs-lookup"><span data-stu-id="1c065-132">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1c065-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1c065-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c065-134">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="1c065-134">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

