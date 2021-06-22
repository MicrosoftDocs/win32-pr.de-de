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
# <a name="uploading-texture-data-through-buffers"></a><span data-ttu-id="11f1c-103">Hochladen von Texturdaten über Puffer</span><span class="sxs-lookup"><span data-stu-id="11f1c-103">Uploading Texture Data Through Buffers</span></span>

<span data-ttu-id="11f1c-104">Das Hochladen von 2D- oder 3D-Texturdaten ähnelt dem Hochladen von 1D-Daten, mit der Ausnahme, dass Anwendungen die Datenausrichtung im Zusammenhang mit der Zeilenhöhe genauer beachten müssen.</span><span class="sxs-lookup"><span data-stu-id="11f1c-104">Uploading 2D or 3D texture data is similar to uploading 1D data, except that applications need to pay closer attention to data alignment related to row pitch.</span></span> <span data-ttu-id="11f1c-105">Puffer können orthogonal und gleichzeitig aus mehreren Teilen der Grafikpipeline verwendet werden und sind sehr flexibel.</span><span class="sxs-lookup"><span data-stu-id="11f1c-105">Buffers can be used orthogonally and concurrently from multiple parts of the graphics pipeline, and are very flexible.</span></span>

-   [<span data-ttu-id="11f1c-106">Hochladen von Texturdaten über Puffer</span><span class="sxs-lookup"><span data-stu-id="11f1c-106">Upload Texture Data via Buffers</span></span>](#upload-texture-data-via-buffers)
-   [<span data-ttu-id="11f1c-107">Wird kopiert</span><span class="sxs-lookup"><span data-stu-id="11f1c-107">Copying</span></span>](#copying)
-   [<span data-ttu-id="11f1c-108">Zuordnung und Entmapping</span><span class="sxs-lookup"><span data-stu-id="11f1c-108">Mapping and unmapping</span></span>](#mapping-and-unmapping)
-   [<span data-ttu-id="11f1c-109">Pufferausrichtung</span><span class="sxs-lookup"><span data-stu-id="11f1c-109">Buffer alignment</span></span>](#buffer-alignment)
-   [<span data-ttu-id="11f1c-110">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="11f1c-110">Related topics</span></span>](#related-topics)

## <a name="upload-texture-data-via-buffers"></a><span data-ttu-id="11f1c-111">Hochladen von Texturdaten über Puffer</span><span class="sxs-lookup"><span data-stu-id="11f1c-111">Upload Texture Data via Buffers</span></span>

<span data-ttu-id="11f1c-112">Anwendungen müssen Daten über [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) oder [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)hochladen.</span><span class="sxs-lookup"><span data-stu-id="11f1c-112">Applications must upload data via [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) or [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion).</span></span> <span data-ttu-id="11f1c-113">Texturdaten sind viel wahrscheinlicher größer, greifen wiederholt darauf zu und profitieren von der verbesserten Cachekoherität von nicht linearen Speicherlayouts als andere Ressourcendaten.</span><span class="sxs-lookup"><span data-stu-id="11f1c-113">Texture data is much more likely to be larger, accessed repeatedly, and benefit from the improved cache-coherency of non-linear memory layouts than other resource data.</span></span> <span data-ttu-id="11f1c-114">Wenn Puffer in D3D12 verwendet werden, haben Anwendungen vollständige Kontrolle über die Datenplatzierung und Anordnung im Zusammenhang mit dem Kopieren von Ressourcendaten, solange die Anforderungen an die Arbeitsspeicherausrichtung erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="11f1c-114">When buffers are used in D3D12, applications have full control on data placement and arrangement associated with copying resource data around, as long as the memory alignment requirements are satisfied.</span></span>

<span data-ttu-id="11f1c-115">Im Beispiel wird hervorgehoben, wo die Anwendung 2D-Daten einfach in 1D vereinfacht, bevor sie im Puffer platziert werden.</span><span class="sxs-lookup"><span data-stu-id="11f1c-115">The sample highlights where the application simply flattens 2D data into 1D before placing it in the buffer.</span></span> <span data-ttu-id="11f1c-116">Für das Mipmap-2D-Szenario kann die Anwendung entweder jede untergeordnete Ressource diskret abschwächen und schnell einen 1D-Algorithmus für die untergeordnete Zuordnung verwenden oder eine kompliziertere 2D-Unterzuordnungsmethode verwenden, um die Videospeicherauslastung zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="11f1c-116">For the mipmap 2D scenario, the application can either flatten each sub-resource discretely and quickly use a 1D sub-allocation algorithm, or, use a more complicated 2D sub-allocation technique to minimize video memory utilization.</span></span> <span data-ttu-id="11f1c-117">Es wird erwartet, dass die erste Technik häufiger verwendet wird, da sie einfacher ist.</span><span class="sxs-lookup"><span data-stu-id="11f1c-117">The first technique is expected to be used more often as it is simpler.</span></span> <span data-ttu-id="11f1c-118">Die zweite Technik kann beim Packen von Daten auf einem Datenträger oder über ein Netzwerk nützlich sein.</span><span class="sxs-lookup"><span data-stu-id="11f1c-118">The second technique may be useful when packing data onto a disk or across a network.</span></span> <span data-ttu-id="11f1c-119">In beiden Fällen muss die Anwendung weiterhin die Kopier-APIs für jede Unterressource aufrufen.</span><span class="sxs-lookup"><span data-stu-id="11f1c-119">In either case, the application must still call the copy APIs for each sub-resource.</span></span>

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

<span data-ttu-id="11f1c-120">Beachten Sie die Verwendung der Hilfsstrukturen [**CD3DX12 \_ HEAP \_ PROPERTIES**](cd3dx12-heap-properties.md) und [**CD3DX12 \_ TEXTURE COPY \_ \_ LOCATION**](cd3dx12-texture-copy-location.md)und die Methoden [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) und [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).</span><span class="sxs-lookup"><span data-stu-id="11f1c-120">Note the use of the helper structures [**CD3DX12\_HEAP\_PROPERTIES**](cd3dx12-heap-properties.md) and [**CD3DX12\_TEXTURE\_COPY\_LOCATION**](cd3dx12-texture-copy-location.md), and the methods [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) and [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).</span></span>

## <a name="copying"></a><span data-ttu-id="11f1c-121">Wird kopiert</span><span class="sxs-lookup"><span data-stu-id="11f1c-121">Copying</span></span>

<span data-ttu-id="11f1c-122">D3D12-Methoden ermöglichen Es Anwendungen, D3D11 [**UpdateSubresource,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource) [**CopySubresourceRegion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion)und Ressourcen-Anfangsdaten zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="11f1c-122">D3D12 methods enable applications to replace D3D11 [**UpdateSubresource**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource), [**CopySubresourceRegion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion), and resource initial data.</span></span> <span data-ttu-id="11f1c-123">Eine einzelne 3D-Unterressource mit Zeilen-Haupttexturdaten kann sich in Pufferressourcen befinden.</span><span class="sxs-lookup"><span data-stu-id="11f1c-123">A single 3D subresource worth of row-major texture data may be located in buffer resources.</span></span> <span data-ttu-id="11f1c-124">[**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) kann diese Texturdaten aus dem Puffer in eine Texturressource mit unbekanntem Texturlayout kopieren und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="11f1c-124">[**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) can copy that texture data from the buffer to a texture resource with an unknown texture layout, and vice versa.</span></span> <span data-ttu-id="11f1c-125">Anwendungen sollten diese Art von Technik bevorzugen, um häufig genutzte GPU-Ressourcen aufzufüllen, indem große Puffer in einem UPLOAD-Heap erstellt werden, während die häufig verwendeten GPU-Ressourcen in einem DEFAULT-Heap ohne CPU-Zugriff erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="11f1c-125">Applications should prefer this type of technique to populate frequently accessed GPU resources, by creating large buffers in an UPLOAD heap while creating the frequently accessed GPU resources in a DEFAULT heap that has no CPU access.</span></span> <span data-ttu-id="11f1c-126">Eine solche Technik unterstützt diskrete GPUs und deren große Mengen an cpu-unzugänglichem Arbeitsspeicher effizient, ohne dass UMA-Architekturen häufig beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="11f1c-126">Such a technique efficiently supports discrete GPUs and their large amounts of CPU-inaccessible memory, without commonly impairing UMA architectures.</span></span>

<span data-ttu-id="11f1c-127">Beachten Sie die folgenden beiden Konstanten:</span><span class="sxs-lookup"><span data-stu-id="11f1c-127">Note the following two constants:</span></span>

``` syntax
const UINT D3D12_TEXTURE_DATA_PITCH_ALIGNMENT = 256;
const UINT D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT = 512;
```

-   [<span data-ttu-id="11f1c-128">**D3D12 \_ SUBRESOURCE \_ FOOTPRINT**</span><span class="sxs-lookup"><span data-stu-id="11f1c-128">**D3D12\_SUBRESOURCE\_FOOTPRINT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
-   [<span data-ttu-id="11f1c-129">**D3D12 \_ \_ PLATZIERTER \_ SUBRESOURCE-SPEICHERBEDARF**</span><span class="sxs-lookup"><span data-stu-id="11f1c-129">**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)
-   [<span data-ttu-id="11f1c-130">**D3D12 \_ TEXTURE \_ COPY \_ LOCATION**</span><span class="sxs-lookup"><span data-stu-id="11f1c-130">**D3D12\_TEXTURE\_COPY\_LOCATION**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
-   [<span data-ttu-id="11f1c-131">**D3D12 \_ TEXTURE \_ COPY \_ TYPE**</span><span class="sxs-lookup"><span data-stu-id="11f1c-131">**D3D12\_TEXTURE\_COPY\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)
-   [<span data-ttu-id="11f1c-132">**ID3D12Device::GetCopyableFootprints**</span><span class="sxs-lookup"><span data-stu-id="11f1c-132">**ID3D12Device::GetCopyableFootprints**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
-   [<span data-ttu-id="11f1c-133">**ID3D12GraphicsCommandList::CopyResource**</span><span class="sxs-lookup"><span data-stu-id="11f1c-133">**ID3D12GraphicsCommandList::CopyResource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [<span data-ttu-id="11f1c-134">**ID3D12GraphicsCommandList::CopyTextureRegion**</span><span class="sxs-lookup"><span data-stu-id="11f1c-134">**ID3D12GraphicsCommandList::CopyTextureRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [<span data-ttu-id="11f1c-135">**ID3D12GraphicsCommandList::CopyBufferRegion**</span><span class="sxs-lookup"><span data-stu-id="11f1c-135">**ID3D12GraphicsCommandList::CopyBufferRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [<span data-ttu-id="11f1c-136">**ID3D12GraphicsCommandList::CopyTiles**</span><span class="sxs-lookup"><span data-stu-id="11f1c-136">**ID3D12GraphicsCommandList::CopyTiles**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [<span data-ttu-id="11f1c-137">**ID3D12CommandQueue::UpdateTileMappings**</span><span class="sxs-lookup"><span data-stu-id="11f1c-137">**ID3D12CommandQueue::UpdateTileMappings**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)

## <a name="mapping-and-unmapping"></a><span data-ttu-id="11f1c-138">Zuordnung und Entmapping</span><span class="sxs-lookup"><span data-stu-id="11f1c-138">Mapping and unmapping</span></span>

<span data-ttu-id="11f1c-139">[**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) und [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) können sicher von mehreren Threads aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="11f1c-139">[**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) can be called by multiple threads safely.</span></span> <span data-ttu-id="11f1c-140">Der erste Aufruf von **Map** ordnet einen virtuellen CPU-Adressbereich für die Ressource zu.</span><span class="sxs-lookup"><span data-stu-id="11f1c-140">The first call to **Map** allocates a CPU virtual address range for the resource.</span></span> <span data-ttu-id="11f1c-141">Der letzte Aufruf von **Zuordnung** aufheben hebt die Zuordnung des virtuellen CPU-Adressbereichs auf.</span><span class="sxs-lookup"><span data-stu-id="11f1c-141">The last call to **Unmap** deallocates the CPU virtual address range.</span></span> <span data-ttu-id="11f1c-142">Die virtuelle CPU-Adresse wird häufig an die Anwendung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="11f1c-142">The CPU virtual address is commonly returned to the application.</span></span>

<span data-ttu-id="11f1c-143">Wenn Daten zwischen CPU und GPU über Ressourcen in Rückleseheaps übergeben werden, müssen [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) und [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) verwendet werden, um alle Systeme zu unterstützen, auf der D3D12 unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="11f1c-143">Whenever data is passed between the CPU and GPU through resources in readback heaps, [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) must be used to support all systems D3D12 is supported on.</span></span> <span data-ttu-id="11f1c-144">Wenn Die Bereiche so eng wie möglich gehalten werden, wird die Effizienz der Systeme maximiert, die Bereiche erfordern (siehe [**D3D12 \_ RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).</span><span class="sxs-lookup"><span data-stu-id="11f1c-144">Keeping the ranges as tight as possible maximizes efficiency on the systems that require ranges (refer to [**D3D12\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).</span></span>

<span data-ttu-id="11f1c-145">Die Leistung von Debugtools profitiert nicht nur von [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)der genauen Nutzung von Bereichen bei allen  /  [**Zuordnungs-Unmap-Aufrufen,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) sondern auch von Anwendungen, die Ressourcen aufheben, wenn CPU-Änderungen nicht mehr vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="11f1c-145">The performance of debugging tools benefit not only from the accurate usage of ranges on all [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) / [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) calls, but also from applications unmapping resources when CPU modifications will no longer be made.</span></span>

<span data-ttu-id="11f1c-146">Die D3D11-Methode zur Verwendung von [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (mit festgelegter DISCARD-Parameter) zum Umbenennen von Ressourcen wird in D3D12 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="11f1c-146">The D3D11 method of using [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (with the DISCARD parameter set) to rename resources is not supported in D3D12.</span></span> <span data-ttu-id="11f1c-147">Anwendungen müssen das Umbenennen von Ressourcen selbst implementieren.</span><span class="sxs-lookup"><span data-stu-id="11f1c-147">Applications must implement resource renaming themselves.</span></span> <span data-ttu-id="11f1c-148">Alle  Zuordnungsaufrufe sind implizit NO \_ OVERWRITE und Multithreading.</span><span class="sxs-lookup"><span data-stu-id="11f1c-148">All **Map** calls are implicitly NO\_OVERWRITE and multi-threaded.</span></span> <span data-ttu-id="11f1c-149">Es liegt in der Verantwortung der Anwendung, sicherzustellen, dass alle relevanten GPU-Aufgaben in Befehlslisten abgeschlossen sind, bevor der Zugriff auf Daten mit der CPU abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="11f1c-149">It is the application’s responsibility to ensure that any relevant GPU work contained in command lists is finished before the accessing data with the CPU.</span></span> <span data-ttu-id="11f1c-150">D3D12-Aufrufe von **Map** leeren weder implizit Befehlspuffer, noch blockieren sie das Warten auf den Abschluss der Arbeit durch die GPU.</span><span class="sxs-lookup"><span data-stu-id="11f1c-150">D3D12 calls to **Map** do not implicitly flush any command buffers, nor do they block waiting for the GPU to finish work.</span></span> <span data-ttu-id="11f1c-151">Daher können **Map** und [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) in einigen Szenarien sogar optimiert werden.</span><span class="sxs-lookup"><span data-stu-id="11f1c-151">As a result, **Map** and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) may even be optimized out in some scenarios.</span></span>

## <a name="buffer-alignment"></a><span data-ttu-id="11f1c-152">Pufferausrichtung</span><span class="sxs-lookup"><span data-stu-id="11f1c-152">Buffer alignment</span></span>

<span data-ttu-id="11f1c-153">Einschränkungen bei der Pufferausrichtung:</span><span class="sxs-lookup"><span data-stu-id="11f1c-153">Buffer alignment restrictions:</span></span>

-   <span data-ttu-id="11f1c-154">Das lineare Kopieren von Unterressourcen muss auf 512 Byte ausgerichtet sein (wobei die Zeilenhöhe an D3D12 TEXTURE DATA PITCH ALIGNMENT Bytes ausgerichtet \_ \_ \_ \_ ist).</span><span class="sxs-lookup"><span data-stu-id="11f1c-154">Linear subresource copying must be aligned to 512 bytes (with the row pitch aligned to D3D12\_TEXTURE\_DATA\_PITCH\_ALIGNMENT bytes).</span></span>
-   <span data-ttu-id="11f1c-155">Konstante Datenlesedaten müssen ein Vielfaches von 256 Bytes vom Anfang des Heaps sein (d. h. nur von Adressen, die 256 Byte ausgerichtet sind).</span><span class="sxs-lookup"><span data-stu-id="11f1c-155">Constant data reads must be a multiple of 256 bytes from the beginning of the heap (i.e. only from addresses that are 256-byte aligned).</span></span>
-   <span data-ttu-id="11f1c-156">Indexdatenleseungen müssen ein Vielfaches der Größe des Indexdatentyps sein (d. h. nur von Adressen, die natürlich für die Daten ausgerichtet sind).</span><span class="sxs-lookup"><span data-stu-id="11f1c-156">Index data reads must be a multiple of the index data type size (i.e. only from addresses that are naturally aligned for the data).</span></span>
-   <span data-ttu-id="11f1c-157">[**ID3D12GraphicsCommandList::ExecuteIndirect-Daten**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) müssen aus Offsets stammen, die ein Vielfaches von 4 sind (d.h. nur von Adressen, die DWORD ausgerichtet sind).</span><span class="sxs-lookup"><span data-stu-id="11f1c-157">[**ID3D12GraphicsCommandList::ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) data must be from offsets that are multiples of 4 (i.e. only from addresses that are DWORD aligned).</span></span>

## <a name="related-topics"></a><span data-ttu-id="11f1c-158">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="11f1c-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11f1c-159">Unterzuweisung innerhalb von Puffern</span><span class="sxs-lookup"><span data-stu-id="11f1c-159">Suballocation Within Buffers</span></span>](large-buffers.md)
</dt> </dl>

 

 
