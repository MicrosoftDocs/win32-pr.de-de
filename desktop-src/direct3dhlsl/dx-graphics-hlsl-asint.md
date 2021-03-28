---
title: asint
description: Interpretiert das Bitmuster von x als ganze Zahl.
ms.assetid: e17e0a11-ef52-4b23-94b8-5db0b18aff4d
keywords:
- asint HLSL
topic_type:
- apiref
api_name:
- asint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce1b0ca7e1c7b3716be1a3029c5478f96e261ce5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039380"
---
# <a name="asint"></a><span data-ttu-id="a1833-104">asint</span><span class="sxs-lookup"><span data-stu-id="a1833-104">asint</span></span>

<span data-ttu-id="a1833-105">Interpretiert das Bitmuster von *x* als ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="a1833-105">Interprets the bit pattern of *x* as an integer.</span></span>



| <span data-ttu-id="a1833-106">Ret asint (*x*)</span><span class="sxs-lookup"><span data-stu-id="a1833-106">ret asint(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="a1833-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1833-107">Parameters</span></span>



| <span data-ttu-id="a1833-108">Element</span><span class="sxs-lookup"><span data-stu-id="a1833-108">Item</span></span>                                                   | <span data-ttu-id="a1833-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a1833-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="a1833-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="a1833-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="a1833-111">\[im \] Eingabe Wert.</span><span class="sxs-lookup"><span data-stu-id="a1833-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="a1833-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1833-112">Return Value</span></span>

<span data-ttu-id="a1833-113">Die als ganze Zahl interpretierte Eingabe.</span><span class="sxs-lookup"><span data-stu-id="a1833-113">The input interpreted as an integer.</span></span>

## <a name="type-description"></a><span data-ttu-id="a1833-114">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="a1833-114">Type Description</span></span>



| <span data-ttu-id="a1833-115">Name</span><span class="sxs-lookup"><span data-stu-id="a1833-115">Name</span></span>  | [<span data-ttu-id="a1833-116">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="a1833-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="a1833-117">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="a1833-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                  | <span data-ttu-id="a1833-118">Size</span><span class="sxs-lookup"><span data-stu-id="a1833-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="a1833-119">*x*</span><span class="sxs-lookup"><span data-stu-id="a1833-119">*x*</span></span>   | <span data-ttu-id="a1833-120">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="a1833-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="a1833-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **uint**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="a1833-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="a1833-122">any</span><span class="sxs-lookup"><span data-stu-id="a1833-122">any</span></span>                            |
| <span data-ttu-id="a1833-123">*TZI*</span><span class="sxs-lookup"><span data-stu-id="a1833-123">*ret*</span></span> | <span data-ttu-id="a1833-124">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="a1833-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="a1833-125">**INT**</span><span class="sxs-lookup"><span data-stu-id="a1833-125">**int**</span></span>](/windows/desktop/WinProg/windows-data-types)                                           | <span data-ttu-id="a1833-126">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="a1833-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a1833-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="a1833-127">Minimum Shader Model</span></span>

<span data-ttu-id="a1833-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a1833-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a1833-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="a1833-129">Shader Model</span></span>                                                        | <span data-ttu-id="a1833-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="a1833-130">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="a1833-131">[Shader Model 4](dx-graphics-hlsl-sm4.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="a1833-131">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="a1833-132">ja</span><span class="sxs-lookup"><span data-stu-id="a1833-132">yes</span></span>       |
| [<span data-ttu-id="a1833-133">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a1833-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="a1833-134">nein</span><span class="sxs-lookup"><span data-stu-id="a1833-134">no</span></span>        |
| [<span data-ttu-id="a1833-135">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a1833-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="a1833-136">nein</span><span class="sxs-lookup"><span data-stu-id="a1833-136">no</span></span>        |
| [<span data-ttu-id="a1833-137">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a1833-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="a1833-138">Nein</span><span class="sxs-lookup"><span data-stu-id="a1833-138">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="a1833-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1833-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1833-140">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="a1833-140">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

