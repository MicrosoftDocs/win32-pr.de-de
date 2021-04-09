---
description: Bei einer Szene, die viele Objekte enthält, die dieselbe Geometrie verwenden, können Sie viele Instanzen dieser Geometrie mit unterschiedlicher Ausrichtung, Größe, Farben usw. mit einer erheblich besseren Leistung erstellen, indem Sie die Menge an Daten verringern, die Sie für den Renderer bereitstellen müssen.
ms.assetid: d8d9b0c8-b1c4-406d-bf2a-9716d725aec7
title: Effizientes Zeichnen mehrerer Instanzen von Geometry (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9981dff913b704fca5e6b211b57e3647fddd28c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860094"
---
# <a name="efficiently-drawing-multiple-instances-of-geometry-direct3d-9"></a><span data-ttu-id="7d00a-103">Effizientes Zeichnen mehrerer Instanzen von Geometry (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7d00a-103">Efficiently Drawing Multiple Instances of Geometry (Direct3D 9)</span></span>

<span data-ttu-id="7d00a-104">Bei einer Szene, die viele Objekte enthält, die dieselbe Geometrie verwenden, können Sie viele Instanzen dieser Geometrie mit unterschiedlicher Ausrichtung, Größe, Farben usw. mit einer erheblich besseren Leistung erstellen, indem Sie die Menge an Daten verringern, die Sie für den Renderer bereitstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="7d00a-104">Given a scene that contains many objects that use the same geometry, you can draw many instances of that geometry at different orientations, sizes, colors, and so on with dramatically better performance by reducing the amount of data you need to supply to the renderer.</span></span>

<span data-ttu-id="7d00a-105">Dies kann durch die Verwendung von zwei Techniken erreicht werden: das erste zum Zeichnen der indizierten Geometrie und das zweite für die nicht indizierte Geometrie.</span><span class="sxs-lookup"><span data-stu-id="7d00a-105">This can be accomplished through the use of two techniques: the first for drawing indexed geometry and the second for non-indexed geometry.</span></span> <span data-ttu-id="7d00a-106">Beide Verfahren verwenden zwei Scheitelpunkt Puffer: einen für die Bereitstellung von Geometriedaten und einen für die Bereitstellung von pro-Objekt-Instanzdaten.</span><span class="sxs-lookup"><span data-stu-id="7d00a-106">Both techniques use two vertex buffers: one to supply geometry data and one to supply per-object instance data.</span></span> <span data-ttu-id="7d00a-107">Bei den Instanzdaten kann es sich um eine Vielzahl von Informationen handeln, wie z. b. eine Transformation, Farbdaten oder Beleuchtungs Daten, was Sie in einer Scheitelpunkt Deklaration beschreiben können.</span><span class="sxs-lookup"><span data-stu-id="7d00a-107">The instance data can be a wide variety of information such as a transform, color data, or lighting data - basically anything that you can describe in a vertex declaration.</span></span> <span data-ttu-id="7d00a-108">Wenn viele Instanzen der Geometrie mit diesen Techniken gezeichnet werden, kann die Menge an Daten, die an den Renderer gesendet werden, drastisch reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="7d00a-108">Drawing many instances of geometry with these techniques can dramatically reduce the amount of data sent to the renderer.</span></span>

-   [<span data-ttu-id="7d00a-109">Zeichnen der indizierten Geometrie</span><span class="sxs-lookup"><span data-stu-id="7d00a-109">Drawing Indexed Geometry</span></span>](#drawing-indexed-geometry)
    -   [<span data-ttu-id="7d00a-110">Vergleich der indizierten Geometrie Leistung</span><span class="sxs-lookup"><span data-stu-id="7d00a-110">Indexed Geometry Performance Comparison</span></span>](#indexed-geometry-performance-comparison)
-   [<span data-ttu-id="7d00a-111">Zeichnen von nicht indizierten Geometrie</span><span class="sxs-lookup"><span data-stu-id="7d00a-111">Drawing Non-Indexed Geometry</span></span>](#drawing-non-indexed-geometry)
    -   [<span data-ttu-id="7d00a-112">Vergleich der nicht indizierten Geometrie Leistung</span><span class="sxs-lookup"><span data-stu-id="7d00a-112">Non-Indexed Geometry Performance Comparison</span></span>](#non-indexed-geometry-performance-comparison)
-   [<span data-ttu-id="7d00a-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7d00a-113">Related topics</span></span>](#related-topics)

## <a name="drawing-indexed-geometry"></a><span data-ttu-id="7d00a-114">Zeichnen der indizierten Geometrie</span><span class="sxs-lookup"><span data-stu-id="7d00a-114">Drawing Indexed Geometry</span></span>

<span data-ttu-id="7d00a-115">Der Vertex-Puffer enthält pro-Vertex-Daten, die durch eine Scheitelpunkt Deklaration definiert werden.</span><span class="sxs-lookup"><span data-stu-id="7d00a-115">The vertex buffer contains per-vertex data that is defined by a vertex declaration.</span></span> <span data-ttu-id="7d00a-116">Angenommen, ein Teil eines Scheitel Punkts enthält Geometry-Daten, und ein Teil jedes Scheitel Punkts enthält Objektinstanzdaten, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7d00a-116">Suppose that part of each vertex contains geometry data, and part of each vertex contains per-object instance data, as shown in the following diagram.</span></span>

![Diagramm eines Scheitelpunkt Puffers für die indizierte Geometrie](images/drawingmultipleinstances.png)

<span data-ttu-id="7d00a-118">Diese Technik erfordert ein Gerät, das das 3 \_ 0-Vertex-Shader-Modell unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7d00a-118">This technique requires a device that supports the 3\_0 vertex shader model.</span></span> <span data-ttu-id="7d00a-119">Diese Methode funktioniert mit jedem programmierbaren Shader, aber nicht mit der Fixed-Funktions Pipeline.</span><span class="sxs-lookup"><span data-stu-id="7d00a-119">This technique works with any programmable shader but not with the fixed function pipeline.</span></span>

<span data-ttu-id="7d00a-120">Für die oben gezeigten Scheitelpunkt Puffer sind hier die entsprechenden Vertex-Puffer Deklarationen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="7d00a-120">For the vertex buffers shown above, here are the corresponding vertex buffer declarations:</span></span>


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



<span data-ttu-id="7d00a-121">Diese Deklarationen definieren zwei Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="7d00a-121">These declarations define two vertex buffers.</span></span> <span data-ttu-id="7d00a-122">Die erste Deklaration (für Stream 0, angegeben durch die Nullen in Spalte 1) definiert die Geometry-Daten, die aus folgenden Elementen bestehen: Position, normal, Tangens, Binormal und Texturkoordinaten Daten.</span><span class="sxs-lookup"><span data-stu-id="7d00a-122">The first declaration (for stream 0, indicated by the zeros in column 1) defines the geometry data which consists of: position, normal, tangent, binormal, and texture coordinate data.</span></span>

<span data-ttu-id="7d00a-123">Die zweite Deklaration (für Stream 1, die durch die in Spalte 1 angegeben ist) definiert die Instanzdaten pro Objekt.</span><span class="sxs-lookup"><span data-stu-id="7d00a-123">The second declaration (for stream 1, indicated by the ones in column 1) defines the per-object instance data.</span></span> <span data-ttu-id="7d00a-124">Jede Instanz wird von Gleit Komma Zahlen der 4 4-Komponente und einer Farbe mit vier Komponenten definiert.</span><span class="sxs-lookup"><span data-stu-id="7d00a-124">Each instance is defined by four four-component floating point numbers, and a four-component color.</span></span> <span data-ttu-id="7d00a-125">Die ersten vier Werte können verwendet werden, um eine 4 x 4-Matrix zu initialisieren, was bedeutet, dass diese Daten jede Instanz der Geometrie eindeutig anpassen, positionieren und drehen.</span><span class="sxs-lookup"><span data-stu-id="7d00a-125">The first four values could be used to initialize a 4x4 matrix, which means that this data will uniquely size, position, and rotate each instance of the geometry.</span></span> <span data-ttu-id="7d00a-126">Die ersten vier Komponenten verwenden eine Texturkoordinaten Semantik, die in diesem Fall "Dies ist eine allgemeine vier-Komponenten-Zahl" bedeutet.</span><span class="sxs-lookup"><span data-stu-id="7d00a-126">The first four components use a texture coordinate semantic which, in this case, means "this is a general four-component number."</span></span> <span data-ttu-id="7d00a-127">Wenn Sie in einer Scheitelpunkt Deklaration beliebige Daten verwenden, verwenden Sie eine Texturkoordinaten Semantik, um Sie zu markieren.</span><span class="sxs-lookup"><span data-stu-id="7d00a-127">When you use arbitrary data in a vertex declaration, use a texture coordinate semantic to mark it.</span></span> <span data-ttu-id="7d00a-128">Das letzte Element im Stream wird für Farbdaten verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d00a-128">The last element in the stream is used for color data.</span></span> <span data-ttu-id="7d00a-129">Dies kann im Vertex-Shader angewendet werden, um jeder Instanz eine eindeutige Farbe zu geben.</span><span class="sxs-lookup"><span data-stu-id="7d00a-129">This could be applied in the vertex shader to give each instance a unique color.</span></span>

<span data-ttu-id="7d00a-130">Vor dem Rendering müssen Sie [**setstreamsourcefreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) aufrufen, um die Vertex-Puffer Datenströme an das Gerät zu binden.</span><span class="sxs-lookup"><span data-stu-id="7d00a-130">Before rendering, you need to call [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) to bind the vertex buffer streams to the device.</span></span> <span data-ttu-id="7d00a-131">Es folgt ein Beispiel, das beide Scheitel Punkte bindet:</span><span class="sxs-lookup"><span data-stu-id="7d00a-131">Here is an example that binds both vertex buffers:</span></span>


```
// Set up the geometry data stream
pd3dDevice->SetStreamSourceFreq(0,
    (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
    D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1,
    (D3DSTREAMSOURCE_INSTANCEDATA | 1));
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
    D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



<span data-ttu-id="7d00a-132">[**Setstreamsourcefreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) verwendet [D3DSTREAMSOURCE \_ indexeddata](other-direct3d-constants.md) , um die indizierten Geometriedaten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7d00a-132">[**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) uses [D3DSTREAMSOURCE\_INDEXEDDATA](other-direct3d-constants.md) to identify the indexed geometry data.</span></span> <span data-ttu-id="7d00a-133">In diesem Fall enthält Stream 0 die indizierten Daten, die die Objekt Geometrie beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7d00a-133">In this case, stream 0 contains the indexed data that describes the object geometry.</span></span> <span data-ttu-id="7d00a-134">Dieser Wert wird logisch mit der Anzahl der zu zeichnenden Instanzen der Geometrie kombiniert.</span><span class="sxs-lookup"><span data-stu-id="7d00a-134">This value is logically combined with the number of instances of the geometry to draw.</span></span>

<span data-ttu-id="7d00a-135">Beachten Sie, dass D3DSTREAMSOURCE \_ indexeddata und die Anzahl der zu zeichnenden Instanzen immer im Stream NULL festgelegt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="7d00a-135">Note that D3DSTREAMSOURCE\_INDEXEDDATA and the number of instances to draw must always be set in stream zero.</span></span>

<span data-ttu-id="7d00a-136">Im zweiten Befehl verwendet [**setstreamsourcefreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) [D3DSTREAMSOURCE \_ InstanceData](other-direct3d-constants.md) , um den Stream zu identifizieren, der die Instanzdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="7d00a-136">In the second call, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) uses [D3DSTREAMSOURCE\_INSTANCEDATA](other-direct3d-constants.md) to identify the stream containing the instance data.</span></span> <span data-ttu-id="7d00a-137">Dieser Wert wird logisch mit 1 kombiniert, da jeder Scheitelpunkt einen Satz von Instanzdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="7d00a-137">This value is logically combined with 1 since each vertex contains one set of instance data.</span></span>

<span data-ttu-id="7d00a-138">Mit den letzten zwei Aufrufen von [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) werden die Vertex-Puffer Zeiger an das Gerät gebunden.</span><span class="sxs-lookup"><span data-stu-id="7d00a-138">The last two calls to [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) bind the vertex buffer pointers to the device.</span></span>

<span data-ttu-id="7d00a-139">Wenn Sie das Rendering der Instanzdaten abgeschlossen haben, stellen Sie sicher, dass die vertexstreamfrequenz auf den Standardzustand zurückgesetzt wird (der keine Instanziierung verwendet).</span><span class="sxs-lookup"><span data-stu-id="7d00a-139">When you are finished rendering the instance data, be sure to reset the vertex stream frequency back to its default state (which does not use instancing).</span></span> <span data-ttu-id="7d00a-140">Da in diesem Beispiel zwei Streams verwendet werden, legen Sie beide Streams wie unten dargestellt fest:</span><span class="sxs-lookup"><span data-stu-id="7d00a-140">Because this example used two streams, set both streams as shown below:</span></span>


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="indexed-geometry-performance-comparison"></a><span data-ttu-id="7d00a-141">Vergleich der indizierten Geometrie Leistung</span><span class="sxs-lookup"><span data-stu-id="7d00a-141">Indexed Geometry Performance Comparison</span></span>

<span data-ttu-id="7d00a-142">Es ist zwar nicht möglich, eine einzelne Schlussfolgerung zu treffen, wie viel diese Technik die Renderingzeit in jeder Anwendung reduzieren könnte, aber berücksichtigen Sie den Unterschied in der Menge der Daten, die in die Laufzeit gestreamt werden, sowie die Anzahl der Zustandsänderungen, die bei Verwendung der instanziierungsmethode reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="7d00a-142">While it is not possible to make a single conclusion about how much this technique could reduce the render time in every application, consider the difference in the amount of data streamed into the runtime and the number of state changes that will be reduced if you use the instancing technique.</span></span> <span data-ttu-id="7d00a-143">Diese Rendering-Sequenz nutzt das Zeichnen mehrerer Instanzen derselben Geometrie:</span><span class="sxs-lookup"><span data-stu-id="7d00a-143">This render sequence takes advantage of drawing multiple instances of the same geometry:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set up the geometry data stream
    pd3dDevice->SetStreamSourceFreq(0,
                (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1,
                (D3DSTREAMSOURCE_INSTANCEDATA | 1));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="7d00a-144">Beachten Sie, dass die Renderschleife einmal aufgerufen wird, die Geometry-Daten einmal gestreamt werden und n Instanzen einmal gestreamt werden.</span><span class="sxs-lookup"><span data-stu-id="7d00a-144">Notice that the render loop is called once, the geometry data is streamed once, and n instances are streamed once.</span></span> <span data-ttu-id="7d00a-145">Diese nächste Rendering-Sequenz ist identisch mit der Funktionalität, aber Sie nutzt nicht die Instanziierung:</span><span class="sxs-lookup"><span data-stu-id="7d00a-145">This next render sequence is identical in functionality, but does not take advantage of instancing:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));


        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }                             
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="7d00a-146">Beachten Sie, dass die gesamte Renderschleife durch eine zweite Schleife umschließt, um jedes Objekt zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="7d00a-146">Notice that the entire render loop is wrapped by a second loop to draw each object.</span></span> <span data-ttu-id="7d00a-147">Nun werden die Geometry-Daten in den Renderer n-Mal (anstatt einmal) gestreamt, und alle Pipeline Zustände können auch redundant für jedes gezeichnete Objekt festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7d00a-147">Now the geometry data is streamed into the renderer n times (instead of once) and any pipeline states may also be set redundantly for each object drawn.</span></span> <span data-ttu-id="7d00a-148">Diese Rendering-Sequenz ist sehr wahrscheinlich bedeutend langsamer.</span><span class="sxs-lookup"><span data-stu-id="7d00a-148">This render sequence is very likely to be significantly slower.</span></span> <span data-ttu-id="7d00a-149">Beachten Sie auch, dass sich die Parameter für [**drawindexedprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) nicht zwischen den beiden Rendering-Schleifen geändert haben.</span><span class="sxs-lookup"><span data-stu-id="7d00a-149">Notice also that the parameters to [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) have not changed between the two render loops.</span></span>

## <a name="drawing-non-indexed-geometry"></a><span data-ttu-id="7d00a-150">Zeichnen von nicht indizierten Geometrie</span><span class="sxs-lookup"><span data-stu-id="7d00a-150">Drawing Non-Indexed Geometry</span></span>

<span data-ttu-id="7d00a-151">Beim [Zeichnen indizierter Geometrie](#drawing-indexed-geometry)wurden Vertex-Puffer so konfiguriert, dass mehrere Instanzen der indizierten Geometrie mit größerer Effizienz gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="7d00a-151">In [Drawing Indexed Geometry](#drawing-indexed-geometry), vertex buffers were configured to draw multiple instances of indexed geometry with greater efficiency.</span></span> <span data-ttu-id="7d00a-152">Sie können auch [**setstreamsourcefreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) verwenden, um eine nicht indizierte Geometrie zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="7d00a-152">You can also use [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) to draw non-indexed geometry.</span></span> <span data-ttu-id="7d00a-153">Hierfür ist ein anderes Vertex-Puffer Layout erforderlich, das über unterschiedliche Einschränkungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="7d00a-153">This requires a different vertex buffer layout and has different constraints.</span></span> <span data-ttu-id="7d00a-154">Um die nicht indizierte Geometrie zu zeichnen, bereiten Sie die Scheitelpunkt Puffer wie das folgende Diagramm vor.</span><span class="sxs-lookup"><span data-stu-id="7d00a-154">To draw non-indexed geometry, prepare your vertex buffers like the following diagram.</span></span>

![Diagramm eines Scheitelpunkt Puffers für nicht indizierte Geometrie](images/olderstyleinstancing.png)

<span data-ttu-id="7d00a-156">Diese Technik wird von der Hardwarebeschleunigung auf keinem Gerät unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7d00a-156">This technique is not supported by hardware acceleration on any device.</span></span> <span data-ttu-id="7d00a-157">Sie wird nur von der Verarbeitung von Software Scheitel Punkten unterstützt und funktioniert nur mit [vs \_ 3 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md) -Shadern.</span><span class="sxs-lookup"><span data-stu-id="7d00a-157">It is only supported by software vertex processing and will work only with [vs\_3\_0](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md) shaders.</span></span>

<span data-ttu-id="7d00a-158">Da diese Technik mit nicht indizierter Geometrie funktioniert, gibt es keinen Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="7d00a-158">Because this technique works with non-indexed geometry, there is no index buffer.</span></span> <span data-ttu-id="7d00a-159">Wie das Diagramm zeigt, enthält der Vertex-Puffer, der die Geometrie enthält, n Kopien der Geometriedaten.</span><span class="sxs-lookup"><span data-stu-id="7d00a-159">As the diagram shows, the vertex buffer that contains geometry contains n copies of the geometry data.</span></span> <span data-ttu-id="7d00a-160">Für jede Instanz, die gezeichnet wird, werden die Geometriedaten aus dem ersten Vertex-Puffer gelesen, und die Instanzdaten werden aus dem zweiten Vertex-Puffer gelesen.</span><span class="sxs-lookup"><span data-stu-id="7d00a-160">For each instance drawn, the geometry data is read from the first vertex buffer and the instance data is read from the second vertex buffer.</span></span>

<span data-ttu-id="7d00a-161">Im folgenden sind die entsprechenden Vertex-Puffer Deklarationen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="7d00a-161">Here are the corresponding vertex buffer declarations:</span></span>


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



<span data-ttu-id="7d00a-162">Diese Deklarationen sind identisch mit den Deklarationen, die im Beispiel für indizierte Geometrie vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="7d00a-162">These declarations are identical to the declarations made in the indexed geometry example.</span></span> <span data-ttu-id="7d00a-163">Die erste Deklaration (für Stream 0) definiert die Geometry-Daten, und die zweite Deklaration (für Stream 1) definiert die Instanzdaten pro Objekt.</span><span class="sxs-lookup"><span data-stu-id="7d00a-163">Once again, the first declaration (for stream 0) defines the geometry data and the second declaration (for stream 1) defines the per-object instance data.</span></span> <span data-ttu-id="7d00a-164">Wenn Sie den ersten Vertex-Puffer erstellen, achten Sie darauf, dass Sie ihn mit der Anzahl von Instanzen der Geometry-Daten laden, die Sie zeichnen werden.</span><span class="sxs-lookup"><span data-stu-id="7d00a-164">When you create the first vertex buffer, be sure to load it with the number of instances of the geometry data that you will be drawing.</span></span>

<span data-ttu-id="7d00a-165">Vor dem Rendering müssen Sie den unter Teiler einrichten, der der Laufzeit mitteilt, wie der erste Vertex-Puffer in n Instanzen aufgeteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d00a-165">Before rendering, you need to set up the divider which tells the runtime how to divide up the first vertex buffer into n instances.</span></span> <span data-ttu-id="7d00a-166">Legen Sie dann den unter Teiler mithilfe von [**setstreamsourcefreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) wie folgt fest:</span><span class="sxs-lookup"><span data-stu-id="7d00a-166">Then set the divider using [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) like this:</span></span>


```
// Set the divider
pd3dDevice->SetStreamSourceFreq(0, 1);
// Bind the stream to the vertex buffer
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
        D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance);
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
        D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



<span data-ttu-id="7d00a-167">Der erste Aufrufen von [**setstreamsourcefreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) besagt, dass Stream 0 n Instanzen von m Scheitel Punkten enthält.</span><span class="sxs-lookup"><span data-stu-id="7d00a-167">The first call to [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) says that stream 0 contains n instances of m vertices.</span></span> <span data-ttu-id="7d00a-168">[**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) bindet dann Stream 0 an den Geometrie Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="7d00a-168">[**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) then binds stream 0 to the geometry vertex buffer.</span></span>

<span data-ttu-id="7d00a-169">Im zweiten-Befehl identifiziert [**setstreamsourcefreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) Stream 1 als Quelle der Instanzdaten.</span><span class="sxs-lookup"><span data-stu-id="7d00a-169">In the second call, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) identifies stream 1 as the source of the instance data.</span></span> <span data-ttu-id="7d00a-170">Der zweite Parameter ist die Anzahl der Vertices in jedem Objekt (m).</span><span class="sxs-lookup"><span data-stu-id="7d00a-170">The second parameter is the number of vertices in each object (m).</span></span> <span data-ttu-id="7d00a-171">Beachten Sie, dass der instanzdatenstream immer als zweiter Stream deklariert werden muss.</span><span class="sxs-lookup"><span data-stu-id="7d00a-171">Remember that the instance data stream must always be declared as the second stream.</span></span> <span data-ttu-id="7d00a-172">[**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) bindet dann Stream 1 an den Vertex-Puffer, der die Instanzdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="7d00a-172">[**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) then binds stream 1 to the vertex buffer that contains the instance data.</span></span>

<span data-ttu-id="7d00a-173">Wenn Sie mit dem Rendern der Instanzdaten fertig sind, stellen Sie sicher, dass die vertexstreamfrequenz auf ihren Standardzustand zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="7d00a-173">When you are finished rendering the instance data, be sure to reset the vertex stream frequency back to its default state.</span></span> <span data-ttu-id="7d00a-174">Da in diesem Beispiel zwei Streams verwendet werden, legen Sie beide Streams wie unten dargestellt fest:</span><span class="sxs-lookup"><span data-stu-id="7d00a-174">Because this example used two streams, set both streams as shown below:</span></span>


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="non-indexed-geometry-performance-comparison"></a><span data-ttu-id="7d00a-175">Vergleich der nicht indizierten Geometrie Leistung</span><span class="sxs-lookup"><span data-stu-id="7d00a-175">Non-Indexed Geometry Performance Comparison</span></span>

<span data-ttu-id="7d00a-176">Der Hauptvorteil dieses instanziierungsstils besteht darin, dass er für nicht indizierte Geometrie verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7d00a-176">The major advantage of this instancing style is that it can be used on non-indexed geometry.</span></span> <span data-ttu-id="7d00a-177">Es ist zwar nicht möglich, eine einzelne Schlussfolgerung zu treffen, wie viel diese Technik die Renderingzeit in jeder Anwendung reduzieren könnte, aber berücksichtigen Sie den Unterschied in der Menge der Daten, die in die Laufzeit gestreamt werden, sowie die Anzahl der Zustandsänderungen, die für die folgende rendersequenz reduziert werden:</span><span class="sxs-lookup"><span data-stu-id="7d00a-177">While it is not possible to make a single conclusion about how much this technique could reduce the render time in every application, consider the difference in the amount of data streamed into the runtime, and the number of state changes that will be reduced for the following render sequence:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set the divider
    pd3dDevice->SetStreamSourceFreq(0, 1);
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="7d00a-178">Beachten Sie, dass die Renderschleife einmal aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7d00a-178">Notice that the render loop is called once.</span></span> <span data-ttu-id="7d00a-179">Die Geometry-Daten werden einmal gestreamt, obwohl n Instanzen der Geometrie vorhanden sind, die gestreamt werden.</span><span class="sxs-lookup"><span data-stu-id="7d00a-179">The geometry data is streamed once although there are n instances of the geometry being streamed.</span></span> <span data-ttu-id="7d00a-180">Die Daten aus dem Vertex-instanzpuffer werden einmal gestreamt.</span><span class="sxs-lookup"><span data-stu-id="7d00a-180">The data from the instance vertex buffer is streamed once.</span></span> <span data-ttu-id="7d00a-181">Diese nächste Rendering-Sequenz ist identisch mit der Funktionalität, aber Sie nutzt nicht die Instanziierung:</span><span class="sxs-lookup"><span data-stu-id="7d00a-181">This next render sequence is identical in functionality, but does not take advantage of instancing:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="7d00a-182">Ohne Instanziierung muss die Renderschleife durch eine zweite Schleife umschließt werden, um jedes Objekt zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="7d00a-182">Without instancing, the render loop needs to be wrapped by a second loop to draw each object.</span></span> <span data-ttu-id="7d00a-183">Durch das Eliminieren der zweiten Renderschleife sollten Sie eine bessere Leistung erwarten, da weniger renderstatusänderungen innerhalb der Schleife aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7d00a-183">By eliminating the second render loop, you should expect better performance due to fewer render state changes that are called inside the loop.</span></span>

<span data-ttu-id="7d00a-184">Insgesamt empfiehlt es sich zu erwarten, dass die indizierte Technik ([Zeichnen der indizierten Geometrie](#drawing-indexed-geometry)) eine bessere Leistung als die nicht indizierte Technik ([Zeichnen nicht indizierter Geometrie](#drawing-non-indexed-geometry)) erwartet, da die indizierte Technik nur eine Kopie der Geometriedaten streamt.</span><span class="sxs-lookup"><span data-stu-id="7d00a-184">Overall, it is reasonable to expect the indexed technique ([Drawing Indexed Geometry](#drawing-indexed-geometry)) to perform better than the non-indexed technique ([Drawing Non-Indexed Geometry](#drawing-non-indexed-geometry)) because the indexed technique only streams one copy of the geometry data.</span></span> <span data-ttu-id="7d00a-185">Beachten Sie, dass die Parameter für [**drawindexedprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) für eine der Rendering-Sequenzen nicht geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="7d00a-185">Notice that the parameters to [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) have not changed for any of the render sequences.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d00a-186">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7d00a-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d00a-187">Erweiterte Themen</span><span class="sxs-lookup"><span data-stu-id="7d00a-187">Advanced Topics</span></span>](advanced-topics.md)
</dt> <dt>

<span data-ttu-id="7d00a-188">[Instanziierungsbeispiel](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="7d00a-188">[Instancing Sample](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
