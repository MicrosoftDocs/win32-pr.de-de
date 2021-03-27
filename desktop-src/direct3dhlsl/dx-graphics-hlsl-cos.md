---
title: cos
description: Gibt den Kosinus des angegebenen-Werts zurück.
ms.assetid: 96c15702-98be-45bc-9abc-60ccc3c217b6
keywords:
- COS HLSL
topic_type:
- apiref
api_name:
- cos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f5c0f4f071d47102c673301a397bfe3ecf178e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390962"
---
# <a name="cos"></a><span data-ttu-id="5f6da-104">cos</span><span class="sxs-lookup"><span data-stu-id="5f6da-104">cos</span></span>

<span data-ttu-id="5f6da-105">Gibt den Kosinus des angegebenen-Werts zurück.</span><span class="sxs-lookup"><span data-stu-id="5f6da-105">Returns the cosine of the specified value.</span></span>



| <span data-ttu-id="5f6da-106">*ret* cos (*x*)</span><span class="sxs-lookup"><span data-stu-id="5f6da-106">*ret* cos(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="5f6da-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f6da-107">Parameters</span></span>



| <span data-ttu-id="5f6da-108">Element</span><span class="sxs-lookup"><span data-stu-id="5f6da-108">Item</span></span>                                                   | <span data-ttu-id="5f6da-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f6da-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="5f6da-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="5f6da-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="5f6da-111">\[im \] angegebenen Wert im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="5f6da-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="5f6da-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f6da-112">Return Value</span></span>

<span data-ttu-id="5f6da-113">Der Kosinus des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="5f6da-113">The cosine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="5f6da-114">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="5f6da-114">Type Description</span></span>



| <span data-ttu-id="5f6da-115">Name</span><span class="sxs-lookup"><span data-stu-id="5f6da-115">Name</span></span>  | [<span data-ttu-id="5f6da-116">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="5f6da-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="5f6da-117">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="5f6da-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="5f6da-118">Size</span><span class="sxs-lookup"><span data-stu-id="5f6da-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="5f6da-119">*x*</span><span class="sxs-lookup"><span data-stu-id="5f6da-119">*x*</span></span>   | <span data-ttu-id="5f6da-120">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="5f6da-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="5f6da-121">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="5f6da-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5f6da-122">any</span><span class="sxs-lookup"><span data-stu-id="5f6da-122">any</span></span>                            |
| <span data-ttu-id="5f6da-123">*TZI*</span><span class="sxs-lookup"><span data-stu-id="5f6da-123">*ret*</span></span> | <span data-ttu-id="5f6da-124">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="5f6da-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="5f6da-125">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="5f6da-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5f6da-126">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="5f6da-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5f6da-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="5f6da-127">Minimum Shader Model</span></span>

<span data-ttu-id="5f6da-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5f6da-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5f6da-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="5f6da-129">Shader Model</span></span>                                                                       | <span data-ttu-id="5f6da-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="5f6da-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="5f6da-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="5f6da-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="5f6da-132">ja</span><span class="sxs-lookup"><span data-stu-id="5f6da-132">yes</span></span>       |
| [<span data-ttu-id="5f6da-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5f6da-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="5f6da-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="5f6da-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="5f6da-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5f6da-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f6da-136">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="5f6da-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

