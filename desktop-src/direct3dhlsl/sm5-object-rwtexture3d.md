---
title: RWTexture3D
description: Eine Ressource mit Lese-/Schreibzugriff. | RWTexture3D
ms.assetid: 4d02810e-4f3c-4b20-b057-0ff27d6732b5
keywords:
- RWTexture3D HLSL
topic_type:
- apiref
api_name:
- RWTexture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b89ed7ff724eabef9fc2b2757c6ac0e5272c69e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352669"
---
# <a name="rwtexture3d"></a><span data-ttu-id="2f4de-105">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="2f4de-105">RWTexture3D</span></span>

<span data-ttu-id="2f4de-106">Eine Ressource mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="2f4de-106">A read/write resource.</span></span>



| <span data-ttu-id="2f4de-107">Methode</span><span class="sxs-lookup"><span data-stu-id="2f4de-107">Method</span></span>                                                        | <span data-ttu-id="2f4de-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f4de-108">Description</span></span>                   |
|---------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="2f4de-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="2f4de-109">**GetDimensions**</span></span>](sm5-object-rwtexture3d-getdimensions.md) | <span data-ttu-id="2f4de-110">Ruft die Ressourcen Dimensionen ab.</span><span class="sxs-lookup"><span data-stu-id="2f4de-110">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="2f4de-111">**Laden**</span><span class="sxs-lookup"><span data-stu-id="2f4de-111">**Load**</span></span>](rwtexture3d-load.md)                              | <span data-ttu-id="2f4de-112">Liest Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="2f4de-112">Reads texture data.</span></span>           |
| <span data-ttu-id="2f4de-113">[**KOM\[\]**](sm5-object-rwtexture3d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="2f4de-113">[**Operator\[\]**](sm5-object-rwtexture3d-operatorindex.md)</span></span>  | <span data-ttu-id="2f4de-114">Ruft eine Ressourcen Variable ab.</span><span class="sxs-lookup"><span data-stu-id="2f4de-114">Gets a resource variable.</span></span>     |



 

<span data-ttu-id="2f4de-115">Sie können **RWTexture3D** -Objekten mit der Speicher Klasse **globallycoherent** als Präfix versehen.</span><span class="sxs-lookup"><span data-stu-id="2f4de-115">You can prefix **RWTexture3D** objects with the storage class **globallycoherent**.</span></span> <span data-ttu-id="2f4de-116">Diese Speicher Klasse bewirkt, dass Speicherbarrieren und Synchronisierungen Daten über die gesamte GPU leeren, sodass andere Gruppen Schreibvorgänge sehen können.</span><span class="sxs-lookup"><span data-stu-id="2f4de-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="2f4de-117">Ohne diesen Spezifizierer leert eine Speicherbarriere oder Synchronisierung eine UAV nur innerhalb der aktuellen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="2f4de-117">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

<span data-ttu-id="2f4de-118">Ein **RWTexture3D** -Objekt erfordert einen Elementtyp in einer Deklarations Anweisung für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2f4de-118">A **RWTexture3D** object requires an element type in a declaration statement for the object.</span></span> <span data-ttu-id="2f4de-119">Beispielsweise ist die folgende Deklaration richtig:</span><span class="sxs-lookup"><span data-stu-id="2f4de-119">For example, the following declaration is correct:</span></span>


```
RWTexture3D<float> tex;
```



<span data-ttu-id="2f4de-120">Da ein **RWTexture3D** -Objekt ein Objekt vom Typ "UAV" ist, unterscheiden sich seine Eigenschaften von einem Objekt der Shader-Ressourcen Ansicht (SRV), z. b. einem [**Texture3D**](sm5-object-texture3d.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="2f4de-120">Because a **RWTexture3D** object is a UAV-type object, its properties differ from a shader resource view (SRV)-type object, such as a [**Texture3D**](sm5-object-texture3d.md) object.</span></span> <span data-ttu-id="2f4de-121">Beispielsweise können Sie aus einem **RWTexture3D** -Objekt lesen und darin schreiben, aber Sie können nur aus einem **Texture3D** -Objekt lesen.</span><span class="sxs-lookup"><span data-stu-id="2f4de-121">For example, you can read from and write to a **RWTexture3D** object, but you can only read from a **Texture3D** object.</span></span>

<span data-ttu-id="2f4de-122">Ein **RWTexture3D** -Objekt kann keine Methoden aus einem [**Texture3D**](sm5-object-texture3d.md) -Objekt verwenden, z. b. [Sample](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="2f4de-122">A **RWTexture3D** object cannot use methods from a [**Texture3D**](sm5-object-texture3d.md) object, such as [Sample](dx-graphics-hlsl-to-sample.md).</span></span> <span data-ttu-id="2f4de-123">Da Sie jedoch mehrere Ansichts Typen für dieselbe Ressource erstellen können, können Sie mehrere Textur Typen als einzelne Textur in mehreren Shadern deklarieren.</span><span class="sxs-lookup"><span data-stu-id="2f4de-123">However, because you can create multiple view types to the same resource, you can declare multiple texture types as a single texture in multiple shaders.</span></span> <span data-ttu-id="2f4de-124">Beispielsweise können Sie ein **RWTexture3D** -Objekt als *tex* in einem Compute-Shader deklarieren und verwenden und dann ein **Texture3D** -Objekt als *tex* in einem Pixelshader deklarieren und verwenden.</span><span class="sxs-lookup"><span data-stu-id="2f4de-124">For example, you can declare and use a **RWTexture3D** object as *tex* in a compute shader and then declare and use a **Texture3D** object as *tex* in a pixel shader.</span></span>

> [!Note]  
> <span data-ttu-id="2f4de-125">Die Runtime erzwingt bestimmte Verwendungs Muster, wenn Sie mehrere Ansichts Typen für dieselbe Ressource erstellen.</span><span class="sxs-lookup"><span data-stu-id="2f4de-125">The runtime enforces certain usage patterns when you create multiple view types to the same resource.</span></span> <span data-ttu-id="2f4de-126">Beispielsweise können Sie mit der Laufzeit nicht gleichzeitig eine UAV-Zuordnung für eine Ressource und eine SRV-Zuordnung für dieselbe Ressource aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2f4de-126">For example, the runtime does not allow you to have both a UAV mapping for a resource and SRV mapping for the same resource active at the same time.</span></span>

 

## <a name="minimum-shader-model"></a><span data-ttu-id="2f4de-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="2f4de-127">Minimum Shader Model</span></span>

<span data-ttu-id="2f4de-128">Dieses Objekt wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2f4de-128">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="2f4de-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="2f4de-129">Shader Model</span></span>                                                                | <span data-ttu-id="2f4de-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="2f4de-130">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="2f4de-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="2f4de-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="2f4de-132">ja</span><span class="sxs-lookup"><span data-stu-id="2f4de-132">yes</span></span>       |



 

<span data-ttu-id="2f4de-133">Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="2f4de-133">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2f4de-134">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="2f4de-134">Vertex</span></span> | <span data-ttu-id="2f4de-135">Hülle</span><span class="sxs-lookup"><span data-stu-id="2f4de-135">Hull</span></span> | <span data-ttu-id="2f4de-136">Domain</span><span class="sxs-lookup"><span data-stu-id="2f4de-136">Domain</span></span> | <span data-ttu-id="2f4de-137">Geometrie</span><span class="sxs-lookup"><span data-stu-id="2f4de-137">Geometry</span></span> | <span data-ttu-id="2f4de-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="2f4de-138">Pixel</span></span> | <span data-ttu-id="2f4de-139">Compute</span><span class="sxs-lookup"><span data-stu-id="2f4de-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="2f4de-140">x</span><span class="sxs-lookup"><span data-stu-id="2f4de-140">x</span></span>     | <span data-ttu-id="2f4de-141">x</span><span class="sxs-lookup"><span data-stu-id="2f4de-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2f4de-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2f4de-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f4de-143">Shader Model 5-Objekte</span><span class="sxs-lookup"><span data-stu-id="2f4de-143">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




