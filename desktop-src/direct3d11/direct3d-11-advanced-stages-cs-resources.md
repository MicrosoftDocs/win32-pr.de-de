---
title: Neue Ressourcentypen
description: In Direct3D 11 wurden mehrere neue Ressourcentypen hinzugefügt.
ms.assetid: 597cc12f-dd0e-4603-b670-3f584f25e192
keywords:
- Byte Adress Puffer (Übersicht)
- Lese-/Schreibpuffer (Übersicht)
- Strukturierter Puffer (Übersicht)
- Ungeordneter Zugriffs Puffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b7a75ec95917a5ee819126e42dce3117994574
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390652"
---
# <a name="new-resource-types"></a><span data-ttu-id="b99e5-107">Neue Ressourcentypen</span><span class="sxs-lookup"><span data-stu-id="b99e5-107">New Resource Types</span></span>

<span data-ttu-id="b99e5-108">In Direct3D 11 wurden mehrere neue Ressourcentypen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b99e5-108">Several new resource types have been added in Direct3D 11.</span></span>

-   [<span data-ttu-id="b99e5-109">Puffer und Texturen mit Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="b99e5-109">Read/Write Buffers and Textures</span></span>](#readwrite-buffers-and-textures)
-   [<span data-ttu-id="b99e5-110">Strukturierter Puffer</span><span class="sxs-lookup"><span data-stu-id="b99e5-110">Structured Buffer</span></span>](#structured-buffer)
-   [<span data-ttu-id="b99e5-111">Byte Adress Puffer</span><span class="sxs-lookup"><span data-stu-id="b99e5-111">Byte Address Buffer</span></span>](#byte-address-buffer)
-   [<span data-ttu-id="b99e5-112">Ungeordneter Zugriffs Puffer oder Textur</span><span class="sxs-lookup"><span data-stu-id="b99e5-112">Unordered Access Buffer or Texture</span></span>](#unordered-access-buffer-or-texture)
    -   [<span data-ttu-id="b99e5-113">Puffer anfügen und nutzen</span><span class="sxs-lookup"><span data-stu-id="b99e5-113">Append and Consume Buffer</span></span>](#append-and-consume-buffer)
-   [<span data-ttu-id="b99e5-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b99e5-114">Related topics</span></span>](#related-topics)

## <a name="readwrite-buffers-and-textures"></a><span data-ttu-id="b99e5-115">Puffer und Texturen mit Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="b99e5-115">Read/Write Buffers and Textures</span></span>

<span data-ttu-id="b99e5-116">Shadermodell 4-Ressourcen sind schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b99e5-116">Shader model 4 resources are read only.</span></span> <span data-ttu-id="b99e5-117">Shader Model 5 implementiert einen neuen entsprechenden Satz von Lese-/Schreibressourcen:</span><span class="sxs-lookup"><span data-stu-id="b99e5-117">Shader model 5 implements a new corresponding set of read/write resources:</span></span>

-   [<span data-ttu-id="b99e5-118">Rwbuffer</span><span class="sxs-lookup"><span data-stu-id="b99e5-118">RWBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-rwbuffer)
-   <span data-ttu-id="b99e5-119">[RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)</span><span class="sxs-lookup"><span data-stu-id="b99e5-119">[RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)</span></span>
-   <span data-ttu-id="b99e5-120">[RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)</span><span class="sxs-lookup"><span data-stu-id="b99e5-120">[RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)</span></span>
-   [<span data-ttu-id="b99e5-121">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="b99e5-121">RWTexture3D</span></span>](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)

<span data-ttu-id="b99e5-122">Diese Ressourcen erfordern eine Ressourcen Variable für den Zugriff auf den Arbeitsspeicher (durch Indizierung), da keine Methoden für den direkten Zugriff auf den Speicher vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="b99e5-122">These resources require a resource variable to access memory (through indexing) as there are no methods for accessing memory directly.</span></span> <span data-ttu-id="b99e5-123">Eine Ressourcen Variable kann auf der linken und der rechten Seite einer Gleichung verwendet werden. Wenn Sie auf der rechten Seite verwendet wird, muss es sich bei dem Vorlagentyp um eine einzelne Komponente (float, int oder uint) handeln.</span><span class="sxs-lookup"><span data-stu-id="b99e5-123">A resource variable can be used on the left and right sides of an equation; if used on the right side, the template type must be single component (float, int, or uint).</span></span>

## <a name="structured-buffer"></a><span data-ttu-id="b99e5-124">Strukturierter Puffer</span><span class="sxs-lookup"><span data-stu-id="b99e5-124">Structured Buffer</span></span>

<span data-ttu-id="b99e5-125">Ein strukturierter Puffer ist ein Puffer, der Elemente gleicher Größen enthält.</span><span class="sxs-lookup"><span data-stu-id="b99e5-125">A structured buffer is a buffer that contains elements of equal sizes.</span></span> <span data-ttu-id="b99e5-126">Verwenden Sie eine Struktur mit einem oder mehreren Elementtypen, um ein Element zu definieren.</span><span class="sxs-lookup"><span data-stu-id="b99e5-126">Use a structure with one or more member types to define an element.</span></span> <span data-ttu-id="b99e5-127">Im folgenden finden Sie eine Struktur mit drei Membern.</span><span class="sxs-lookup"><span data-stu-id="b99e5-127">Here is a structure with three members.</span></span>


```
struct MyStruct
{
    float4 Color;
    float4 Normal;
    bool isAwesome;
};
```



<span data-ttu-id="b99e5-128">Verwenden Sie diese Struktur, um einen strukturierten Puffer wie den folgenden zu deklarieren:</span><span class="sxs-lookup"><span data-stu-id="b99e5-128">Use this structure to declare a structured buffer like this:</span></span>


```
StructuredBuffer<MyStruct> mySB;
```



<span data-ttu-id="b99e5-129">Zusätzlich zur Indizierung unterstützt ein strukturierter Puffer den Zugriff auf einen einzelnen Member wie den folgenden:</span><span class="sxs-lookup"><span data-stu-id="b99e5-129">In addition to indexing, a structured buffer supports accessing a single member like this:</span></span>


```
float4 myColor = mySb[27].Color;
```



<span data-ttu-id="b99e5-130">Verwenden Sie die folgenden Objekttypen, um auf einen strukturierten Puffer zuzugreifen:</span><span class="sxs-lookup"><span data-stu-id="b99e5-130">Use the following object types to access a structured buffer:</span></span>

-   <span data-ttu-id="b99e5-131">[Structuredbuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) ist ein strukturierter Schreib geschützter Puffer.</span><span class="sxs-lookup"><span data-stu-id="b99e5-131">[StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) is a read only structured buffer.</span></span>
-   <span data-ttu-id="b99e5-132">[Rwstructuredbuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) ist ein strukturierter Lese-/Schreib-Puffer.</span><span class="sxs-lookup"><span data-stu-id="b99e5-132">[RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) is a read/write structured buffer.</span></span>

<span data-ttu-id="b99e5-133">[Atomarische Funktionen](direct3d-11-advanced-stages-cs-atomic-functions.md) , die Interlocked-Vorgänge implementieren, sind für int-und uint-Elemente in einem **rwstructuredbuffer** zulässig.</span><span class="sxs-lookup"><span data-stu-id="b99e5-133">[Atomic functions](direct3d-11-advanced-stages-cs-atomic-functions.md) which implement interlocked operations are allowed on int and uint elements in an **RWStructuredBuffer**.</span></span>

## <a name="byte-address-buffer"></a><span data-ttu-id="b99e5-134">Byte Adress Puffer</span><span class="sxs-lookup"><span data-stu-id="b99e5-134">Byte Address Buffer</span></span>

<span data-ttu-id="b99e5-135">Ein Byte Adress Puffer ist ein Puffer, dessen Inhalt durch einen Byte Offset adressierbar ist.</span><span class="sxs-lookup"><span data-stu-id="b99e5-135">A byte address buffer is a buffer whose contents are addressable by a byte offset.</span></span> <span data-ttu-id="b99e5-136">Normalerweise wird der Inhalt eines [Puffers](overviews-direct3d-11-resources-buffers-intro.md) pro Element mithilfe eines Stride-Elements für jedes Element und der Element Nummer (n) indiziert, wie von S \* N angegeben.</span><span class="sxs-lookup"><span data-stu-id="b99e5-136">Normally, the contents of a [buffer](overviews-direct3d-11-resources-buffers-intro.md) are indexed per element using a stride for each element (S) and the element number (N) as given by S\*N.</span></span> <span data-ttu-id="b99e5-137">Ein Byte Adress Puffer, der auch als Rohdaten Puffer bezeichnet werden kann, verwendet einen Byte-Wert Offset vom Anfang des Puffers für den Zugriff auf Daten.</span><span class="sxs-lookup"><span data-stu-id="b99e5-137">A byte address buffer, which can also be called a raw buffer, uses a byte value offset from the beginning of the buffer to access data.</span></span> <span data-ttu-id="b99e5-138">Der Bytewert muss ein Vielfaches von vier sein, damit er mit DWORD ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="b99e5-138">The byte value must be a multiple of four so that it is DWORD aligned.</span></span> <span data-ttu-id="b99e5-139">Wenn ein anderer Wert angegeben wird, ist das Verhalten nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="b99e5-139">If any other value is provided, behavior is undefined.</span></span>

<span data-ttu-id="b99e5-140">Mit Shader Model 5 werden Objekte für den Zugriff auf einen schreibgeschützten [Byte Adress Puffer](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) sowie einen [Byte Adress Puffer mit Lese-/Schreibzugriff](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b99e5-140">Shader model 5 introduces objects for accessing a [read-only byte address buffer](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) as well as a [read-write byte address buffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer).</span></span> <span data-ttu-id="b99e5-141">Der Inhalt eines Byte Adress Puffers ist als 32-Bit-Ganzzahl ohne Vorzeichen konzipiert. Wenn der Wert im Puffer nicht wirklich eine Ganzzahl ohne Vorzeichen ist, verwenden Sie eine Funktion wie [**asfloat**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) , um Sie zu lesen.</span><span class="sxs-lookup"><span data-stu-id="b99e5-141">The contents of a byte address buffer is designed to be a 32-bit unsigned integer; if the value in the buffer is not really an unsigned integer, use a function such as [**asfloat**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) to read it.</span></span>

## <a name="unordered-access-buffer-or-texture"></a><span data-ttu-id="b99e5-142">Ungeordneter Zugriffs Puffer oder Textur</span><span class="sxs-lookup"><span data-stu-id="b99e5-142">Unordered Access Buffer or Texture</span></span>

<span data-ttu-id="b99e5-143">Eine unsorderte Zugriffs Ressource (einschließlich Puffer, Texturen und Textur Arrays ohne Multisampling) ermöglicht Temporale ungeordnete Lese-/Schreibzugriffe aus mehreren Threads.</span><span class="sxs-lookup"><span data-stu-id="b99e5-143">An unordered access resource (which includes buffers, textures, and texture arrays - without multisampling), allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="b99e5-144">Dies bedeutet, dass dieser Ressourcentyp gleichzeitig von mehreren Threads gelesen/geschrieben werden kann, ohne dass Arbeitsspeicher Konflikte durch die Verwendung von [atomaren Funktionen](direct3d-11-advanced-stages-cs-atomic-functions.md)entstehen.</span><span class="sxs-lookup"><span data-stu-id="b99e5-144">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts through the use of [Atomic Functions](direct3d-11-advanced-stages-cs-atomic-functions.md).</span></span>

<span data-ttu-id="b99e5-145">Erstellen Sie einen ungeordneten Zugriffs Puffer oder eine Textur, indem Sie eine Funktion wie z. b. [**ID3D11Device:: createbuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) oder [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) aufrufen und in der Enumeration [**D3D11 \_ Bind- \_ Flag**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) das Flag **D3D11 \_ Bind \_ ungeordnete \_ Zugriffe** übergeben.</span><span class="sxs-lookup"><span data-stu-id="b99e5-145">Create an unordered access buffer or texture by calling a function such as [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) or [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) and passing in the **D3D11\_BIND\_UNORDERED\_ACCESS** flag from the [**D3D11\_BIND\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) enumeration.</span></span>

<span data-ttu-id="b99e5-146">Ungeordnete Zugriffs Ressourcen können nur an Pixel-Shader und Compute-Shader gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="b99e5-146">Unordered access resources can only be bound to pixel shaders and compute shaders.</span></span> <span data-ttu-id="b99e5-147">Während der Ausführung verfügen Pixel-Shader oder COMPUTE-Shader, die parallel ausgeführt werden, über die gleichen unbestellten Zugriffs Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b99e5-147">During execution, pixel shaders or compute shaders running in parallel have the same unordered access resources bound.</span></span>

### <a name="append-and-consume-buffer"></a><span data-ttu-id="b99e5-148">Puffer anfügen und nutzen</span><span class="sxs-lookup"><span data-stu-id="b99e5-148">Append and Consume Buffer</span></span>

<span data-ttu-id="b99e5-149">Ein Anfüge-und-Wert-Puffer ist ein spezieller Typ einer ungeordneten Ressource, der das Hinzufügen und Entfernen von Werten am Ende eines Puffers unterstützt, ähnlich der Art und Weise, wie ein Stapel funktioniert.</span><span class="sxs-lookup"><span data-stu-id="b99e5-149">An append and consume buffer is a special type of an unordered resource that supports adding and removing values from the end of a buffer similar to the way a stack works.</span></span>

<span data-ttu-id="b99e5-150">Ein Anfüge-und-Verb-Puffer muss ein strukturierter Puffer sein:</span><span class="sxs-lookup"><span data-stu-id="b99e5-150">An append and consume buffer must be a structured buffer:</span></span>

-   [<span data-ttu-id="b99e5-151">Appendstructuredbuffer</span><span class="sxs-lookup"><span data-stu-id="b99e5-151">AppendStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [<span data-ttu-id="b99e5-152">Consumestructuredbuffer</span><span class="sxs-lookup"><span data-stu-id="b99e5-152">ConsumeStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)

<span data-ttu-id="b99e5-153">Diese Ressourcen werden über ihre Methoden verwendet, von denen diese Ressourcen keine Ressourcenvariablen verwenden.</span><span class="sxs-lookup"><span data-stu-id="b99e5-153">Use these resources through their methods, these resources do not use resource variables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b99e5-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b99e5-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b99e5-155">Übersicht über Compute-Shader</span><span class="sxs-lookup"><span data-stu-id="b99e5-155">Compute Shader Overview</span></span>](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 