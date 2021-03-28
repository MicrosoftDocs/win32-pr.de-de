---
title: D3DCOLORtoUBYTE4
description: Konvertiert einen Gleit Komma-4D-Vektor, der durch ein D3DCOLOR-Element festgelegt ist, in einen UBYTE4.
ms.assetid: 20a7be00-1e36-41c3-bc98-933b3faa8f35
keywords:
- D3DCOLORtoUBYTE4 HLSL
topic_type:
- apiref
api_name:
- D3DCOLORtoUBYTE4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c60f0934d6700ec7fbd9e6d9e6443cb6409ab15f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517072"
---
# <a name="d3dcolortoubyte4"></a><span data-ttu-id="50908-104">D3DCOLORtoUBYTE4</span><span class="sxs-lookup"><span data-stu-id="50908-104">D3DCOLORtoUBYTE4</span></span>

<span data-ttu-id="50908-105">Konvertiert einen Gleit Komma-4D-Vektor, der durch ein D3DCOLOR-Element festgelegt ist, in einen UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="50908-105">Converts a floating-point, 4D vector set by a D3DCOLOR to a UBYTE4.</span></span>



| <span data-ttu-id="50908-106">*ret* D3DCOLORtoUBYTE4 (*x*)</span><span class="sxs-lookup"><span data-stu-id="50908-106">*ret* D3DCOLORtoUBYTE4(*x*)</span></span> |
|-----------------------------|



 

<span data-ttu-id="50908-107">Diese Funktion durch schwimmt und skaliert Komponenten des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="50908-107">This function swizzles and scales components of the *x* parameter.</span></span> <span data-ttu-id="50908-108">Verwenden Sie diese Funktion, um den Mangel an UBYTE4-Unterstützung in gewisser Hardware auszugleichen.</span><span class="sxs-lookup"><span data-stu-id="50908-108">Use this function to compensate for the lack of UBYTE4 support in some hardware.</span></span>

## <a name="parameters"></a><span data-ttu-id="50908-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="50908-109">Parameters</span></span>



| <span data-ttu-id="50908-110">Element</span><span class="sxs-lookup"><span data-stu-id="50908-110">Item</span></span>                                                   | <span data-ttu-id="50908-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50908-111">Description</span></span>                                              |
|--------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="50908-112"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="50908-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="50908-113">\[in \] der zu konvertierenden Gleit Komma Vector4.</span><span class="sxs-lookup"><span data-stu-id="50908-113">\[in\] The floating-point vector4 to convert.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="50908-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50908-114">Return Value</span></span>

<span data-ttu-id="50908-115">Die UBYTE4-Darstellung des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="50908-115">The UBYTE4 representation of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="50908-116">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="50908-116">Type Description</span></span>



| <span data-ttu-id="50908-117">Name</span><span class="sxs-lookup"><span data-stu-id="50908-117">Name</span></span>  | [<span data-ttu-id="50908-118">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="50908-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="50908-119">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="50908-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="50908-120">Size</span><span class="sxs-lookup"><span data-stu-id="50908-120">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="50908-121">*x*</span><span class="sxs-lookup"><span data-stu-id="50908-121">*x*</span></span>   | [<span data-ttu-id="50908-122">**ve**</span><span class="sxs-lookup"><span data-stu-id="50908-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="50908-123">**float**</span><span class="sxs-lookup"><span data-stu-id="50908-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="50908-124">4</span><span class="sxs-lookup"><span data-stu-id="50908-124">4</span></span>    |
| <span data-ttu-id="50908-125">*TZI*</span><span class="sxs-lookup"><span data-stu-id="50908-125">*ret*</span></span> | [<span data-ttu-id="50908-126">**ve**</span><span class="sxs-lookup"><span data-stu-id="50908-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="50908-127">**Zah**</span><span class="sxs-lookup"><span data-stu-id="50908-127">**integer**</span></span>](/windows/desktop/WinProg/windows-data-types)                      | <span data-ttu-id="50908-128">4</span><span class="sxs-lookup"><span data-stu-id="50908-128">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="50908-129">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="50908-129">Minimum Shader Model</span></span>

<span data-ttu-id="50908-130">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="50908-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="50908-131">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="50908-131">Shader Model</span></span>                                                                       | <span data-ttu-id="50908-132">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="50908-132">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="50908-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="50908-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="50908-134">ja</span><span class="sxs-lookup"><span data-stu-id="50908-134">yes</span></span>       |
| [<span data-ttu-id="50908-135">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="50908-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="50908-136">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="50908-136">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="50908-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="50908-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50908-138">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="50908-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

