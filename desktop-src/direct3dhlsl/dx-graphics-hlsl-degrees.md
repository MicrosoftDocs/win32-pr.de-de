---
title: Grad
description: Konvertiert den angegebenen Wert von Bogenmaß in Grad.
ms.assetid: e60a3ec4-9177-457a-8314-a5788f353633
keywords:
- Grad HLSL
topic_type:
- apiref
api_name:
- degrees
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 47d8bba0ee43da81a18baaeaffca0e3c917e460d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390507"
---
# <a name="degrees"></a><span data-ttu-id="916c1-104">Grad</span><span class="sxs-lookup"><span data-stu-id="916c1-104">degrees</span></span>

<span data-ttu-id="916c1-105">Konvertiert den angegebenen Wert von Bogenmaß in Grad.</span><span class="sxs-lookup"><span data-stu-id="916c1-105">Converts the specified value from radians to degrees.</span></span>



| <span data-ttu-id="916c1-106">*ret* -Grad (*x*)</span><span class="sxs-lookup"><span data-stu-id="916c1-106">*ret* degrees(*x*)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="916c1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="916c1-107">Parameters</span></span>



| <span data-ttu-id="916c1-108">Element</span><span class="sxs-lookup"><span data-stu-id="916c1-108">Item</span></span>                                                   | <span data-ttu-id="916c1-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="916c1-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="916c1-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="916c1-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="916c1-111">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="916c1-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="916c1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="916c1-112">Return Value</span></span>

<span data-ttu-id="916c1-113">Das Ergebnis der typumrechnung des *x* -Parameters von Bogenmaß in Grad.</span><span class="sxs-lookup"><span data-stu-id="916c1-113">The result of converting the *x* parameter from radians to degrees.</span></span>

## <a name="type-description"></a><span data-ttu-id="916c1-114">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="916c1-114">Type Description</span></span>



| <span data-ttu-id="916c1-115">Name</span><span class="sxs-lookup"><span data-stu-id="916c1-115">Name</span></span>  | [<span data-ttu-id="916c1-116">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="916c1-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="916c1-117">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="916c1-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="916c1-118">Size</span><span class="sxs-lookup"><span data-stu-id="916c1-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="916c1-119">*x*</span><span class="sxs-lookup"><span data-stu-id="916c1-119">*x*</span></span>   | <span data-ttu-id="916c1-120">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="916c1-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="916c1-121">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="916c1-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="916c1-122">any</span><span class="sxs-lookup"><span data-stu-id="916c1-122">any</span></span>                            |
| <span data-ttu-id="916c1-123">*TZI*</span><span class="sxs-lookup"><span data-stu-id="916c1-123">*ret*</span></span> | <span data-ttu-id="916c1-124">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="916c1-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="916c1-125">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="916c1-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="916c1-126">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="916c1-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="916c1-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="916c1-127">Minimum Shader Model</span></span>

<span data-ttu-id="916c1-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="916c1-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="916c1-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="916c1-129">Shader Model</span></span>                                                                       | <span data-ttu-id="916c1-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="916c1-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="916c1-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="916c1-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="916c1-132">ja</span><span class="sxs-lookup"><span data-stu-id="916c1-132">yes</span></span>       |
| [<span data-ttu-id="916c1-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="916c1-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="916c1-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="916c1-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="916c1-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="916c1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="916c1-136">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="916c1-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

