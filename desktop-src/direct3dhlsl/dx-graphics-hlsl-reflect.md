---
title: widerzuspiegeln
description: Gibt einen Reflektionsvektor mit einem incidentray und einem Oberflächen normalen zurück.
ms.assetid: e321b399-f382-4585-83a6-a7da1f7b2327
keywords:
- HLSL reflektieren
topic_type:
- apiref
api_name:
- reflect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46c981f636a797ecc4e0dd341ce44ed886c202cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729928"
---
# <a name="reflect"></a><span data-ttu-id="1db1e-104">widerzuspiegeln</span><span class="sxs-lookup"><span data-stu-id="1db1e-104">reflect</span></span>

<span data-ttu-id="1db1e-105">Gibt einen Reflektionsvektor mit einem incidentray und einem Oberflächen normalen zurück.</span><span class="sxs-lookup"><span data-stu-id="1db1e-105">Returns a reflection vector using an incident ray and a surface normal.</span></span>



| <span data-ttu-id="1db1e-106">*ret* reflektieren (*i*, *n*)</span><span class="sxs-lookup"><span data-stu-id="1db1e-106">*ret* reflect(*i*, *n*)</span></span> |
|-------------------------|



 

## <a name="parameters"></a><span data-ttu-id="1db1e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1db1e-107">Parameters</span></span>



| <span data-ttu-id="1db1e-108">Element</span><span class="sxs-lookup"><span data-stu-id="1db1e-108">Item</span></span>                                                   | <span data-ttu-id="1db1e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1db1e-109">Description</span></span>                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1db1e-110"><span id="i"></span><span id="I"></span>*Ich*</span><span class="sxs-lookup"><span data-stu-id="1db1e-110"><span id="i"></span><span id="I"></span>*i*</span></span><br/> | <span data-ttu-id="1db1e-111">\[in \] einem Gleit Komma-und incidentvektor.</span><span class="sxs-lookup"><span data-stu-id="1db1e-111">\[in\] A floating-point, incident vector.</span></span><br/> |
| <span data-ttu-id="1db1e-112"><span id="n"></span><span id="N"></span>*Nr*</span><span class="sxs-lookup"><span data-stu-id="1db1e-112"><span id="n"></span><span id="N"></span>*n*</span></span><br/> | <span data-ttu-id="1db1e-113">\[in \] einem Gleit Komma-, normal-Vektor.</span><span class="sxs-lookup"><span data-stu-id="1db1e-113">\[in\] A floating-point, normal vector.</span></span><br/>   |



 

## <a name="return-value"></a><span data-ttu-id="1db1e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1db1e-114">Return Value</span></span>

<span data-ttu-id="1db1e-115">Ein Gleit Komma Wert, reflektionvektor.</span><span class="sxs-lookup"><span data-stu-id="1db1e-115">A floating-point, reflection vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="1db1e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1db1e-116">Remarks</span></span>

<span data-ttu-id="1db1e-117">Diese Funktion berechnet den Reflektionsvektor mithilfe der folgenden Formel: v = i-2 \* n \* Punkt (i n).</span><span class="sxs-lookup"><span data-stu-id="1db1e-117">This function calculates the reflection vector using the following formula: v = i - 2 \* n \* dot(i n) .</span></span>

## <a name="type-description"></a><span data-ttu-id="1db1e-118">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="1db1e-118">Type Description</span></span>



| <span data-ttu-id="1db1e-119">Name</span><span class="sxs-lookup"><span data-stu-id="1db1e-119">Name</span></span>  | [<span data-ttu-id="1db1e-120">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="1db1e-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="1db1e-121">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="1db1e-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="1db1e-122">Size</span><span class="sxs-lookup"><span data-stu-id="1db1e-122">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="1db1e-123">*i*</span><span class="sxs-lookup"><span data-stu-id="1db1e-123">*i*</span></span>   | [<span data-ttu-id="1db1e-124">**ve**</span><span class="sxs-lookup"><span data-stu-id="1db1e-124">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="1db1e-125">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="1db1e-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1db1e-126">any</span><span class="sxs-lookup"><span data-stu-id="1db1e-126">any</span></span>                            |
| <span data-ttu-id="1db1e-127">*n*</span><span class="sxs-lookup"><span data-stu-id="1db1e-127">*n*</span></span>   | [<span data-ttu-id="1db1e-128">**ve**</span><span class="sxs-lookup"><span data-stu-id="1db1e-128">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="1db1e-129">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="1db1e-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1db1e-130">gleiche Dimension (n) wie Eingabe *i*</span><span class="sxs-lookup"><span data-stu-id="1db1e-130">same dimension(s) as input *i*</span></span> |
| <span data-ttu-id="1db1e-131">*TZI*</span><span class="sxs-lookup"><span data-stu-id="1db1e-131">*ret*</span></span> | [<span data-ttu-id="1db1e-132">**ve**</span><span class="sxs-lookup"><span data-stu-id="1db1e-132">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="1db1e-133">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="1db1e-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1db1e-134">gleiche Dimension (n) wie Eingabe *i*</span><span class="sxs-lookup"><span data-stu-id="1db1e-134">same dimension(s) as input *i*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1db1e-135">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="1db1e-135">Minimum Shader Model</span></span>

<span data-ttu-id="1db1e-136">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1db1e-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1db1e-137">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="1db1e-137">Shader Model</span></span>                                                                       | <span data-ttu-id="1db1e-138">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="1db1e-138">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="1db1e-139">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="1db1e-139">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="1db1e-140">ja</span><span class="sxs-lookup"><span data-stu-id="1db1e-140">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1db1e-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1db1e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1db1e-142">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="1db1e-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

