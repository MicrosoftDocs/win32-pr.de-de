---
title: Hochladen von Texturdaten über Puffer
description: Das Hochladen von 2D- oder 3D-Texturdaten ähnelt dem Hochladen von 1D-Daten, mit der Ausnahme, dass Anwendungen die Datenausrichtung im Zusammenhang mit der Zeilenhöhe genauer beachten müssen.
ms.assetid: 22A25A94-A45C-482D-853A-FA6860EE7E4E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c095d93237a44369cb249d6de9e514fa7021a91fb78430ddc428c88e4e71b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027990"
---
# <a name="uploading-texture-data-through-buffers"></a>Hochladen von Texturdaten über Puffer

Das Hochladen von 2D- oder 3D-Texturdaten ähnelt dem Hochladen von 1D-Daten, mit der Ausnahme, dass Anwendungen die Datenausrichtung im Zusammenhang mit der Zeilenhöhe genauer beachten müssen. Puffer können orthogonal und gleichzeitig aus mehreren Teilen der Grafikpipeline verwendet werden und sind sehr flexibel.

-   [Hochladen Texturdaten über Puffer](#upload-texture-data-via-buffers)
-   [Wird kopiert](#copying)
-   [Zuordnung und Entmapping](#mapping-and-unmapping)
-   [Pufferausrichtung](#buffer-alignment)
-   [Zugehörige Themen](#related-topics)

## <a name="upload-texture-data-via-buffers"></a>Hochladen Texturdaten über Puffer

Anwendungen müssen Daten über [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) oder [**ID3D12GraphicsCommandList::CopyBufferRegion hochladen.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) Texturdaten sind viel größer, werden wiederholt aufgerufen und profitieren von der verbesserten Cachekoherenz nicht linearer Speicherlayouts als andere Ressourcendaten. Wenn Puffer in D3D12 verwendet werden, haben Anwendungen vollständige Kontrolle über die Datenplatzierung und Anordnung, die mit dem Kopieren von Ressourcendaten verbunden sind, solange die Anforderungen an die Arbeitsspeicherausrichtung erfüllt sind.

Das Beispiel zeigt, wo die Anwendung 2D-Daten einfach in 1D vereinfacht, bevor sie in den Puffer platziert werden. Für das Mipmap-2D-Szenario kann die Anwendung entweder jede Unterressource diskret abflachen und schnell einen 1D-Unterzuordnungsalgorithmus verwenden oder eine kompliziertere 2D-Unterzuordnungsmethode verwenden, um die Auslastung des Videospeichers zu minimieren. Es wird erwartet, dass die erste Technik häufiger verwendet wird, da sie einfacher ist. Die zweite Technik kann beim Packen von Daten auf einem Datenträger oder über ein Netzwerk nützlich sein. In beiden Fällen muss die Anwendung weiterhin die Kopier-APIs für jede Unterressource aufrufen.

```cpp
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

Beachten Sie die Verwendung der Hilfsstrukturen [**CD3DX12 \_ HEAP \_ PROPERTIES**](cd3dx12-heap-properties.md) und [**CD3DX12 \_ TEXTURE COPY \_ \_ LOCATION**](cd3dx12-texture-copy-location.md)sowie der [**Methoden CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) und [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).

## <a name="copying"></a>Wird kopiert

D3D12-Methoden ermöglichen Es Anwendungen, D3D11 [**UpdateSubresource,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource) [**CopySubresourceRegion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion)und anfängliche Ressourcendaten zu ersetzen. Eine einzelne 3D-Unterressource mit Zeilen-Haupttexturdaten kann sich in Pufferressourcen befinden. [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) kann diese Texturdaten aus dem Puffer in eine Texturressource mit einem unbekannten Texturlayout kopieren und umgekehrt. Anwendungen sollten diese Art von Technik bevorzugen, um häufig genutzte GPU-Ressourcen zu füllen, indem große Puffer in einem UPLOAD-Heap erstellt werden, während die häufig aufgerufenen GPU-Ressourcen in einem DEFAULT-Heap ohne CPU-Zugriff erstellt werden. Eine solche Technik unterstützt effizient diskrete GPUs und ihre große Menge an ARBEITSSPEICHER, auf die nicht zugegriffen werden kann, ohne dass UMA-Architekturen häufig beeinträchtigt werden.

Beachten Sie die folgenden beiden Konstanten:

```cpp
const UINT D3D12_TEXTURE_DATA_PITCH_ALIGNMENT = 256;
const UINT D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT = 512;
```

-   [**D3D12 \_ SUBRESOURCE \_ FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
-   [**D3D12– \_ \_ UNTERRESSOURCENBEDARF \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)
-   [**SPEICHERORT DER \_ D3D12-TEXTURKOPIE \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
-   [**D3D12 \_ \_ \_ TEXTURKOPIERTYP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)
-   [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
-   [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**ID3D12GraphicsCommandList::CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**ID3D12CommandQueue::UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)

## <a name="mapping-and-unmapping"></a>Zuordnung und Entmapping

[**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) und [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) können von mehreren Threads sicher aufgerufen werden. Beim ersten Aufruf von **Map** wird ein virtueller CPU-Adressbereich für die Ressource reserviert. Beim letzten Aufruf von **Unmap wird** die Adresszuordnung des virtuellen CPU-Adressbereichs wieder verfügbar. Die virtuelle CPU-Adresse wird häufig an die Anwendung zurückgegeben.

Wenn Daten zwischen CPU und GPU über Ressourcen in Rücklesehaps übergeben werden, müssen [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) und [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) verwendet werden, um alle Systeme zu unterstützen, auf die D3D12 unterstützt wird. Wenn die Bereiche so eng wie möglich bleiben, wird die Effizienz der Systeme maximiert, die Bereiche erfordern (siehe [**D3D12 \_ RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).

Die Leistung von Debugtools profitiert nicht nur von der genauen Verwendung von Bereichen bei allen [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)  /  [**Unmap-Aufrufen,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) sondern auch von Anwendungen, die Ressourcen entmappingen, wenn keine CPU-Änderungen mehr vorgenommen werden.

Die D3D11-Methode zur Verwendung von [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (mit festgelegten DISCARD-Parametern) zum Umbenennen von Ressourcen wird in D3D12 nicht unterstützt. Anwendungen müssen die Umbenennung von Ressourcen selbst implementieren. Alle **Map-Aufrufe** sind implizit NO \_ OVERWRITE und Multithreading. Es liegt in der Verantwortung der Anwendung, sicherzustellen, dass alle relevanten GPU-Arbeiten, die in Befehlslisten enthalten sind, vor dem Zugriff auf Daten mit der CPU abgeschlossen sind. D3D12-Aufrufe von **Map** leeren weder implizit Befehlspuffer, noch blockieren sie das Warten auf den Abschluss der GPU-Arbeit. Daher können **Map und** [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) in einigen Szenarien sogar optimiert werden.

## <a name="buffer-alignment"></a>Pufferausrichtung

Einschränkungen der Pufferausrichtung:

-   Das lineare Kopieren von Unterressourcen muss auf 512 Byte ausgerichtet sein (mit ausrichtung der Zeilenhöhe an D3D12 \_ TEXTURE DATA PITCH ALIGNMENT \_ \_ \_ Bytes).
-   Konstante Datenlesedaten müssen ein Vielfaches von 256 Bytes vom Anfang des Heaps sein (d. h. nur von Adressen, die mit 256 Byte ausgerichtet sind).
-   Indexdatenlese müssen ein Vielfaches der Indexdatentypgröße sein (d. h. nur von Adressen, die für die Daten natürlich ausgerichtet sind).
-   [**ID3D12GraphicsCommandList::ExecuteIndirect-Daten**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) müssen aus Offsets sein, die Vielfaches von 4 sind (d. h. nur von Adressen, die DWORD-ausgerichtet sind).

## <a name="related-topics"></a>Zugehörige Themen

* [Unterzuweisung innerhalb von Puffern](large-buffers.md)
