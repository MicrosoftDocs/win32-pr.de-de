---
title: RWTexture2D
description: Eine Ressource mit Lese-/Schreibzugriff. | RWTexture2D
ms.assetid: 19b383f1-c787-4c20-b77a-60ef9f212b9f
keywords:
- RWTexture2D HLSL
topic_type:
- apiref
api_name:
- RWTexture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccdeae4dd47d3ad4bf5d756c2ca362033eae6814
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352969"
---
# <a name="rwtexture2d"></a><span data-ttu-id="4775d-105">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="4775d-105">RWTexture2D</span></span>

<span data-ttu-id="4775d-106">Eine Ressource mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4775d-106">A read/write resource.</span></span>



| <span data-ttu-id="4775d-107">Methode</span><span class="sxs-lookup"><span data-stu-id="4775d-107">Method</span></span>                                                        | <span data-ttu-id="4775d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4775d-108">Description</span></span>                   |
|---------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="4775d-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="4775d-109">**GetDimensions**</span></span>](sm5-object-rwtexture2d-getdimensions.md) | <span data-ttu-id="4775d-110">Ruft die Ressourcen Dimensionen ab.</span><span class="sxs-lookup"><span data-stu-id="4775d-110">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="4775d-111">**Laden**</span><span class="sxs-lookup"><span data-stu-id="4775d-111">**Load**</span></span>](rwtexture2d-load.md)                              | <span data-ttu-id="4775d-112">Liest Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="4775d-112">Reads texture data.</span></span>           |
| <span data-ttu-id="4775d-113">[**KOM\[\]**](sm5-object-rwtexture2d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="4775d-113">[**Operator\[\]**](sm5-object-rwtexture2d-operatorindex.md)</span></span>  | <span data-ttu-id="4775d-114">Ruft eine Ressourcen Variable ab.</span><span class="sxs-lookup"><span data-stu-id="4775d-114">Gets a resource variable.</span></span>     |



 

<span data-ttu-id="4775d-115">Sie können RWTexture2D-Objekten mit der Speicher Klasse **globallycoherent** als Präfix versehen.</span><span class="sxs-lookup"><span data-stu-id="4775d-115">You can prefix RWTexture2D objects with the storage class **globallycoherent**.</span></span> <span data-ttu-id="4775d-116">Diese Speicher Klasse bewirkt, dass Speicherbarrieren und Synchronisierungen Daten über die gesamte GPU leeren, sodass andere Gruppen Schreibvorgänge sehen können.</span><span class="sxs-lookup"><span data-stu-id="4775d-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="4775d-117">Ohne diesen Spezifizierer leert eine Speicherbarriere oder Synchronisierung nur eine unsorderte Zugriffs Ansicht (UAV) innerhalb der aktuellen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="4775d-117">Without this specifier, a memory barrier or sync will flush only an unordered access view (UAV) within the current group.</span></span>

<span data-ttu-id="4775d-118">Ein RWTexture2D-Objekt erfordert einen Elementtyp in einer Deklarations Anweisung für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4775d-118">A RWTexture2D object requires an element type in a declaration statement for the object.</span></span> <span data-ttu-id="4775d-119">Beispielsweise ist die folgende Deklaration nicht korrekt:</span><span class="sxs-lookup"><span data-stu-id="4775d-119">For example, the following declaration is not correct:</span></span>


```
// The following declaration is incorrectly coded.
RWTexture2D myTexture;
```



<span data-ttu-id="4775d-120">Die folgende Deklaration ist korrekt:</span><span class="sxs-lookup"><span data-stu-id="4775d-120">The following declaration is correct:</span></span>


```
// The following declaration is correctly coded.
RWTexture2D<float> tex;
```



<span data-ttu-id="4775d-121">Da ein RWTexture2D-Objekt ein Objekt vom Typ "UAV" ist, unterscheiden sich seine Eigenschaften von einem Objekt der Shader-Ressourcen Ansicht (SRV), z. b. einem [Texture2D](sm5-object-texture2d.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="4775d-121">Because a RWTexture2D object is a UAV-type object, its properties differ from a shader resource view (SRV)-type object, such as a [Texture2D](sm5-object-texture2d.md) object.</span></span> <span data-ttu-id="4775d-122">Beispielsweise können Sie aus einem RWTexture2D-Objekt lesen und darin schreiben, aber Sie können nur aus einem Texture2D-Objekt lesen.</span><span class="sxs-lookup"><span data-stu-id="4775d-122">For example, you can read from and write to a RWTexture2D object, but you can only read from a Texture2D object.</span></span>

<span data-ttu-id="4775d-123">Ein RWTexture2D-Objekt kann keine Methoden aus einem [Texture2D](sm5-object-texture2d.md) -Objekt verwenden, z. b. [Sample](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="4775d-123">A RWTexture2D object cannot use methods from a [Texture2D](sm5-object-texture2d.md) object, such as [Sample](dx-graphics-hlsl-to-sample.md).</span></span> <span data-ttu-id="4775d-124">Da Sie jedoch mehrere Ansichts Typen für dieselbe Ressource erstellen können, können Sie mehrere Textur Typen als einzelne Textur in mehreren Shadern deklarieren.</span><span class="sxs-lookup"><span data-stu-id="4775d-124">However, because you can create multiple view types to the same resource, you can declare multiple texture types as a single texture in multiple shaders.</span></span> <span data-ttu-id="4775d-125">Die folgenden Code Ausschnitte zeigen z. b., wie Sie ein RWTexture2D-Objekt als *tex* in einem Compute-Shader deklarieren und verwenden können, und dann ein Texture2D-Objekt als *tex* in einem Pixelshader deklarieren und verwenden.</span><span class="sxs-lookup"><span data-stu-id="4775d-125">For example, the following code snippets show how you can declare and use a RWTexture2D object as *tex* in a compute shader and then declare and use a Texture2D object as *tex* in a pixel shader.</span></span>

> [!Note]  
> <span data-ttu-id="4775d-126">Die Runtime erzwingt bestimmte Verwendungs Muster, wenn Sie mehrere Ansichts Typen für dieselbe Ressource erstellen.</span><span class="sxs-lookup"><span data-stu-id="4775d-126">The runtime enforces certain usage patterns when you create multiple view types to the same resource.</span></span> <span data-ttu-id="4775d-127">Beispielsweise können Sie mit der Laufzeit nicht gleichzeitig eine UAV-Zuordnung für eine Ressource und eine SRV-Zuordnung für dieselbe Ressource aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4775d-127">For example, the runtime does not allow you to have both a UAV mapping for a resource and SRV mapping for the same resource active at the same time.</span></span>

 

<span data-ttu-id="4775d-128">Der folgende Code ist für den Compute-Shader:</span><span class="sxs-lookup"><span data-stu-id="4775d-128">The following code is for the compute shader:</span></span>


```
RWTexture2D<float> tex;
[numthreads(groupDim_x, groupDim_y, 1)]
void main(
    uint3 groupId : SV_GroupID,
    uint3 groupThreadId : SV_GroupThreadID,
    uint3 dispatchThreadId : SV_DispatchThreadID,
    uint groupIndex : SV_GroupIndex)
{
    tex [dispatchThreadId.xy] = <something>;
}
```



<span data-ttu-id="4775d-129">Der folgende Code ist für den Pixelshader:</span><span class="sxs-lookup"><span data-stu-id="4775d-129">The following code is for the pixel shader:</span></span>


```
struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float2 tex : TEXTURE;
};

Texture2D<float> tex;
float4 main(PixelShaderInput input) : SV_TARGET
{
    return tex.Sample(TextureSampler, input.tex);
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="4775d-130">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="4775d-130">Minimum Shader Model</span></span>

<span data-ttu-id="4775d-131">Dieses Objekt wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4775d-131">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="4775d-132">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="4775d-132">Shader Model</span></span>                                                                | <span data-ttu-id="4775d-133">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="4775d-133">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="4775d-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="4775d-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="4775d-135">ja</span><span class="sxs-lookup"><span data-stu-id="4775d-135">yes</span></span>       |



 

<span data-ttu-id="4775d-136">Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="4775d-136">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4775d-137">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="4775d-137">Vertex</span></span> | <span data-ttu-id="4775d-138">Hülle</span><span class="sxs-lookup"><span data-stu-id="4775d-138">Hull</span></span> | <span data-ttu-id="4775d-139">Domain</span><span class="sxs-lookup"><span data-stu-id="4775d-139">Domain</span></span> | <span data-ttu-id="4775d-140">Geometrie</span><span class="sxs-lookup"><span data-stu-id="4775d-140">Geometry</span></span> | <span data-ttu-id="4775d-141">Pixel</span><span class="sxs-lookup"><span data-stu-id="4775d-141">Pixel</span></span> | <span data-ttu-id="4775d-142">Compute</span><span class="sxs-lookup"><span data-stu-id="4775d-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="4775d-143">x</span><span class="sxs-lookup"><span data-stu-id="4775d-143">x</span></span>     | <span data-ttu-id="4775d-144">x</span><span class="sxs-lookup"><span data-stu-id="4775d-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4775d-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4775d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4775d-146">Shader Model 5-Objekte</span><span class="sxs-lookup"><span data-stu-id="4775d-146">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




