---
title: Getsampleposition (DirectX HLSL-Textur Objekt)
description: Ruft die Position des angegebenen Beispiels ab.
ms.assetid: 4e622b85-82d6-4339-b03a-becbe5f9aa57
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 062bf08064faf112fdc1efe5b371fcad72efeeea
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389496"
---
# <a name="getsampleposition-directx-hlsl-texture-object"></a><span data-ttu-id="cb4f3-103">Getsampleposition (DirectX HLSL-Textur Objekt)</span><span class="sxs-lookup"><span data-stu-id="cb4f3-103">GetSamplePosition (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="cb4f3-104">Ruft die Position des angegebenen Beispiels ab.</span><span class="sxs-lookup"><span data-stu-id="cb4f3-104">Gets the position of the specified sample.</span></span>



|                                        |
|----------------------------------------|
| <span data-ttu-id="cb4f3-105">Ret Object. getsampleposition (int s);</span><span class="sxs-lookup"><span data-stu-id="cb4f3-105">ret Object.GetSamplePosition( int s );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="cb4f3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb4f3-106">Parameters</span></span>



| <span data-ttu-id="cb4f3-107">Element</span><span class="sxs-lookup"><span data-stu-id="cb4f3-107">Item</span></span>                                                                                           | <span data-ttu-id="cb4f3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb4f3-108">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb4f3-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objekt*</span><span class="sxs-lookup"><span data-stu-id="cb4f3-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span><br/> | <span data-ttu-id="cb4f3-110">Ein Texture2DMS-oder Texture2DMSArray [-Textur-Objekttyp](dx-graphics-hlsl-to-type.md) .</span><span class="sxs-lookup"><span data-stu-id="cb4f3-110">A Texture2DMS or a Texture2DMSArray [texture-object](dx-graphics-hlsl-to-type.md) type.</span></span><br/> |
| <span data-ttu-id="cb4f3-111"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="cb4f3-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>                                         | <span data-ttu-id="cb4f3-112">\[im \] NULL basierten Beispiel Index.</span><span class="sxs-lookup"><span data-stu-id="cb4f3-112">\[in\] The zero-based sample index.</span></span><br/>                                                      |



 

## <a name="return-value"></a><span data-ttu-id="cb4f3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb4f3-113">Return Value</span></span>

<span data-ttu-id="cb4f3-114">Gibt die Beispiel Position (x, y), einen Gleit Komma Vektor mit zwei Komponenten, zurück.</span><span class="sxs-lookup"><span data-stu-id="cb4f3-114">Returns the (x,y) sample position, a two-component floating-point vector.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="cb4f3-115">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="cb4f3-115">Minimum Shader Model</span></span>

<span data-ttu-id="cb4f3-116">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cb4f3-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="cb4f3-117">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cb4f3-117">vs\_4\_0</span></span> | <span data-ttu-id="cb4f3-118">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="cb4f3-118">vs\_4\_1</span></span>  | <span data-ttu-id="cb4f3-119">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cb4f3-119">ps\_4\_0</span></span> | <span data-ttu-id="cb4f3-120">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="cb4f3-120">ps\_4\_1</span></span>  | <span data-ttu-id="cb4f3-121">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cb4f3-121">gs\_4\_0</span></span> | <span data-ttu-id="cb4f3-122">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="cb4f3-122">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          | <span data-ttu-id="cb4f3-123">x</span><span class="sxs-lookup"><span data-stu-id="cb4f3-123">x</span></span>         |          | <span data-ttu-id="cb4f3-124">x</span><span class="sxs-lookup"><span data-stu-id="cb4f3-124">x</span></span>         |          | <span data-ttu-id="cb4f3-125">x</span><span class="sxs-lookup"><span data-stu-id="cb4f3-125">x</span></span>         |



 

-   <span data-ttu-id="cb4f3-126">Das Shader-Modell 4,1 ist in Direct3D 10,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cb4f3-126">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb4f3-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb4f3-127">Remarks</span></span>

<span data-ttu-id="cb4f3-128">Ein Pixelshader kann bei der Stichproben Häufigkeit (Ausführen eines Pixelshaders einmal pro Stichprobe) oder bei Pixel Häufigkeit (Ausführen eines Pixel-Shader einmal pro Pixel) ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="cb4f3-128">A pixel shader can be evaluated at sample frequency (run a pixel shader once per sample) or at pixel frequency (run a pixel shader once per pixel).</span></span> <span data-ttu-id="cb4f3-129">Fügen Sie die \_ Semantik "SV sampleindex" an eine Pixel-Shadereingabe an, um einen PixelShader bei der Stichproben Häufigkeit aufzurufen. der Eingabe Wert wird dann als Beispiel Index verwendet, wenn das Rendern des Renderziels</span><span class="sxs-lookup"><span data-stu-id="cb4f3-129">Attach the SV\_SampleIndex semantic to a pixel shader input to invoke a pixel shader at sample frequency, the input value is then used as a sample index when sampling the render target.</span></span>

<span data-ttu-id="cb4f3-130">Sie können eine Pixel-Shadereingabe auf verschiedene Weise interpolieren.</span><span class="sxs-lookup"><span data-stu-id="cb4f3-130">You can interpolate a pixel shader input in several ways.</span></span> <span data-ttu-id="cb4f3-131">So interpolieren Sie an:</span><span class="sxs-lookup"><span data-stu-id="cb4f3-131">To interpolate at:</span></span>

-   <span data-ttu-id="cb4f3-132">Ein Pixel Center verwendet keine Semantik.</span><span class="sxs-lookup"><span data-stu-id="cb4f3-132">A pixel center, don't use any semantic.</span></span>
-   <span data-ttu-id="cb4f3-133">Beispiel: Verwenden Sie die \_ Semantik "SV samplindex".</span><span class="sxs-lookup"><span data-stu-id="cb4f3-133">A sample, use the SV\_SampleIndex semantic.</span></span>
-   <span data-ttu-id="cb4f3-134">Einen Schwerpunkt Speicherort verwenden Sie den [ \_ Schwerpunkt](dx-graphics-hlsl-struct.md) -Modifizierer.</span><span class="sxs-lookup"><span data-stu-id="cb4f3-134">A centroid location, use the [\_centroid](dx-graphics-hlsl-struct.md) modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb4f3-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cb4f3-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb4f3-136">Texture-Objekt</span><span class="sxs-lookup"><span data-stu-id="cb4f3-136">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





