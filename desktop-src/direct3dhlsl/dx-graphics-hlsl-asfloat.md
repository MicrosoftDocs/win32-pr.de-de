---
title: asfloat
description: Interpretiert das Bitmuster von x als Gleit Komma Zahl.
ms.assetid: 48e1e0cb-8578-4e6d-8c46-2b8b201906c1
keywords:
- asfloat HLSL
topic_type:
- apiref
api_name:
- asfloat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a5701d959fb59519318dd7f2e91b6790f4c0b6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993534"
---
# <a name="asfloat"></a><span data-ttu-id="cc8ff-104">asfloat</span><span class="sxs-lookup"><span data-stu-id="cc8ff-104">asfloat</span></span>

<span data-ttu-id="cc8ff-105">Interpretiert das Bitmuster von *x* als Gleit Komma Zahl.</span><span class="sxs-lookup"><span data-stu-id="cc8ff-105">Interprets the bit pattern of *x* as a floating-point number.</span></span>



| <span data-ttu-id="cc8ff-106">Ret asfloat (*x*)</span><span class="sxs-lookup"><span data-stu-id="cc8ff-106">ret asfloat(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="cc8ff-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc8ff-107">Parameters</span></span>



| <span data-ttu-id="cc8ff-108">Element</span><span class="sxs-lookup"><span data-stu-id="cc8ff-108">Item</span></span>                                                   | <span data-ttu-id="cc8ff-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc8ff-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="cc8ff-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="cc8ff-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="cc8ff-111">\[im \] Eingabe Wert.</span><span class="sxs-lookup"><span data-stu-id="cc8ff-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="cc8ff-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cc8ff-112">Return Value</span></span>

<span data-ttu-id="cc8ff-113">Die als Gleit Komma Zahl interpretierte Eingabe.</span><span class="sxs-lookup"><span data-stu-id="cc8ff-113">The input interpreted as a floating-point number.</span></span>

## <a name="type-description"></a><span data-ttu-id="cc8ff-114">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="cc8ff-114">Type Description</span></span>



| <span data-ttu-id="cc8ff-115">Name</span><span class="sxs-lookup"><span data-stu-id="cc8ff-115">Name</span></span>  | [<span data-ttu-id="cc8ff-116">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="cc8ff-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="cc8ff-117">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="cc8ff-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="cc8ff-118">Size</span><span class="sxs-lookup"><span data-stu-id="cc8ff-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="cc8ff-119">*x*</span><span class="sxs-lookup"><span data-stu-id="cc8ff-119">*x*</span></span>   | <span data-ttu-id="cc8ff-120">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="cc8ff-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="cc8ff-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="cc8ff-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="cc8ff-122">any</span><span class="sxs-lookup"><span data-stu-id="cc8ff-122">any</span></span>                            |
| <span data-ttu-id="cc8ff-123">*TZI*</span><span class="sxs-lookup"><span data-stu-id="cc8ff-123">*ret*</span></span> | <span data-ttu-id="cc8ff-124">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="cc8ff-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="cc8ff-125">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="cc8ff-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                                                                                | <span data-ttu-id="cc8ff-126">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="cc8ff-126">same dimension(s) as input *x*</span></span> |



 

## <a name="function-overloads"></a><span data-ttu-id="cc8ff-127">Funktions Überladungen</span><span class="sxs-lookup"><span data-stu-id="cc8ff-127">Function Overloads</span></span>

<dl> <span data-ttu-id="cc8ff-128">' float <x> asfloat (float- <x> Wert); `  
` float <x> asfloat (int- <x> Wert); `  
` float <x> asfloat (uint- <x> Wert); '</span><span class="sxs-lookup"><span data-stu-id="cc8ff-128">`float<x> asfloat(float<x> value);`  
`float<x> asfloat(int<x> value);`  
`float<x> asfloat(uint<x> value);`</span></span>
</dl>

## <a name="minimum-shader-model"></a><span data-ttu-id="cc8ff-129">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="cc8ff-129">Minimum Shader Model</span></span>

<span data-ttu-id="cc8ff-130">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cc8ff-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="cc8ff-131">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="cc8ff-131">Shader Model</span></span>                                                        | <span data-ttu-id="cc8ff-132">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="cc8ff-132">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="cc8ff-133">[Shader Model 4](dx-graphics-hlsl-sm4.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="cc8ff-133">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="cc8ff-134">ja</span><span class="sxs-lookup"><span data-stu-id="cc8ff-134">yes</span></span>       |
| [<span data-ttu-id="cc8ff-135">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cc8ff-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="cc8ff-136">nein</span><span class="sxs-lookup"><span data-stu-id="cc8ff-136">no</span></span>        |
| [<span data-ttu-id="cc8ff-137">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cc8ff-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="cc8ff-138">nein</span><span class="sxs-lookup"><span data-stu-id="cc8ff-138">no</span></span>        |
| [<span data-ttu-id="cc8ff-139">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cc8ff-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="cc8ff-140">nein</span><span class="sxs-lookup"><span data-stu-id="cc8ff-140">no</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="cc8ff-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc8ff-141">Remarks</span></span>

<span data-ttu-id="cc8ff-142">Ältere Compiler sind falsch zulässig `asfloat(bool)` , aber beachten Sie, dass keine booleschen Eingaben unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="cc8ff-142">Older compilers incorrectly allowed `asfloat(bool)`, but note that bool inputs are not supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="cc8ff-143">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cc8ff-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc8ff-144">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="cc8ff-144">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

