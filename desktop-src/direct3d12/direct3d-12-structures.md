---
title: Kernstrukturen (Direct3D 12-Grafiken)
description: Die folgenden Strukturen werden in d3d12.h deklariert.
ms.assetid: 7FE8796A-98D1-4333-8755-2A47567460B3
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 2b748793cfdc1d2d74111cfb48e020108f32ec07
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436435"
---
# <a name="core-structures"></a>Core-Strukturen

Die folgenden Strukturen werden in d3d12.h deklariert.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema und Beschreibung |
|-|
| [**D3D12_AUTO_BREADCRUMB_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_auto_breadcrumb_node). Stellt DRED-Daten (Device Removed Extended Data) automatisch als Knoten in einer verknüpften Liste dar. |
| [**D3D12_BLEND_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc). Beschreibt den Blendzustand. |
| [**D3D12_BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box). Beschreibt ein 3D-Feld. |
| [**D3D12_BUFFER_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_rtv). Beschreibt die Elemente in einer Pufferressource, die in einer Renderzielansicht verwendet werden sollen. |
| [**D3D12_BUFFER_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_srv). Beschreibt die Elemente in einer Pufferressource, die in einer Shader-Ressourcenansicht verwendet werden sollen. |
| [**D3D12_BUFFER_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav). Beschreibt die Elemente in einem Puffer, die in einer Ansicht mit ungeordneten Zugriffen verwendet werden sollen. |
| [**D3D12_CACHED_PIPELINE_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state). Speichert einen Pipelinezustand. |
| [**D3D12_CLEAR_VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value). Beschreibt einen Wert, der zum Optimieren von clear-Vorgängen für eine bestimmte Ressource verwendet wird. |
| [**D3D12_COMMAND_QUEUE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_queue_desc). Beschreibt eine Befehlswarteschlange. |
| [**D3D12_COMMAND_SIGNATURE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc). Beschreibt die Argumente (Parameter) einer Befehlssignatur. |
| [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc). Beschreibt ein Computepipeline-Zustandsobjekt. |
| [**D3D12_CONSTANT_BUFFER_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc). Beschreibt einen anzuzeigende konstanten Puffer. |
| [**D3D12_CPU_DESCRIPTOR_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle). Beschreibt ein CPU-Deskriptorhandle. |
| [**D3D12_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc). Beschreibt den Tiefenschablonenzustand. |
| [**D3D12_DEPTH_STENCIL_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1). Beschreibt den Tiefenschablonenzustand. |
| [**D3D12_DEPTH_STENCIL_VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_value). Gibt einen Tiefen- und Schablonenwert an. |
| [**D3D12_DEPTH_STENCIL_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc). Beschreibt die Unterressourcen einer Textur, auf die über eine Tiefenschablonenansicht zugegriffen werden kann. |
| [**D3D12_DEPTH_STENCILOP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencilop_desc). Beschreibt Schablonenvorgänge, die basierend auf den Ergebnissen des Schablonentests ausgeführt werden können. |
| [**D3D12_DESCRIPTOR_HEAP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc). Beschreibt den Deskriptorheap. |
| [**D3D12_DESCRIPTOR_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range). Beschreibt einen Deskriptorbereich. |
| [**D3D12_DESCRIPTOR_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1). Beschreibt einen Deskriptorbereich mit Flags, um deren Flüchtigkeit zu bestimmen. |
| [**D3D12_DEVICE_REMOVED_EXTENDED_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data). Stellt Daten der Version 1.0 von DRED (Device Removed Extended Data) dar. |
| [**D3D12_DEVICE_REMOVED_EXTENDED_DATA1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data1). Stellt Geräteentfernungsdaten der Version 1.1 (Device Removed Extended Data, DRED) dar, sodass Debugger und Debuggererweiterungen auf DRED-Daten zugreifen können. |
| [**D3D12_DISCARD_REGION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region). Beschreibt Details für den Vorgang discard-resource. |
| [**D3D12_DISPATCH_ARGUMENTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dispatch_arguments). Beschreibt Dispatchparameter zur Verwendung durch den Compute-Shader. |
| [**D3D12_DRAW_ARGUMENTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_arguments). Beschreibt Parameter zum Zeichnen von -Instanzen. |
| [**D3D12_DRAW_INDEXED_ARGUMENTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_indexed_arguments). Beschreibt Parameter zum Zeichnen indizierter Instanzen. |
| [**D3D12_DRED_ALLOCATION_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dred_allocation_node). Beschreibt als Knoten in einer verknüpften Liste Daten zu einer Zuordnung, die von vom Gerät entfernten erweiterten Daten (DEVICE Removed Extended Data, DRED) nachverfolgt wird. |
| [**D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dred_auto_breadcrumbs_output). Enthält einen Zeiger auf den Kopf [](/windows/desktop/api/d3d12/ns-d3d12-d3d12_auto_breadcrumb_node) einer verknüpften Liste von D3D12_AUTO_BREADCRUMB_NODE-Objekten. Die Liste stellt den Auto breadcrumb-Zustand vor dem Entfernen des Geräts dar. |
| [**D3D12_DRED_PAGE_FAULT_OUTPUT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dred_page_fault_output). Beschreibt Zuordnungsdaten, die sich auf einen GPU-Seitenfehler an einer bestimmten virtuellen Adresse beziehen. |
| [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture). Geben Sie Details zur Adapterarchitektur an, damit Anwendungen bestimmte Adaptereigenschaften besser optimieren können. |
| [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1). Geben Sie Details zur Adapterarchitektur an, damit Anwendungen bestimmte Adaptereigenschaften besser optimieren können. |
| [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority). Beschreibt die Unterstützung des Adapters für die Priorisierung verschiedener Befehlswarteschlangentypen. |
| [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node). Gibt den Grad der Unterstützung für die Gemeinsame Nutzung von Ressourcen zwischen verschiedenen Adaptern an. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options). Beschreibt Direct3D 12-Featureoptionen im aktuellen Grafiktreiber. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1). Beschreibt den Grad der Unterstützung für HLSL 6.0-Wellenvorgänge. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2). Beschreibt die Unterstützung des Adapters für bestimmte optionale Features von Direct3D 12. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3). Wird verwendet, um den Grad der Unterstützung anzugeben, den der Adapter für optionale Features von Direct3D 12 bereitstellt. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4). Gibt den Grad der Unterstützung für MSAA-Texturen mit 64 KB, API-übergreifende Freigabe und native 16-Bit-Shadervorgänge an. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5). Gibt den Grad der Unterstützung an, den der Adapter für Renderdurchläufe, Die Ray-Ablaufverfolgung und shader-resource view tier 3-kachelte Ressourcen bereitstellt. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6). Gibt die Unterstützungsebene an, die der Adapter für die Schattierung variabler Raten (Variable Rate Shading, VRS) bereitstellt, und gibt an, ob die Hintergrundverarbeitung unterstützt wird oder nicht. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS7**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options7). Gibt die Unterstützungsebene an, die der Adapter für Mesh- und Amplification-Shader sowie für Samplerfeedback bereitstellt. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS8**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options8). Gibt an, ob nicht ausgerichtete blockkomprimierte Texturen unterstützt werden. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS9**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options9). Gibt an, ob Unterstützung für Mesh-Shader, Werte *von SV_RenderTargetArrayIndex* mit 8 oder höher, typisierte 64-Bit-Ganzzahl-Atomarzahlen für Ressourcen, ableitungs- und ableitungsabhängige Texturbeispielvorgänge und der Grad der Unterstützung für WaveMMA-Vorgänge (wave_matrix) vorhanden ist. |
| [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps). Wird verwendet, um zu bestimmen, ob der Adapter das Erstellen von Heaps aus vorhandenem Systemspeicher unterstützt. Solche Heaps sind nicht für die allgemeine Verwendung vorgesehen, sind aber für Diagnosezwecke besonders nützlich, da sie garantiert auch nach dem Fehler des Adapters beibehalten werden oder ein Ereignis zum Entfernen des Geräts auftritt. |
| [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels). Beschreibt Informationen zu den [Featureebenen,](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) die vom aktuellen Grafiktreiber unterstützt werden. |
| [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info). Beschreibt das DXGI-Datenformat. |
| [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support). Beschreibt, welche Ressourcen vom aktuellen Grafiktreiber für ein bestimmtes Format unterstützt werden. |
| [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support). Beschreibt die Einschränkungen des virtuellen GPU-Adressraums des Adapters, einschließlich der maximalen Adressbits pro Ressource und pro Prozess. |
| [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels). Beschreibt die Qualitätsebenen der Bilder für ein bestimmtes Format und die Stichprobenanzahl. |
| [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support). Gibt den Grad der Unterstützung für Sitzungen mit geschützten Ressourcen an. |
| [**D3D12_FEATURE_DATA_QUERY_META_COMMAND**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_query_meta_command). Gibt den Grad der Unterstützung an, den der Adapter für Metacommands bereitstellt. |
| [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature). Übergeben Sie diese Struktur an [**CheckFeatureSupport,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) um zu überprüfen, ob die Stammsignaturversion unterstützt wird. |
| [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_serialization). Gibt den Grad der Unterstützung für die Heapserialisierung an. |
| [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache). Beschreibt die Ebene der Shaderzwischenspeicherung, die im aktuellen Grafiktreiber unterstützt wird. |
| [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model). Enthält das unterstützte Shadermodell. |
| [**D3D12_GPU_DESCRIPTOR_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle). Beschreibt ein GPU-Deskriptorhandle. |
| [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc). Beschreibt ein Grafikpipelinezustandsobjekt. |
| [**D3D12_HEAP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc). Beschreibt einen Heap. |
| [**D3D12_HEAP_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties). Beschreibt Heapeigenschaften. |
| [**D3D12_INDEX_BUFFER_VIEW**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_index_buffer_view). Beschreibt den anzuzeigende Indexpuffer. |
| [**D3D12_INDIRECT_ARGUMENT_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc). Beschreibt ein indirektes Argument (einen indirekten Parameter) zur Verwendung mit einer Befehlssignatur. |
| [**D3D12_INPUT_ELEMENT_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_element_desc). Beschreibt ein einzelnes Element für die Eingabeassembliererphase der Grafikpipeline. |
| [**D3D12_INPUT_LAYOUT_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc). Beschreibt die Eingabepufferdaten für die Eingabeassembliererphase. |
| [**D3D12_MEMCPY_DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest). Beschreibt das Ziel eines Speicherkopiervorgangs. |
| [**D3D12_META_COMMAND_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_meta_command_desc). Beschreibt einen Metabefehl. |
| [**D3D12_META_COMMAND_PARAMETER_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_meta_command_parameter_desc). Beschreibt einen Parameter für einen Metabefehl. |
| [**D3D12_PACKED_MIP_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info). Beschreibt die Kachelstruktur einer gekachelten Ressource mit Mipmaps. |
| [**D3D12_PIPELINE_STATE_STREAM_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc). Beschreibt einen Pipelinezustandsstream. |
| [**D3D12_PLACED_SUBRESOURCE_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint). Beschreibt den Speicherbedarf einer platzierten Unterressource, einschließlich des Offsets und der D3D12_SUBRESOURCE_FOOTPRINT. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_protected_resource_session_desc). Beschreibt Flags für eine geschützte Ressourcensitzung pro Adapter. |
| [**D3D12_QUERY_DATA_PIPELINE_STATISTICS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_data_pipeline_statistics). Fragen Sie Informationen zur Grafikpipelineaktivität zwischen Aufrufen von [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) und [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)ab. |
| [**D3D12_QUERY_DATA_SO_STATISTICS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_data_so_statistics). Beschreibt Abfragedaten für die Streamausgabe. |
| [**D3D12_QUERY_HEAP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc). Beschreibt den Zweck eines Abfrageheaps. Ein Abfrageheap enthält ein Array einzelner Abfragen. |
| [**D3D12_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range). Beschreibt einen Speicherbereich. |
| [**D3D12_RANGE_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64). Beschreibt einen Speicherbereich in einem 64-Bit-Adressraum. |
| [**D3D12_RASTERIZER_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc). Beschreibt den Rasterizerzustand. |
| [**D3D12_RAYTRACING_AABB**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_aabb). Stellt ein an einer Achse ausgerichtetes Begrenzungsfeld (AABB) dar, das als Raytracinggeometrie verwendet wird. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_COMPACTED_SIZE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_compacted_size_desc). Beschreibt die Speicherplatzanforderungen für die Beschleunigungsstruktur nach der Komprimierung. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_CURRENT_SIZE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_current_size_desc). Beschreibt den Speicherplatz, der derzeit von einer Beschleunigungsstruktur verwendet wird. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_desc). Beschreibung der Postbuildinformationen, die aus einer Beschleunigungsstruktur generiert werden sollen. Verwenden Sie diese Struktur in Aufrufen von [**EmitRaytracingAccelerationStructurePostbuildInfo**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo) und [**BuildRaytracingAccelerationStructure**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_serialization_desc). Beschreibt die Größe und das Layout der serialisierten Beschleunigungsstruktur und des Headers. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TOOLS_VISUALIZATION_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_tools_visualization_desc). Beschreibt die Speicherplatzanforderungen für das Decodieren einer Beschleunigungsstruktur in ein Formular, das von Tools visualisiert werden kann. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_prebuild_info). Stellt Prebuildinformationen zu einer Raytracingbeschleunigungsstruktur dar. Rufen Sie [**getRaytracingAccelerationStructurePrebuildInfo**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device5-getraytracingaccelerationstructureprebuildinfo)auf, um eine Instanz dieser Struktur abzurufen. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_srv). Eine Shaderressourcenansichtsstruktur (SRV) zum Speichern einer Raytracingbeschleunigungsstruktur. |
| [**D3D12_RAYTRACING_GEOMETRY_AABBS_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_aabbs_desc). Beschreibt eine Reihe von an der Achse ausgerichteten Begrenzungsfeldern, die in der [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) verwendet werden, um Eingabedaten für einen Raytracingbeschleunigungsstruktur-Buildvorgang bereitzustellen. |
| [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc). Beschreibt einen Satz von Geometrie, der in der [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) verwendet wird, um Eingabedaten für einen Raytracingbeschleunigungsstrukturbuildvorgang bereitzustellen. |
| [**D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_triangles_desc). Beschreibt eine Gruppe von Dreiecken, die als Raytracinggeometrie verwendet werden. Die Geometrie, auf die diese Struktur zeigt, ist immer in Dreieckslistenform, indiziert oder nicht indiziert. Dreiecksstreifen werden nicht unterstützt. |
| [**D3D12_RAYTRACING_INSTANCE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_instance_desc). Beschreibt eine Instanz einer Raytracingbeschleunigungsstruktur, die während des Erstellungsprozesses der Beschleunigungsstruktur im GPU-Arbeitsspeicher verwendet wird. |
| [**D3D12_RAYTRACING_PIPELINE_CONFIG**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config). Ein Zustandsunterobjekt, das eine Raytracingpipelinekonfiguration darstellt. |
| [**D3D12_RAYTRACING_SHADER_CONFIG**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config). Ein Zustandsunterobjekt, das eine Shaderkonfiguration darstellt. |
| [**D3D12_RECT**](d3d12-rect.md). D3D12_RECT wird als RECT deklariert. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access). Beschreibt den Zugriff auf Ressourcen, die von einer Anwendung beim Übergang in einen Renderdurchlauf angefordert werden. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS_CLEAR_PARAMETERS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access_clear_parameters). Beschreibt den eindeutigen Wert, für den(n) Ressource(n) am Anfang eines Renderpasses löschen werden sollen. |
| [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc). Beschreibt eine Bindung (für die Dauer des Renderpasses festgelegt) an eine Tiefen-Schablonenansicht (Depth Stencil View, DSV) sowie deren Anfangs- und Endzugriffsmerkmale. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access). Beschreibt den Zugriff auf Ressourcen, die von einer Anwendung beim Übergang aus einem Renderpass angefordert werden. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access_resolve_parameters). Beschreibt eine Ressource, in die am Ende eines Renderpasses aufzulösen ist. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access_resolve_subresource_parameters). Beschreibt die Unterressourcen, die am Auflösen am Ende eines Renderpasses beteiligt sind. |
| [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc). Beschreibt Bindungen (für die Dauer des Renderpasses festgelegt) an eine oder mehrere Renderzielansichten (RTVs) sowie deren Anfangs- und Endzugriffsmerkmale. |
| [**D3D12_RENDER_TARGET_BLEND_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_blend_desc). Beschreibt den Überblendungszustand für ein Renderziel. |
| [**D3D12_RENDER_TARGET_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_view_desc). Beschreibt die Unterressourcen einer Ressource, auf die über eine Renderzielansicht zugegriffen werden kann. |
| [**D3D12_RESOURCE_ALIASING_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier). Beschreibt den Übergang zwischen der Verwendung von zwei verschiedenen Ressourcen, die Zuordnungen zum gleichen Heap haben. |
| [**D3D12_RESOURCE_ALLOCATION_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info). Beschreibt die Parameter, die zum Zuordnen von Ressourcen erforderlich sind. |
| [**D3D12_RESOURCE_ALLOCATION_INFO1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info1). Beschreibt parameter, die zum Zuordnen von Ressourcen erforderlich sind, einschließlich Offset. |
| [**D3D12_RESOURCE_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier). Beschreibt eine Ressourcenbarriere (Übergang bei der Ressourcennutzung). |
| [**D3D12_RESOURCE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc). Beschreibt eine Ressource, z. B. eine Textur. Diese Struktur wird häufig verwendet. |
| [**D3D12_RESOURCE_TRANSITION_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier). Beschreibt den Übergang von Unterressourcen zwischen verschiedenen Verwendungen. |
| [**D3D12_RESOURCE_UAV_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier). Stellt eine Ressource dar, in der alle UAV-Zugriffe abgeschlossen werden müssen, bevor zukünftige UAV-Zugriffe beginnen können. |
| [**D3D12_ROOT_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants). Beschreibt Konstanten inline in der Stammsignatur, die in Shadern als ein konstanter Puffer angezeigt werden. |
| [**D3D12_ROOT_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor). Beschreibt Inlinedeskriptoren in der Stammsignaturversion 1.0, die in Shadern angezeigt werden. |
| [**D3D12_ROOT_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1). Beschreibt Inlinedeskriptoren in der Stammsignaturversion 1.1, die in Shadern angezeigt werden. |
| [**D3D12_ROOT_DESCRIPTOR_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table). Beschreibt das Stammsignatur 1.0-Layout einer Deskriptortabelle als Auflistung von Deskriptorbereichen, die nacheinander in einem Deskriptorhap angezeigt werden. |
| [**D3D12_ROOT_DESCRIPTOR_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1). Beschreibt das Stammsignatur 1.1-Layout einer Deskriptortabelle als Auflistung von Deskriptorbereichen, die nacheinander in einem Deskriptorhap angezeigt werden. |
| [**D3D12_ROOT_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter). Beschreibt den Slot einer Stammsignaturversion 1.0. |
| [**D3D12_ROOT_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1). Beschreibt den Slot einer Stammsignaturversion 1.1. |
| [**D3D12_ROOT_SIGNATURE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc). Beschreibt das Layout einer Stammsignaturversion 1.0. |
| [**D3D12_ROOT_SIGNATURE_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1). Beschreibt das Layout einer Stammsignaturversion 1.1. |
| [**D3D12_RT_FORMAT_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array). Umschließt ein Array von Renderzielformaten. |
| [**D3D12_SAMPLE_POSITION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_sample_position). Beschreibt eine Unterpixel-Beispielposition für die Verwendung mit programmierbaren Beispielpositionen. |
| [**D3D12_SAMPLER_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc). Beschreibt einen Samplerzustand. |
| [**D3D12_SHADER_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode). Beschreibt Shaderdaten. |
| [**D3D12_SHADER_RESOURCE_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc). Beschreibt eine Shaderressourcenansicht. |
| [**D3D12_SO_DECLARATION_ENTRY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_so_declaration_entry). Beschreibt ein Scheitelpunktelement in einem Scheitelpunktpuffer in einem Ausgabeslot. |
| [**D3D12_STATIC_SAMPLER_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc). Beschreibt einen statischen Sampler. |
| [**D3D12_STREAM_OUTPUT_BUFFER_VIEW**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_buffer_view). Beschreibt einen Streamausgabepuffer. |
| [**D3D12_STREAM_OUTPUT_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc). Beschreibt einen Streamingausgabepuffer. |
| [**D3D12_SUBRESOURCE_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data). Beschreibt Unterressourcendaten. |
| [**D3D12_SUBRESOURCE_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint). Beschreibt format, width, height, depth und row-pitch der Unterressource in der übergeordneten Ressource. |
| [**D3D12_SUBRESOURCE_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info). Beschreibt Unterressourcendaten. |
| [**D3D12_SUBRESOURCE_RANGE_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64). Beschreibt einen Unterressourcenspeicherbereich. |
| [**D3D12_SUBRESOURCE_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling). Beschreibt ein gekacheltes Unterressourcenvolumen. |
| [**D3D12_TEX1D_ARRAY_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv). Beschreibt die Unterressourcen aus einem Array von 1D-Texturen, die in einer Tiefen-Schablonenansicht verwendet werden. |
| [**D3D12_TEX1D_ARRAY_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv). Beschreibt die Unterressourcen aus einem Array von 1D-Texturen, die in einer Renderzielansicht verwendet werden. |
| [**D3D12_TEX1D_ARRAY_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv). Beschreibt die Unterressourcen aus einem Array von 1D-Texturen, die in einer Shaderressourcenansicht verwendet werden. |
| [**D3D12_TEX1D_ARRAY_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav). Beschreibt ein Array von 1D-Texturressourcen mit ungeordneten Zugriffen. |
| [**D3D12_TEX1D_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv). Beschreibt die Unterressource aus einer 1D-Textur, die für eine Tiefen-Schablonenansicht zugänglich ist. |
| [**D3D12_TEX1D_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv). Beschreibt die Unterressource aus einer 1D-Textur, die in einer Renderzielansicht verwendet werden soll. |
| [**D3D12_TEX1D_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_srv). Gibt die Unterressource aus einer 1D-Textur an, die in einer Shaderressourcenansicht verwendet werden soll. |
| [**D3D12_TEX1D_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav). Beschreibt eine 1D-Texturressource mit ungeordneten Zugriffen. |
| [**D3D12_TEX2D_ARRAY_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv). Beschreibt die Unterressourcen aus einem Array von 2D-Texturen, auf die für eine Tiefen-Schablonenansicht zugegriffen werden kann. |
| [**D3D12_TEX2D_ARRAY_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv). Beschreibt die Unterressourcen aus einem Array von 2D-Texturen, die in einer Renderzielansicht verwendet werden. |
| [**D3D12_TEX2D_ARRAY_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv). Beschreibt die Unterressourcen aus einem Array von 2D-Texturen, die in einer Shaderressourcenansicht verwendet werden. |
| [**D3D12_TEX2D_ARRAY_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav). Beschreibt ein Array von 2D-Texturressourcen mit ungeordneten Zugriffen. |
| [**D3D12_TEX2D_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv). Beschreibt die Unterressource aus einer 2D-Textur, auf die eine Tiefenschablonenansicht zugreifen kann. |
| [**D3D12_TEX2D_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv). Beschreibt die Unterressource aus einer 2D-Textur, die in einer Renderzielansicht verwendet werden soll. |
| [**D3D12_TEX2D_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv). Beschreibt die Unterressource aus einer 2D-Textur, die in einer Shader-Ressourcenansicht verwendet werden soll. |
| [**D3D12_TEX2D_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav). Beschreibt eine 2D-Texturressource mit ungeordneten Zugriffen. |
| [**D3D12_TEX2DMS_ARRAY_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv). Beschreibt die Unterressourcen aus einem Array von 2D-Texturen mit mehreren Stichproben für eine Tiefenschablonenansicht. |
| [**D3D12_TEX2DMS_ARRAY_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv). Beschreibt die Unterressourcen aus einem Array von 2D-Texturen mit mehreren Stichproben, die in einer Renderzielansicht verwendet werden sollen. |
| [**D3D12_TEX2DMS_ARRAY_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv). Beschreibt die Unterressourcen aus einem Array von 2D-Texturen mit mehreren Stichproben, die in einer Shader-Ressourcenansicht verwendet werden sollen. |
| [**D3D12_TEX2DMS_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_dsv). Beschreibt die Unterressource aus einer 2D-Textur mit mehreren Stichproben, auf die eine Tiefenschablonenansicht zugreifen kann. |
| [**D3D12_TEX2DMS_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_rtv). Beschreibt die Unterressource aus einer 2D-Textur mit mehreren Stichproben, die in einer Renderzielansicht verwendet werden soll. |
| [**D3D12_TEX2DMS_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_srv). Beschreibt die Unterressourcen aus einer 2D-Textur mit mehreren Stichproben, die in einer Shader-Ressourcenansicht verwendet werden sollen. |
| [**D3D12_TEX3D_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv). Beschreibt die Unterressourcen aus einer 3D-Textur, die in einer Renderzielansicht verwendet werden sollen. |
| [**D3D12_TEX3D_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_srv). Beschreibt die Unterressourcen aus einer 3D-Textur, die in einer Shader-Ressourcenansicht verwendet werden sollen. |
| [**D3D12_TEX3D_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav). Beschreibt eine 3D-Texturressource mit ungeordneten Zugriffen. |
| [**D3D12_TEXCUBE_ARRAY_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_array_srv). Beschreibt die Unterressourcen aus einem Array von Cubetexturen, die in einer Shader-Ressourcenansicht verwendet werden sollen. |
| [**D3D12_TEXCUBE_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_srv). Beschreibt die Unterressource aus einer Cubetextur, die in einer Shader-Ressourcenansicht verwendet werden soll. |
| [**D3D12_TEXTURE_COPY_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location). Beschreibt einen Teil einer Textur zum Zweck von Texturkopien. |
| [**D3D12_TILE_REGION_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size). Beschreibt die Größe eines gekachelten Bereichs. |
| [**D3D12_TILE_SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape). Beschreibt die Form einer Kachel, indem ihre Dimensionen angegeben werden. |
| [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate). Beschreibt die Koordinaten einer gekachelten Ressource. |
| [**D3D12_UNORDERED_ACCESS_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc). Beschreibt die Unterressourcen einer Ressource, auf die über eine Ansicht mit ungeordneten Zugriff zugegriffen werden kann. |
| [**D3D12_VERTEX_BUFFER_VIEW**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view). Beschreibt eine Vertexpufferansicht. |
| [**D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_device_removed_extended_data). Stellt mit Versionsangaben erweiterte Daten (Device Removed Extended Data, DRED) dar, sodass Debugger und Debuggererweiterungen auf DRED-Daten zugreifen können. |
| [**D3D12_VERSIONED_ROOT_SIGNATURE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc). Enthält eine beliebige Version einer Stammsignaturbeschreibung und ist für die Verwendung mit Serialisierungs-/Deserialisierungsfunktionen konzipiert. |
| [**D3D12_VIEW_INSTANCE_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_view_instance_location). Gibt den Viewport/die Schablone und das Renderziel an, die einer Ansichtsinstanz zugeordnet sind. |
| [**D3D12_VIEW_INSTANCING_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_view_instancing_desc). Gibt Parameter an, die während der Konfiguration der Ansichtsinstanzierung verwendet werden. |
| [**D3D12_VIEWPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport). Beschreibt die Dimensionen eines Viewports. |
| [**D3D12_WRITEBUFFERIMMEDIATE_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_writebufferimmediate_parameter). Gibt den unmittelbaren Wert und die Zieladresse an, die mit [**ID3D12CommandList2::WriteBufferImmediate**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2)geschrieben wurden. |

## <a name="related-topics"></a>Zugehörige Themen

* [Kernreferenz](direct3d-12-core-reference.md)
* [Referenz für Direct3D 12](direct3d-12-reference.md)