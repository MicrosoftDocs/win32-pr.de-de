---
title: Systeme mit mehreren Adaptern
description: Beschreibt die Unterstützung in Direct3D 12 für Systeme, auf denen mehrere Adapter installiert sind, und deckt Szenarien ab, in denen Ihre Anwendung explizit auf mehrere GPU-Adapter ausgerichtet ist, und Szenarien, in denen Treiber implizit mehrere GPU-Adapter im Auftrag Ihrer Anwendung verwenden.
ms.assetid: CC4C6594-D48F-40C1-93EE-9F98532BC038
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: e76c5c1295dab8858ff04830030efb479fe3ae8a09bcdb37ff8c4820f4fd08c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119728815"
---
# <a name="multi-adapter-systems"></a>Systeme mit mehreren Adaptern

Beschreibt die Unterstützung in Direct3D 12 für Systeme, auf denen mehrere Adapter installiert sind, und deckt Szenarien ab, in denen Ihre Anwendung explizit auf mehrere GPU-Adapter ausgerichtet ist, und Szenarien, in denen Treiber implizit mehrere GPU-Adapter im Auftrag Ihrer Anwendung verwenden.

## <a name="multi-adapter-overview"></a>Übersicht über mehrere Adapter

Ein GPU-Adapter kann ein beliebiger Adapter (Grafiken oder Compute, diskret oder integriert) eines beliebigen Herstellers sein, der Direct3D 12 unterstützt.

Auf mehrere Adapter wird als *Knoten* verwiesen. Eine Reihe von Elementen, z. B. die Warteschlangen, gelten für jeden Knoten. Wenn also zwei Knoten vorhanden sind, gibt es zwei standardmäßige 3D-Warteschlangen. Andere Elemente, z. B. der Pipelinezustand sowie Stamm- und Befehlssignaturen, können auf einen oder mehrere oder alle Knoten verweisen, wie im Diagramm dargestellt.

![Warteschlangen gelten für jeden Grafikkarten](images/multigpu.png)

## <a name="sharing-heaps-across-adapters"></a>Freigeben von Heaps über Adapter hinweg

Weitere Informationen finden Sie im Thema [Freigegebene Heaps.](shared-heaps.md)

## <a name="multi-adapter-apis-and-node-masks"></a>APIs mit mehreren Adaptern und Knotenmasken

Ähnlich wie bei früheren Direct3D-APIs wird jeder Satz von verknüpften Adaptern als einzelnes [**IDXGIAdapter3-Objekt**](/windows/win32/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) aufzählt. Alle Ausgaben, die an einen beliebigen Adapter im Link angefügt sind, werden als an das einzelne **IDXGIAdapter3-Objekt** angefügt aufgeführt.

Ihre Anwendung kann die Anzahl der physischen Adapter bestimmen, die einem bestimmten Gerät zugeordnet sind, indem [**SIE ID3D12Device::GetNodeCount**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount)aufrufen.

Viele APIs in Direct3D 12 akzeptieren eine *Knotenmaske* (eine Bitmaske), die den Knotensatz angibt, auf den der API-Aufruf verweist. Jeder Knoten verfügt über einen nullbasierten Index. In der Knotenmaske wird 0 jedoch in Bit 1 übersetzt. 1 wird in Bit 2 übersetzt; Und so weiter.

### <a name="single-nodes"></a>Einzelne Knoten

Beim Aufrufen der folgenden APIs (einzelner Knoten) gibt Ihre Anwendung einen einzelnen Knoten an, dem der API-Aufruf zugeordnet wird. In den meisten Jahren wird dies durch eine Knotenmaske angegeben. Jedes Bit in der Maske entspricht einem einzelnen Knoten. Für alle in diesem Abschnitt beschriebenen APIs müssen Sie genau ein Bit in der Knotenmaske festlegen.

-   [**D3D12 \_ COMMAND \_ QUEUE \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) : verfügt über einen *NodeMask-Member.*
-   [**CreateCommandQueue:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) Erstellt eine Warteschlange aus einer [**D3D12 \_ COMMAND QUEUE \_ \_ DESC-Struktur.**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc)
-   [**CreateCommandList:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) verwendet einen *nodeMask-Parameter.*
-   [**D3D12 \_ DESCRIPTOR \_ HEAP \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) : weist einen *NodeMask-Member* auf.
-   [**CreateDescriptorHeap:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap) Erstellt einen Deskriptorheap aus einer [**D3D12 \_ DESCRIPTOR \_ HEAP \_ DESC-Struktur.**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc)
-   [**D3D12 \_ QUERY \_ HEAP \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc) : weist einen *NodeMask-Member* auf.
-   [**CreateQueryHeap:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap) Erstellt einen Abfrageheap aus einer [**D3D12 \_ QUERY HEAP \_ \_ DESC-Struktur.**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc)

### <a name="multiple-nodes"></a>Mehrere Knoten

Beim Aufrufen der folgenden APIs (mehrere Knoten) gibt Ihre Anwendung eine Gruppe von Knoten an, denen der API-Aufruf zugeordnet wird. Sie geben Knotenaffinität als Knotenmaske an, wobei möglicherweise mehrere Bits festgelegt sind. Wenn Ihre Anwendung 0 für diese Bitmaske übergibt, konvertiert der Direct3D 12-Treiber diese in die Bitmaske 1 (was angibt, dass das Objekt Knoten 0 zugeordnet ist).

-   [**D3D12 \_ \_ \_ KNOTENÜBERGREIFENDER \_ FREIGABETARIF:**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier) Bestimmt die Unterstützung für knotenübergreifende Freigabe.
-   [**D3D12 \_ FEATURE \_ DATA \_ D3D12 \_ OPTIONS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : Struktur, die auf [**D3D12 \_ CROSS NODE SHARING \_ \_ \_ TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier)verweist.
-   [**D3D12 \_ FEATURE \_ DATA \_ ARCHITECTURE:**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture) enthält einen *NodeIndex-Member.*
-   [**D3D12 \_ GRAPHICS \_ PIPELINE \_ STATE \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) : weist einen *NodeMask-Member* auf.
-   [**CreateGraphicsPipelineState:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) Erstellt ein Grafikpipelinezustandsobjekt aus einer [**D3D12 \_ GRAPHICS PIPELINE STATE \_ \_ \_ DESC-Struktur.**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
-   [**D3D12 \_ COMPUTE \_ PIPELINE \_ STATE \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) : weist einen *NodeMask-Member* auf.
-   [**CreateComputePipelineState:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) Erstellt ein Computepipelinezustandsobjekt aus einer [**D3D12 \_ COMPUTE PIPELINE STATE \_ \_ \_ DESC-Struktur.**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
-   [**CreateRootSignature:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)verwendet einen *nodeMask-Parameter.*
-   [**D3D12 \_ COMMAND \_ SIGNATURE \_ DESC:**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc)weist einen *NodeMask-Member* auf.
-   [**CreateCommandSignature:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature) Erstellt ein Befehlssignaturobjekt aus einer [**D3D12 \_ COMMAND SIGNATURE \_ \_ DESC-Struktur.**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc)

### <a name="resource-creation-apis"></a>RESSOURCENERSTELLUNGS-APIs

Die folgenden APIs verweisen auf Knotenmasken.

-   [**D3D12 \_ HEAP \_ PROPERTIES**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties) : enthält sowohl *CreationNodeMask-* als auch *VisibleNodeMask-Member.*
-   [**GetResourceAllocationInfo:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo) weist einen *visibleMask-Parameter* auf.
-   [**GetCustomHeapProperties**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties) : verfügt über einen *nodeMask-Parameter.*

Beim Erstellen einer reservierten Ressource wird kein Knotenindex oder keine Knotenmaske angegeben. Die reservierte Ressource kann einem Heap auf einem beliebigen Knoten zugeordnet werden (gemäß den Regeln für die knotenübergreifende Freigabe).

Die [**MakeResident-Methode**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident) funktioniert intern mit Adapterwarteschlangen. Ihre Anwendung muss hierfür nichts angeben.

Beim Aufrufen der folgenden [**ID3D12Device-APIs**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) muss Ihre Anwendung keinen Knotensatz angeben, dem der API-Aufruf zugeordnet wird, da der API-Aufruf für alle Knoten gilt.

-   [**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
-   [**GetDescriptorHandleIncrementSize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
-   [**SetStablePowerState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
-   [**CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
-   [**CreateSampler**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsampler)
-   [**CopyDescriptors**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
-   [**CopyDescriptorsSimple**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
-   [**CreateSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
-   [**OpenSharedHandleByName**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
-   [**OpenSharedHandle:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle) mit einem *Fence* als Parameter. Bei einer *Ressource* oder einem *Heap* als Parameter akzeptiert diese Methode knoten nicht als Parameter, da Knotenmasken von zuvor erstellten Objekten geerbt werden.
-   [**CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
-   [**CreateConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [**CreateRenderTargetView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)
-   [**CreateUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
-   [**CreateDepthStencilView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdepthstencilview)
-   [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)

## <a name="related-topics"></a>Zugehörige Themen

[Direct3D 12-Programmieranleitung](directx-12-programming-guide.md)