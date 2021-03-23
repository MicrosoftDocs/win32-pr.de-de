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
# <a name="predication-queries"></a>Prädikationsabfragen

Das **D3D12PredicationQueries** -Beispiel veranschaulicht die Verschleierung von Okklusion mithilfe von DirectX 12-Abfrage Heaps und-Prädikaten. In der exemplarischen Vorgehensweise wird der zusätzliche Code beschrieben, der zum Erweitern des **helloconstbuffer** -Beispiels für die Behandlung von prädikationsabfragen

-   [Erstellen Sie einen tiefen Schablone-deskriptorheap und einen oksions Abfrage Heap.](#create-a-depth-stencil-descriptor-heap-and-an-occlusion-query-heap)
-   [Alpha Blending aktivieren](#enable-alpha-blending)
-   [Farben und Tiefe Schreibvorgänge deaktivieren](#disable-color-and-depth-writes)
-   [Erstellen eines Puffers zum Speichern der Abfrageergebnisse](#create-a-buffer-to-store-the-results-of-the-query)
-   [Zeichnen der Quads und ausführen und Auflösen der Okklusions Abfrage](#draw-the-quads-and-perform-and-resolve-the-occlusion-query)
-   [Ausführen des Beispiels](#run-the-sample)
-   [Verwandte Themen](#related-topics)

## <a name="create-a-depth-stencil-descriptor-heap-and-an-occlusion-query-heap"></a>Erstellen Sie einen tiefen Schablone-deskriptorheap und einen oksions Abfrage Heap.

Erstellen Sie in der **loadpipeline** -Methode einen tiefen Schablone-deskriptorheap.

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
<th>Aufruffluss</th>
<th>Parameter</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc"><strong>D3D12_DESCRIPTOR_HEAP_DESC</strong></a></td>
<td><dl><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type"><strong>D3D12_DESCRIPTOR_HEAP_TYPE</strong></a><br />
[<strong>D3D12_DESCRIPTOR_HEAP_FLAG</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_descriptor_heap_flags)<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap"><strong>"Kreatedescriptorheap"</strong></a></td>

</tr>
</tbody>
</table>



 

Erstellen Sie in der **loadassets** -Methode einen Heap für oksions Abfragen.

``` syntax
     // Describe and create a heap for occlusion queries.
              D3D12_QUERY_HEAP_DESC queryHeapDesc = {};
              queryHeapDesc.Count = 1;
              queryHeapDesc.Type = D3D12_QUERY_HEAP_TYPE_OCCLUSION;
              ThrowIfFailed(m_device->CreateQueryHeap(&queryHeapDesc, IID_PPV_ARGS(&m_queryHeap)));
```



| Aufruffluss                                                 | Parameter                                                |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [**D3D12 \_ Abfrage \_ Heap- \_ ABSC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc) | [**D3D12- \_ Abfrage \_ heaptyp \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type) |
| [**"Kreatequeryheap"**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap)   |                                                           |



 

## <a name="enable-alpha-blending"></a>Alpha Blending aktivieren

In diesem Beispiel werden zwei Quads gezeichnet und eine binäre Okklusions Abfrage veranschaulicht. Das Vierfache im Vordergrund wird auf dem Bildschirm animiert, und der im Hintergrund wird gelegentlich ausgeblendet. In der **loadassets** -Methode ist Alpha Blending für dieses Beispiel aktiviert, sodass wir sehen können, zu welchem Punkt D3D das Vierfache im Hintergrund wieder gibt.

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
<th>Aufruffluss</th>
<th>Parameter</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="cd3dx12-blend-desc.md"><strong>CD3DX12_BLEND_DESC</strong></a></td>
<td><dl><a href="cd3dx12-default.md"><strong>CD3DX12_DEFAULT</strong></a><br />
[<strong>D3D12_BLEND</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_blend)<br />
[<strong>D3D12_BLEND_OP</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_blend_op)<br />
[<strong>D3D12_LOGIC_OP</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_logic_op)<br />
[<strong>D3D12_COLOR_WRITE_ENABLE</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_color_write_enable)<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="disable-color-and-depth-writes"></a>Farben und Tiefe Schreibvorgänge deaktivieren

Die oksions Abfrage wird durch das Rendern eines Quad durchgeführt, das denselben Bereich abdeckt wie das Vierfache, dessen Sichtbarkeit getestet werden soll. In komplexeren Szenen wäre die Abfrage wahrscheinlich ein Begrenzungs Volume und kein einfaches Quad. In beiden Fällen wird ein neuer Pipeline Status erstellt, der das Schreiben in das Renderziel und den z-Puffer deaktiviert, sodass sich die Okklusions Abfrage selbst nicht auf die sichtbare Ausgabe des Renderings auswirkt.

Deaktivieren Sie in der **loadassets** -Methode Farb Schreibvorgänge und Tiefe Schreibvorgänge für den Zustand der oksion-Abfrage.

``` syntax
 // Disable color writes and depth writes for the occlusion query's state.
              psoDesc.BlendState.RenderTarget[0].RenderTargetWriteMask = 0;
              psoDesc.DepthStencilState.DepthWriteMask = D3D12_DEPTH_WRITE_MASK_ZERO;

              ThrowIfFailed(m_device->CreateGraphicsPipelineState(&psoDesc, IID_PPV_ARGS(&m_queryState)));
```



| Aufruffluss                                                                            | Parameter                                                  |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [**D3D12- \_ Grafik \_ Pipeline \_ Status \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) | [**D3D12 \_ Tiefe \_ Schreib \_ Maske**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) |
| [**"Kreategraphicspipelinestate"**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)      |                                                             |



 

## <a name="create-a-buffer-to-store-the-results-of-the-query"></a>Erstellen eines Puffers zum Speichern der Abfrageergebnisse

In der **loadassets** -Methode muss ein Puffer erstellt werden, um die Ergebnisse der Abfrage zu speichern. Jede Abfrage benötigt im GPU-Speicher 8 Bytes Speicherplatz. In diesem Beispiel wird nur eine Abfrage durchführen, und aus Gründen der Einfachheit und Lesbarkeit wird ein Puffer genau dieser Größe erstellt (auch wenn dieser Funktionsbefehl eine 64-KB-Seite mit GPU-Speicher zuweist, wird wahrscheinlich ein größerer Puffer erstellt).

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
<th>Aufruffluss</th>
<th>Parameter</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>"Kreatecommittedresource"</strong></a></td>
<td><dl><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a><br />
[<strong>D3D12_HEAP_TYPE</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_heap_type)<br />
[<strong>D3D12_HEAP_FLAG</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_heap_flags)<br />
[<strong>CD3DX12_RESOURCE_DESC</strong>] (cd3dx12-Resource-DESC.MD)<br />
[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_states)<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="draw-the-quads-and-perform-and-resolve-the-occlusion-query"></a>Zeichnen der Quads und ausführen und Auflösen der Okklusions Abfrage

Nachdem das Setup abgeschlossen ist, wird die Hauptschleife in der **populatecommandlists** -Methode aktualisiert.

<dl> 1. Zeichnen Sie die Quads von hinten nach vorne, damit der Transparenz Effekt ordnungsgemäß funktioniert. Das Zurückziehen des Quad in den Vordergrund basiert auf dem Ergebnis der Abfrage des vorherigen Frames und ist hierfür eine gängige Methode.  
2. Ändern Sie das PSO, dass Renderziel-und tiefen Schablonen Schreibvorgänge deaktiviert werden.  
3. Führen Sie die oksions Abfrage aus.  
4. Auflösen der Okklusions Abfrage.  
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
<th>Aufruffluss</th>
<th>Parameter</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>Getgpudescriptor Lenker forheapstart</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>Iasetprimitivetopology</strong></a></td>
<td><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>Iasetvertexbuffers</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>Setgraphicsrootdescriptor Table</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>Setprediation</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>Drawinstanzierte</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>Setprediation</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>Setgraphicsrootdescriptor Table</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>Drawinstanzierte</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>Setgraphicsrootdescriptor Table</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate"><strong>Setpipelinestate</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery"><strong>Beginquery</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>Drawinstanzierte</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery"><strong>Endquery</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>Resourcebarrier</strong></a></td>
<td><dl><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a><br />
[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_states)<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata"><strong>Resolvequerydata</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>Resourcebarrier</strong></a></td>
<td><dl><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a><br />
[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_states)<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="run-the-sample"></a>Ausführen des Beispiels

Nicht okkludiert:

![zwei Felder nicht verdeckt](images/not-occluded.png)

Zähler okkludierte

![ein Feld, das vollständig verdeckt ist](images/occluded.png)

Teilweise okkludiert:

![ein Feld ist teilweise verdeckt.](images/partially-occluded.png)

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[D3D12-Code Exemplarische Vorgehensweisen](d3d12-code-walk-throughs.md)
</dt> <dt>

[Prädikation übersprungen](predication.md)
</dt> <dt>

[Abfragen](queries.md)
</dt> </dl>

 

 
