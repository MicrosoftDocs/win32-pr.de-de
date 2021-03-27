---
title: Appendstructuredbuffer
description: Ausgabepuffer, der als Stream angezeigt wird, an den der Shader anfügen kann. Nur strukturierte Puffer können T-Typen annehmen, die Strukturen sind.
ms.assetid: 377b0358-0f9d-4021-9140-19c3d1bfed38
keywords:
- Appendstructuredbuffer HLSL
topic_type:
- apiref
api_name:
- AppendStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c140052c861c8da3df6378fc3bc49816998c130
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728185"
---
# <a name="appendstructuredbuffer"></a><span data-ttu-id="e406d-105">Appendstructuredbuffer</span><span class="sxs-lookup"><span data-stu-id="e406d-105">AppendStructuredBuffer</span></span>

<span data-ttu-id="e406d-106">Ausgabepuffer, der als Stream angezeigt wird, an den der Shader anfügen kann.</span><span class="sxs-lookup"><span data-stu-id="e406d-106">Output buffer that appears as a stream the shader may append to.</span></span> <span data-ttu-id="e406d-107">Nur strukturierte Puffer können T-Typen annehmen, die Strukturen sind.</span><span class="sxs-lookup"><span data-stu-id="e406d-107">Only structured buffers can take T types that are structures.</span></span>



| <span data-ttu-id="e406d-108">Methode</span><span class="sxs-lookup"><span data-stu-id="e406d-108">Method</span></span>                                                                   | <span data-ttu-id="e406d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e406d-109">Description</span></span>                               |
|--------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="e406d-110">**Anfügen**</span><span class="sxs-lookup"><span data-stu-id="e406d-110">**Append**</span></span>](sm5-object-appendstructuredbuffer-append.md)               | <span data-ttu-id="e406d-111">Fügt einen Wert an das Ende des Puffers an.</span><span class="sxs-lookup"><span data-stu-id="e406d-111">Appends a value to the end of the buffer.</span></span> |
| [<span data-ttu-id="e406d-112">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="e406d-112">**GetDimensions**</span></span>](sm5-object-appendstructuredbuffer-getdimensions.md) | <span data-ttu-id="e406d-113">Ruft die Ressourcen Dimensionen ab.</span><span class="sxs-lookup"><span data-stu-id="e406d-113">Gets the resource dimensions.</span></span>             |



 

<span data-ttu-id="e406d-114">Das an diese Ressource gebundene UAV-Format muss mit dem \_ unbekanntem DXGI-Format erstellt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="e406d-114">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="e406d-115">Die an diese Ressource gebundene UAV muss mit dem D3D11- [**\_ Puffer- \_ UAV- \_ Flag " \_ Append**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag)" erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e406d-115">The UAV bound to this resource must have been created with [**D3D11\_BUFFER\_UAV\_FLAG\_APPEND**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span></span>

<span data-ttu-id="e406d-116">Weitere Informationen zu einem strukturierteren Anfüge Puffer finden Sie in beiden Abschnitten: [Anfügen und](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) Verwenden von Puffer und [strukturiertem Puffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span><span class="sxs-lookup"><span data-stu-id="e406d-116">For more information about an append structured buffer, see both sections: [append and consume buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) and [structured buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="e406d-117">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="e406d-117">Minimum Shader Model</span></span>

<span data-ttu-id="e406d-118">Dieses Objekt wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e406d-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="e406d-119">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="e406d-119">Shader Model</span></span>                                                                | <span data-ttu-id="e406d-120">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="e406d-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="e406d-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="e406d-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="e406d-122">ja</span><span class="sxs-lookup"><span data-stu-id="e406d-122">yes</span></span>       |



 

<span data-ttu-id="e406d-123">Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e406d-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e406d-124">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="e406d-124">Vertex</span></span> | <span data-ttu-id="e406d-125">Hülle</span><span class="sxs-lookup"><span data-stu-id="e406d-125">Hull</span></span> | <span data-ttu-id="e406d-126">Domain</span><span class="sxs-lookup"><span data-stu-id="e406d-126">Domain</span></span> | <span data-ttu-id="e406d-127">Geometrie</span><span class="sxs-lookup"><span data-stu-id="e406d-127">Geometry</span></span> | <span data-ttu-id="e406d-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="e406d-128">Pixel</span></span> | <span data-ttu-id="e406d-129">Compute</span><span class="sxs-lookup"><span data-stu-id="e406d-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e406d-130">x</span><span class="sxs-lookup"><span data-stu-id="e406d-130">x</span></span>     | <span data-ttu-id="e406d-131">x</span><span class="sxs-lookup"><span data-stu-id="e406d-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e406d-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e406d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e406d-133">Shader Model 5-Objekte</span><span class="sxs-lookup"><span data-stu-id="e406d-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 