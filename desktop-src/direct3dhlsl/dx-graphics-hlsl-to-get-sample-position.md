---
title: GetSamplePosition (DirectX HLSL-Texturobjekt)
description: Ruft die Position des angegebenen Beispiels ab.
ms.assetid: 4e622b85-82d6-4339-b03a-becbe5f9aa57
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9a1e5f4dc71d5af2e7973ef180c919a49e65ef81
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118585"
---
# <a name="getsampleposition-directx-hlsl-texture-object"></a><span data-ttu-id="52635-103">GetSamplePosition (DirectX HLSL-Texturobjekt)</span><span class="sxs-lookup"><span data-stu-id="52635-103">GetSamplePosition (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="52635-104">Ruft die Position des angegebenen Beispiels ab.</span><span class="sxs-lookup"><span data-stu-id="52635-104">Gets the position of the specified sample.</span></span>

<span data-ttu-id="52635-105">ret Object.GetSamplePosition( int s );</span><span class="sxs-lookup"><span data-stu-id="52635-105">ret Object.GetSamplePosition( int s );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="52635-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="52635-106">Parameters</span></span>



| <span data-ttu-id="52635-107">Element</span><span class="sxs-lookup"><span data-stu-id="52635-107">Item</span></span>                                                                                           | <span data-ttu-id="52635-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52635-108">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52635-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objekt*</span><span class="sxs-lookup"><span data-stu-id="52635-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span><br/> | <span data-ttu-id="52635-110">Ein Texture2DMS- oder ein Texture2DMSArray-Texturobjekttyp. [](dx-graphics-hlsl-to-type.md)</span><span class="sxs-lookup"><span data-stu-id="52635-110">A Texture2DMS or a Texture2DMSArray [texture-object](dx-graphics-hlsl-to-type.md) type.</span></span><br/> |
| <span data-ttu-id="52635-111"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="52635-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>                                         | <span data-ttu-id="52635-112">\[in \] Der nullbasierte Beispielindex.</span><span class="sxs-lookup"><span data-stu-id="52635-112">\[in\] The zero-based sample index.</span></span><br/>                                                      |



 

## <a name="return-value"></a><span data-ttu-id="52635-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52635-113">Return Value</span></span>

<span data-ttu-id="52635-114">Gibt die (x,y)-Beispielposition zurück, einen Gleitkommavektor mit zwei Komponenten.</span><span class="sxs-lookup"><span data-stu-id="52635-114">Returns the (x,y) sample position, a two-component floating-point vector.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="52635-115">Minimales Shadermodell</span><span class="sxs-lookup"><span data-stu-id="52635-115">Minimum Shader Model</span></span>

<span data-ttu-id="52635-116">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="52635-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="52635-117">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="52635-117">vs\_4\_0</span></span> | <span data-ttu-id="52635-118">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="52635-118">vs\_4\_1</span></span>  | <span data-ttu-id="52635-119">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="52635-119">ps\_4\_0</span></span> | <span data-ttu-id="52635-120">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="52635-120">ps\_4\_1</span></span>  | <span data-ttu-id="52635-121">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="52635-121">gs\_4\_0</span></span> | <span data-ttu-id="52635-122">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="52635-122">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          | <span data-ttu-id="52635-123">x</span><span class="sxs-lookup"><span data-stu-id="52635-123">x</span></span>         |          | <span data-ttu-id="52635-124">x</span><span class="sxs-lookup"><span data-stu-id="52635-124">x</span></span>         |          | <span data-ttu-id="52635-125">x</span><span class="sxs-lookup"><span data-stu-id="52635-125">x</span></span>         |



 

-   <span data-ttu-id="52635-126">ShaderModell 4.1 ist in Direct3D 10.1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="52635-126">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="remarks"></a><span data-ttu-id="52635-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52635-127">Remarks</span></span>

<span data-ttu-id="52635-128">Ein Pixel-Shader kann mit der Abtastfrequenz (einmal pro Beispiel einen Pixels shader ausführen) oder mit Pixelfrequenz (einmal pro Pixel ausführen) ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="52635-128">A pixel shader can be evaluated at sample frequency (run a pixel shader once per sample) or at pixel frequency (run a pixel shader once per pixel).</span></span> <span data-ttu-id="52635-129">Fügen Sie die SV SampleIndex-Semantik an eine Pixel-Shadereingabe an, um einen Pixel-Shader mit Samplinghäufigkeit aufzurufen. Der Eingabewert wird dann als Beispielindex verwendet, wenn das Renderziel samplingt \_ wird.</span><span class="sxs-lookup"><span data-stu-id="52635-129">Attach the SV\_SampleIndex semantic to a pixel shader input to invoke a pixel shader at sample frequency, the input value is then used as a sample index when sampling the render target.</span></span>

<span data-ttu-id="52635-130">Sie können eine Pixel-Shadereingabe auf verschiedene Weise interpolieren.</span><span class="sxs-lookup"><span data-stu-id="52635-130">You can interpolate a pixel shader input in several ways.</span></span> <span data-ttu-id="52635-131">So interpolieren Sie unter:</span><span class="sxs-lookup"><span data-stu-id="52635-131">To interpolate at:</span></span>

-   <span data-ttu-id="52635-132">Ein Pixelzentriert, verwenden Sie keine Semantik.</span><span class="sxs-lookup"><span data-stu-id="52635-132">A pixel center, don't use any semantic.</span></span>
-   <span data-ttu-id="52635-133">Ein Beispiel: Verwenden Sie die SV \_ SampleIndex-Semantik.</span><span class="sxs-lookup"><span data-stu-id="52635-133">A sample, use the SV\_SampleIndex semantic.</span></span>
-   <span data-ttu-id="52635-134">Verwenden Sie als Schwerpunktposition den [ \_ Modifizierer "schwerpunkt".](dx-graphics-hlsl-struct.md)</span><span class="sxs-lookup"><span data-stu-id="52635-134">A centroid location, use the [\_centroid](dx-graphics-hlsl-struct.md) modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52635-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="52635-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52635-136">Texture-Object</span><span class="sxs-lookup"><span data-stu-id="52635-136">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





