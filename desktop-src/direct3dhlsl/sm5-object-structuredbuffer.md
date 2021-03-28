---
title: Structuredbuffer
description: Ein Schreib geschützter Puffer, der einen T-Typ, der eine Struktur ist, annehmen kann.
ms.assetid: fe2ec0b8-0e19-42b6-9dad-c992ecdeb19e
keywords:
- Structuredbuffer HLSL
topic_type:
- apiref
api_name:
- StructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 524078780ac28d691c4999491bed146a04d34439
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993407"
---
# <a name="structuredbuffer"></a><span data-ttu-id="1adfb-104">Structuredbuffer</span><span class="sxs-lookup"><span data-stu-id="1adfb-104">StructuredBuffer</span></span>

<span data-ttu-id="1adfb-105">Ein Schreib geschützter Puffer, der einen T-Typ, der eine Struktur ist, annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="1adfb-105">A read-only buffer, which can take a T type that is a structure.</span></span>



| <span data-ttu-id="1adfb-106">Methode</span><span class="sxs-lookup"><span data-stu-id="1adfb-106">Method</span></span>                                                             | <span data-ttu-id="1adfb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1adfb-107">Description</span></span>                            |
|--------------------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="1adfb-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="1adfb-108">**GetDimensions**</span></span>](sm5-object-structuredbuffer-getdimensions.md) | <span data-ttu-id="1adfb-109">Ruft die Ressourcen Dimensionen ab.</span><span class="sxs-lookup"><span data-stu-id="1adfb-109">Gets the resource dimensions.</span></span>          |
| [<span data-ttu-id="1adfb-110">**Laden**</span><span class="sxs-lookup"><span data-stu-id="1adfb-110">**Load**</span></span>](structuredbuffer-load.md)                              | <span data-ttu-id="1adfb-111">Liest Puffer Daten.</span><span class="sxs-lookup"><span data-stu-id="1adfb-111">Reads buffer data.</span></span>                     |
| <span data-ttu-id="1adfb-112">[**KOM\[\]**](sm5-object-structuredbuffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="1adfb-112">[**Operator\[\]**](sm5-object-structuredbuffer-operatorindex.md)</span></span>  | <span data-ttu-id="1adfb-113">Gibt eine schreibgeschützte Ressourcen Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="1adfb-113">Returns a read-only resource variable.</span></span> |



 

<span data-ttu-id="1adfb-114">Das an diese Ressource gebundene UAV-Format muss mit dem \_ unbekanntem DXGI-Format erstellt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="1adfb-114">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="1adfb-115">Weitere Informationen über [strukturierte Puffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)finden Sie im Übersichts Material.</span><span class="sxs-lookup"><span data-stu-id="1adfb-115">To find out more about [structured buffers](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), see the overview material.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="1adfb-116">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="1adfb-116">Minimum Shader Model</span></span>

<span data-ttu-id="1adfb-117">Dieses Objekt wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1adfb-117">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="1adfb-118">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="1adfb-118">Shader Model</span></span>                                                                                                                                                                                                            | <span data-ttu-id="1adfb-119">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="1adfb-119">Supported</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="1adfb-120">Shader [Model 5](d3d11-graphics-reference-sm5.md) und höhere Shader-Modelle Shader [Model 4](dx-graphics-hlsl-sm4.md) (verfügbar für Compute-und Pixel-Shader in Direct3D 11 auf einigen Direct3D 10-Geräten)</span><span class="sxs-lookup"><span data-stu-id="1adfb-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available for compute and pixel shaders in Direct3D 11 on some Direct3D 10 devices.)</span></span><br/> | <span data-ttu-id="1adfb-121">ja</span><span class="sxs-lookup"><span data-stu-id="1adfb-121">yes</span></span>       |



 

<span data-ttu-id="1adfb-122">Dieses Objekt wird für die folgenden Typen von Shadern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1adfb-122">This object is supported for the following types of shaders.</span></span>



| <span data-ttu-id="1adfb-123">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="1adfb-123">Vertex</span></span> | <span data-ttu-id="1adfb-124">Hülle</span><span class="sxs-lookup"><span data-stu-id="1adfb-124">Hull</span></span> | <span data-ttu-id="1adfb-125">Domain</span><span class="sxs-lookup"><span data-stu-id="1adfb-125">Domain</span></span> | <span data-ttu-id="1adfb-126">Geometrie</span><span class="sxs-lookup"><span data-stu-id="1adfb-126">Geometry</span></span> | <span data-ttu-id="1adfb-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="1adfb-127">Pixel</span></span> | <span data-ttu-id="1adfb-128">Compute</span><span class="sxs-lookup"><span data-stu-id="1adfb-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1adfb-129">x</span><span class="sxs-lookup"><span data-stu-id="1adfb-129">x</span></span>      | <span data-ttu-id="1adfb-130">x</span><span class="sxs-lookup"><span data-stu-id="1adfb-130">x</span></span>    | <span data-ttu-id="1adfb-131">x</span><span class="sxs-lookup"><span data-stu-id="1adfb-131">x</span></span>      | <span data-ttu-id="1adfb-132">x</span><span class="sxs-lookup"><span data-stu-id="1adfb-132">x</span></span>        | <span data-ttu-id="1adfb-133">x</span><span class="sxs-lookup"><span data-stu-id="1adfb-133">x</span></span>     | <span data-ttu-id="1adfb-134">x</span><span class="sxs-lookup"><span data-stu-id="1adfb-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1adfb-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1adfb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1adfb-136">Shader Model 5-Objekte</span><span class="sxs-lookup"><span data-stu-id="1adfb-136">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

