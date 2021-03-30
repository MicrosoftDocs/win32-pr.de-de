---
title: abs
description: Gibt den absoluten Wert des angegebenen-Werts zurück.
ms.assetid: 8c4cfd8f-8aac-4db3-8247-ce2bbf501e80
keywords:
- ABS HLSL
topic_type:
- apiref
api_name:
- abs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1acd1903e1a65a38f5af7549ab52577bc6cba51c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976793"
---
# <a name="abs"></a><span data-ttu-id="79e8b-104">abs</span><span class="sxs-lookup"><span data-stu-id="79e8b-104">abs</span></span>

<span data-ttu-id="79e8b-105">Gibt den absoluten Wert des angegebenen-Werts zurück.</span><span class="sxs-lookup"><span data-stu-id="79e8b-105">Returns the absolute value of the specified value.</span></span>



| <span data-ttu-id="79e8b-106">Ret Abs (*x*)</span><span class="sxs-lookup"><span data-stu-id="79e8b-106">ret abs(*x*)</span></span> |
|--------------|



 

## <a name="parameters"></a><span data-ttu-id="79e8b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="79e8b-107">Parameters</span></span>



| <span data-ttu-id="79e8b-108">Element</span><span class="sxs-lookup"><span data-stu-id="79e8b-108">Item</span></span>                                                   | <span data-ttu-id="79e8b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79e8b-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="79e8b-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="79e8b-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="79e8b-111">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="79e8b-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="79e8b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79e8b-112">Return Value</span></span>

<span data-ttu-id="79e8b-113">Der absolute Wert des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="79e8b-113">The absolute value of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="79e8b-114">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="79e8b-114">Type Description</span></span>



| <span data-ttu-id="79e8b-115">Name</span><span class="sxs-lookup"><span data-stu-id="79e8b-115">Name</span></span>  | [<span data-ttu-id="79e8b-116">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="79e8b-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="79e8b-117">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="79e8b-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="79e8b-118">Size</span><span class="sxs-lookup"><span data-stu-id="79e8b-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="79e8b-119">*x*</span><span class="sxs-lookup"><span data-stu-id="79e8b-119">*x*</span></span>   | <span data-ttu-id="79e8b-120">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="79e8b-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="79e8b-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="79e8b-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="79e8b-122">any</span><span class="sxs-lookup"><span data-stu-id="79e8b-122">any</span></span>                            |
| <span data-ttu-id="79e8b-123">*TZI*</span><span class="sxs-lookup"><span data-stu-id="79e8b-123">*ret*</span></span> | <span data-ttu-id="79e8b-124">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="79e8b-124">same as input *x*</span></span>                                                                                              | <span data-ttu-id="79e8b-125">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="79e8b-125">same as input *x*</span></span>                                                              | <span data-ttu-id="79e8b-126">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="79e8b-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="79e8b-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="79e8b-127">Minimum Shader Model</span></span>

<span data-ttu-id="79e8b-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="79e8b-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="79e8b-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="79e8b-129">Shader Model</span></span>                                                                       | <span data-ttu-id="79e8b-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="79e8b-130">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="79e8b-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="79e8b-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="79e8b-132">ja</span><span class="sxs-lookup"><span data-stu-id="79e8b-132">yes</span></span>                   |
| [<span data-ttu-id="79e8b-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="79e8b-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="79e8b-134">vs \_ 1 \_ 1 und PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="79e8b-134">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="79e8b-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="79e8b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79e8b-136">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="79e8b-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

