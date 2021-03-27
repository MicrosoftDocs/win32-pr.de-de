---
title: atan
description: Gibt den Arkus Tangens des angegebenen-Werts zurück.
ms.assetid: e3ce3ac3-1012-414f-a193-102208083e39
keywords:
- Atan HLSL
topic_type:
- apiref
api_name:
- atan
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 290ced1e5100e3bbc780fab6ab984deaca38528f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727865"
---
# <a name="atan"></a><span data-ttu-id="3f1b9-104">atan</span><span class="sxs-lookup"><span data-stu-id="3f1b9-104">atan</span></span>

<span data-ttu-id="3f1b9-105">Gibt den Arkus Tangens des angegebenen-Werts zurück.</span><span class="sxs-lookup"><span data-stu-id="3f1b9-105">Returns the arctangent of the specified value.</span></span>



| <span data-ttu-id="3f1b9-106">*ret* Atan (*x*)</span><span class="sxs-lookup"><span data-stu-id="3f1b9-106">*ret* atan(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="3f1b9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f1b9-107">Parameters</span></span>



| <span data-ttu-id="3f1b9-108">Element</span><span class="sxs-lookup"><span data-stu-id="3f1b9-108">Item</span></span>                                                   | <span data-ttu-id="3f1b9-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f1b9-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="3f1b9-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="3f1b9-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="3f1b9-111">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="3f1b9-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="3f1b9-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f1b9-112">Return Value</span></span>

<span data-ttu-id="3f1b9-113">Der Arkus Tangens des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="3f1b9-113">The arctangent of the *x* parameter.</span></span> <span data-ttu-id="3f1b9-114">Dieser Wert liegt im Bereich von--/2 bis 1 bis 2.</span><span class="sxs-lookup"><span data-stu-id="3f1b9-114">This value is within the range of -π/2 to π/2.</span></span>

## <a name="type-description"></a><span data-ttu-id="3f1b9-115">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="3f1b9-115">Type Description</span></span>



| <span data-ttu-id="3f1b9-116">Name</span><span class="sxs-lookup"><span data-stu-id="3f1b9-116">Name</span></span>  | [<span data-ttu-id="3f1b9-117">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="3f1b9-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="3f1b9-118">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="3f1b9-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="3f1b9-119">Size</span><span class="sxs-lookup"><span data-stu-id="3f1b9-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="3f1b9-120">*x*</span><span class="sxs-lookup"><span data-stu-id="3f1b9-120">*x*</span></span>   | <span data-ttu-id="3f1b9-121">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="3f1b9-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="3f1b9-122">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="3f1b9-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3f1b9-123">any</span><span class="sxs-lookup"><span data-stu-id="3f1b9-123">any</span></span>                            |
| <span data-ttu-id="3f1b9-124">*TZI*</span><span class="sxs-lookup"><span data-stu-id="3f1b9-124">*ret*</span></span> | <span data-ttu-id="3f1b9-125">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="3f1b9-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="3f1b9-126">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="3f1b9-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3f1b9-127">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="3f1b9-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3f1b9-128">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="3f1b9-128">Minimum Shader Model</span></span>

<span data-ttu-id="3f1b9-129">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3f1b9-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3f1b9-130">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="3f1b9-130">Shader Model</span></span>                                                                       | <span data-ttu-id="3f1b9-131">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="3f1b9-131">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="3f1b9-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="3f1b9-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="3f1b9-133">ja</span><span class="sxs-lookup"><span data-stu-id="3f1b9-133">yes</span></span>       |
| [<span data-ttu-id="3f1b9-134">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3f1b9-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="3f1b9-135">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3f1b9-135">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="3f1b9-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3f1b9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f1b9-137">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="3f1b9-137">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

