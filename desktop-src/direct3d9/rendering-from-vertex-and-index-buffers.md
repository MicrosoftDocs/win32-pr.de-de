---
description: Indizierte und nicht indizierte Zeichnungs Methoden werden von Direct3D unterstützt.
ms.assetid: 9b94ab86-2a6a-4abd-ab56-95315f473226
title: Rendering aus Scheitelpunkt-und Index Puffer (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc42da3f25787d42b0bdccdd808013f51bfa3e4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860088"
---
# <a name="rendering-from-vertex-and-index-buffers-direct3d-9"></a><span data-ttu-id="3a06d-103">Rendering aus Scheitelpunkt-und Index Puffer (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3a06d-103">Rendering from Vertex and Index Buffers (Direct3D 9)</span></span>

<span data-ttu-id="3a06d-104">Indizierte und nicht indizierte Zeichnungs Methoden werden von Direct3D unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3a06d-104">Both indexed and nonindexed drawing methods are supported by Direct3D.</span></span> <span data-ttu-id="3a06d-105">Die indizierten Methoden verwenden einen einzelnen Satz von Indizes für alle Scheitelpunkt Komponenten.</span><span class="sxs-lookup"><span data-stu-id="3a06d-105">The indexed methods use a single set of indices for all vertex components.</span></span> <span data-ttu-id="3a06d-106">Vertex-Daten werden in Scheitelpunkt Puffern gespeichert, und Indexdaten werden in Index Puffern gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3a06d-106">Vertex data is stored in vertex buffers, and index data is stored in index buffers.</span></span> <span data-ttu-id="3a06d-107">Nachstehend sind einige gängige Szenarien für das Zeichnen von primitiven mithilfe von Scheitel Punkten und Index Puffern aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a06d-107">Listed below are a few common scenarios for drawing primitives using vertex and index buffers.</span></span>

<span data-ttu-id="3a06d-108">Diese Beispiele vergleichen die Verwendung von [**IDirect3DDevice9::D rawprimitiv**](/windows/desktop/api) und [**IDirect3DDevice9::D rawindexedprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) .</span><span class="sxs-lookup"><span data-stu-id="3a06d-108">These examples compare the use of [**IDirect3DDevice9::DrawPrimitive**](/windows/desktop/api) and [**IDirect3DDevice9::DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)</span></span>

## <a name="scenario-1-drawing-two-triangles-without-indexing"></a><span data-ttu-id="3a06d-109">Szenario 1: Zeichnen von zwei Dreiecken ohne Indizierung</span><span class="sxs-lookup"><span data-stu-id="3a06d-109">Scenario 1: Drawing Two Triangles without Indexing</span></span>

<span data-ttu-id="3a06d-110">Nehmen wir an, Sie möchten das Vierfache zeichnen, das in der folgenden Abbildung gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3a06d-110">Let's say you want to draw the quad that is shown in the following illustration.</span></span>

![Abbildung eines Quadrats, das aus zwei Dreiecken besteht](images/dip-fig1.png)

<span data-ttu-id="3a06d-112">Wenn Sie den primitiven Objekttyp für die Dreiecks Liste zum Rendern der beiden Dreiecke verwenden, wird jedes Dreieck als 3 einzelne Scheitel Punkte gespeichert, was in der folgenden Abbildung zu einem ähnlichen Scheitelpunkt Puffer führt.</span><span class="sxs-lookup"><span data-stu-id="3a06d-112">If you use the Triangle List primitive type to render the two triangles, each triangle will be stored as 3 individual vertices, resulting in a similar vertex buffer to the following illustration.</span></span>

![Diagramm eines Scheitelpunkt Puffers, der drei Vertices für zwei Dreiecke definiert](images/dip-fig2.png)

<span data-ttu-id="3a06d-114">Der Zeichnungs Befehl ist sehr unkompliziert. Zeichnen Sie an Position 0 innerhalb des Vertex-Puffers zwei Dreiecke.</span><span class="sxs-lookup"><span data-stu-id="3a06d-114">The drawing call is very straightforward; starting at location 0 within the vertex buffer, draw two triangles.</span></span> <span data-ttu-id="3a06d-115">Wenn das cullingfunktionsgruppe aktiviert ist, ist die Reihenfolge der Scheitel Punkte wichtig.</span><span class="sxs-lookup"><span data-stu-id="3a06d-115">If culling is enabled, the order of the vertices will be important.</span></span> <span data-ttu-id="3a06d-116">In diesem Beispiel wird angenommen, dass der Standardzustand gegen den Uhrzeigersinn besteht, sodass sichtbare Dreiecke im Uhrzeigersinn gezeichnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="3a06d-116">This example assumes the default counter-clockwise culling state, so visible triangles must be drawn in clockwise order.</span></span> <span data-ttu-id="3a06d-117">Der primitive Typ der Dreiecks Liste liest einfach drei Scheitel Punkte in linearer Reihenfolge aus dem Puffer für jedes Dreieck. daher zeichnet dieser Befehl Dreiecke (0, 1, 2) und (3, 4, 5):</span><span class="sxs-lookup"><span data-stu-id="3a06d-117">The Triangle List primitive type simply reads three vertices in linear order from the buffer for each triangle, so this call will draw triangles (0, 1, 2) and (3, 4, 5):</span></span>


```
DrawPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
               0,                  // StartVertex
               2 );                // PrimitiveCount
```



## <a name="scenario-2-drawing-two-triangles-with-indexing"></a><span data-ttu-id="3a06d-118">Szenario 2: Zeichnen von zwei Dreiecken mit Indizierung</span><span class="sxs-lookup"><span data-stu-id="3a06d-118">Scenario 2: Drawing Two Triangles with Indexing</span></span>

<span data-ttu-id="3a06d-119">Wie Sie bemerken werden, enthält der Vertex-Puffer doppelte Daten an den Standorten 0 und 4, 2 und 5.</span><span class="sxs-lookup"><span data-stu-id="3a06d-119">As you'll notice, the vertex buffer contains duplicate data in locations 0 and 4, 2 and 5.</span></span> <span data-ttu-id="3a06d-120">Das ist sinnvoll, da die beiden Dreiecke zwei gängige Scheitel Punkte gemeinsam nutzen.</span><span class="sxs-lookup"><span data-stu-id="3a06d-120">That makes sense because the two triangles share two common vertices.</span></span> <span data-ttu-id="3a06d-121">Diese doppelten Daten sind verschwenderisch, und der Vertex-Puffer kann mithilfe eines Index Puffers komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="3a06d-121">This duplicate data is wasteful, and the vertex buffer can be compressed by using an index buffer.</span></span> <span data-ttu-id="3a06d-122">Ein kleinerer Scheitelpunkt Puffer reduziert die Menge der Vertex-Daten, die an den Grafikadapter gesendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="3a06d-122">A smaller vertex buffer reduces the amount of vertex data that has to be sent to the graphics adapter.</span></span> <span data-ttu-id="3a06d-123">Noch wichtiger ist, dass durch die Verwendung eines Index Puffers Scheitel Punkte in einem Scheitelpunkt Cache gespeichert werden können. Wenn das primitive, das gezeichnet wird, einen zuletzt verwendeten Scheitelpunkt enthält, kann dieser Scheitelpunkt aus dem Cache abgerufen werden, anstatt ihn aus dem Scheitelpunkt Puffer zu lesen. Dies führt zu einer großen Leistungssteigerung.</span><span class="sxs-lookup"><span data-stu-id="3a06d-123">Even more importantly, using an index buffer allows the adapter to store vertices in a vertex cache; if the primitive being drawn contains a recently-used vertex, that vertex can be fetched from the cache instead of reading it from the vertex buffer, which results in a big performance increase.</span></span>

<span data-ttu-id="3a06d-124">Ein Index Puffer ' Indexes ' in den Scheitelpunkt Puffer, sodass jeder eindeutige Scheitelpunkt nur einmal im Vertexpuffer gespeichert werden muss.</span><span class="sxs-lookup"><span data-stu-id="3a06d-124">An index buffer 'indexes' into the vertex buffer so each unique vertex needs to be stored only once in the vertex buffer.</span></span> <span data-ttu-id="3a06d-125">Das folgende Diagramm zeigt einen indizierten Ansatz für das frühere Zeichnungs Szenario.</span><span class="sxs-lookup"><span data-stu-id="3a06d-125">The following diagram shows an indexed approach to the earlier drawing scenario.</span></span>

![Diagramm eines Index Puffers für den früheren Vertex-Puffer](images/dip-fig3.png)

<span data-ttu-id="3a06d-127">Der Index Puffer speichert VB-Indexwerte, die auf einen bestimmten Scheitelpunkt innerhalb des Scheitelpunkt Puffers verweisen.</span><span class="sxs-lookup"><span data-stu-id="3a06d-127">The index buffer stores VB Index values, which reference a particular vertex within the vertex buffer.</span></span> <span data-ttu-id="3a06d-128">Ein Scheitelpunkt Puffer kann als ein Array von Scheitel Punkten betrachtet werden, sodass der VB-Index einfach der Index in den Scheitelpunkt Puffer für den Ziel Scheitelpunkt ist.</span><span class="sxs-lookup"><span data-stu-id="3a06d-128">A vertex buffer can be thought of as an array of vertices, so the VB Index is simply the index into the vertex buffer for the target vertex.</span></span> <span data-ttu-id="3a06d-129">Ebenso ist ein IB-Index ein Index im Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="3a06d-129">Similarly, an IB Index is an index into the index buffer.</span></span> <span data-ttu-id="3a06d-130">Dies kann sehr schnell sehr verwirrend sein, wenn Sie nicht vorsichtig sind. Stellen Sie also sicher, dass Sie das verwendete Vokabular nicht kennen: VB Index Values Index in den Vertex-Puffer, Indexwerte Index von IB in den Index Puffer, und der Index Puffer selbst speichert VB-Indexwerte.</span><span class="sxs-lookup"><span data-stu-id="3a06d-130">This can get very confusing very quickly if you're not careful, so make sure you're clear on the vocabulary being used: VB Index values index into the vertex buffer, IB Index values index into the index buffer, and the index buffer itself stores VB Index values.</span></span>

<span data-ttu-id="3a06d-131">Der Zeichnungs Befehl wird unten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3a06d-131">The drawing call is shown below.</span></span> <span data-ttu-id="3a06d-132">Die Bedeutungen aller Argumente werden für das nächste Zeichnungs Szenario in der Länge erörtert. Beachten Sie vorerst, dass dieser-Befehl Direct3D erneut anweist, eine Dreiecks Liste mit zwei Dreiecken zu rendernden, beginnend an Position 0 innerhalb des Index Puffers.</span><span class="sxs-lookup"><span data-stu-id="3a06d-132">The meanings of all the arguments are discussed at length for the next drawing scenario; for now, just note that this call is again instructing Direct3D to render a triangle list containing two triangles, starting at location 0 within the index buffer.</span></span> <span data-ttu-id="3a06d-133">Dieser Befehl zeichnet dieselben zwei Dreiecke in genau derselben Reihenfolge wie zuvor, um eine angemessene Ausrichtung im Uhrzeigersinn sicherzustellen:</span><span class="sxs-lookup"><span data-stu-id="3a06d-133">This call will draw the same two triangles in the exact same order as before, ensuring a proper clockwise orientation:</span></span>


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    0,                  // StartIndex
                    2 );                // PrimitiveCount
```



## <a name="scenario-3-drawing-one-triangle-with-indexing"></a><span data-ttu-id="3a06d-134">Szenario 3: Zeichnen eines Dreiecks mit Indizierung</span><span class="sxs-lookup"><span data-stu-id="3a06d-134">Scenario 3: Drawing One Triangle with Indexing</span></span>

<span data-ttu-id="3a06d-135">Legen Sie jetzt fest, dass Sie nur das zweite Dreieck zeichnen möchten, aber Sie möchten denselben Vertex-Puffer und Index Puffer verwenden, die beim Zeichnen des gesamten Quad verwendet werden, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3a06d-135">Pretend now that you want to draw only the second triangle, but you want to use the same vertex buffer and index buffer that are used when drawing the entire quad, as shown in the following diagram.</span></span>

![Diagramm des Index Puffers und des Scheitelpunkt Puffers für das zweite Dreieck](images/dip-fig4.png)

<span data-ttu-id="3a06d-137">Für diesen Zeichnungs Befehl ist der erste verwendete IB-Index 3. Dieser Wert wird als startIndex bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3a06d-137">For this drawing call, the first IB Index used is 3; this value is called the StartIndex.</span></span> <span data-ttu-id="3a06d-138">Der niedrigste verwendete VB-Index ist 0 (null). Dieser Wert wird als minindex bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3a06d-138">The lowest VB Index used is 0; this value is called the MinIndex.</span></span> <span data-ttu-id="3a06d-139">Obwohl nur drei Scheitel Punkte zum Zeichnen des Dreiecks erforderlich sind, werden diese drei Scheitel Punkte über vier angrenzende Positionen im Vertexpuffer verteilt. die Anzahl der Speicherorte innerhalb des zusammenhängenden Blocks des Vertex-Pufferspeichers, der für den Zeichnungs Aufruf benötigt wird, wird als numvertices bezeichnet und in diesem Aufruf auf 4 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3a06d-139">Even though only three vertices are required to draw the triangle, those three vertices are spread across four adjacent locations in the vertex buffer; the number of locations within the contiguous block of vertex buffer memory required for the drawing call is called NumVertices, and will be set to 4 in this call.</span></span> <span data-ttu-id="3a06d-140">Die Werte "minindex" und "numvertices" sind wirklich lediglich Hinweise, um den Speicherzugriff während der Verarbeitung von Software Scheitel Punkten zu vereinfachen Direct3D und könnten einfach so festgelegt werden, dass Sie den gesamten Vertex-Puffer zum Preis der Leistung einschließen.</span><span class="sxs-lookup"><span data-stu-id="3a06d-140">The MinIndex and NumVertices values are really just hints to help Direct3D optimize memory access during software vertex processing, and could simply be set to include the entire vertex buffer at the price of performance.</span></span>

<span data-ttu-id="3a06d-141">Dies ist der Zeichnungs Befehl für den Fall eines einzelnen Dreiecks. die Bedeutung des basevertexindex-Arguments wird im folgenden erläutert:</span><span class="sxs-lookup"><span data-stu-id="3a06d-141">Here is the drawing call for the single triangle case; the meaning of the BaseVertexIndex argument will be explained next:</span></span>


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="scenario-4-drawing-one-triangle-with-offset-indexing"></a><span data-ttu-id="3a06d-142">Szenario 4: Zeichnen eines Dreiecks mit Offset Indizierung</span><span class="sxs-lookup"><span data-stu-id="3a06d-142">Scenario 4: Drawing One Triangle with Offset Indexing</span></span>

<span data-ttu-id="3a06d-143">Basevertexindex ist ein Wert, der jedem VB-Index, der im Index Puffer gespeichert ist, tatsächlich hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="3a06d-143">BaseVertexIndex is a value that's effectively added to every VB Index stored in the index buffer.</span></span> <span data-ttu-id="3a06d-144">Wenn z. b. während des vorherigen Aufrufes den Wert 50 für basevertexindex angenommen hätte, wäre dies funktionell identisch mit der Verwendung des Index Puffers im folgenden Diagramm für die Dauer des DrawIndexedPrimitive-Aufrufes:</span><span class="sxs-lookup"><span data-stu-id="3a06d-144">For example, if we had passed in a value of 50 for BaseVertexIndex during the previous call, that would functionally be the same as using the index buffer in the following diagram for the duration of the DrawIndexedPrimitive call:</span></span>

![Diagramm eines Index Puffers mit dem Wert 50 für basevertexindex](images/dip-fig5.png)

<span data-ttu-id="3a06d-146">Dieser Wert wird nur selten auf einen anderen Wert als 0 festgelegt, kann jedoch nützlich sein, wenn Sie den Index Puffer vom Vertex-Puffer entkoppeln möchten: Wenn Sie den Index Puffer für ein bestimmtes Mesh ausfüllen, ist die Position des Netzes im Vertex-Puffer noch nicht bekannt, Sie können einfach festlegen, dass sich die Gitter Scheitel Punkte am Anfang des Vertexpuffers befinden. Wenn es an der Zeit ist, den zeichnen-Befehl zu erstellen, übergeben Sie einfach den eigentlichen Start Speicherort als basevertexindex.</span><span class="sxs-lookup"><span data-stu-id="3a06d-146">This value is rarely set to anything other than 0, but can be useful if you want to decouple the index buffer from the vertex buffer: If when filling in the index buffer for a particular mesh the location of the mesh within the vertex buffer isn't yet known, you can simply pretend the mesh vertices will be located at the start of the vertex buffer; when it comes time to make the draw call, simply pass the actual starting location as the BaseVertexIndex.</span></span>

<span data-ttu-id="3a06d-147">Diese Technik kann auch verwendet werden, wenn mehrere Instanzen eines Mesh mithilfe eines einzelnen Index Puffers gezeichnet werden. Wenn der Scheitelpunkt Puffer z. b. zwei Netzen mit identischer Zeichnungsreihenfolge, aber leicht unterschiedlichen Vertices (z. b. unterschiedliche diffuse Farben oder Texturkoordinaten) enthielt, können beide Netzen mithilfe verschiedener Werte für basevertexindex gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="3a06d-147">This technique can also be used when drawing multiple instances of a mesh using a single index buffer; for example, if the vertex buffer contained two meshes with identical draw order but slightly different vertices (perhaps different diffuse colors or texture coordinates), both meshes could be drawn by using different values for BaseVertexIndex.</span></span> <span data-ttu-id="3a06d-148">Wenn Sie dieses Konzept noch einen Schritt weiter gehen, können Sie einen Index Puffer verwenden, um mehrere Instanzen eines Mesh zu zeichnen, die jeweils in einem anderen Scheitelpunkt Puffer enthalten sind, indem Sie einfach einen Drilldown durchführen und den basevertexindex nach Bedarf anpassen.</span><span class="sxs-lookup"><span data-stu-id="3a06d-148">Taking this concept one step further, you could use one index buffer to draw multiple instances of a mesh, each contained in a different vertex buffer, simply by cycling which vertex buffer is active and adjusting the BaseVertexIndex as needed.</span></span> <span data-ttu-id="3a06d-149">Beachten Sie, dass der Wert basevertexindex auch automatisch dem minindex-Argument hinzugefügt wird, was sinnvoll ist, wenn Sie sehen, wie es verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="3a06d-149">Note that the BaseVertexIndex value is also automatically added to the MinIndex argument, which makes sense when you see how it's used:</span></span>

<span data-ttu-id="3a06d-150">Stellen Sie jetzt fest, dass wir wieder nur das zweite Dreieck des Quad mit dem gleichen Index Puffer wie zuvor zeichnen möchten. Es wird jedoch ein anderer Scheitelpunkt Puffer verwendet, in dem sich das Vierfache im VB-Index 50 befindet.</span><span class="sxs-lookup"><span data-stu-id="3a06d-150">Pretend now that we again want to draw only the second triangle of the quad using the same index buffer as before; however, a different vertex buffer is being used in which the quad is located at VB Index 50.</span></span> <span data-ttu-id="3a06d-151">Die relative Reihenfolge der vier Scheitel Punkte bleibt unverändert, nur die Anfangsposition im Scheitelpunkt Puffer unterscheidet sich.</span><span class="sxs-lookup"><span data-stu-id="3a06d-151">The relative order of the quad vertices remains unchanged, only the starting location within the vertex buffer is different.</span></span> <span data-ttu-id="3a06d-152">Der Index Puffer und der Vertex-Puffer würden wie im folgenden Diagramm aussehen.</span><span class="sxs-lookup"><span data-stu-id="3a06d-152">The index buffer and vertex buffer would look like the following diagram.</span></span>

![Diagramm des Index Puffers und des Scheitelpunkt Puffers mit einem VB-Index von 50](images/dip-fig6.png)

<span data-ttu-id="3a06d-154">Hier ist der geeignete Draw-Befehl. Beachten Sie, dass "basevertexindex" der einzige Wert ist, der sich seit dem vorherigen Szenario geändert hat:</span><span class="sxs-lookup"><span data-stu-id="3a06d-154">Here is the appropriate draw call; note that BaseVertexIndex is the only value which has changed from the previous scenario:</span></span>


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    50,                 // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="related-topics"></a><span data-ttu-id="3a06d-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3a06d-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a06d-156">Rendern von primitiven</span><span class="sxs-lookup"><span data-stu-id="3a06d-156">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 
