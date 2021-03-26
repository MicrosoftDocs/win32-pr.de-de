---
title: acos
description: Gibt den Arkus Kosinus des angegebenen-Werts zurück.
ms.assetid: c9bc33b8-d586-4c64-9453-5ab97396f2cf
keywords:
- ACOS HLSL
topic_type:
- apiref
api_name:
- acos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2cd909c4a4c1300374bba723f1edabb48d51b2e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102250"
---
# <a name="acos"></a><span data-ttu-id="27887-104">acos</span><span class="sxs-lookup"><span data-stu-id="27887-104">acos</span></span>

<span data-ttu-id="27887-105">Gibt den Arkus Kosinus des angegebenen-Werts zurück.</span><span class="sxs-lookup"><span data-stu-id="27887-105">Returns the arccosine of the specified value.</span></span>



| <span data-ttu-id="27887-106">*ret* -acos (*x*)</span><span class="sxs-lookup"><span data-stu-id="27887-106">*ret* acos(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="27887-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="27887-107">Parameters</span></span>



| <span data-ttu-id="27887-108">Element</span><span class="sxs-lookup"><span data-stu-id="27887-108">Item</span></span>                                                   | <span data-ttu-id="27887-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27887-109">Description</span></span>                                                                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27887-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="27887-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="27887-111">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="27887-111">\[in\] The specified value.</span></span> <span data-ttu-id="27887-112">Jede Komponente muss ein Gleit Komma Wert im Bereich von-1 bis 1 sein.</span><span class="sxs-lookup"><span data-stu-id="27887-112">Each component should be a floating-point value within the range of -1 to 1.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="27887-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27887-113">Return Value</span></span>

<span data-ttu-id="27887-114">Der Arkus Kosinus des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="27887-114">The arccosine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="27887-115">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="27887-115">Type Description</span></span>



| <span data-ttu-id="27887-116">Name</span><span class="sxs-lookup"><span data-stu-id="27887-116">Name</span></span>  | [<span data-ttu-id="27887-117">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="27887-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="27887-118">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="27887-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="27887-119">Size</span><span class="sxs-lookup"><span data-stu-id="27887-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="27887-120">*x*</span><span class="sxs-lookup"><span data-stu-id="27887-120">*x*</span></span>   | <span data-ttu-id="27887-121">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="27887-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="27887-122">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="27887-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="27887-123">any</span><span class="sxs-lookup"><span data-stu-id="27887-123">any</span></span>                            |
| <span data-ttu-id="27887-124">*TZI*</span><span class="sxs-lookup"><span data-stu-id="27887-124">*ret*</span></span> | <span data-ttu-id="27887-125">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="27887-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="27887-126">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="27887-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="27887-127">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="27887-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="27887-128">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="27887-128">Minimum Shader Model</span></span>

<span data-ttu-id="27887-129">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="27887-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="27887-130">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="27887-130">Shader Model</span></span>                                                                       | <span data-ttu-id="27887-131">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="27887-131">Supported</span></span>     |
|------------------------------------------------------------------------------------|---------------|
| <span data-ttu-id="27887-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="27887-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="27887-133">ja</span><span class="sxs-lookup"><span data-stu-id="27887-133">yes</span></span>           |
| [<span data-ttu-id="27887-134">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="27887-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="27887-135">\_nur vs 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="27887-135">vs\_1\_1 only</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="27887-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="27887-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27887-137">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="27887-137">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

