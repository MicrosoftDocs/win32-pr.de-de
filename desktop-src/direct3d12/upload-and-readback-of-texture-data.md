---
title: Hochladen von Textur Daten über Puffer
description: Das Hochladen von 2D-oder 3D-Textur Daten ähnelt dem Hochladen von 1D-Daten, mit dem Unterschied, dass Anwendungen die Daten Ausrichtung im Zusammenhang mit der Zeilen Tonhöhe genauer berücksichtigen müssen.
ms.assetid: 22A25A94-A45C-482D-853A-FA6860EE7E4E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aadbd1e71b3c9895b75c973397488472b57f8eb1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548744"
---
# <a name="uploading-texture-data-through-buffers"></a>Hochladen von Textur Daten über Puffer

Das Hochladen von 2D-oder 3D-Textur Daten ähnelt dem Hochladen von 1D-Daten, mit dem Unterschied, dass Anwendungen die Daten Ausrichtung im Zusammenhang mit der Zeilen Tonhöhe genauer berücksichtigen müssen. Puffer können von mehreren Teilen der Grafik Pipeline orthogonell und gleichzeitig verwendet werden und sind sehr flexibel.

-   [Hochladen von Textur Daten über Puffer](#upload-texture-data-via-buffers)
-   [Wird kopiert](#copying)
-   [Zuordnung und Zuordnung von Zuordnung](#mapping-and-unmapping)
-   [Puffer Ausrichtung](#buffer-alignment)
-   [Verwandte Themen](#related-topics)

## <a name="upload-texture-data-via-buffers"></a>Hochladen von Textur Daten über Puffer

Anwendungen müssen Daten über [**ID3D12GraphicsCommandList:: copytextureregion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) oder [**ID3D12GraphicsCommandList:: copybufferregion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)hochladen. Textur Daten sind viel wahrscheinlicher größer, greifen auf wiederholt zu, und profitieren von der verbesserten Cache Kohärenz der nichtlinearen Speicher Layouts als bei anderen Ressourcen Daten. Wenn Puffer in D3D12 verwendet werden, haben Anwendungen vollständige Kontrolle über die Platzierung und Anordnung von Daten, die dem Kopieren von Ressourcen Daten zugeordnet sind, sofern die Anforderungen an die Arbeitsspeicher Ausrichtung erfüllt sind.

Im Beispiel wird hervorgehoben, wo die Anwendung 2D-Daten einfach in 1D vereinfacht, bevor Sie in den Puffer platziert wird. Für das MipMap 2D-Szenario kann die Anwendung jede unter Ressource diskret vereinfachen und schnell einen 1D-unter Zuordnungs Algorithmus verwenden, oder Sie verwenden eine kompliziertere 2D-unter Zuordnungs Technik, um die Videospeicher Auslastung zu minimieren. Das erste Verfahren wird wahrscheinlich häufiger verwendet, da es einfacher ist. Das zweite Verfahren kann nützlich sein, wenn Sie Daten auf einem Datenträger oder in einem Netzwerk verpacken. In beiden Fällen muss die Anwendung weiterhin die Kopier-APIs für jede unter Ressource abrufen.

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

Beachten Sie die Verwendung der Hilfsstrukturen [**CD3DX12 \_ Heap \_ Eigenschaften**](cd3dx12-heap-properties.md) und [**CD3DX12 \_ Textur \_ Kopier \_ Speicherort**](cd3dx12-texture-copy-location.md)sowie die Methoden " [**kreatecommittedresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) " und " [**copytextureregion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)".

## <a name="copying"></a>Wird kopiert

D3D12-Methoden ermöglichen es Anwendungen, die anfänglichen Daten D3D11 [**updatesubresource**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource), [**copysubresourceregion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion)und Resource zu ersetzen. Eine einzelne 3D-unter Quelle, die Zeilen haupttextur-Daten enthält, befindet sich möglicherweise in Puffer Ressourcen. [**Copytextureregion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) kann diese Textur Daten aus dem Puffer in eine Textur Ressource mit einem unbekannten Textur Layout kopieren (und umgekehrt). Anwendungen sollten diese Art von Technik bevorzugen, um häufig verwendete GPU-Ressourcen aufzufüllen, indem große Puffer in einem uploadheap erstellt werden, während die häufig verwendeten GPU-Ressourcen in einem Standard Heap erstellt werden, der keinen CPU-Zugriff hat. Eine solche Technik unterstützt auf effiziente Weise diskrete GPUs und ihre große Menge an CPU-ungenügenden Arbeitsspeicher, ohne dass die UMA-Architekturen häufig beeinträchtigt werden.

Beachten Sie die folgenden zwei Konstanten:

``` syntax
const UINT D3D12_TEXTURE_DATA_PITCH_ALIGNMENT = 256;
const UINT D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT = 512;
```

-   [**D3D12 Ressourcen \_ \_ Bedarf**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
-   [**D3D12 Speicherort der untergeordneten \_ \_ Quelle \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)
-   [**Speicherort der D3D12- \_ Textur \_ Kopie \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
-   [**D3D12 \_ Textur \_ \_ kopierungstyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)
-   [**ID3D12Device:: getcopyablefootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
-   [**ID3D12GraphicsCommandList:: copyresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**ID3D12GraphicsCommandList:: copytextureregion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**ID3D12GraphicsCommandList:: copybufferregion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**ID3D12GraphicsCommandList:: copytiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**ID3D12CommandQueue:: updatetilemappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)

## <a name="mapping-and-unmapping"></a>Zuordnung und Zuordnung von Zuordnung

[**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) und [**unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) können von mehreren Threads sicher aufgerufen werden. Der erste Befehl von **map** ordnet einen virtuellen CPU-Adressbereich für die Ressource zu. Der letzte aufzurufende aufrufungs Befehl hebt die Zuordnung des virtuellen CPU-Adress **Bereichs auf.** Die virtuelle CPU-Adresse wird in der Regel an die Anwendung zurückgegeben.

Jedes Mal, wenn Daten zwischen CPU und GPU über Ressourcen in den rückgängig-Heaps übermittelt werden, müssen [**map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) und [**unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) zur Unterstützung aller Systeme verwendet werden D3D12 wird unter unterstützt. Wenn Sie die Bereiche so eng wie möglich halten, wird die Effizienz der Systeme maximiert, die Bereiche erfordern (siehe [**D3D12 \_ Range**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).

Die Leistung der Debuggingtools profitiert nicht nur von der exakten Verwendung von Bereichen in allen Zuordnungs Aufrufen von [**Karten**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)  /  [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) , sondern auch von Anwendungen, die die Zuordnung von Ressourcen aufheben, wenn keine CPU-Änderungen mehr vorgenommen werden.

Die D3D11-Methode der Verwendung von [**map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (mit dem Parametersatz verwerfen) zum Umbenennen von Ressourcen wird in D3D12 nicht unterstützt. Anwendungen müssen das Umbenennen von Ressourcen implementieren. Alle  Zuordnungs Aufrufe sind implizit kein über \_ schreiben und Multithread. Es liegt in der Verantwortung der Anwendung, sicherzustellen, dass alle relevanten GPU-Aufgaben, die in den Befehlslisten enthalten sind, abgeschlossen sind, bevor der Datenzugriff mit der CPU D3D12 Aufrufe von **map** leeren keine impliziten Befehls Puffer, und es wird nicht blockiert, dass Sie warten, bis die GPU abgeschlossen ist. Daher können **map** und [**unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) in einigen Szenarios sogar optimiert werden.

## <a name="buffer-alignment"></a>Puffer Ausrichtung

Einschränkungen der Puffer Ausrichtung:

-   Das Kopieren von linearen unter Quellen muss auf 512 Byte ausgerichtet werden (wobei die Zeilengröße an D3D12- \_ Textur- \_ \_ datenpitch- \_ Ausrichtungs Bytes ausgerichtet ist).
-   Bei Konstanten Daten Lesevorgängen muss es sich um ein Vielfaches von 256 Bytes vom Anfang des Heaps handeln (d. h. nur aus Adressen, die 256 Byte ausrichten).
-   Indexdaten Lesevorgänge müssen ein Vielfaches der Größe des Index Datentyps sein (d. h. nur aus Adressen, die auf natürliche Weise für die Daten ausgerichtet sind).
-   [**ID3D12GraphicsCommandList::D rawinstanzierte**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) und [**ID3D12GraphicsCommandList::D rawindexedinstanzierten**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) Daten müssen aus Offsets stammen, die vielfachen von 4 sind (d. h. nur aus Adressen, die DWORD ausrichten).

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Untergeordnete Zuordnung innerhalb von Puffern](large-buffers.md)
</dt> </dl>

 

 