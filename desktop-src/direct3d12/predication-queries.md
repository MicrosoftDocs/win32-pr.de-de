---
title: Prädikationsabfragen
description: Das D3D12PredicationQueries-Beispiel veranschaulicht die Verschleierung von Okklusion mithilfe von DirectX 12-Abfrage Heaps und-Prädikaten. In der exemplarischen Vorgehensweise wird der zusätzliche Code beschrieben, der zum Erweitern des helloconstbuffer-Beispiels für die Behandlung von prädikationsabfragen
ms.assetid: F61817BB-45BC-4977-BE4A-EE0FDAFBCB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad14e55864ee8d568acc0c9eb46134834d27ff54
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548631"
---
# <a name="predication-queries"></a><span data-ttu-id="611e8-104">Prädikationsabfragen</span><span class="sxs-lookup"><span data-stu-id="611e8-104">Predication queries</span></span>

<span data-ttu-id="611e8-105">Das **D3D12PredicationQueries** -Beispiel veranschaulicht die Verschleierung von Okklusion mithilfe von DirectX 12-Abfrage Heaps und-Prädikaten.</span><span class="sxs-lookup"><span data-stu-id="611e8-105">The **D3D12PredicationQueries** sample demonstrates occlusion culling using DirectX 12 query heaps and predication.</span></span> <span data-ttu-id="611e8-106">In der exemplarischen Vorgehensweise wird der zusätzliche Code beschrieben, der zum Erweitern des **helloconstbuffer** -Beispiels für die Behandlung von prädikationsabfragen</span><span class="sxs-lookup"><span data-stu-id="611e8-106">The walkthrough describes the additional code needed to extend the **HelloConstBuffer** sample to handle predication queries.</span></span>

-   [<span data-ttu-id="611e8-107">Erstellen Sie einen tiefen Schablone-deskriptorheap und einen oksions Abfrage Heap.</span><span class="sxs-lookup"><span data-stu-id="611e8-107">Create a depth stencil descriptor heap and an occlusion query heap</span></span>](#create-a-depth-stencil-descriptor-heap-and-an-occlusion-query-heap)
-   [<span data-ttu-id="611e8-108">Alpha Blending aktivieren</span><span class="sxs-lookup"><span data-stu-id="611e8-108">Enable alpha blending</span></span>](#enable-alpha-blending)
-   [<span data-ttu-id="611e8-109">Farben und Tiefe Schreibvorgänge deaktivieren</span><span class="sxs-lookup"><span data-stu-id="611e8-109">Disable color and depth writes</span></span>](#disable-color-and-depth-writes)
-   [<span data-ttu-id="611e8-110">Erstellen eines Puffers zum Speichern der Abfrageergebnisse</span><span class="sxs-lookup"><span data-stu-id="611e8-110">Create a buffer to store the results of the query</span></span>](#create-a-buffer-to-store-the-results-of-the-query)
-   [<span data-ttu-id="611e8-111">Zeichnen der Quads und ausführen und Auflösen der Okklusions Abfrage</span><span class="sxs-lookup"><span data-stu-id="611e8-111">Draw the quads and perform and resolve the occlusion query</span></span>](#draw-the-quads-and-perform-and-resolve-the-occlusion-query)
-   [<span data-ttu-id="611e8-112">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="611e8-112">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="611e8-113">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="611e8-113">Related topics</span></span>](#related-topics)

## <a name="create-a-depth-stencil-descriptor-heap-and-an-occlusion-query-heap"></a><span data-ttu-id="611e8-114">Erstellen Sie einen tiefen Schablone-deskriptorheap und einen oksions Abfrage Heap.</span><span class="sxs-lookup"><span data-stu-id="611e8-114">Create a depth stencil descriptor heap and an occlusion query heap</span></span>

<span data-ttu-id="611e8-115">Erstellen Sie in der **loadpipeline** -Methode einen tiefen Schablone-deskriptorheap.</span><span class="sxs-lookup"><span data-stu-id="611e8-115">In the **LoadPipeline** method create a depth stencil descriptor heap.</span></span>

``` syntax
              // Describe and create a depth stencil view (DSV) descriptor heap.
              D3D12_DESCRIPTOR_HEAP_DESC dsvHeapDesc = {};
              dsvHeapDesc.NumDescriptors = 1;
              dsvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_DSV;
              dsvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
              ThrowIfFailed(m_device->CreateDescriptorHeap(&dsvHeapDesc, IID_PPV_ARGS(&m_dsvHeap)));
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="611e8-116">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="611e8-116">Call flow</span></span></th>
<th><span data-ttu-id="611e8-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="611e8-117">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="611e8-118"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc"><strong>D3D12_DESCRIPTOR_HEAP_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-118"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc"><strong>D3D12_DESCRIPTOR_HEAP_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="611e8-119"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type"><strong>D3D12_DESCRIPTOR_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-119"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type"><strong>D3D12_DESCRIPTOR_HEAP_TYPE</strong></a></span></span><br />
<span data-ttu-id="611e8-120">[<strong>D3D12_DESCRIPTOR_HEAP_FLAG</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_descriptor_heap_flags)</span><span class="sxs-lookup"><span data-stu-id="611e8-120">[<strong>D3D12_DESCRIPTOR_HEAP_FLAG</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="611e8-121"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap"><strong>"Kreatedescriptorheap"</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-121"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap"><strong>CreateDescriptorHeap</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="611e8-122">Erstellen Sie in der **loadassets** -Methode einen Heap für oksions Abfragen.</span><span class="sxs-lookup"><span data-stu-id="611e8-122">In the **LoadAssets** method create a heap for occlusion queries.</span></span>

``` syntax
     // Describe and create a heap for occlusion queries.
              D3D12_QUERY_HEAP_DESC queryHeapDesc = {};
              queryHeapDesc.Count = 1;
              queryHeapDesc.Type = D3D12_QUERY_HEAP_TYPE_OCCLUSION;
              ThrowIfFailed(m_device->CreateQueryHeap(&queryHeapDesc, IID_PPV_ARGS(&m_queryHeap)));
```



| <span data-ttu-id="611e8-123">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="611e8-123">Call flow</span></span>                                                 | <span data-ttu-id="611e8-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="611e8-124">Parameters</span></span>                                                |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="611e8-125">**D3D12 \_ Abfrage \_ Heap- \_ ABSC**</span><span class="sxs-lookup"><span data-stu-id="611e8-125">**D3D12\_QUERY\_HEAP\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc) | [<span data-ttu-id="611e8-126">**D3D12- \_ Abfrage \_ heaptyp \_**</span><span class="sxs-lookup"><span data-stu-id="611e8-126">**D3D12\_QUERY\_HEAP\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type) |
| [<span data-ttu-id="611e8-127">**"Kreatequeryheap"**</span><span class="sxs-lookup"><span data-stu-id="611e8-127">**CreateQueryHeap**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap)   |                                                           |



 

## <a name="enable-alpha-blending"></a><span data-ttu-id="611e8-128">Alpha Blending aktivieren</span><span class="sxs-lookup"><span data-stu-id="611e8-128">Enable alpha blending</span></span>

<span data-ttu-id="611e8-129">In diesem Beispiel werden zwei Quads gezeichnet und eine binäre Okklusions Abfrage veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="611e8-129">This sample draws two quads and illustrates a binary occlusion query.</span></span> <span data-ttu-id="611e8-130">Das Vierfache im Vordergrund wird auf dem Bildschirm animiert, und der im Hintergrund wird gelegentlich ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="611e8-130">The quad in front animates across the screen, and the one in back will occasionally be occluded.</span></span> <span data-ttu-id="611e8-131">In der **loadassets** -Methode ist Alpha Blending für dieses Beispiel aktiviert, sodass wir sehen können, zu welchem Punkt D3D das Vierfache im Hintergrund wieder gibt.</span><span class="sxs-lookup"><span data-stu-id="611e8-131">In the **LoadAssets** method, alpha blending is enabled for this sample so that we can see at what point D3D considers the quad in back occluded.</span></span>

``` syntax
     // Enable alpha blending so we can visualize the occlusion query results.
              CD3DX12_BLEND_DESC blendDesc(CD3DX12_DEFAULT);
              blendDesc.RenderTarget[0] =
              {
                     TRUE, FALSE,
                     D3D12_BLEND_SRC_ALPHA, D3D12_BLEND_INV_SRC_ALPHA, D3D12_BLEND_OP_ADD,
                     D3D12_BLEND_ONE, D3D12_BLEND_ZERO, D3D12_BLEND_OP_ADD,
                     D3D12_LOGIC_OP_NOOP,
                     D3D12_COLOR_WRITE_ENABLE_ALL,
              };
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="611e8-132">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="611e8-132">Call flow</span></span></th>
<th><span data-ttu-id="611e8-133">Parameter</span><span class="sxs-lookup"><span data-stu-id="611e8-133">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="611e8-134"><a href="cd3dx12-blend-desc.md"><strong>CD3DX12_BLEND_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-134"><a href="cd3dx12-blend-desc.md"><strong>CD3DX12_BLEND_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="611e8-135"><a href="cd3dx12-default.md"><strong>CD3DX12_DEFAULT</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-135"><a href="cd3dx12-default.md"><strong>CD3DX12_DEFAULT</strong></a></span></span><br />
<span data-ttu-id="611e8-136">[<strong>D3D12_BLEND</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_blend)</span><span class="sxs-lookup"><span data-stu-id="611e8-136">[<strong>D3D12_BLEND</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend)</span></span><br />
<span data-ttu-id="611e8-137">[<strong>D3D12_BLEND_OP</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_blend_op)</span><span class="sxs-lookup"><span data-stu-id="611e8-137">[<strong>D3D12_BLEND_OP</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend_op)</span></span><br />
<span data-ttu-id="611e8-138">[<strong>D3D12_LOGIC_OP</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_logic_op)</span><span class="sxs-lookup"><span data-stu-id="611e8-138">[<strong>D3D12_LOGIC_OP</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_logic_op)</span></span><br />
<span data-ttu-id="611e8-139">[<strong>D3D12_COLOR_WRITE_ENABLE</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_color_write_enable)</span><span class="sxs-lookup"><span data-stu-id="611e8-139">[<strong>D3D12_COLOR_WRITE_ENABLE</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_color_write_enable)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="disable-color-and-depth-writes"></a><span data-ttu-id="611e8-140">Farben und Tiefe Schreibvorgänge deaktivieren</span><span class="sxs-lookup"><span data-stu-id="611e8-140">Disable color and depth writes</span></span>

<span data-ttu-id="611e8-141">Die oksions Abfrage wird durch das Rendern eines Quad durchgeführt, das denselben Bereich abdeckt wie das Vierfache, dessen Sichtbarkeit getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="611e8-141">The occlusion query is performed by rendering a quad that covers the same area as the quad whose visibility we want to test.</span></span> <span data-ttu-id="611e8-142">In komplexeren Szenen wäre die Abfrage wahrscheinlich ein Begrenzungs Volume und kein einfaches Quad.</span><span class="sxs-lookup"><span data-stu-id="611e8-142">In more complex scenes, the query would likely be a bounding volume, rather than a simple quad.</span></span> <span data-ttu-id="611e8-143">In beiden Fällen wird ein neuer Pipeline Status erstellt, der das Schreiben in das Renderziel und den z-Puffer deaktiviert, sodass sich die Okklusions Abfrage selbst nicht auf die sichtbare Ausgabe des Renderings auswirkt.</span><span class="sxs-lookup"><span data-stu-id="611e8-143">In either case, a new pipeline state is created that disables writing to the render target and the z buffer so that the occlusion query itself does not affect the visible output of the rendering pass.</span></span>

<span data-ttu-id="611e8-144">Deaktivieren Sie in der **loadassets** -Methode Farb Schreibvorgänge und Tiefe Schreibvorgänge für den Zustand der oksion-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="611e8-144">In the **LoadAssets** method, disable color writes and depth writes for the occlusion query's state.</span></span>

``` syntax
 // Disable color writes and depth writes for the occlusion query's state.
              psoDesc.BlendState.RenderTarget[0].RenderTargetWriteMask = 0;
              psoDesc.DepthStencilState.DepthWriteMask = D3D12_DEPTH_WRITE_MASK_ZERO;

              ThrowIfFailed(m_device->CreateGraphicsPipelineState(&psoDesc, IID_PPV_ARGS(&m_queryState)));
```



| <span data-ttu-id="611e8-145">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="611e8-145">Call flow</span></span>                                                                            | <span data-ttu-id="611e8-146">Parameter</span><span class="sxs-lookup"><span data-stu-id="611e8-146">Parameters</span></span>                                                  |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="611e8-147">**D3D12- \_ Grafik \_ Pipeline \_ Status \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="611e8-147">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) | [<span data-ttu-id="611e8-148">**D3D12 \_ Tiefe \_ Schreib \_ Maske**</span><span class="sxs-lookup"><span data-stu-id="611e8-148">**D3D12\_DEPTH\_WRITE\_MASK**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) |
| [<span data-ttu-id="611e8-149">**"Kreategraphicspipelinestate"**</span><span class="sxs-lookup"><span data-stu-id="611e8-149">**CreateGraphicsPipelineState**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)      |                                                             |



 

## <a name="create-a-buffer-to-store-the-results-of-the-query"></a><span data-ttu-id="611e8-150">Erstellen eines Puffers zum Speichern der Abfrageergebnisse</span><span class="sxs-lookup"><span data-stu-id="611e8-150">Create a buffer to store the results of the query</span></span>

<span data-ttu-id="611e8-151">In der **loadassets** -Methode muss ein Puffer erstellt werden, um die Ergebnisse der Abfrage zu speichern.</span><span class="sxs-lookup"><span data-stu-id="611e8-151">In the **LoadAssets** method a buffer needs to be created to store the results of the query.</span></span> <span data-ttu-id="611e8-152">Jede Abfrage benötigt im GPU-Speicher 8 Bytes Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="611e8-152">Each query requires 8 bytes of space in GPU memory.</span></span> <span data-ttu-id="611e8-153">In diesem Beispiel wird nur eine Abfrage durchführen, und aus Gründen der Einfachheit und Lesbarkeit wird ein Puffer genau dieser Größe erstellt (auch wenn dieser Funktionsbefehl eine 64-KB-Seite mit GPU-Speicher zuweist, wird wahrscheinlich ein größerer Puffer erstellt).</span><span class="sxs-lookup"><span data-stu-id="611e8-153">This sample only performs one query and for simplicity and readability creates a buffer exactly that size (even though this function call will allocate a 64K page of GPU memory - most real apps would likely create a larger buffer).</span></span>

``` syntax
 // Create the query result buffer.
              CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_DEFAULT);
              auto queryBufferDesc = CD3DX12_RESOURCE_DESC::Buffer(8);
              ThrowIfFailed(m_device->CreateCommittedResource(
                     &heapProps,
                     D3D12_HEAP_FLAG_NONE,
                     &queryBufferDesc,
                     D3D12_RESOURCE_STATE_GENERIC_READ,
                     nullptr,
                     IID_PPV_ARGS(&m_queryResult)
                     ));
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="611e8-154">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="611e8-154">Call flow</span></span></th>
<th><span data-ttu-id="611e8-155">Parameter</span><span class="sxs-lookup"><span data-stu-id="611e8-155">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="611e8-156"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>"Kreatecommittedresource"</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-156"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="611e8-157"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-157"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br />
<span data-ttu-id="611e8-158">[<strong>D3D12_HEAP_TYPE</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_heap_type)</span><span class="sxs-lookup"><span data-stu-id="611e8-158">[<strong>D3D12_HEAP_TYPE</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span></span><br />
<span data-ttu-id="611e8-159">[<strong>D3D12_HEAP_FLAG</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_heap_flags)</span><span class="sxs-lookup"><span data-stu-id="611e8-159">[<strong>D3D12_HEAP_FLAG</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags)</span></span><br />
<span data-ttu-id="611e8-160">[<strong>CD3DX12_RESOURCE_DESC</strong>] (cd3dx12-Resource-DESC.MD)</span><span class="sxs-lookup"><span data-stu-id="611e8-160">[<strong>CD3DX12_RESOURCE_DESC</strong>](cd3dx12-resource-desc.md)</span></span><br />
<span data-ttu-id="611e8-161">[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="611e8-161">[<strong>D3D12_RESOURCE_STATES</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="draw-the-quads-and-perform-and-resolve-the-occlusion-query"></a><span data-ttu-id="611e8-162">Zeichnen der Quads und ausführen und Auflösen der Okklusions Abfrage</span><span class="sxs-lookup"><span data-stu-id="611e8-162">Draw the quads and perform and resolve the occlusion query</span></span>

<span data-ttu-id="611e8-163">Nachdem das Setup abgeschlossen ist, wird die Hauptschleife in der **populatecommandlists** -Methode aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="611e8-163">Having done the setup, the main loop is updated in the **PopulateCommandLists** method.</span></span>

<dl> 1. <span data-ttu-id="611e8-164">Zeichnen Sie die Quads von hinten nach vorne, damit der Transparenz Effekt ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="611e8-164">Draw the quads from back to front to make the transparency effect work properly.</span></span> <span data-ttu-id="611e8-165">Das Zurückziehen des Quad in den Vordergrund basiert auf dem Ergebnis der Abfrage des vorherigen Frames und ist hierfür eine gängige Methode.</span><span class="sxs-lookup"><span data-stu-id="611e8-165">Drawing the quad in back to front is predicated on the result of the previous frame’s query and is a fairly common technique for this.</span></span>  
2. <span data-ttu-id="611e8-166">Ändern Sie das PSO, dass Renderziel-und tiefen Schablonen Schreibvorgänge deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="611e8-166">Change the PSO to disable render target and depth stencil writes.</span></span>  
3. <span data-ttu-id="611e8-167">Führen Sie die oksions Abfrage aus.</span><span class="sxs-lookup"><span data-stu-id="611e8-167">Perform the occlusion query.</span></span>  
4. <span data-ttu-id="611e8-168">Auflösen der Okklusions Abfrage.</span><span class="sxs-lookup"><span data-stu-id="611e8-168">Resolve the occlusion query.</span></span>  
</dl>

``` syntax
       // Draw the quads and perform the occlusion query.
       {
              CD3DX12_GPU_DESCRIPTOR_HANDLE cbvFarQuad(m_cbvHeap->GetGPUDescriptorHandleForHeapStart(), m_frameIndex * CbvCountPerFrame, m_cbvSrvDescriptorSize);
              CD3DX12_GPU_DESCRIPTOR_HANDLE cbvNearQuad(cbvFarQuad, m_cbvSrvDescriptorSize);

              m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP);
              m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);

              // Draw the far quad conditionally based on the result of the occlusion query
              // from the previous frame.
              m_commandList->SetGraphicsRootDescriptorTable(0, cbvFarQuad);
              m_commandList->SetPredication(m_queryResult.Get(), 0, D3D12_PREDICATION_OP_EQUAL_ZERO);
              m_commandList->DrawInstanced(4, 1, 0, 0);

              // Disable predication and always draw the near quad.
              m_commandList->SetPredication(nullptr, 0, D3D12_PREDICATION_OP_EQUAL_ZERO);
              m_commandList->SetGraphicsRootDescriptorTable(0, cbvNearQuad);
              m_commandList->DrawInstanced(4, 1, 4, 0);

              // Run the occlusion query with the bounding box quad.
              m_commandList->SetGraphicsRootDescriptorTable(0, cbvFarQuad);
              m_commandList->SetPipelineState(m_queryState.Get());
              m_commandList->BeginQuery(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0);
              m_commandList->DrawInstanced(4, 1, 8, 0);
              m_commandList->EndQuery(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0);

              // Resolve the occlusion query and store the results in the query result buffer
              // to be used on the subsequent frame.
              m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_queryResult.Get(), D3D12_RESOURCE_STATE_GENERIC_READ, D3D12_RESOURCE_STATE_COPY_DEST));
              m_commandList->ResolveQueryData(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0, 1, m_queryResult.Get(), 0);
              m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_queryResult.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_GENERIC_READ));
       }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="611e8-169">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="611e8-169">Call flow</span></span></th>
<th><span data-ttu-id="611e8-170">Parameter</span><span class="sxs-lookup"><span data-stu-id="611e8-170">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="611e8-171"><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-171"><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="611e8-172"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>Getgpudescriptor Lenker forheapstart</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-172"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>GetGPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="611e8-173"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>Iasetprimitivetopology</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-173"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>IASetPrimitiveTopology</strong></a></span></span></td>
<td><span data-ttu-id="611e8-174"><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-174"><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="611e8-175"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>Iasetvertexbuffers</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-175"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>IASetVertexBuffers</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="611e8-176"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>Setgraphicsrootdescriptor Table</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-176"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="611e8-177"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>Setprediation</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-177"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></span></span></td>
<td><span data-ttu-id="611e8-178"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-178"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="611e8-179"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>Drawinstanzierte</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-179"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="611e8-180"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>Setprediation</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-180"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></span></span></td>
<td><span data-ttu-id="611e8-181"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-181"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="611e8-182"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>Setgraphicsrootdescriptor Table</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-182"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="611e8-183"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>Drawinstanzierte</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-183"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="611e8-184"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>Setgraphicsrootdescriptor Table</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-184"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="611e8-185"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate"><strong>Setpipelinestate</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-185"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate"><strong>SetPipelineState</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="611e8-186"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery"><strong>Beginquery</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-186"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery"><strong>BeginQuery</strong></a></span></span></td>
<td><span data-ttu-id="611e8-187"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-187"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="611e8-188"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>Drawinstanzierte</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-188"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="611e8-189"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery"><strong>Endquery</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-189"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery"><strong>EndQuery</strong></a></span></span></td>
<td><span data-ttu-id="611e8-190"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-190"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="611e8-191"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>Resourcebarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-191"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><dl><span data-ttu-id="611e8-192"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-192"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br />
<span data-ttu-id="611e8-193">[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="611e8-193">[<strong>D3D12_RESOURCE_STATES</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="611e8-194"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata"><strong>Resolvequerydata</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-194"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata"><strong>ResolveQueryData</strong></a></span></span></td>
<td><span data-ttu-id="611e8-195"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-195"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="611e8-196"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>Resourcebarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-196"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><dl><span data-ttu-id="611e8-197"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="611e8-197"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br />
<span data-ttu-id="611e8-198">[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="611e8-198">[<strong>D3D12_RESOURCE_STATES</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="run-the-sample"></a><span data-ttu-id="611e8-199">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="611e8-199">Run the sample</span></span>

<span data-ttu-id="611e8-200">Nicht okkludiert:</span><span class="sxs-lookup"><span data-stu-id="611e8-200">Not occluded:</span></span>

![zwei Felder nicht verdeckt](images/not-occluded.png)

<span data-ttu-id="611e8-202">Zähler okkludierte</span><span class="sxs-lookup"><span data-stu-id="611e8-202">Occluded:</span></span>

![ein Feld, das vollständig verdeckt ist](images/occluded.png)

<span data-ttu-id="611e8-204">Teilweise okkludiert:</span><span class="sxs-lookup"><span data-stu-id="611e8-204">Partially occluded:</span></span>

![ein Feld ist teilweise verdeckt.](images/partially-occluded.png)

## <a name="related-topics"></a><span data-ttu-id="611e8-206">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="611e8-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="611e8-207">D3D12-Code Exemplarische Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="611e8-207">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)
</dt> <dt>

[<span data-ttu-id="611e8-208">Prädikation übersprungen</span><span class="sxs-lookup"><span data-stu-id="611e8-208">Predication</span></span>](predication.md)
</dt> <dt>

[<span data-ttu-id="611e8-209">Abfragen</span><span class="sxs-lookup"><span data-stu-id="611e8-209">Queries</span></span>](queries.md)
</dt> </dl>

 

 
