---
title: Prädikationsabfragen
description: Das D3D12PredicationQueries-Beispiel veranschaulicht okklusions-culling mit DirectX 12-Abfrageheaps und Prädikation. In der exemplarischen Vorgehensweise wird der zusätzliche Code beschrieben, der erforderlich ist, um das HelloConstBuffer-Beispiel für die Verarbeitung von Prädikationsabfragen zu erweitern.
ms.assetid: F61817BB-45BC-4977-BE4A-EE0FDAFBCB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d37bd4653ec7610e36214cce31955f1742e5b27a42a381cc2aa7d758daaf5b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733396"
---
# <a name="predication-queries"></a>Prädikationsabfragen

Das **D3D12PredicationQueries-Beispiel** veranschaulicht okklusions-culling mit DirectX 12-Abfrageheaps und Prädikation. In der exemplarischen Vorgehensweise wird der zusätzliche Code beschrieben, der erforderlich ist, um das **HelloConstBuffer-Beispiel** für die Verarbeitung von Prädikationsabfragen zu erweitern.

-   [Erstellen eines Tiefenschablonendeskriptorheaps und eines Verdeckungsabfrageheaps](#create-a-depth-stencil-descriptor-heap-and-an-occlusion-query-heap)
-   [Aktivieren von Alphablending](#enable-alpha-blending)
-   [Deaktivieren von Farb- und Tiefen-Schreibvorgängen](#disable-color-and-depth-writes)
-   [Erstellen eines Puffers zum Speichern der Ergebnisse der Abfrage](#create-a-buffer-to-store-the-results-of-the-query)
-   [Zeichnen der Quader und Ausführen und Auflösen der Verdeckungsabfrage](#draw-the-quads-and-perform-and-resolve-the-occlusion-query)
-   [Ausführen des Beispiels](#run-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="create-a-depth-stencil-descriptor-heap-and-an-occlusion-query-heap"></a>Erstellen eines Tiefenschablonendeskriptorheaps und eines Verdeckungsabfrageheaps

Erstellen Sie in der **LoadPipeline-Methode** einen Tiefenschablonendeskriptorheap.

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
<th>Aufrufflow</th>
<th>Parameter</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc"><strong>D3D12_DESCRIPTOR_HEAP_DESC</strong></a></td>
<td><dl><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type"><strong>D3D12_DESCRIPTOR_HEAP_TYPE</strong></a><br />
[<strong>D3D12_DESCRIPTOR_HEAP_FLAG</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags)<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap"><strong>CreateDescriptorHeap</strong></a></td>

</tr>
</tbody>
</table>



 

Erstellen Sie in der **LoadAssets-Methode** einen Heap für Okklusionsabfragen.

``` syntax
     // Describe and create a heap for occlusion queries.
              D3D12_QUERY_HEAP_DESC queryHeapDesc = {};
              queryHeapDesc.Count = 1;
              queryHeapDesc.Type = D3D12_QUERY_HEAP_TYPE_OCCLUSION;
              ThrowIfFailed(m_device->CreateQueryHeap(&queryHeapDesc, IID_PPV_ARGS(&m_queryHeap)));
```



| Aufrufflow                                                 | Parameter                                                |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [**\_ \_ D3D12-ABFRAGEHEAP-DESC \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc) | [**\_D3D12-ABFRAGEHEAPTYP \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type) |
| [**CreateQueryHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap)   |                                                           |



 

## <a name="enable-alpha-blending"></a>Aktivieren von Alphablending

Dieses Beispiel zeichnet zwei Quader und veranschaulicht eine binäre Verdeckungsabfrage. Das Quad-Element im Vordergrund wird über den Bildschirm animiert, und das quad-Element im Hintergrund wird gelegentlich verdeckt. In der **LoadAssets-Methode** ist das Alphablending für dieses Beispiel aktiviert, damit wir sehen können, an welchem Punkt D3D das Quad in back occluded betrachtet.

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
<th>Aufrufflow</th>
<th>Parameter</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="cd3dx12-blend-desc.md"><strong>CD3DX12_BLEND_DESC</strong></a></td>
<td><dl><a href="cd3dx12-default.md"><strong>CD3DX12_DEFAULT</strong></a><br />
[<strong>D3D12_BLEND</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend)<br />
[<strong>D3D12_BLEND_OP</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend_op)<br />
[<strong>D3D12_LOGIC_OP</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_logic_op)<br />
[<strong>D3D12_COLOR_WRITE_ENABLE</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_color_write_enable)<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="disable-color-and-depth-writes"></a>Deaktivieren von Farb- und Tiefen-Schreibvorgängen

Die Verdeckungsabfrage wird ausgeführt, indem ein Quader gerendert wird, der den gleichen Bereich wie der Quader abdeckt, dessen Sichtbarkeit wir testen möchten. In komplexeren Szenen handelt es sich bei der Abfrage wahrscheinlich um ein begrenzungsvolumes und nicht um ein einfaches Quader. In beiden Fällen wird ein neuer Pipelinezustand erstellt, der das Schreiben in das Renderziel und den Z-Puffer deaktiviert, sodass sich die Verdeckungsabfrage selbst nicht auf die sichtbare Ausgabe des Renderingdurchlaufs auswirkt.

Deaktivieren Sie in der **LoadAssets-Methode** Farb- und Tiefen-Schreibvorgänge für den Zustand der Verdeckungsabfrage.

``` syntax
 // Disable color writes and depth writes for the occlusion query's state.
              psoDesc.BlendState.RenderTarget[0].RenderTargetWriteMask = 0;
              psoDesc.DepthStencilState.DepthWriteMask = D3D12_DEPTH_WRITE_MASK_ZERO;

              ThrowIfFailed(m_device->CreateGraphicsPipelineState(&psoDesc, IID_PPV_ARGS(&m_queryState)));
```



| Aufrufflow                                                                            | Parameter                                                  |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [**D3D12 \_ GRAPHICS \_ PIPELINE \_ STATE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) | [**D3D12 \_ DEPTH \_ WRITE \_ MASK**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) |
| [**CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)      |                                                             |



 

## <a name="create-a-buffer-to-store-the-results-of-the-query"></a>Erstellen eines Puffers zum Speichern der Ergebnisse der Abfrage

In der **LoadAssets-Methode** muss ein Puffer erstellt werden, um die Ergebnisse der Abfrage zu speichern. Jede Abfrage erfordert 8 Bytes Speicherplatz im GPU-Arbeitsspeicher. In diesem Beispiel wird nur eine Abfrage ausgeführt, und der Einfachheit halber und der Lesbarkeit wird ein Puffer erstellt, der genau diese Größe aufweist (obwohl dieser Funktionsaufruf eine 64.000-Seite gpu-Arbeitsspeicher zuordnet– die meisten echten Apps würden wahrscheinlich einen größeren Puffer erstellen).

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
<th>Aufrufflow</th>
<th>Parameter</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></td>
<td><dl><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a><br />
[<strong>D3D12_HEAP_TYPE</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)<br />
[<strong>D3D12_HEAP_FLAG</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags)<br />
[<strong>CD3DX12_RESOURCE_DESC</strong>] (cd3dx12-resource-desc.md)<br />
[<strong>D3D12_RESOURCE_STATES</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="draw-the-quads-and-perform-and-resolve-the-occlusion-query"></a>Zeichnen der Quader und Ausführen und Auflösen der Verdeckungsabfrage

Nach dem Setup wird die Main-Schleife in der **PopulateCommandLists-Methode** aktualisiert.

<dl> 1. Zeichnen Sie die Quads von zurück nach vorne, damit der Transparenzeffekt ordnungsgemäß funktioniert. Das Zurückstellen des Quaders nach vorn basiert auf dem Ergebnis der Abfrage des vorherigen Frames und ist hierfür eine recht gängige Technik.  
2. Ändern Sie die PSO, um Renderziel- und Tiefenschablonen-Schreibvorgänge zu deaktivieren.  
3. Führen Sie die Verdeckungsabfrage aus.  
4. Lösen Sie die Verdeckungsabfrage auf.  
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
<th>Aufrufflow</th>
<th>Parameter</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>GetGPUDescriptorHandleForHeapStart</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>IASetPrimitiveTopology</strong></a></td>
<td><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>IASetVertexBuffers</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate"><strong>SetPipelineState</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery"><strong>BeginQuery</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery"><strong>EndQuery</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></td>
<td><dl><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a><br />
[<strong>D3D12_RESOURCE_STATES</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata"><strong>ResolveQueryData</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></td>
<td><dl><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a><br />
[<strong>D3D12_RESOURCE_STATES</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="run-the-sample"></a>Ausführen des Beispiels

Nicht occluded:

![Zwei Felder, die nicht verblendet sind](images/not-occluded.png)

Verdeckt:

![Ein Feld vollständig verblendet](images/occluded.png)

Teilweise verblendet:

![ein Feld teilweise verblendet](images/partially-occluded.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Exemplarische Vorgehensweisen zu D3D12-Code](d3d12-code-walk-throughs.md)
</dt> <dt>

[Prädikation](predication.md)
</dt> <dt>

[Abfragen](queries.md)
</dt> </dl>

 

 
