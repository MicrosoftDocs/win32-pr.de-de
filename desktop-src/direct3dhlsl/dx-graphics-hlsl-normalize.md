---
title: Normalisieren
description: Normalisiert den angegebenen Gleit Komma Vektor gemäß x/length (x).
ms.assetid: 7fd6f8ff-f3ff-4d14-b3fc-b44fdddf6c75
keywords:
- HLSL normalisieren
topic_type:
- apiref
api_name:
- normalize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f48c78f80f5f92f950795018f05a46c7883d9736
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949083"
---
# <a name="normalize"></a><span data-ttu-id="93229-104">Normalisieren</span><span class="sxs-lookup"><span data-stu-id="93229-104">normalize</span></span>

<span data-ttu-id="93229-105">Normalisiert den angegebenen Gleit Komma Vektor gemäß x/length (x).</span><span class="sxs-lookup"><span data-stu-id="93229-105">Normalizes the specified floating-point vector according to x / length(x).</span></span>



| <span data-ttu-id="93229-106">*ret* Normalize (*x*)</span><span class="sxs-lookup"><span data-stu-id="93229-106">*ret* normalize(*x*)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="93229-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="93229-107">Parameters</span></span>



| <span data-ttu-id="93229-108">Element</span><span class="sxs-lookup"><span data-stu-id="93229-108">Item</span></span>                                                   | <span data-ttu-id="93229-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="93229-109">Description</span></span>                                            |
|--------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="93229-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="93229-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="93229-111">\[im \] angegebenen Gleit Komma Vektor.</span><span class="sxs-lookup"><span data-stu-id="93229-111">\[in\] The specified floating-point vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="93229-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="93229-112">Return Value</span></span>

<span data-ttu-id="93229-113">Der normalisierte *x* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="93229-113">The normalized *x* parameter.</span></span> <span data-ttu-id="93229-114">Wenn die Länge des *x* -Parameters 0 beträgt, ist das Ergebnis unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="93229-114">If the length of the *x* parameter is 0, the result is indefinite.</span></span>

## <a name="remarks"></a><span data-ttu-id="93229-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93229-115">Remarks</span></span>

<span data-ttu-id="93229-116">Die intrinsische Funktion " **normalisieren** HLSL" verwendet die folgende Formel: *x*  /  [**length**](dx-graphics-hlsl-length.md)(*x*).</span><span class="sxs-lookup"><span data-stu-id="93229-116">The **normalize** HLSL intrinsic function uses the following formula: *x* / [**length**](dx-graphics-hlsl-length.md)(*x*).</span></span>

## <a name="type-description"></a><span data-ttu-id="93229-117">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="93229-117">Type Description</span></span>



| <span data-ttu-id="93229-118">Name</span><span class="sxs-lookup"><span data-stu-id="93229-118">Name</span></span>  | [<span data-ttu-id="93229-119">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="93229-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="93229-120">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="93229-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="93229-121">Size</span><span class="sxs-lookup"><span data-stu-id="93229-121">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="93229-122">*x*</span><span class="sxs-lookup"><span data-stu-id="93229-122">*x*</span></span>   | [<span data-ttu-id="93229-123">**ve**</span><span class="sxs-lookup"><span data-stu-id="93229-123">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="93229-124">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="93229-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="93229-125">any</span><span class="sxs-lookup"><span data-stu-id="93229-125">any</span></span>                            |
| <span data-ttu-id="93229-126">*TZI*</span><span class="sxs-lookup"><span data-stu-id="93229-126">*ret*</span></span> | <span data-ttu-id="93229-127">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="93229-127">same as input *x*</span></span>                                                                   | [<span data-ttu-id="93229-128">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="93229-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="93229-129">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="93229-129">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="93229-130">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="93229-130">Minimum Shader Model</span></span>

<span data-ttu-id="93229-131">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="93229-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="93229-132">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="93229-132">Shader Model</span></span>                                                                       | <span data-ttu-id="93229-133">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="93229-133">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="93229-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="93229-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="93229-135">ja</span><span class="sxs-lookup"><span data-stu-id="93229-135">yes</span></span>                 |
| [<span data-ttu-id="93229-136">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="93229-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="93229-137">Ja ( \_ nur vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="93229-137">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="93229-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="93229-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93229-139">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="93229-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

