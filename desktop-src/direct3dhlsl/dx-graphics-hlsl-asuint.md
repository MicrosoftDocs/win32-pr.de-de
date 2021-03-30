---
title: asuint
description: Interpretiert das Bitmuster von x als ganze Zahl ohne Vorzeichen.
ms.assetid: 8401001d-f9ee-43da-9756-f311e9f2bb20
keywords:
- asuint HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a2d351eb36c6910790e2dceb94e3a97951ad850
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976800"
---
# <a name="asuint"></a><span data-ttu-id="3e3ae-104">asuint</span><span class="sxs-lookup"><span data-stu-id="3e3ae-104">asuint</span></span>

<span data-ttu-id="3e3ae-105">Interpretiert das Bitmuster von *x* als ganze Zahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="3e3ae-105">Interprets the bit pattern of *x* as an unsigned integer.</span></span>



| <span data-ttu-id="3e3ae-106">Ret-Taste (*x*)</span><span class="sxs-lookup"><span data-stu-id="3e3ae-106">ret asuint(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="3e3ae-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e3ae-107">Parameters</span></span>



| <span data-ttu-id="3e3ae-108">Element</span><span class="sxs-lookup"><span data-stu-id="3e3ae-108">Item</span></span>                                                   | <span data-ttu-id="3e3ae-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e3ae-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="3e3ae-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="3e3ae-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="3e3ae-111">\[im \] Eingabe Wert.</span><span class="sxs-lookup"><span data-stu-id="3e3ae-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="3e3ae-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e3ae-112">Return Value</span></span>

<span data-ttu-id="3e3ae-113">Die Eingabe, die als ganze Zahl ohne Vorzeichen interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="3e3ae-113">The input interpreted as an unsigned integer.</span></span>

## <a name="type-description"></a><span data-ttu-id="3e3ae-114">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="3e3ae-114">Type Description</span></span>



| <span data-ttu-id="3e3ae-115">Name</span><span class="sxs-lookup"><span data-stu-id="3e3ae-115">Name</span></span>  | [<span data-ttu-id="3e3ae-116">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="3e3ae-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="3e3ae-117">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="3e3ae-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="3e3ae-118">Size</span><span class="sxs-lookup"><span data-stu-id="3e3ae-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="3e3ae-119">*x*</span><span class="sxs-lookup"><span data-stu-id="3e3ae-119">*x*</span></span>   | <span data-ttu-id="3e3ae-120">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="3e3ae-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="3e3ae-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="3e3ae-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="3e3ae-122">any</span><span class="sxs-lookup"><span data-stu-id="3e3ae-122">any</span></span>                            |
| <span data-ttu-id="3e3ae-123">*TZI*</span><span class="sxs-lookup"><span data-stu-id="3e3ae-123">*ret*</span></span> | <span data-ttu-id="3e3ae-124">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="3e3ae-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="3e3ae-125">**uint**</span><span class="sxs-lookup"><span data-stu-id="3e3ae-125">**uint**</span></span>](/windows/desktop/WinProg/windows-data-types)                                         | <span data-ttu-id="3e3ae-126">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="3e3ae-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3e3ae-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="3e3ae-127">Minimum Shader Model</span></span>

<span data-ttu-id="3e3ae-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3e3ae-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3e3ae-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="3e3ae-129">Shader Model</span></span>                                                        | <span data-ttu-id="3e3ae-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="3e3ae-130">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="3e3ae-131">[Shader Model 4](dx-graphics-hlsl-sm4.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="3e3ae-131">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="3e3ae-132">ja</span><span class="sxs-lookup"><span data-stu-id="3e3ae-132">yes</span></span>       |
| [<span data-ttu-id="3e3ae-133">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3e3ae-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="3e3ae-134">nein</span><span class="sxs-lookup"><span data-stu-id="3e3ae-134">no</span></span>        |
| [<span data-ttu-id="3e3ae-135">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3e3ae-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="3e3ae-136">nein</span><span class="sxs-lookup"><span data-stu-id="3e3ae-136">no</span></span>        |
| [<span data-ttu-id="3e3ae-137">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3e3ae-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="3e3ae-138">Nein</span><span class="sxs-lookup"><span data-stu-id="3e3ae-138">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="3e3ae-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e3ae-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e3ae-140">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="3e3ae-140">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

