---
title: Hilfsstrukturen für Direct3D 12
description: Diese Hilfsstrukturen helfen, viele der Direct3D 12-Strukturen zu initialisieren. Sie werden in `d3dx12.h` deklariert.
ms.assetid: 822CACCE-4A45-4104-91BD-4968A657662E
keywords:
- Hilfsstrukturen
- d3dx12.h
ms.localizationpriority: low
ms.topic: article
ms.date: 07/28/2021
ms.openlocfilehash: 16dfa0349a815a07db810d67c21747cb767f7c39
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812365"
---
# <a name="helper-structures-for-direct3d-12"></a>Hilfsstrukturen für Direct3D 12

Diese Hilfsstrukturen helfen, viele der Direct3D 12-Strukturen zu initialisieren. Sie werden in `d3dx12.h` deklariert.

`d3dx12.h` ist getrennt von den Direct3D 12-Headern verfügbar. Sie können unter `d3dx12.h` [The D3D12 Helper Library (Hilfsbibliothek D3D12) herunterladen.](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h)

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|-|-|
| [**CD3DX12_BLEND_DESC**](cd3dx12-blend-desc.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_BLEND_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_blend_desc) ermöglicht. |
| [**CD3DX12_BOX**](cd3dx12-box.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_BOX**](/windows/win32/api/d3d12/ns-d3d12-d3d12_box) ermöglicht. |
| [**CD3DX12_CLEAR_VALUE**](cd3dx12-clear-value.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_CLEAR_VALUE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_clear_value) ermöglicht. |
| [**CD3DX12_CPU_DESCRIPTOR_HANDLE**](cd3dx12-cpu-descriptor-handle.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_CPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) ermöglicht. |
| [**CD3DX12_DEFAULT**](cd3dx12-default.md) | Übergibt **D3D12_DEFAULT** an einen Konstruktor für jede Hilfsstruktur. Diese Struktur wird einfach als Mechanismus zum Festlegen von Standardparametern für die anderen Hilfsstrukturen verwendet. |
| [**CD3DX12_DEPTH_STENCIL_DESC**](cd3dx12-depth-stencil-desc.md) | Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12_DEPTH_STENCIL_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) zu ermöglichen. |
| [**CD3DX12_DEPTH_STENCIL_DESC1**](cd3dx12-depth-stencil-desc1.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_DEPTH_STENCIL_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) ermöglicht. |
| [**CD3DX12_DESCRIPTOR_RANGE**](cd3dx12-descriptor-range.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_DESCRIPTOR_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range) ermöglicht. |
| [**CD3DX12_DESCRIPTOR_RANGE1**](cd3dx12-descriptor-range1.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_DESCRIPTOR_RANGE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range1) ermöglicht. |
| [**CD3DX12_DXIL_LIBRARY_SUBOBJECT**](cd3dx12-dxil-library-subobject.md) | Eine Hilfsklasse zum Erstellen eines DXIL-Bibliothekszustandsunterobjekts. |
| [**CD3DX12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION**](cd3dx12-dxil-subobject-to-exports-association.md) | Eine Hilfsklasse zum Erstellen eines DXIL-subobject-to-exports-Zuordnungszustandsunterobjekts. |
| [**CD3DX12_EXISTING_COLLECTION_SUBOBJECT**](cd3dx12-existing-collection-subobject.md) | Eine Hilfsklasse zum Erstellen eines vorhandenen Auflistungszustands-Unterobjekts. |
| [**CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT**](cd3dx12-global-root-signature-subobject.md) | Eine Hilfsklasse zum Erstellen eines globalen Stammsignatur-Zustandsunterjektivs. |
| [**CD3DX12_GPU_DESCRIPTOR_HANDLE**](cd3dx12-gpu-descriptor-handle.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_GPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) ermöglicht. |
| [**CD3DX12_HEAP_DESC**](cd3dx12-heap-desc.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_HEAP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_desc) ermöglicht. |
| [**CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_HEAP_PROPERTIES**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties) ermöglicht. |
| [**CD3DX12_HIT_GROUP_SUBOBJECT**](cd3dx12-hit-group-subobject.md) | Eine Hilfsklasse zum Erstellen eines Treffergruppenzustands-Unterobjekts. |
| [**CD3DX12_NODE_MASK_SUBOBJECT**](cd3dx12-node-mask-subobject.md) | Eine Hilfsklasse zum Erstellen eines Zustandsunterobjekts, das die GPU-Knoten identifiziert, auf die das Zustandsobjekt angewendet wird. |
| [**CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT**](cd3dx12-local-root-signature-subobject.md) | Eine Hilfsklasse zum Erstellen eines Subjektivs für den lokalen Stammsignaturzustand. |
| [**CD3DX12_PACKED_MIP_INFO**](cd3dx12-packed-mip-info.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_PACKED_MIP_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_packed_mip_info) ermöglicht. |
| [**CD3DX12_PIPELINE_STATE_STREAM**](cd3dx12-pipeline-state-stream.md) | Eine Hilfsstruktur zum Erstellen und Arbeiten mit Grafik- und Computepipelinezuständen über eine kombinierte Schnittstelle. Siehe [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) und [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc). |
| [**CD3DX12_PIPELINE_STATE_STREAM1**](cd3dx12-pipeline-state-stream1.md) | Eine Hilfsstruktur zum Erstellen und Arbeiten mit Grafik- und Computepipelinezuständen über eine kombinierte Schnittstelle. Siehe [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) und [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc). |
| [**CD3DX12_PIPELINE_STATE_STREAM2**](cd3dx12-pipeline-state-stream2.md) | Eine Hilfsstruktur zum Erstellen und Arbeiten mit Grafik- und Computepipelinezuständen über eine kombinierte Schnittstelle. |
| [**CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC**](cd3dx12-pipeline-state-stream-blend-desc.md) | Eine Hilfsstruktur, die verwendet wird, um eine Blendbeschreibung als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. |
| [**CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO**](cd3dx12-pipeline-state-stream-cached-pso.md) | Eine Hilfsstruktur, die verwendet wird, um ein zwischengespeichertes PSO als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. |
| [**CD3DX12_PIPELINE_STATE_STREAM_CS**](cd3dx12-pipeline-state-stream-cs.md) | Eine Hilfsstruktur, die verwendet wird, um einen Compute-Shader als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL**](cd3dx12-pipeline-state-stream-depth-stencil.md) | Eine Hilfsstruktur, die verwendet wird, um eine Tiefen-Schablonenbeschreibung als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md) | Eine Hilfsstruktur, die verwendet wird, um eine Tiefen-Schablonenbeschreibung als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT**](cd3dx12-pipeline-state-stream-depth-stencil-format.md) | Eine Hilfsstruktur, die verwendet wird, um das Tiefen schablonenformat als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DS**](cd3dx12-pipeline-state-stream-ds.md) | Eine Hilfsstruktur, die verwendet wird, um einen Domänen-Shader als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. |
| [**CD3DX12_PIPELINE_STATE_STREAM_FLAGS**](cd3dx12-pipeline-state-stream-flags.md) | Eine Hilfsstruktur, die verwendet wird, um Pipelinezustandsflags als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. |
| [**CD3DX12_PIPELINE_STATE_STREAM_GS**](cd3dx12-pipeline-state-stream-gs.md) | Eine Hilfsstruktur, die verwendet wird, um einen Geometrie-Shader als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. |
| [**CD3DX12_PIPELINE_STATE_STREAM_HS**](cd3dx12-pipeline-state-stream-hs.md) | Eine Hilfsstruktur, die verwendet wird, um einen Hüllen-Shader als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. |
| [**CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE**](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md) | Eine Hilfsstruktur, die verwendet wird, um den Wert des Indexpufferstrips als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. |
| [**CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT**](cd3dx12-pipeline-state-stream-input-layout.md) | Eine Hilfsstruktur, die verwendet wird, um ein Eingabelayout als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. |
| [**CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK**](cd3dx12-pipeline-state-stream-node-mask.md) | Eine Hilfsstruktur, die verwendet wird, um eine Knotenmaske als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. |
| [**CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER**](cd3dx12-pipeline-state-stream-parse-helper.md) | Erstellt ein internes CD3DX12_PIPELINE_STATE_STREAM-Objekt aus Unterobjektdetails, die an die entsprechenden Memberfunktionen übergeben werden. Diese Struktur implementiert die [**ID3DX12PipelineParserCallbacks-Schnittstelle.**](id3dx12pipelineparsercallbacks.md) |
| [**CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY**](cd3dx12-pipeline-state-stream-primitive-topology.md) | Eine Hilfsstruktur, die verwendet wird, um die primitive Topologie als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. |
| [**CD3DX12_PIPELINE_STATE_STREAM_PS**](cd3dx12-pipeline-state-stream-ps.md) | Eine Hilfsstruktur, die verwendet wird, um einen Pixel-Shader als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. |
| [**CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER**](cd3dx12-pipeline-state-stream-rasterizer.md) | Eine Hilfsstruktur, die verwendet wird, um eine Rasterizerbeschreibung als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. |
| [**CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS**](cd3dx12-pipeline-state-stream-render-target-formats.md) | Eine Hilfsstruktur, die verwendet wird, um die Renderzielformate als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. |
| [**CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE**](cd3dx12-pipeline-state-stream-root-signature.md) | Eine Hilfsstruktur, die verwendet wird, um die Stammsignatur als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. |
| [**CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC**](cd3dx12-pipeline-state-stream-sample-desc.md) | Eine Hilfsstruktur, die verwendet wird, um eine Beispielbeschreibung als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. |
| [**CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK**](cd3dx12-pipeline-state-stream-sample-mask.md) | Eine Hilfsstruktur, die verwendet wird, um eine Beispielmaske als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. |
| [**CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT**](cd3dx12-pipeline-state-stream-stream-output.md) | Eine Hilfsstruktur, die verwendet wird, um die Streamausgabebeschreibung als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. |
| [**CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) | Eine Vorlagen-Hilfsstruktur, die verwendet wird, um Unterobjekttyp- und Unterobjektdatenpaare als einzelnes Objekt zu kapseln, das für eine Streambeschreibung geeignet ist. |
| [**CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING**](cd3dx12-pipeline-state-stream-view-instancing.md) | Eine Hilfsstruktur, die verwendet wird, um [eine](cd3dx12-view-instancing-desc.md) CD3DX12_VIEW_INSTANCING_DESC umschließen. Ermöglicht Shadern das Rendern in mehreren Ansichten mit einem einzigen Zeichnen-Aufruf. nützlich für die Stereosicht- oder Cubemapgenerierung. |
| [**CD3DX12_PIPELINE_STATE_STREAM_VS**](cd3dx12-pipeline-state-stream-vs.md) | Eine Hilfsstruktur, die verwendet wird, um einen Vertex-Shader als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist. |
| [**CD3DX12_RANGE**](cd3dx12-range.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range) ermöglicht. |
| [**CD3DX12_RANGE_UINT64**](cd3dx12-range-uint64.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range_uint64) ermöglicht. |
| [**CD3DX12_RASTERIZER_DESC**](cd3dx12-rasterizer-desc.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_RASTERIZER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) ermöglicht. |
| [**CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT**](cd3dx12-raytracing-pipeline-config-subobject.md) | Eine Hilfsklasse zum Erstellen eines Raytracing-Pipelinekonfigurationszustands-Unterobjekts. |
| [**CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT**](cd3dx12-raytracing-pipeline-config1-subobject.md) | Eine Hilfsklasse zum Erstellen eines Raytracing-Pipelinekonfigurationszustands-Unterobjekts mit Flags. |
| [**CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT**](cd3dx12-raytracing-shader-config-subobject.md) | Eine Hilfsklasse zum Erstellen eines Raytracing-Shaderkonfigurationszustands-Unterobjekts. |
| [**CD3DX12_RECT**](cd3dx12-rect.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_RECT**](d3d12-rect.md) ermöglicht. |
| [**CD3DX12_RESOURCE_ALLOCATION_INFO**](cd3dx12-resource-allocation-info.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_RESOURCE_ALLOCATION_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) ermöglicht. |
| [**CD3DX12_RESOURCE_BARRIER**](cd3dx12-resource-barrier.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_RESOURCE_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_barrier) ermöglicht. |
| [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_RESOURCE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc) ermöglicht. |
| [**CD3DX12_RESOURCE_DESC1**](cd3dx12-resource-desc1.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_RESOURCE_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1) ermöglicht. |
| [**CD3DX12_ROOT_CONSTANTS**](cd3dx12-root-constants.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_ROOT_CONSTANTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_constants) ermöglicht. |
| [**CD3DX12_ROOT_DESCRIPTOR**](cd3dx12-root-descriptor.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_ROOT_DESCRIPTOR**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor) ermöglicht. |
| [**CD3DX12_ROOT_DESCRIPTOR1**](cd3dx12-root-descriptor1.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_ROOT_DESCRIPTOR1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor1) ermöglicht. |
| [**CD3DX12_ROOT_DESCRIPTOR_TABLE**](cd3dx12-root-descriptor-table.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_ROOT_DESCRIPTOR_TABLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) ermöglicht. |
| [**CD3DX12_ROOT_DESCRIPTOR_TABLE1**](cd3dx12-root-descriptor-table1.md) | Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12_ROOT_DESCRIPTOR_TABLE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) zu ermöglichen. |
| [**CD3DX12_ROOT_PARAMETER**](cd3dx12-root-parameter.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_ROOT_PARAMETER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter) ermöglicht. |
| [**CD3DX12_ROOT_PARAMETER1**](cd3dx12-root-parameter1.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_ROOT_PARAMETER1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter1) ermöglicht. |
| [**CD3DX12_ROOT_SIGNATURE_DESC**](cd3dx12-root-signature-desc.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc) ermöglicht. |
| [**CD3DX12_RT_FORMAT_ARRAY**](cd3dx12-rt-format-array.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_RT_FORMAT_ARRAY**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rt_format_array) ermöglicht. |
| [**CD3DX12_SHADER_BYTECODE**](cd3dx12-shader-bytecode.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_SHADER_BYTECODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode) ermöglicht. |
| [**CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT**](cd3dx12-state-object-config-subobject.md) | Eine Hilfsklasse zum Erstellen eines Unterobjekts, das die allgemeinen Eigenschaften eines Zustandsobjekts definiert. |
| [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) | Die zentrale Klasse der D3DX12 State Object Creation Helpers, die Hilfsklassen zum Erstellen von Zustandsobjekten aus einem beliebigen Satz von Unterobjekten sind. |
| [**CD3DX12_STATIC_SAMPLER_DESC**](cd3dx12-static-sampler-desc.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_STATIC_SAMPLER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) ermöglicht. |
| [**CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT**](cd3dx12-subobject-to-exports-association-subobject.md) | Eine Hilfsklasse zum Erstellen eines Unterobjekts zum Exportieren eines Zuordnungszustandsunterobjekts. |
| [**CD3DX12_SUBRESOURCE_FOOTPRINT**](cd3dx12-subresource-footprint.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_SUBRESOURCE_FOOTPRINT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_footprint) ermöglicht. |
| [**CD3DX12_SUBRESOURCE_RANGE_UINT64**](cd3dx12-subresource-range-uint64.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_SUBRESOURCE_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) ermöglicht. |
| [**CD3DX12_SUBRESOURCE_TILING**](cd3dx12-subresource-tiling.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_SUBRESOURCE_TILING**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_tiling) ermöglicht. |
| [**CD3DX12_TEXTURE_COPY_LOCATION**](cd3dx12-texture-copy-location.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_TEXTURE_COPY_LOCATION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_texture_copy_location) ermöglicht. |
| [**CD3DX12_TILE_REGION_SIZE**](cd3dx12-tile-region-size.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_TILE_REGION_SIZE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_region_size) ermöglicht. |
| [**CD3DX12_TILE_SHAPE**](cd3dx12-tile-shape.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_TILE_SHAPE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_shape) ermöglicht. |
| [**CD3DX12_TILED_RESOURCE_COORDINATE**](cd3dx12-tiled-resource-coordinate.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) ermöglicht. |
| [**CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC**](cd3dx12-versioned-root-signature-desc.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_VERSIONED_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) ermöglicht. |
| [**CD3DX12_VIEW_INSTANCING_DESC**](cd3dx12-view-instancing-desc.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc) ermöglicht. |
| [**CD3DX12_VIEWPORT**](cd3dx12-viewport.md) | Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3D12_VIEWPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport) ermöglicht. |
| [**D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**](d3dx12-mesh-shader-pipeline-state-desc.md) | Für [Gitternetz-/Amplification-Shader](https://microsoft.github.io/DirectX-Specs/d3d/MeshShader.html)können Sie die Daten aus einem [EffectPipelineStateDescription-Objekt](https://github.com/Microsoft/DirectXTK12/wiki/EffectPipelineStateDescription)mit D3DX12_MESH_SHADER_PIPELINE_STATE_DESC **verwenden,** um den ganzen Zustand zur Verfügung zu stellen. |

## <a name="related-topics"></a>Zugehörige Themen

* [Hilfsstrukturen und -funktionen für D3D12](helper-structures-and-functions-for-d3d12.md)
* [Referenz zu Direct3D 12](direct3d-12-reference.md)
