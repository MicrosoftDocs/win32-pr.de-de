---
title: sätftigen (HLSL-Referenz)
description: Bindet den angegebenen Wert im Bereich von 0 bis 1.
ms.assetid: efe4dedd-732a-4643-8a57-61814434f6ff
keywords:
- HLSL sätftigen
topic_type:
- apiref
api_name:
- saturate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 609443bdc1d0cff6a4c81c8eb26d86a30ea1e721
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315188"
---
# <a name="saturate-hlsl-reference"></a><span data-ttu-id="1ba5c-104">sätftigen (HLSL-Referenz)</span><span class="sxs-lookup"><span data-stu-id="1ba5c-104">saturate (HLSL reference)</span></span>

<span data-ttu-id="1ba5c-105">Bindet den angegebenen Wert im Bereich von 0 bis 1.</span><span class="sxs-lookup"><span data-stu-id="1ba5c-105">Clamps the specified value within the range of 0 to 1.</span></span>



| <span data-ttu-id="1ba5c-106">*ret* -vollständig (*x*)</span><span class="sxs-lookup"><span data-stu-id="1ba5c-106">*ret* saturate(*x*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="1ba5c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ba5c-107">Parameters</span></span>



| <span data-ttu-id="1ba5c-108">Element</span><span class="sxs-lookup"><span data-stu-id="1ba5c-108">Item</span></span>                                                   | <span data-ttu-id="1ba5c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ba5c-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="1ba5c-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="1ba5c-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="1ba5c-111">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="1ba5c-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="1ba5c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ba5c-112">Return Value</span></span>

<span data-ttu-id="1ba5c-113">Der *x* -Parameter, der innerhalb des Bereichs von 0 bis 1 geklemmt ist.</span><span class="sxs-lookup"><span data-stu-id="1ba5c-113">The *x* parameter, clamped within the range of 0 to 1.</span></span>

## <a name="type-description"></a><span data-ttu-id="1ba5c-114">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="1ba5c-114">Type Description</span></span>



| <span data-ttu-id="1ba5c-115">Name</span><span class="sxs-lookup"><span data-stu-id="1ba5c-115">Name</span></span>  | [<span data-ttu-id="1ba5c-116">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="1ba5c-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="1ba5c-117">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="1ba5c-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="1ba5c-118">Size</span><span class="sxs-lookup"><span data-stu-id="1ba5c-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="1ba5c-119">*x*</span><span class="sxs-lookup"><span data-stu-id="1ba5c-119">*x*</span></span>   | <span data-ttu-id="1ba5c-120">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="1ba5c-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="1ba5c-121">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="1ba5c-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1ba5c-122">any</span><span class="sxs-lookup"><span data-stu-id="1ba5c-122">any</span></span>                            |
| <span data-ttu-id="1ba5c-123">*TZI*</span><span class="sxs-lookup"><span data-stu-id="1ba5c-123">*ret*</span></span> | <span data-ttu-id="1ba5c-124">identisch mit Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="1ba5c-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="1ba5c-125">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="1ba5c-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1ba5c-126">gleiche Dimension (n) wie Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="1ba5c-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1ba5c-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="1ba5c-127">Minimum Shader Model</span></span>

<span data-ttu-id="1ba5c-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1ba5c-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1ba5c-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="1ba5c-129">Shader Model</span></span>                                                                       | <span data-ttu-id="1ba5c-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="1ba5c-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="1ba5c-131">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="1ba5c-131">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="1ba5c-132">ja</span><span class="sxs-lookup"><span data-stu-id="1ba5c-132">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1ba5c-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1ba5c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ba5c-134">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="1ba5c-134">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

