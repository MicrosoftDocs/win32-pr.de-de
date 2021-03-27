---
title: RWTexture1D
description: Eine Ressource mit Lese-/Schreibzugriff. | RWTexture1D
ms.assetid: 47866e5a-b26b-4264-9291-c8940882d662
keywords:
- RWTexture1D HLSL
topic_type:
- apiref
api_name:
- RWTexture1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 695b73cc14541505ee1b2d4391aac2d145eec8d7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981152"
---
# <a name="rwtexture1d"></a><span data-ttu-id="36529-105">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="36529-105">RWTexture1D</span></span>

<span data-ttu-id="36529-106">Eine Ressource mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="36529-106">A read/write resource.</span></span>



| <span data-ttu-id="36529-107">Methode</span><span class="sxs-lookup"><span data-stu-id="36529-107">Method</span></span>                                                        | <span data-ttu-id="36529-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36529-108">Description</span></span>                   |
|---------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="36529-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="36529-109">**GetDimensions**</span></span>](sm5-object-rwtexture1d-getdimensions.md) | <span data-ttu-id="36529-110">Ruft die Ressourcen Dimensionen ab.</span><span class="sxs-lookup"><span data-stu-id="36529-110">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="36529-111">**Laden**</span><span class="sxs-lookup"><span data-stu-id="36529-111">**Load**</span></span>](rwtexture1d-load.md)                              | <span data-ttu-id="36529-112">Liest Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="36529-112">Reads texture data.</span></span>           |
| <span data-ttu-id="36529-113">[**KOM\[\]**](sm5-object-rwtexture1d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="36529-113">[**Operator\[\]**](sm5-object-rwtexture1d-operatorindex.md)</span></span>  | <span data-ttu-id="36529-114">Ruft eine Ressourcen Variable ab.</span><span class="sxs-lookup"><span data-stu-id="36529-114">Gets a resource variable.</span></span>     |



 

<span data-ttu-id="36529-115">Sie können **RWTexture1D** -Objekten mit der Speicher Klasse **globallycoherent** als Präfix versehen.</span><span class="sxs-lookup"><span data-stu-id="36529-115">You can prefix **RWTexture1D** objects with the storage class **globallycoherent**.</span></span> <span data-ttu-id="36529-116">Diese Speicher Klasse bewirkt, dass Speicherbarrieren und Synchronisierungen Daten über die gesamte GPU leeren, sodass andere Gruppen Schreibvorgänge sehen können.</span><span class="sxs-lookup"><span data-stu-id="36529-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="36529-117">Ohne diesen Spezifizierer leert eine Speicherbarriere oder Synchronisierung eine UAV nur innerhalb der aktuellen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="36529-117">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

<span data-ttu-id="36529-118">Ein **RWTexture1D** -Objekt erfordert einen Elementtyp in einer Deklarations Anweisung für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="36529-118">A **RWTexture1D** object requires an element type in a declaration statement for the object.</span></span> <span data-ttu-id="36529-119">Beispielsweise ist die folgende Deklaration richtig:</span><span class="sxs-lookup"><span data-stu-id="36529-119">For example, the following declaration is correct:</span></span>


```
RWTexture1D<float> tex;
```



<span data-ttu-id="36529-120">Da ein **RWTexture1D** -Objekt ein Objekt vom Typ "UAV" ist, unterscheiden sich seine Eigenschaften von einem Objekt der Shader-Ressourcen Ansicht (SRV), z. b. einem [**Texture1D**](sm5-object-texture1d.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="36529-120">Because a **RWTexture1D** object is a UAV-type object, its properties differ from a shader resource view (SRV)-type object, such as a [**Texture1D**](sm5-object-texture1d.md) object.</span></span> <span data-ttu-id="36529-121">Beispielsweise können Sie aus einem **RWTexture1D** -Objekt lesen und darin schreiben, aber Sie können nur aus einem **Texture1D** -Objekt lesen.</span><span class="sxs-lookup"><span data-stu-id="36529-121">For example, you can read from and write to a **RWTexture1D** object, but you can only read from a **Texture1D** object.</span></span>

<span data-ttu-id="36529-122">Ein **RWTexture1D** -Objekt kann keine Methoden aus einem [**Texture1D**](sm5-object-texture1d.md) -Objekt verwenden, z. b. [Sample](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="36529-122">A **RWTexture1D** object cannot use methods from a [**Texture1D**](sm5-object-texture1d.md) object, such as [Sample](dx-graphics-hlsl-to-sample.md).</span></span> <span data-ttu-id="36529-123">Da Sie jedoch mehrere Ansichts Typen für dieselbe Ressource erstellen können, können Sie mehrere Textur Typen als einzelne Textur in mehreren Shadern deklarieren.</span><span class="sxs-lookup"><span data-stu-id="36529-123">However, because you can create multiple view types to the same resource, you can declare multiple texture types as a single texture in multiple shaders.</span></span> <span data-ttu-id="36529-124">Beispielsweise können Sie ein **RWTexture1D** -Objekt als *tex* in einem Compute-Shader deklarieren und verwenden und dann ein **Texture1D** -Objekt als *tex* in einem Pixelshader deklarieren und verwenden.</span><span class="sxs-lookup"><span data-stu-id="36529-124">For example, you can declare and use a **RWTexture1D** object as *tex* in a compute shader and then declare and use a **Texture1D** object as *tex* in a pixel shader.</span></span>

> [!Note]  
> <span data-ttu-id="36529-125">Die Runtime erzwingt bestimmte Verwendungs Muster, wenn Sie mehrere Ansichts Typen für dieselbe Ressource erstellen.</span><span class="sxs-lookup"><span data-stu-id="36529-125">The runtime enforces certain usage patterns when you create multiple view types to the same resource.</span></span> <span data-ttu-id="36529-126">Beispielsweise können Sie mit der Laufzeit nicht gleichzeitig eine UAV-Zuordnung für eine Ressource und eine SRV-Zuordnung für dieselbe Ressource aktivieren.</span><span class="sxs-lookup"><span data-stu-id="36529-126">For example, the runtime does not allow you to have both a UAV mapping for a resource and SRV mapping for the same resource active at the same time.</span></span>

 

## <a name="minimum-shader-model"></a><span data-ttu-id="36529-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="36529-127">Minimum Shader Model</span></span>

<span data-ttu-id="36529-128">Dieses Objekt wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="36529-128">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="36529-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="36529-129">Shader Model</span></span>                                                                | <span data-ttu-id="36529-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="36529-130">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="36529-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="36529-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="36529-132">ja</span><span class="sxs-lookup"><span data-stu-id="36529-132">yes</span></span>       |



 

<span data-ttu-id="36529-133">Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="36529-133">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="36529-134">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="36529-134">Vertex</span></span> | <span data-ttu-id="36529-135">Hülle</span><span class="sxs-lookup"><span data-stu-id="36529-135">Hull</span></span> | <span data-ttu-id="36529-136">Domain</span><span class="sxs-lookup"><span data-stu-id="36529-136">Domain</span></span> | <span data-ttu-id="36529-137">Geometrie</span><span class="sxs-lookup"><span data-stu-id="36529-137">Geometry</span></span> | <span data-ttu-id="36529-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="36529-138">Pixel</span></span> | <span data-ttu-id="36529-139">Compute</span><span class="sxs-lookup"><span data-stu-id="36529-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="36529-140">x</span><span class="sxs-lookup"><span data-stu-id="36529-140">x</span></span>     | <span data-ttu-id="36529-141">x</span><span class="sxs-lookup"><span data-stu-id="36529-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="36529-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="36529-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36529-143">Shader Model 5-Objekte</span><span class="sxs-lookup"><span data-stu-id="36529-143">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




