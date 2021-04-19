---
title: Kern Strukturen (Direct3D 12-Grafiken)
description: Die folgenden Strukturen werden in d3d12. h deklariert.
ms.assetid: 7FE8796A-98D1-4333-8755-2A47567460B3
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 456ca501426142182d9823427c7d13599e4a92db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339907"
---
# <a name="core-structures"></a>Core-Strukturen

Die folgenden Strukturen werden in d3d12. h deklariert.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema und Beschreibung |
|-|
| [**D3D12_AUTO_BREADCRUMB_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_auto_breadcrumb_node). Stellt die durch das Gerät entfernten Daten der erweiterten Daten (Dred) als Knoten in einer verknüpften Liste dar. |
| [**D3D12_BLEND_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc). Beschreibt den Blend-Zustand. |
| [**D3D12_BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box). Beschreibt ein 3D-Feld. |
| [**D3D12_BUFFER_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_rtv). Beschreibt die Elemente in einer Puffer Ressource, die in einer renderzielansicht verwendet werden sollen. |
| [**D3D12_BUFFER_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_srv). Beschreibt die Elemente in einer Puffer Ressource, die in einer Shader-Resource-Ansicht verwendet werden soll. |
| [**D3D12_BUFFER_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav). Beschreibt die Elemente in einem Puffer, die in einer Ansicht mit ungeordneten Zugriffen verwendet werden sollen. |
| [**D3D12_CACHED_PIPELINE_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state). Speichert einen Pipeline Zustand. |
| [**D3D12_CLEAR_VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value). Beschreibt einen Wert, der zum Optimieren von Lösch Vorgängen für eine bestimmte Ressource verwendet wird. |
| [**D3D12_COMMAND_QUEUE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_queue_desc). Beschreibt eine Befehls Warteschlange. |
| [**D3D12_COMMAND_SIGNATURE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc). Beschreibt die Argumente (Parameter) einer Befehls Signatur. |
| [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc). Beschreibt ein Zustands Objekt der COMPUTE-Pipeline. |
| [**D3D12_CONSTANT_BUFFER_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc). Beschreibt einen konstanten Puffer, der angezeigt werden soll. |
| [**D3D12_CPU_DESCRIPTOR_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle). Beschreibt ein CPU-Deskriptorhandle. |
| [**D3D12_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc). Beschreibt den Status der tiefen Schablone. |
| [**D3D12_DEPTH_STENCIL_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1). Beschreibt den Status der tiefen Schablone. |
| [**D3D12_DEPTH_STENCIL_VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_value). Gibt einen tiefen-und Schablonen Wert an. |
| [**D3D12_DEPTH_STENCIL_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc). Beschreibt die unter Ressourcen einer Textur, auf die von einer Ansicht der tiefen Schablone aus zugegriffen werden kann. |
| [**D3D12_DEPTH_STENCILOP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencilop_desc). Beschreibt die Vorgänge, die auf der Grundlage der Ergebnisse des Schablonen Tests ausgeführt werden können. |
| [**D3D12_DESCRIPTOR_HEAP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc). Beschreibt den deskriptorheap. |
| [**D3D12_DESCRIPTOR_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range). Beschreibt einen Deskriptorbereich. |
| [**D3D12_DESCRIPTOR_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1). Beschreibt einen Deskriptorbereich mit Flags zum Bestimmen der Volatilität. |
| [**D3D12_DEVICE_REMOVED_EXTENDED_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data). Stellt die vom Gerät entfernten erweiterten Daten (Dred) Version 1,0-Daten dar. |
| [**D3D12_DEVICE_REMOVED_EXTENDED_DATA1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data1). Stellt vom Gerät entfernte erweiterte Daten (Dred), Version 1,1, Geräte Entfernungs Daten dar, sodass Debugger und Debugger-Erweiterungen auf Dred Data zugreifen können. |
| [**D3D12_DISCARD_REGION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region). Beschreibt Details für den Vorgang zum Verwerfen von Ressourcen. |
| [**D3D12_DISPATCH_ARGUMENTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dispatch_arguments). Beschreibt dispatchparameter für die Verwendung durch den Compute-Shader. |
| [**D3D12_DRAW_ARGUMENTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_arguments). Beschreibt Parameter für das Zeichnen von Instanzen. |
| [**D3D12_DRAW_INDEXED_ARGUMENTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_indexed_arguments). Beschreibt Parameter zum Zeichnen indizierter Instanzen. |
| [**D3D12_DRED_ALLOCATION_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dred_allocation_node). Beschreibt als Knoten in einer verknüpften Liste Daten zu einer Zuordnung, die vom Gerät nachverfolgt wurden, entfernte erweiterte Daten (Dred). |
| [**D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dred_auto_breadcrumbs_output). Enthält einen Zeiger auf den Anfang einer verknüpften Liste von [D3D12_AUTO_BREADCRUMB_NODE](/windows/desktop/api/d3d12/ns-d3d12-d3d12_auto_breadcrumb_node) -Objekten. Die Liste stellt den Auto-Breadcrumb-Zustand vor dem Entfernen des Geräts dar. |
| [**D3D12_DRED_PAGE_FAULT_OUTPUT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dred_page_fault_output). Beschreibt Zuordnungs Daten im Zusammenhang mit einem GPU-Seiten Fehler für eine bestimmte virtuelle Adresse (VA). |
| [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture). Geben Sie Details zur Adapter Architektur an, um Anwendungen bei bestimmten Adapter Eigenschaften besser zu optimieren. |
| [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1). Geben Sie Details zur Adapter Architektur an, um Anwendungen bei bestimmten Adapter Eigenschaften besser zu optimieren. |
| [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority). Erläutert die Unterstützung der Adapter für die Priorisierung verschiedener Befehls Warteschlangen Typen. |
| [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node). Gibt die Ebene der Unterstützung für die gemeinsame Nutzung von Ressourcen zwischen verschiedenen Adaptern an. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options). Beschreibt Direct3D 12-Funktions Optionen im aktuellen Grafiktreiber. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1). Beschreibt die Ebene der Unterstützung für HLSL 6,0-Wellen Vorgänge. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2). Erläutert die Unterstützung der Adapter für bestimmte optionale Features von Direct3D 12. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3). Wird verwendet, um die Unterstützungs Ebene anzugeben, die der Adapter für optionale Features von Direct3D 12 bereitstellt. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4). Gibt die Ebene der Unterstützung für MSAA-Texturen (64 KB), die API-übergreifende Freigabe und systemeigene 16-Bit-Shader-Vorgänge an. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5). Gibt die Ebene der Unterstützung an, die der Adapter für die Kacheln von Rendering, Ray Tracing und Shader-Resource View Tier 3 enthält. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6). Gibt die Ebene der Unterstützung an, die der Adapter für das Schattieren von Variablen Sätzen (VRS) bereitstellt, und gibt an, ob die Hintergrundverarbeitung unterstützt wird. |
| [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps). Wird verwendet, um zu bestimmen, ob der Adapter das Erstellen von Heaps aus vorhandenem Systemspeicher unterstützt. Solche Heaps sind nicht für die allgemeine Verwendung gedacht, aber Sie sind für Diagnosezwecke besonders nützlich, da Sie sicher sind, dass Sie dauerhaft gespeichert werden, auch wenn der Adapter Fehler aufweist oder ein Geräte Entfernungs Ereignis auftritt. |
| [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels). Beschreibt Informationen zu den [Funktionsebenen](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) , die vom aktuellen Grafiktreiber unterstützt werden. |
| [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info). Beschreibt das DXGI-Datenformat. |
| [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support). Beschreibt, welche Ressourcen vom aktuellen Grafiktreiber für ein bestimmtes Format unterstützt werden. |
| [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support). Erläutert die Einschränkungen für den virtuellen GPU-Adressraum des Adapters, einschließlich der maximalen Adress Bits pro Ressource und pro Prozess. |
| [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels). Beschreibt die Bild Qualitäts Ebenen für ein bestimmtes Format und eine bestimmte Anzahl von Stichproben. |
| [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support). Gibt die Ebene der Unterstützung für geschützte Ressourcen Sitzungen an. |
| [**D3D12_FEATURE_DATA_QUERY_META_COMMAND**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_query_meta_command). Gibt den Grad der Unterstützung an, den der Adapter für Metacommands bereitstellt. |
| [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature). Übergeben Sie diese Struktur an [**checkfeaturesupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) , um die Unterstützung der Stamm Signatur Version zu überprüfen. |
| [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_serialization). Gibt die Ebene der Unterstützung für die Heap-Serialisierung an. |
| [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache). Beschreibt die Ebene der Shader-Zwischenspeicherung, die im aktuellen Grafiktreiber unterstützt wird. |
| [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model). Enthält das unterstützte Shader-Modell. |
| [**D3D12_GPU_DESCRIPTOR_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle). Beschreibt ein GPU-Deskriptorhandle. |
| [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc). Beschreibt ein Grafik Pipeline-Zustands Objekt. |
| [**D3D12_HEAP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc). Beschreibt einen Heap. |
| [**D3D12_HEAP_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties). Beschreibt Heap Eigenschaften. |
| [**D3D12_INDEX_BUFFER_VIEW**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_index_buffer_view). Beschreibt den Index Puffer, der angezeigt werden soll. |
| [**D3D12_INDIRECT_ARGUMENT_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc). Beschreibt ein indirektes Argument (einen indirekten Parameter) zur Verwendung mit einer Befehls Signatur. |
| [**D3D12_INPUT_ELEMENT_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_element_desc). Beschreibt ein einzelnes-Element für die Eingabe-Assembler-Phase der Grafik Pipeline. |
| [**D3D12_INPUT_LAYOUT_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc). Beschreibt die Eingabepuffer Daten für die Eingabe-Assembler-Stufe. |
| [**D3D12_MEMCPY_DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest). Beschreibt das Ziel eines Speicher Kopiervorgangs. |
| [**D3D12_META_COMMAND_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_meta_command_desc). Beschreibt einen Meta-Befehl. |
| [**D3D12_META_COMMAND_PARAMETER_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_meta_command_parameter_desc). Beschreibt einen Parameter für einen Meta-Befehl. |
| [**D3D12_PACKED_MIP_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info). Beschreibt die Kachel Struktur einer gekachelten Ressource mit Mipmaps. |
| [**D3D12_PIPELINE_STATE_STREAM_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc). Beschreibt einen Pipeline Zustandsdaten Strom. |
| [**D3D12_PLACED_SUBRESOURCE_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint). Beschreibt den Speicherbedarf einer untergeordneten Quelle, einschließlich Offset und D3D12_SUBRESOURCE_FOOTPRINT. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_protected_resource_session_desc). Beschreibt Flags für eine geschützte Ressourcen Sitzung pro Adapter. |
| [**D3D12_QUERY_DATA_PIPELINE_STATISTICS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_data_pipeline_statistics). Abfrage Informationen zur Grafik Pipeline Aktivität zwischen Aufrufen von [**beginquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) und [**endquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery). |
| [**D3D12_QUERY_DATA_SO_STATISTICS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_data_so_statistics). Beschreibt Abfrage Daten für die Datenstrom Ausgabe. |
| [**D3D12_QUERY_HEAP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc). Beschreibt den Zweck eines Abfrage Heaps. Ein Abfrage Heap enthält ein Array einzelner Abfragen. |
| [**D3D12_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range). Beschreibt einen Speicherbereich. |
| [**D3D12_RANGE_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64). Beschreibt einen Speicherbereich in einem 64-Bit-Adressraum. |
| [**D3D12_RASTERIZER_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc). Beschreibt den Status des Rasterizers. |
| [**D3D12_RAYTRACING_AABB**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_aabb). Stellt ein an einer Achse ausgerichtetes Begrenzungsfeld (aabb) dar, das als Raytracing Geometry verwendet wird. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_COMPACTED_SIZE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_compacted_size_desc). Beschreibt die Speicherplatzanforderungen für die Beschleunigungs Struktur nach der Komprimierung. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_CURRENT_SIZE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_current_size_desc). Beschreibt den Speicherplatz, der derzeit von einer Beschleunigungs Struktur verwendet wird. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_desc). Beschreibung der postbuildinformationen, die aus einer Beschleunigungs Struktur generiert werden sollen. Verwenden Sie diese Struktur in Aufrufen von [**emitraytracingaccelerationstructurepostbuildinfo**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo) und [**buildraytracingaccelerationstructure**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_serialization_desc). Beschreibt die Größe und das Layout der serialisierten Beschleunigungs Struktur und des Headers. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TOOLS_VISUALIZATION_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_tools_visualization_desc). Beschreibt den Speicherplatz, der für das Decodieren einer Beschleunigungs Struktur in ein Formular erforderlich ist, das von Tools visualisiert werden kann. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_prebuild_info). Stellt vorbuildinformationen über eine Raytracing-Beschleunigungs Struktur dar. Rufen Sie eine Instanz dieser Stuktur durch Aufrufen von " [**traytracingaccelerationstructureprebuildinfo**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device5-getraytracingaccelerationstructureprebuildinfo)" ab. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_srv). Eine SRV-Struktur (Shader Resource View) zum Speichern einer Raytracing-Beschleunigungs Struktur. |
| [**D3D12_RAYTRACING_GEOMETRY_AABBS_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_aabbs_desc). Beschreibt eine Reihe von Achsen ausgerichteten Begrenzungs Feldern, die in der [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) Struktur verwendet werden, um Eingabedaten für einen Buildvorgang der Raytracing-Beschleunigungs Struktur bereitzustellen. |
| [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc). Beschreibt einen Satz von Geometrie, der in der [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) -Struktur verwendet wird, um Eingabedaten für einen Buildvorgang der Raytracing-Beschleunigungs Struktur bereitzustellen. |
| [**D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_triangles_desc). Beschreibt eine Reihe von Dreiecken, die als Raytracing-Geometrie verwendet werden. Die Geometrie, auf die von dieser Struktur verwiesen wird, ist immer in einer Dreiecks Liste, indiziert oder nicht indiziert. Dreiecks Streifen werden nicht unterstützt. |
| [**D3D12_RAYTRACING_INSTANCE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_instance_desc). Beschreibt eine Instanz einer Raytracing-Beschleunigungs Struktur, die während des Buildprozesses der Beschleunigungs Struktur im GPU-Speicher verwendet wird. |
| [**D3D12_RAYTRACING_PIPELINE_CONFIG**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config). Ein Zustands Objekt, das eine Raytracing-Pipeline Konfiguration darstellt. |
| [**D3D12_RAYTRACING_SHADER_CONFIG**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config). Ein Zustands Objekt, das eine shaderkonfiguration darstellt. |
| [**D3D12_RECT**](d3d12-rect.md). D3D12_RECT wird als "Rect" deklariert. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access). Beschreibt den Zugriff auf Ressourcen, die von einer Anwendung beim Übergang in einen renderdurchlauf angefordert werden. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS_CLEAR_PARAMETERS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access_clear_parameters). Beschreibt den eindeutigen Wert, auf den Ressourcen am Anfang eines Renderpass-Werts gelöscht werden sollen. |
| [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc). Beschreibt eine Bindung (für die Dauer des Renderpass) mit einer tiefen Schablonen Ansicht (DSV) sowie deren Anfangs-und endzugriffsmerkmale. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access). Beschreibt den Zugriff auf Ressourcen, die von einer Anwendung beim Übergang aus einem renderdurchlauf angefordert werden. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access_resolve_parameters). Beschreibt eine Ressource, die beim Abschluss eines Renderpass aufgelöst werden soll. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access_resolve_subresource_parameters). Beschreibt die unter Ressourcen, die an der Auflösung am Ende eines Renderpass beteiligt sind. |
| [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc). Beschreibt Bindungen (für die Dauer des Renderpass) für eine oder mehrere renderzielsichten (rtvs) sowie deren Anfangs-und endzugriffsmerkmale. |
| [**D3D12_RENDER_TARGET_BLEND_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_blend_desc). Beschreibt den Blend-Zustand für ein Renderziel. |
| [**D3D12_RENDER_TARGET_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_view_desc). Beschreibt die unter Ressourcen aus einer Ressource, auf die über eine renderzielsicht zugegriffen werden kann. |
| [**D3D12_RESOURCE_ALIASING_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier). Beschreibt den Übergang zwischen der Verwendung von zwei verschiedenen Ressourcen, die Zuordnungen in denselben Heap haben. |
| [**D3D12_RESOURCE_ALLOCATION_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info). Beschreibt die zum Zuordnen von Ressourcen erforderlichen Parameter. |
| [**D3D12_RESOURCE_ALLOCATION_INFO1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info1). Beschreibt die Parameter, die zum Zuordnen von Ressourcen erforderlich sind, einschließlich Offset. |
| [**D3D12_RESOURCE_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier). Beschreibt eine Ressourcen Barriere (Übergang bei der Ressourcenverwendung). |
| [**D3D12_RESOURCE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc). Beschreibt eine Ressource, z. b. eine Textur. Diese Struktur wird ausgiebig verwendet. |
| [**D3D12_RESOURCE_TRANSITION_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier). Beschreibt den Übergang von unter Ressourcen zwischen unterschiedlichen Verwendungen. |
| [**D3D12_RESOURCE_UAV_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier). Stellt eine Ressource dar, in der alle UAV-Zugriffe vollständig ausgeführt werden müssen, bevor zukünftige UAV-Zugriffe beginnen können. |
| [**D3D12_ROOT_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants). Beschreibt Konstanten Inline in der Stamm Signatur, die in Shadern als ein konstanter Puffer angezeigt werden. |
| [**D3D12_ROOT_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor). Beschreibt Deskriptoren Inline in der Stamm Signatur Version 1,0, die in Shadern angezeigt werden. |
| [**D3D12_ROOT_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1). Beschreibt Deskriptoren Inline in der Stamm Signatur Version 1,1, die in Shadern angezeigt werden. |
| [**D3D12_ROOT_DESCRIPTOR_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table). Beschreibt das Layout der Stamm Signatur 1,0 einer Deskriptortabelle als eine Auflistung von Deskriptorbereichen, die in einem deskriptorheap nacheinander angezeigt werden. |
| [**D3D12_ROOT_DESCRIPTOR_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1). Beschreibt das Layout der Stamm Signatur 1,1 einer Deskriptortabelle als eine Auflistung von Deskriptorbereichen, die in einem deskriptorheap nacheinander angezeigt werden. |
| [**D3D12_ROOT_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter). Beschreibt den Slot einer Stamm Signatur Version 1,0. |
| [**D3D12_ROOT_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1). Beschreibt den Slot einer Stamm Signatur Version 1,1. |
| [**D3D12_ROOT_SIGNATURE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc). Beschreibt das Layout einer Stamm Signatur Version 1,0. |
| [**D3D12_ROOT_SIGNATURE_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1). Beschreibt das Layout einer Stamm Signatur Version 1,1. |
| [**D3D12_RT_FORMAT_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array). Umschließt ein Array von renderzielformaten. |
| [**D3D12_SAMPLE_POSITION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_sample_position). Beschreibt eine unter Pixel-Beispiel Position für die Verwendung mit programmierbaren Beispiel Positionen. |
| [**D3D12_SAMPLER_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc). Beschreibt einen samplerzustand. |
| [**D3D12_SHADER_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode). Beschreibt Shader-Daten. |
| [**D3D12_SHADER_RESOURCE_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc). Beschreibt eine Shader-Ressourcen Ansicht. |
| [**D3D12_SO_DECLARATION_ENTRY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_so_declaration_entry). Beschreibt ein Vertex-Element in einem Vertex-Puffer in einem Ausgabe Slot. |
| [**D3D12_STATIC_SAMPLER_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc). Beschreibt einen statischen Sampler. |
| [**D3D12_STREAM_OUTPUT_BUFFER_VIEW**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_buffer_view). Beschreibt einen streamausgabepuffer. |
| [**D3D12_STREAM_OUTPUT_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc). Beschreibt einen streamingausgabepuffer. |
| [**D3D12_SUBRESOURCE_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data). Beschreibt die Daten der untergeordneten Quelle. |
| [**D3D12_SUBRESOURCE_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint). Beschreibt das Format, die Breite, die Höhe, die Tiefe und die Zeilengröße der untergeordneten Quelle in der übergeordneten Ressource. |
| [**D3D12_SUBRESOURCE_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info). Beschreibt die Daten der untergeordneten Quelle. |
| [**D3D12_SUBRESOURCE_RANGE_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64). Beschreibt den Speicherbereich der untergeordneten Quelle. |
| [**D3D12_SUBRESOURCE_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling). Beschreibt ein gespeichertes unter Quell Volume. |
| [**D3D12_TEX1D_ARRAY_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv). Beschreibt die unter Ressourcen aus einem Array von 1D-Texturen, die in einer tiefen Schablone verwendet werden sollen. |
| [**D3D12_TEX1D_ARRAY_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv). Beschreibt die unter Ressourcen aus einem Array von 1D-Texturen, die in einer renderzielansicht verwendet werden sollen. |
| [**D3D12_TEX1D_ARRAY_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv). Beschreibt die unter Ressourcen aus einem Array von 1D-Texturen, die in einer Shader-Resource-Ansicht verwendet werden sollen. |
| [**D3D12_TEX1D_ARRAY_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav). Beschreibt ein Array von 1D-Textur Ressourcen ohne geordneter Zugriff. |
| [**D3D12_TEX1D_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv). Beschreibt die unter Berichte aus einer 1D-Textur, auf die eine Ansicht der tiefen Schablone zugreifen kann. |
| [**D3D12_TEX1D_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv). Beschreibt die unter Berichte aus einer 1D-Textur, die in einer renderzielansicht verwendet werden soll. |
| [**D3D12_TEX1D_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_srv). Gibt die untergeordnete Quelle aus einer 1D-Textur an, die in einer Shader-Resource-Ansicht verwendet werden soll. |
| [**D3D12_TEX1D_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav). Beschreibt eine nicht geordnete Access-1D-Textur Ressource. |
| [**D3D12_TEX2D_ARRAY_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv). Beschreibt die unter Ressourcen aus einem Array von 2D-Texturen, die für eine Ansicht der tiefen Schablone zugänglich sind. |
| [**D3D12_TEX2D_ARRAY_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv). Beschreibt die unter Ressourcen aus einem Array von 2D-Texturen, die in einer renderzielansicht verwendet werden sollen. |
| [**D3D12_TEX2D_ARRAY_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv). Beschreibt die unter Ressourcen aus einem Array von 2D-Texturen, die in einer Shader-Resource-Ansicht verwendet werden sollen. |
| [**D3D12_TEX2D_ARRAY_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav). Beschreibt ein Array von 2D-Textur Ressourcen ohne geordneter Zugriff. |
| [**D3D12_TEX2D_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv). Beschreibt die unter Berichte aus einer 2D-Textur, auf die eine Ansicht der tiefen Schablone zugreifen kann. |
| [**D3D12_TEX2D_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv). Beschreibt die unter Berichte aus einer 2D-Textur, die in einer renderzielansicht verwendet werden soll. |
| [**D3D12_TEX2D_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv). Beschreibt die unter Berichte aus einer 2D-Textur, die in einer Shader-Resource-Ansicht verwendet werden soll. |
| [**D3D12_TEX2D_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav). Beschreibt eine 2D-Textur Ressource mit ungeordneter Zugriffsberechtigung. |
| [**D3D12_TEX2DMS_ARRAY_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv). Beschreibt die unter Ressourcen aus einem Array von Multisampling-2D-Texturen für eine Ansicht der tiefen Schablone. |
| [**D3D12_TEX2DMS_ARRAY_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv). Beschreibt die unter Ressourcen aus einem Array von Multisampling-2D-Texturen, die in einer renderzielansicht verwendet werden sollen. |
| [**D3D12_TEX2DMS_ARRAY_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv). Beschreibt die unter Ressourcen aus einem Array von Multisampling-2D-Texturen, die in einer Shader-Resource-Ansicht verwendet werden sollen. |
| [**D3D12_TEX2DMS_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_dsv). Beschreibt die unter Berichte aus einer Multisampling-2D-Textur, auf die eine Ansicht der tiefen Schablone zugreifen kann. |
| [**D3D12_TEX2DMS_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_rtv). Beschreibt die unter Quelle aus einer Multisampling-2D-Textur, die in einer renderzielansicht verwendet werden soll. |
| [**D3D12_TEX2DMS_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_srv). Beschreibt die unter Ressourcen aus einer Multisampling-2D-Textur, die in einer Shader-Resource-Ansicht verwendet werden soll. |
| [**D3D12_TEX3D_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv). Beschreibt die unter Ressourcen aus einer 3D-Textur, die in einer renderzielansicht verwendet werden sollen. |
| [**D3D12_TEX3D_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_srv). Beschreibt die unter Ressourcen aus einer 3D-Textur, die in einer Shader-Ressourcen Ansicht verwendet werden sollen. |
| [**D3D12_TEX3D_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav). Beschreibt eine 3D-Textur Ressource mit ungeordneter Zugriffsberechtigung. |
| [**D3D12_TEXCUBE_ARRAY_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_array_srv). Beschreibt die unter Ressourcen aus einem Array von Cube-Texturen, die in einer Shader-Resource-Ansicht verwendet werden sollen. |
| [**D3D12_TEXCUBE_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_srv). Beschreibt die unter Berichte aus einer cubetextur, die in einer Shader-Resource-Ansicht verwendet werden soll. |
| [**D3D12_TEXTURE_COPY_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location). Beschreibt einen Teil einer Textur für Textur Kopien. |
| [**D3D12_TILE_REGION_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size). Beschreibt die Größe eines gekachelten Bereichs. |
| [**D3D12_TILE_SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape). Beschreibt die Form einer Kachel durch Angeben der Abmessungen. |
| [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate). Beschreibt die Koordinaten einer gekachelten Ressource. |
| [**D3D12_UNORDERED_ACCESS_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc). Beschreibt die unter Ressourcen aus einer Ressource, auf die mithilfe einer Ansicht für ungeordneten Zugriff zugegriffen werden kann. |
| [**D3D12_VERTEX_BUFFER_VIEW**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view). Beschreibt eine Vertex-Puffer Ansicht. |
| [**D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_device_removed_extended_data). Stellt die von der Version entfernten erweiterten Daten (Dred)-Daten dar, sodass Debugger und Debugger-Erweiterungen auf Dred Data zugreifen können. |
| [**D3D12_VERSIONED_ROOT_SIGNATURE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc). Enthält eine beliebige Version einer Stamm Signatur Beschreibung und ist für die Verwendung mit Serialisierungs-/Deserialisierungsfunktionen vorgesehen. |
| [**D3D12_VIEW_INSTANCE_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_view_instance_location). Gibt die einer Ansichts Instanz zugeordneten Viewport/Schablone und Renderziel an. |
| [**D3D12_VIEW_INSTANCING_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_view_instancing_desc). Gibt Parameter an, die während der instanziierungskonfiguration verwendet werden |
| [**D3D12_VIEWPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport). Beschreibt die Dimensionen eines Viewports. |
| [**D3D12_WRITEBUFFERIMMEDIATE_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_writebufferimmediate_parameter). Gibt den unmittelbaren Wert und die Zieladresse an, die mit [**ID3D12CommandList2:: schreitebufferimmediate**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2)geschrieben wurden. |

## <a name="related-topics"></a>Zugehörige Themen

* [Kern Referenz](direct3d-12-core-reference.md)
* [Referenz für Direct3D 12](direct3d-12-reference.md)