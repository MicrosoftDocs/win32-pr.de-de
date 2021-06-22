---
title: Hochladen von Texturdaten über Puffer
description: Das Hochladen von 2D- oder 3D-Texturdaten ähnelt dem Hochladen von 1D-Daten, mit der Ausnahme, dass Anwendungen die Datenausrichtung im Zusammenhang mit der Zeilenhöhe genauer beachten müssen.
ms.assetid: 22A25A94-A45C-482D-853A-FA6860EE7E4E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72177be1fefbf102e901d28d47413c8bcff41ab
ms.sourcegitcommit: 39754f1af7853adff2525d0936afe9aad2066a9a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/22/2021
ms.locfileid: "112426964"
---
# <a name="uploading-texture-data-through-buffers"></a>Hochladen von Texturdaten über Puffer

Das Hochladen von 2D- oder 3D-Texturdaten ähnelt dem Hochladen von 1D-Daten, mit der Ausnahme, dass Anwendungen die Datenausrichtung im Zusammenhang mit der Zeilenhöhe genauer beachten müssen. Puffer können orthogonal und gleichzeitig aus mehreren Teilen der Grafikpipeline verwendet werden und sind sehr flexibel.

-   [Hochladen von Texturdaten über Puffer](#upload-texture-data-via-buffers)
-   [Wird kopiert](#copying)
-   [Zuordnung und Entmapping](#mapping-and-unmapping)
-   [Pufferausrichtung](#buffer-alignment)
-   [Verwandte Themen](#related-topics)

## <a name="upload-texture-data-via-buffers"></a>Hochladen von Texturdaten über Puffer

Anwendungen müssen Daten über [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) oder [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)hochladen. Texturdaten sind viel wahrscheinlicher größer, greifen wiederholt darauf zu und profitieren von der verbesserten Cachekoherität von nicht linearen Speicherlayouts als andere Ressourcendaten. Wenn Puffer in D3D12 verwendet werden, haben Anwendungen vollständige Kontrolle über die Datenplatzierung und Anordnung im Zusammenhang mit dem Kopieren von Ressourcendaten, solange die Anforderungen an die Arbeitsspeicherausrichtung erfüllt sind.

Im Beispiel wird hervorgehoben, wo die Anwendung 2D-Daten einfach in 1D vereinfacht, bevor sie im Puffer platziert werden. Für das Mipmap-2D-Szenario kann die Anwendung entweder jede untergeordnete Ressource diskret abschwächen und schnell einen 1D-Algorithmus für die untergeordnete Zuordnung verwenden oder eine kompliziertere 2D-Unterzuordnungsmethode verwenden, um die Videospeicherauslastung zu minimieren. Es wird erwartet, dass die erste Technik häufiger verwendet wird, da sie einfacher ist. Die zweite Technik kann beim Packen von Daten auf einem Datenträger oder über ein Netzwerk nützlich sein. In beiden Fällen muss die Anwendung weiterhin die Kopier-APIs für jede Unterressource aufrufen.

``` syntax
// Prepare a pBitmap in memory, with bitmapWidth, bitmapHeight, and pixel format of DXGI_FORMAT_B8G8R8A8_UNORM. 
//
// Sub-allocate from the buffer for texture data.
//

D3D12_SUBRESOURCE_FOOTPRINT pitchedDesc = { 0 };
pitchedDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
pitchedDesc.Width = bitmapWidth;
pitchedDesc.Height = bitmapHeight;
pitchedDesc.Depth = 1;
pitchedDesc.RowPitch = Align(bitmapWidth * sizeof(DWORD), D3D12_TEXTURE_DATA_PITCH_ALIGNMENT);

//
// Note that the helper function UpdateSubresource in D3DX12.h, and ID3D12Device::GetCopyableFootprints 
// can help applications fill out D3D12_SUBRESOURCE_FOOTPRINT and D3D12_PLACED_SUBRESOURCE_FOOTPRINT structures.
//
// Refer to the D3D12 Code example for the previous section "Uploading Different Types of Resources"
// for the code for SuballocateFromBuffer.
//

SuballocateFromBuffer(
    pitchedDesc.Height * pitchedDesc.RowPitch,
    D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT
    );

D3D12_PLACED_SUBRESOURCE_FOOTPRINT placedTexture2D = { 0 };
placedTexture2D.Offset = m_pDataCur – m_pDataBegin;
placedTexture2D.Footprint = pitchedDesc;

//
// Copy texture data from DWORD* pBitmap->pixels to the buffer
//

for (UINT y = 0; y < bitmapHeight; y++)
{
  UINT8 *pScan = m_pDataBegin + placedTexture2D.Offset + y * pitchedDesc.RowPitch;
  memcpy( pScan, &(pBitmap->pixels[y * bitmapWidth]), sizeof(DWORD) * bitmapWidth );
}

//
// Create default texture2D resource.
//

D3D12_RESOURCE_DESC  textureDesc { ... };

CComPtr<ID3D12Resource> texture2D;
d3dDevice->CreateCommittedResource( 
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT), 
        D3D12_HEAP_FLAG_NONE, &textureDesc, 
        D3D12_RESOURCE_STATE_COPY_DEST, 
        nullptr, 
        IID_PPV_ARGS(&texture2D) );

//
// Copy heap data to texture2D.
//

commandList->CopyTextureRegion( 
        &CD3DX12_TEXTURE_COPY_LOCATION( texture2D, 0 ), 
        0, 0, 0, 
        &CD3DX12_TEXTURE_COPY_LOCATION( m_spUploadHeap, placedTexture2D ), 
        nullptr );
```

Beachten Sie die Verwendung der Hilfsstrukturen [**CD3DX12 \_ HEAP \_ PROPERTIES**](cd3dx12-heap-properties.md) und [**CD3DX12 \_ TEXTURE COPY \_ \_ LOCATION**](cd3dx12-texture-copy-location.md)und die Methoden [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) und [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).

## <a name="copying"></a>Wird kopiert

D3D12-Methoden ermöglichen Es Anwendungen, D3D11 [**UpdateSubresource,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource) [**CopySubresourceRegion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion)und Ressourcen-Anfangsdaten zu ersetzen. Eine einzelne 3D-Unterressource mit Zeilen-Haupttexturdaten kann sich in Pufferressourcen befinden. [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) kann diese Texturdaten aus dem Puffer in eine Texturressource mit unbekanntem Texturlayout kopieren und umgekehrt. Anwendungen sollten diese Art von Technik bevorzugen, um häufig genutzte GPU-Ressourcen aufzufüllen, indem große Puffer in einem UPLOAD-Heap erstellt werden, während die häufig verwendeten GPU-Ressourcen in einem DEFAULT-Heap ohne CPU-Zugriff erstellt werden. Eine solche Technik unterstützt diskrete GPUs und deren große Mengen an cpu-unzugänglichem Arbeitsspeicher effizient, ohne dass UMA-Architekturen häufig beeinträchtigt werden.

Beachten Sie die folgenden beiden Konstanten:

``` syntax
const UINT D3D12_TEXTURE_DATA_PITCH_ALIGNMENT = 256;
const UINT D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT = 512;
```

-   [**D3D12 \_ SUBRESOURCE \_ FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
-   [**D3D12 \_ \_ PLATZIERTER \_ SUBRESOURCE-SPEICHERBEDARF**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)
-   [**D3D12 \_ TEXTURE \_ COPY \_ LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
-   [**D3D12 \_ TEXTURE \_ COPY \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)
-   [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
-   [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**ID3D12GraphicsCommandList::CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**ID3D12CommandQueue::UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)

## <a name="mapping-and-unmapping"></a>Zuordnung und Entmapping

[**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) und [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) können sicher von mehreren Threads aufgerufen werden. Der erste Aufruf von **Map** ordnet einen virtuellen CPU-Adressbereich für die Ressource zu. Der letzte Aufruf von **Zuordnung** aufheben hebt die Zuordnung des virtuellen CPU-Adressbereichs auf. Die virtuelle CPU-Adresse wird häufig an die Anwendung zurückgegeben.

Wenn Daten zwischen CPU und GPU über Ressourcen in Rückleseheaps übergeben werden, müssen [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) und [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) verwendet werden, um alle Systeme zu unterstützen, auf der D3D12 unterstützt wird. Wenn Die Bereiche so eng wie möglich gehalten werden, wird die Effizienz der Systeme maximiert, die Bereiche erfordern (siehe [**D3D12 \_ RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).

Die Leistung von Debugtools profitiert nicht nur von [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)der genauen Nutzung von Bereichen bei allen  /  [**Zuordnungs-Unmap-Aufrufen,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) sondern auch von Anwendungen, die Ressourcen aufheben, wenn CPU-Änderungen nicht mehr vorgenommen werden.

Die D3D11-Methode zur Verwendung von [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (mit festgelegter DISCARD-Parameter) zum Umbenennen von Ressourcen wird in D3D12 nicht unterstützt. Anwendungen müssen das Umbenennen von Ressourcen selbst implementieren. Alle  Zuordnungsaufrufe sind implizit NO \_ OVERWRITE und Multithreading. Es liegt in der Verantwortung der Anwendung, sicherzustellen, dass alle relevanten GPU-Aufgaben in Befehlslisten abgeschlossen sind, bevor der Zugriff auf Daten mit der CPU abgeschlossen ist. D3D12-Aufrufe von **Map** leeren weder implizit Befehlspuffer, noch blockieren sie das Warten auf den Abschluss der Arbeit durch die GPU. Daher können **Map** und [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) in einigen Szenarien sogar optimiert werden.

## <a name="buffer-alignment"></a>Pufferausrichtung

Einschränkungen bei der Pufferausrichtung:

-   Das lineare Kopieren von Unterressourcen muss auf 512 Byte ausgerichtet sein (wobei die Zeilenhöhe an D3D12 TEXTURE DATA PITCH ALIGNMENT Bytes ausgerichtet \_ \_ \_ \_ ist).
-   Konstante Datenlesedaten müssen ein Vielfaches von 256 Bytes vom Anfang des Heaps sein (d. h. nur von Adressen, die 256 Byte ausgerichtet sind).
-   Indexdatenleseungen müssen ein Vielfaches der Größe des Indexdatentyps sein (d. h. nur von Adressen, die natürlich für die Daten ausgerichtet sind).
-   [**ID3D12GraphicsCommandList::ExecuteIndirect-Daten**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) müssen aus Offsets stammen, die ein Vielfaches von 4 sind (d.h. nur von Adressen, die DWORD ausgerichtet sind).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterzuweisung innerhalb von Puffern](large-buffers.md)
</dt> </dl>

 

 
