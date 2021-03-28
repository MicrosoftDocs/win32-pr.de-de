---
title: Consumestructuredbuffer
description: Ein Eingabepuffer, der als Stream angezeigt wird, aus dem der Shader Werte abrufen kann. Nur strukturierte Puffer können T-Typen annehmen, die Strukturen sind.
ms.assetid: 373bdd97-6186-4bce-99bf-738a153234f6
keywords:
- Consumestructuredbuffer HLSL
topic_type:
- apiref
api_name:
- ConsumeStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af7a670713dc5b63839702a04a632dda61ebfa43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993598"
---
# <a name="consumestructuredbuffer"></a><span data-ttu-id="06ca0-105">Consumestructuredbuffer</span><span class="sxs-lookup"><span data-stu-id="06ca0-105">ConsumeStructuredBuffer</span></span>

<span data-ttu-id="06ca0-106">Ein Eingabepuffer, der als Stream angezeigt wird, aus dem der Shader Werte abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="06ca0-106">An input buffer that appears as a stream the shader may pull values from.</span></span> <span data-ttu-id="06ca0-107">Nur strukturierte Puffer können T-Typen annehmen, die Strukturen sind.</span><span class="sxs-lookup"><span data-stu-id="06ca0-107">Only structured buffers can take T types that are structures.</span></span>



| <span data-ttu-id="06ca0-108">Methode</span><span class="sxs-lookup"><span data-stu-id="06ca0-108">Method</span></span>                                                                    | <span data-ttu-id="06ca0-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06ca0-109">Description</span></span>                                 |
|---------------------------------------------------------------------------|---------------------------------------------|
| [<span data-ttu-id="06ca0-110">**Nutzen**</span><span class="sxs-lookup"><span data-stu-id="06ca0-110">**Consume**</span></span>](sm5-object-consumestructuredbuffer-consume.md)             | <span data-ttu-id="06ca0-111">Entfernt einen Wert vom Ende des Puffers.</span><span class="sxs-lookup"><span data-stu-id="06ca0-111">Removes a value from the end of the buffer.</span></span> |
| [<span data-ttu-id="06ca0-112">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="06ca0-112">**GetDimensions**</span></span>](sm5-object-consumestructuredbuffer-getdimensions.md) | <span data-ttu-id="06ca0-113">Ruft die Ressourcen Dimensionen ab.</span><span class="sxs-lookup"><span data-stu-id="06ca0-113">Gets the resource dimensions.</span></span>               |



 

<span data-ttu-id="06ca0-114">Das an diese Ressource gebundene UAV-Format muss mit dem \_ unbekanntem DXGI-Format erstellt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="06ca0-114">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="06ca0-115">Die an diese Ressource gebundene UAV muss mit dem D3D11- [**\_ Puffer- \_ UAV- \_ Flag " \_ Append**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag)" erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="06ca0-115">The UAV bound to this resource must have been created with [**D3D11\_BUFFER\_UAV\_FLAG\_APPEND**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span></span>

<span data-ttu-id="06ca0-116">Weitere Informationen über die Nutzung strukturierter Puffer finden Sie in beiden Abschnitten: [Anfügen und](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) Verwenden von Puffer und [strukturiertem Puffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span><span class="sxs-lookup"><span data-stu-id="06ca0-116">For more info about consume structured buffers, see both sections: [append and consume buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) and [structured buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="06ca0-117">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="06ca0-117">Minimum Shader Model</span></span>

<span data-ttu-id="06ca0-118">Dieses Objekt wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="06ca0-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="06ca0-119">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="06ca0-119">Shader Model</span></span>                                                                | <span data-ttu-id="06ca0-120">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="06ca0-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="06ca0-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="06ca0-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="06ca0-122">ja</span><span class="sxs-lookup"><span data-stu-id="06ca0-122">yes</span></span>       |



 

<span data-ttu-id="06ca0-123">Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="06ca0-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="06ca0-124">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="06ca0-124">Vertex</span></span> | <span data-ttu-id="06ca0-125">Hülle</span><span class="sxs-lookup"><span data-stu-id="06ca0-125">Hull</span></span> | <span data-ttu-id="06ca0-126">Domain</span><span class="sxs-lookup"><span data-stu-id="06ca0-126">Domain</span></span> | <span data-ttu-id="06ca0-127">Geometrie</span><span class="sxs-lookup"><span data-stu-id="06ca0-127">Geometry</span></span> | <span data-ttu-id="06ca0-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="06ca0-128">Pixel</span></span> | <span data-ttu-id="06ca0-129">Compute</span><span class="sxs-lookup"><span data-stu-id="06ca0-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="06ca0-130">x</span><span class="sxs-lookup"><span data-stu-id="06ca0-130">x</span></span>     | <span data-ttu-id="06ca0-131">x</span><span class="sxs-lookup"><span data-stu-id="06ca0-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="06ca0-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="06ca0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06ca0-133">Shader Model 5-Objekte</span><span class="sxs-lookup"><span data-stu-id="06ca0-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 