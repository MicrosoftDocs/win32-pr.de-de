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
# <a name="uploading-texture-data-through-buffers"></a><span data-ttu-id="2273b-103">Hochladen von Textur Daten über Puffer</span><span class="sxs-lookup"><span data-stu-id="2273b-103">Uploading Texture Data Through Buffers</span></span>

<span data-ttu-id="2273b-104">Das Hochladen von 2D-oder 3D-Textur Daten ähnelt dem Hochladen von 1D-Daten, mit dem Unterschied, dass Anwendungen die Daten Ausrichtung im Zusammenhang mit der Zeilen Tonhöhe genauer berücksichtigen müssen.</span><span class="sxs-lookup"><span data-stu-id="2273b-104">Uploading 2D or 3D texture data is similar to uploading 1D data, except that applications need to pay closer attention to data alignment related to row pitch.</span></span> <span data-ttu-id="2273b-105">Puffer können von mehreren Teilen der Grafik Pipeline orthogonell und gleichzeitig verwendet werden und sind sehr flexibel.</span><span class="sxs-lookup"><span data-stu-id="2273b-105">Buffers can be used orthogonally and concurrently from multiple parts of the graphics pipeline, and are very flexible.</span></span>

-   [<span data-ttu-id="2273b-106">Hochladen von Textur Daten über Puffer</span><span class="sxs-lookup"><span data-stu-id="2273b-106">Upload Texture Data via Buffers</span></span>](#upload-texture-data-via-buffers)
-   [<span data-ttu-id="2273b-107">Wird kopiert</span><span class="sxs-lookup"><span data-stu-id="2273b-107">Copying</span></span>](#copying)
-   [<span data-ttu-id="2273b-108">Zuordnung und Zuordnung von Zuordnung</span><span class="sxs-lookup"><span data-stu-id="2273b-108">Mapping and unmapping</span></span>](#mapping-and-unmapping)
-   [<span data-ttu-id="2273b-109">Puffer Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="2273b-109">Buffer alignment</span></span>](#buffer-alignment)
-   [<span data-ttu-id="2273b-110">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2273b-110">Related topics</span></span>](#related-topics)

## <a name="upload-texture-data-via-buffers"></a><span data-ttu-id="2273b-111">Hochladen von Textur Daten über Puffer</span><span class="sxs-lookup"><span data-stu-id="2273b-111">Upload Texture Data via Buffers</span></span>

<span data-ttu-id="2273b-112">Anwendungen müssen Daten über [**ID3D12GraphicsCommandList:: copytextureregion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) oder [**ID3D12GraphicsCommandList:: copybufferregion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)hochladen.</span><span class="sxs-lookup"><span data-stu-id="2273b-112">Applications must upload data via [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) or [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion).</span></span> <span data-ttu-id="2273b-113">Textur Daten sind viel wahrscheinlicher größer, greifen auf wiederholt zu, und profitieren von der verbesserten Cache Kohärenz der nichtlinearen Speicher Layouts als bei anderen Ressourcen Daten.</span><span class="sxs-lookup"><span data-stu-id="2273b-113">Texture data is much more likely to be larger, accessed repeatedly, and benefit from the improved cache-coherency of non-linear memory layouts than other resource data.</span></span> <span data-ttu-id="2273b-114">Wenn Puffer in D3D12 verwendet werden, haben Anwendungen vollständige Kontrolle über die Platzierung und Anordnung von Daten, die dem Kopieren von Ressourcen Daten zugeordnet sind, sofern die Anforderungen an die Arbeitsspeicher Ausrichtung erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="2273b-114">When buffers are used in D3D12, applications have full control on data placement and arrangement associated with copying resource data around, as long as the memory alignment requirements are satisfied.</span></span>

<span data-ttu-id="2273b-115">Im Beispiel wird hervorgehoben, wo die Anwendung 2D-Daten einfach in 1D vereinfacht, bevor Sie in den Puffer platziert wird.</span><span class="sxs-lookup"><span data-stu-id="2273b-115">The sample highlights where the application simply flattens 2D data into 1D before placing it in the buffer.</span></span> <span data-ttu-id="2273b-116">Für das MipMap 2D-Szenario kann die Anwendung jede unter Ressource diskret vereinfachen und schnell einen 1D-unter Zuordnungs Algorithmus verwenden, oder Sie verwenden eine kompliziertere 2D-unter Zuordnungs Technik, um die Videospeicher Auslastung zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="2273b-116">For the mipmap 2D scenario, the application can either flatten each sub-resource discretely and quickly use a 1D sub-allocation algorithm, or, use a more complicated 2D sub-allocation technique to minimize video memory utilization.</span></span> <span data-ttu-id="2273b-117">Das erste Verfahren wird wahrscheinlich häufiger verwendet, da es einfacher ist.</span><span class="sxs-lookup"><span data-stu-id="2273b-117">The first technique is expected to be used more often as it is simpler.</span></span> <span data-ttu-id="2273b-118">Das zweite Verfahren kann nützlich sein, wenn Sie Daten auf einem Datenträger oder in einem Netzwerk verpacken.</span><span class="sxs-lookup"><span data-stu-id="2273b-118">The second technique may be useful when packing data onto a disk or across a network.</span></span> <span data-ttu-id="2273b-119">In beiden Fällen muss die Anwendung weiterhin die Kopier-APIs für jede unter Ressource abrufen.</span><span class="sxs-lookup"><span data-stu-id="2273b-119">In either case, the application must still call the copy APIs for each sub-resource.</span></span>

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

<span data-ttu-id="2273b-120">Beachten Sie die Verwendung der Hilfsstrukturen [**CD3DX12 \_ Heap \_ Eigenschaften**](cd3dx12-heap-properties.md) und [**CD3DX12 \_ Textur \_ Kopier \_ Speicherort**](cd3dx12-texture-copy-location.md)sowie die Methoden " [**kreatecommittedresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) " und " [**copytextureregion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)".</span><span class="sxs-lookup"><span data-stu-id="2273b-120">Note the use of the helper structures [**CD3DX12\_HEAP\_PROPERTIES**](cd3dx12-heap-properties.md) and [**CD3DX12\_TEXTURE\_COPY\_LOCATION**](cd3dx12-texture-copy-location.md), and the methods [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) and [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).</span></span>

## <a name="copying"></a><span data-ttu-id="2273b-121">Wird kopiert</span><span class="sxs-lookup"><span data-stu-id="2273b-121">Copying</span></span>

<span data-ttu-id="2273b-122">D3D12-Methoden ermöglichen es Anwendungen, die anfänglichen Daten D3D11 [**updatesubresource**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource), [**copysubresourceregion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion)und Resource zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="2273b-122">D3D12 methods enable applications to replace D3D11 [**UpdateSubresource**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource), [**CopySubresourceRegion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion), and resource initial data.</span></span> <span data-ttu-id="2273b-123">Eine einzelne 3D-unter Quelle, die Zeilen haupttextur-Daten enthält, befindet sich möglicherweise in Puffer Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="2273b-123">A single 3D subresource worth of row-major texture data may be located in buffer resources.</span></span> <span data-ttu-id="2273b-124">[**Copytextureregion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) kann diese Textur Daten aus dem Puffer in eine Textur Ressource mit einem unbekannten Textur Layout kopieren (und umgekehrt).</span><span class="sxs-lookup"><span data-stu-id="2273b-124">[**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) can copy that texture data from the buffer to a texture resource with an unknown texture layout, and vice versa.</span></span> <span data-ttu-id="2273b-125">Anwendungen sollten diese Art von Technik bevorzugen, um häufig verwendete GPU-Ressourcen aufzufüllen, indem große Puffer in einem uploadheap erstellt werden, während die häufig verwendeten GPU-Ressourcen in einem Standard Heap erstellt werden, der keinen CPU-Zugriff hat.</span><span class="sxs-lookup"><span data-stu-id="2273b-125">Applications should prefer this type of technique to populate frequently accessed GPU resources, by creating large buffers in an UPLOAD heap while creating the frequently accessed GPU resources in a DEFAULT heap that has no CPU access.</span></span> <span data-ttu-id="2273b-126">Eine solche Technik unterstützt auf effiziente Weise diskrete GPUs und ihre große Menge an CPU-ungenügenden Arbeitsspeicher, ohne dass die UMA-Architekturen häufig beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="2273b-126">Such a technique efficiently supports discrete GPUs and their large amounts of CPU-inaccessible memory, without commonly impairing UMA architectures.</span></span>

<span data-ttu-id="2273b-127">Beachten Sie die folgenden zwei Konstanten:</span><span class="sxs-lookup"><span data-stu-id="2273b-127">Note the following two constants:</span></span>

``` syntax
const UINT D3D12_TEXTURE_DATA_PITCH_ALIGNMENT = 256;
const UINT D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT = 512;
```

-   [<span data-ttu-id="2273b-128">**D3D12 Ressourcen \_ \_ Bedarf**</span><span class="sxs-lookup"><span data-stu-id="2273b-128">**D3D12\_SUBRESOURCE\_FOOTPRINT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
-   [<span data-ttu-id="2273b-129">**D3D12 Speicherort der untergeordneten \_ \_ Quelle \_**</span><span class="sxs-lookup"><span data-stu-id="2273b-129">**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)
-   [<span data-ttu-id="2273b-130">**Speicherort der D3D12- \_ Textur \_ Kopie \_**</span><span class="sxs-lookup"><span data-stu-id="2273b-130">**D3D12\_TEXTURE\_COPY\_LOCATION**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
-   [<span data-ttu-id="2273b-131">**D3D12 \_ Textur \_ \_ kopierungstyp**</span><span class="sxs-lookup"><span data-stu-id="2273b-131">**D3D12\_TEXTURE\_COPY\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)
-   [<span data-ttu-id="2273b-132">**ID3D12Device:: getcopyablefootprints**</span><span class="sxs-lookup"><span data-stu-id="2273b-132">**ID3D12Device::GetCopyableFootprints**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
-   [<span data-ttu-id="2273b-133">**ID3D12GraphicsCommandList:: copyresource**</span><span class="sxs-lookup"><span data-stu-id="2273b-133">**ID3D12GraphicsCommandList::CopyResource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [<span data-ttu-id="2273b-134">**ID3D12GraphicsCommandList:: copytextureregion**</span><span class="sxs-lookup"><span data-stu-id="2273b-134">**ID3D12GraphicsCommandList::CopyTextureRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [<span data-ttu-id="2273b-135">**ID3D12GraphicsCommandList:: copybufferregion**</span><span class="sxs-lookup"><span data-stu-id="2273b-135">**ID3D12GraphicsCommandList::CopyBufferRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [<span data-ttu-id="2273b-136">**ID3D12GraphicsCommandList:: copytiles**</span><span class="sxs-lookup"><span data-stu-id="2273b-136">**ID3D12GraphicsCommandList::CopyTiles**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [<span data-ttu-id="2273b-137">**ID3D12CommandQueue:: updatetilemappings**</span><span class="sxs-lookup"><span data-stu-id="2273b-137">**ID3D12CommandQueue::UpdateTileMappings**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)

## <a name="mapping-and-unmapping"></a><span data-ttu-id="2273b-138">Zuordnung und Zuordnung von Zuordnung</span><span class="sxs-lookup"><span data-stu-id="2273b-138">Mapping and unmapping</span></span>

<span data-ttu-id="2273b-139">[**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) und [**unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) können von mehreren Threads sicher aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2273b-139">[**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) can be called by multiple threads safely.</span></span> <span data-ttu-id="2273b-140">Der erste Befehl von **map** ordnet einen virtuellen CPU-Adressbereich für die Ressource zu.</span><span class="sxs-lookup"><span data-stu-id="2273b-140">The first call to **Map** allocates a CPU virtual address range for the resource.</span></span> <span data-ttu-id="2273b-141">Der letzte aufzurufende aufrufungs Befehl hebt die Zuordnung des virtuellen CPU-Adress **Bereichs auf.**</span><span class="sxs-lookup"><span data-stu-id="2273b-141">The last call to **Unmap** deallocates the CPU virtual address range.</span></span> <span data-ttu-id="2273b-142">Die virtuelle CPU-Adresse wird in der Regel an die Anwendung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2273b-142">The CPU virtual address is commonly returned to the application.</span></span>

<span data-ttu-id="2273b-143">Jedes Mal, wenn Daten zwischen CPU und GPU über Ressourcen in den rückgängig-Heaps übermittelt werden, müssen [**map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) und [**unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) zur Unterstützung aller Systeme verwendet werden D3D12 wird unter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2273b-143">Whenever data is passed between the CPU and GPU through resources in readback heaps, [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) must be used to support all systems D3D12 is supported on.</span></span> <span data-ttu-id="2273b-144">Wenn Sie die Bereiche so eng wie möglich halten, wird die Effizienz der Systeme maximiert, die Bereiche erfordern (siehe [**D3D12 \_ Range**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).</span><span class="sxs-lookup"><span data-stu-id="2273b-144">Keeping the ranges as tight as possible maximizes efficiency on the systems that require ranges (refer to [**D3D12\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).</span></span>

<span data-ttu-id="2273b-145">Die Leistung der Debuggingtools profitiert nicht nur von der exakten Verwendung von Bereichen in allen Zuordnungs Aufrufen von [**Karten**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)  /  [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) , sondern auch von Anwendungen, die die Zuordnung von Ressourcen aufheben, wenn keine CPU-Änderungen mehr vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="2273b-145">The performance of debugging tools benefit not only from the accurate usage of ranges on all [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) / [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) calls, but also from applications unmapping resources when CPU modifications will no longer be made.</span></span>

<span data-ttu-id="2273b-146">Die D3D11-Methode der Verwendung von [**map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (mit dem Parametersatz verwerfen) zum Umbenennen von Ressourcen wird in D3D12 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2273b-146">The D3D11 method of using [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (with the DISCARD parameter set) to rename resources is not supported in D3D12.</span></span> <span data-ttu-id="2273b-147">Anwendungen müssen das Umbenennen von Ressourcen implementieren.</span><span class="sxs-lookup"><span data-stu-id="2273b-147">Applications must implement resource renaming themselves.</span></span> <span data-ttu-id="2273b-148">Alle  Zuordnungs Aufrufe sind implizit kein über \_ schreiben und Multithread.</span><span class="sxs-lookup"><span data-stu-id="2273b-148">All **Map** calls are implicitly NO\_OVERWRITE and multi-threaded.</span></span> <span data-ttu-id="2273b-149">Es liegt in der Verantwortung der Anwendung, sicherzustellen, dass alle relevanten GPU-Aufgaben, die in den Befehlslisten enthalten sind, abgeschlossen sind, bevor der Datenzugriff mit der CPU</span><span class="sxs-lookup"><span data-stu-id="2273b-149">It is the application’s responsibility to ensure that any relevant GPU work contained in command lists is finished before the accessing data with the CPU.</span></span> <span data-ttu-id="2273b-150">D3D12 Aufrufe von **map** leeren keine impliziten Befehls Puffer, und es wird nicht blockiert, dass Sie warten, bis die GPU abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="2273b-150">D3D12 calls to **Map** do not implicitly flush any command buffers, nor do they block waiting for the GPU to finish work.</span></span> <span data-ttu-id="2273b-151">Daher können **map** und [**unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) in einigen Szenarios sogar optimiert werden.</span><span class="sxs-lookup"><span data-stu-id="2273b-151">As a result, **Map** and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) may even be optimized out in some scenarios.</span></span>

## <a name="buffer-alignment"></a><span data-ttu-id="2273b-152">Puffer Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="2273b-152">Buffer alignment</span></span>

<span data-ttu-id="2273b-153">Einschränkungen der Puffer Ausrichtung:</span><span class="sxs-lookup"><span data-stu-id="2273b-153">Buffer alignment restrictions:</span></span>

-   <span data-ttu-id="2273b-154">Das Kopieren von linearen unter Quellen muss auf 512 Byte ausgerichtet werden (wobei die Zeilengröße an D3D12- \_ Textur- \_ \_ datenpitch- \_ Ausrichtungs Bytes ausgerichtet ist).</span><span class="sxs-lookup"><span data-stu-id="2273b-154">Linear subresource copying must be aligned to 512 bytes (with the row pitch aligned to D3D12\_TEXTURE\_DATA\_PITCH\_ALIGNMENT bytes).</span></span>
-   <span data-ttu-id="2273b-155">Bei Konstanten Daten Lesevorgängen muss es sich um ein Vielfaches von 256 Bytes vom Anfang des Heaps handeln (d. h. nur aus Adressen, die 256 Byte ausrichten).</span><span class="sxs-lookup"><span data-stu-id="2273b-155">Constant data reads must be a multiple of 256 bytes from the beginning of the heap (i.e. only from addresses that are 256-byte aligned).</span></span>
-   <span data-ttu-id="2273b-156">Indexdaten Lesevorgänge müssen ein Vielfaches der Größe des Index Datentyps sein (d. h. nur aus Adressen, die auf natürliche Weise für die Daten ausgerichtet sind).</span><span class="sxs-lookup"><span data-stu-id="2273b-156">Index data reads must be a multiple of the index data type size (i.e. only from addresses that are naturally aligned for the data).</span></span>
-   <span data-ttu-id="2273b-157">[**ID3D12GraphicsCommandList::D rawinstanzierte**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) und [**ID3D12GraphicsCommandList::D rawindexedinstanzierten**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) Daten müssen aus Offsets stammen, die vielfachen von 4 sind (d. h. nur aus Adressen, die DWORD ausrichten).</span><span class="sxs-lookup"><span data-stu-id="2273b-157">[**ID3D12GraphicsCommandList::DrawInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) and [**ID3D12GraphicsCommandList::DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) data must be from offsets that are multiples of 4 (i.e. only from addresses that are DWORD aligned).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2273b-158">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2273b-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2273b-159">Untergeordnete Zuordnung innerhalb von Puffern</span><span class="sxs-lookup"><span data-stu-id="2273b-159">Suballocation Within Buffers</span></span>](large-buffers.md)
</dt> </dl>

 

 