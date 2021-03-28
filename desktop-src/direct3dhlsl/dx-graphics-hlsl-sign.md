---
title: Signieren
description: Gibt das Vorzeichen von x zurück.
ms.assetid: 3e2e04e8-0ffc-4721-a5d8-1ccfa6ca2a1a
keywords:
- HLSL Signieren
topic_type:
- apiref
api_name:
- sign
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc177e72e116394ffd6241e0616b84c9066a68a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993566"
---
# <a name="sign"></a><span data-ttu-id="08a0a-104">Signieren</span><span class="sxs-lookup"><span data-stu-id="08a0a-104">sign</span></span>

<span data-ttu-id="08a0a-105">Gibt das Vorzeichen von *x* zurück.</span><span class="sxs-lookup"><span data-stu-id="08a0a-105">Returns the sign of *x*.</span></span>



| <span data-ttu-id="08a0a-106">*ret* -Zeichen (*x*)</span><span class="sxs-lookup"><span data-stu-id="08a0a-106">*ret* sign(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="08a0a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="08a0a-107">Parameters</span></span>



| <span data-ttu-id="08a0a-108">Element</span><span class="sxs-lookup"><span data-stu-id="08a0a-108">Item</span></span>                                                   | <span data-ttu-id="08a0a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08a0a-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="08a0a-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="08a0a-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="08a0a-111">\[im \] Eingabe Wert.</span><span class="sxs-lookup"><span data-stu-id="08a0a-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="08a0a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08a0a-112">Return Value</span></span>

<span data-ttu-id="08a0a-113">Gibt-1 zurück, wenn *x* kleiner als 0 (null) ist. 0, wenn *x* gleich NULL ist. und 1, wenn *x* größer als 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="08a0a-113">Returns -1 if *x* is less than zero; 0 if *x* equals zero; and 1 if *x* is greater than zero.</span></span>

## <a name="type-description"></a><span data-ttu-id="08a0a-114">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="08a0a-114">Type Description</span></span>



| <span data-ttu-id="08a0a-115">Name</span><span class="sxs-lookup"><span data-stu-id="08a0a-115">Name</span></span>  | [<span data-ttu-id="08a0a-116">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="08a0a-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="08a0a-117">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="08a0a-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="08a0a-118">Size</span><span class="sxs-lookup"><span data-stu-id="08a0a-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="08a0a-119">*x*</span><span class="sxs-lookup"><span data-stu-id="08a0a-119">*x*</span></span>   | <span data-ttu-id="08a0a-120">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="08a0a-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="08a0a-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="08a0a-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="08a0a-122">any</span><span class="sxs-lookup"><span data-stu-id="08a0a-122">any</span></span>                            |
| <span data-ttu-id="08a0a-123">*TZI*</span><span class="sxs-lookup"><span data-stu-id="08a0a-123">*ret*</span></span> | <span data-ttu-id="08a0a-124">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="08a0a-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="08a0a-125">**INT**</span><span class="sxs-lookup"><span data-stu-id="08a0a-125">**int**</span></span>](/windows/desktop/WinProg/windows-data-types)                                          | <span data-ttu-id="08a0a-126">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="08a0a-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="08a0a-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="08a0a-127">Minimum Shader Model</span></span>

<span data-ttu-id="08a0a-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="08a0a-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="08a0a-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="08a0a-129">Shader Model</span></span>                                                                       | <span data-ttu-id="08a0a-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="08a0a-130">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="08a0a-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="08a0a-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="08a0a-132">ja</span><span class="sxs-lookup"><span data-stu-id="08a0a-132">yes</span></span>                         |
| [<span data-ttu-id="08a0a-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="08a0a-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="08a0a-134">Ja (vs \_ 1 \_ 1 und PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="08a0a-134">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="08a0a-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="08a0a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08a0a-136">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="08a0a-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

