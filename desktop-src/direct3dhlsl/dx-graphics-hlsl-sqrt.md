---
title: sqrt
description: Gibt die Quadratwurzel des angegebenen Gleit Komma Werts pro Komponente zurück.
ms.assetid: e8debc60-1441-4974-9ab3-6d1c2217caaf
keywords:
- SQRT HLSL
topic_type:
- apiref
api_name:
- sqrt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff3c872dac6da28a1ec92993e387bd23daec7f86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390348"
---
# <a name="sqrt"></a><span data-ttu-id="38ef2-104">sqrt</span><span class="sxs-lookup"><span data-stu-id="38ef2-104">sqrt</span></span>

<span data-ttu-id="38ef2-105">Gibt die Quadratwurzel des angegebenen Gleit Komma Werts pro Komponente zurück.</span><span class="sxs-lookup"><span data-stu-id="38ef2-105">Returns the square root of the specified floating-point value, per component.</span></span>



| <span data-ttu-id="38ef2-106">*ret* sqrt (*x*)</span><span class="sxs-lookup"><span data-stu-id="38ef2-106">*ret* sqrt(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="38ef2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="38ef2-107">Parameters</span></span>



| <span data-ttu-id="38ef2-108">Element</span><span class="sxs-lookup"><span data-stu-id="38ef2-108">Item</span></span>                                                   | <span data-ttu-id="38ef2-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38ef2-109">Description</span></span>                                           |
|--------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="38ef2-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="38ef2-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="38ef2-111">\[im \] angegebenen Gleit Komma Wert.</span><span class="sxs-lookup"><span data-stu-id="38ef2-111">\[in\] The specified floating-point value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="38ef2-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38ef2-112">Return Value</span></span>

<span data-ttu-id="38ef2-113">Die Quadratwurzel des *x* -Parameters pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="38ef2-113">The square root of the *x* parameter, per component.</span></span>

## <a name="type-description"></a><span data-ttu-id="38ef2-114">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="38ef2-114">Type Description</span></span>



| <span data-ttu-id="38ef2-115">Name</span><span class="sxs-lookup"><span data-stu-id="38ef2-115">Name</span></span>  | [<span data-ttu-id="38ef2-116">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="38ef2-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="38ef2-117">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="38ef2-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="38ef2-118">Size</span><span class="sxs-lookup"><span data-stu-id="38ef2-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="38ef2-119">*x*</span><span class="sxs-lookup"><span data-stu-id="38ef2-119">*x*</span></span>   | <span data-ttu-id="38ef2-120">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="38ef2-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="38ef2-121">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="38ef2-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="38ef2-122">any</span><span class="sxs-lookup"><span data-stu-id="38ef2-122">any</span></span>                            |
| <span data-ttu-id="38ef2-123">*TZI*</span><span class="sxs-lookup"><span data-stu-id="38ef2-123">*ret*</span></span> | <span data-ttu-id="38ef2-124">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="38ef2-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="38ef2-125">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="38ef2-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="38ef2-126">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="38ef2-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="38ef2-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="38ef2-127">Minimum Shader Model</span></span>

<span data-ttu-id="38ef2-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="38ef2-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="38ef2-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="38ef2-129">Shader Model</span></span>                                                                       | <span data-ttu-id="38ef2-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="38ef2-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="38ef2-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="38ef2-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="38ef2-132">ja</span><span class="sxs-lookup"><span data-stu-id="38ef2-132">yes</span></span>                 |
| [<span data-ttu-id="38ef2-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="38ef2-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="38ef2-134">Ja ( \_ nur vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="38ef2-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="38ef2-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="38ef2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38ef2-136">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="38ef2-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

