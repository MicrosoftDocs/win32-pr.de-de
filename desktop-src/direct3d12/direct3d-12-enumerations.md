---
title: Core-Enumerationen
description: Die folgenden Enumerationen werden in d3d12. h deklariert.
ms.assetid: 76E76C85-128E-4F0E-9711-C72C4CF6C835
ms.localizationpriority: low
ms.topic: article
ms.date: 09/19/2019
ms.openlocfilehash: 7f34266e4afdec14e97caa81f393733f1c1ec684
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2020
ms.locfileid: "106339919"
---
# <a name="core-enumerations"></a>Core-Enumerationen

Die folgenden Enumerationen werden in d3d12. h deklariert.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema und Beschreibung |
|-|
| [**D3D_ROOT_SIGNATURE_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version). Gibt die Version des Stamm Signatur Layouts an. |
| [**D3D_SHADER_MODEL**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model). Gibt ein Shader-Modell an. |
| [**D3D12_AUTO_BREADCRUMB_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_auto_breadcrumb_op). Definiert Konstanten, die Rendering/Compute-GPU-Vorgänge angeben. |
| [**D3D12_BACKGROUND_PROCESSING_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_background_processing_mode). Definiert Konstanten, die eine Ebene dynamischer Optimierungen angeben, die auf GPU-arbeiten angewendet werden soll, die anschließend übermittelt werden. |
| [**D3D12_BLEND**](/windows/win32/api/d3d12/ne-d3d12-d3d12_blend). Gibt Blend-Faktoren an, die Werte für den Pixelshader und das Renderziel modulieren. |
| [**D3D12_BLEND_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_blend_op). Gibt RGB-oder Alpha-Mischungs Vorgänge an. |
| [**D3D12_BUFFER_SRV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags). Gibt an, wie eine Puffer Ressource angezeigt wird. |
| [**D3D12_BUFFER_UAV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags). Identifiziert Ansichtsoptionen für ungeordnete Zugriffe für eine Puffer Ressource. |
| [**D3D12_CLEAR_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_clear_flags). Gibt an, welche Elemente aus der Ansicht der tiefen Schablone gelöscht werden sollen. |
| [**D3D12_COLOR_WRITE_ENABLE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_color_write_enable). Gibt an, welche Komponenten der einzelnen Pixel eines Renderziels während der Mischung geschrieben werden können. |
| [**D3D12_COMMAND_LIST_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_support_flags). Wird verwendet, um zu bestimmen, welche Arten von Befehlslisten verschiedene Vorgänge unterstützen können. |
| [**D3D12_COMMAND_LIST_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type). Gibt den Typ einer Befehlsliste an. |
| [**D3D12_COMMAND_QUEUE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_queue_flags). Gibt Flags an, die beim Erstellen einer Befehls Warteschlange verwendet werden sollen. |
| [**D3D12_COMMAND_QUEUE_PRIORITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_queue_priority). Definiert Prioritäts Ebenen für eine Befehls Warteschlange. |
| [**D3D12_COMPARISON_FUNC**](/windows/win32/api/d3d12/ne-d3d12-d3d12_comparison_func). Gibt Vergleichs Optionen an. |
| [**D3D12_CONSERVATIVE_RASTERIZATION_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode). Gibt an, ob die konservative rasterisierung ein-oder ausgeschaltet ist. |
| [**D3D12_CONSERVATIVE_RASTERIZATION_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_tier). Gibt die Ebene der konservativen rasterisierung an. |
| [**D3D12_CPU_PAGE_PROPERTY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cpu_page_property). Gibt die CPU-Seiteneigenschaften für den Heap an. |
| [**D3D12_CROSS_NODE_SHARING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier). Gibt die Ebene der Freigabe über Knoten eines Adapters an, z. b. Ebene 1 emuliert, Ebene 1 oder Ebene 2.  |
| [**D3D12_CULL_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cull_mode). Gibt an, dass Dreiecke mit einer bestimmten Richtung nicht gezeichnet werden. |
| [**D3D12_DEBUG_DEVICE_PARAMETER_TYPE**](/windows/win32/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type). Gibt den Datentyp des Speichers an, auf den durch den *pData* -Parameter von [**ID3D12DebugDevice1:: setdebugparameter**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter) und [**ID3D12DebugDevice1:: getdebugparameter**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter)verwiesen wird. |
| [**D3D12_DEPTH_WRITE_MASK**](/windows/win32/api/d3d12/ne-d3d12-d3d12_depth_write_mask). Gibt den Teil eines tiefen Schablonen Puffers zum Schreiben von Tiefendaten an. |
| [**D3D12_DESCRIPTOR_HEAP_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags). Gibt die Optionen für einen Heap an. |
| [**D3D12_DESCRIPTOR_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type). Gibt einen Typ von deskriptorheap an.  |
| [**D3D12_DESCRIPTOR_RANGE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags). Gibt die Volatilität beider Deskriptoren und der Daten an, auf die in einer Stamm Signatur 1,1-Beschreibung verwiesen wird. Dadurch können einige Treiber Optimierungen aktiviert werden. |
| [**D3D12_DESCRIPTOR_RANGE_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_type). Gibt einen Bereich an, sodass z. b., wenn ein Teil einer Deskriptortabelle 100-Shader-Ressourcen Sichten (Srvs) aufweist, der Bereich in einem Eintrag anstelle von 100 deklariert werden kann.  |
| [**D3D12_DRED_ALLOCATION_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_allocation_type). Definiert Konstanten, die Rendering/Compute-GPU-Vorgänge angeben. |
| [**D3D12_DRED_ENABLEMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_enablement). Definiert Konstanten (die von der [ID3D12DeviceRemovedExtendedDataSettings-Schnittstelle](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings)verwendet werden), die angeben, wie einzelne Geräte entfernte erweiterte Daten (Dred)-Funktionen aktiviert sind. |
| [**D3D12_DRED_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_flags). Definiert Konstanten, die in der [D3D12_DEVICE_REMOVED_EXTENDED_DATA-Struktur](/windows/win32/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data) verwendet werden, um Steuerungsflags für die Direct3D-Laufzeit anzugeben. |
| [**D3D12_DRED_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_version). Definiert Konstanten, die eine Version der vom Gerät entfernten erweiterten Daten (Dred) angeben, die von der [D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA Struktur](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_device_removed_extended_data)verwendet wird. |
| [**D3D12_DSV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dsv_dimension). Gibt an, wie auf eine Ressource zugegriffen werden kann, die in einer Ansicht der tiefen Schablone verwendet wird. |
| [**D3D12_DSV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dsv_flags). Gibt Optionen für die Ansicht der tiefen Schablone an. |
| [**D3D12_FEATURE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature). Direct3D 12 Feature-Optionen, die vom aktuellen Grafiktreiber unterstützt werden.  |
| [**D3D12_FENCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags). Gibt Optionen für die Fence an.  |
| [**D3D12_FILL_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fill_mode). Gibt den beim Rendern von Dreiecken zu verwendenden Füll Modus an. |
| [**D3D12_FILTER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter). Gibt Filteroptionen während der Textur Stichprobe an. |
| [**D3D12_FILTER_REDUCTION_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter_reduction_type). Gibt den Typ der Filter Reduzierung an.  |
| [**D3D12_FILTER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter_type). Gibt den Typ der Vergrößerungs-oder minierungs-Sampler-Filter an.  |
| [**D3D12_FORMAT_SUPPORT1**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support1). Gibt Ressourcen an, die für ein bereitgestelltes Format unterstützt werden. |
| [**D3D12_FORMAT_SUPPORT2**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support2). Gibt an, welche ungeordneten Ressourcen Optionen für ein bereitgestelltes Format unterstützt werden. |
| [**D3D12_GRAPHICS_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_graphics_states). Definiert Flags, die Zustände angeben, die sich auf eine Grafik Befehlsliste beziehen. Werte können bitweise oder gleich sein. |
| [**D3D12_HEAP_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags). Gibt Heap Optionen an, z. b. ob der Heap Texturen enthalten kann und ob Ressourcen von Adaptern gemeinsam genutzt werden.  |
| [**D3D12_HEAP_SERIALIZATION_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_serialization_tier). Definiert Konstanten, die die Unterstützung der Heap-Serialisierung angeben. |
| [**D3D12_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type). Gibt den Typ des Heaps an. Wenn Sie ansässig sind, befinden sich Heaps in einem bestimmten physischen Speicherpool mit bestimmten CPU-Cache Eigenschaften.  |
| [**D3D12_INDEX_BUFFER_STRIP_CUT_VALUE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value). Bei der Verwendung einer Dreiecks Bereichs primitiven Topologie werden Scheitelpunkt Positionen als Scheitel Punkte eines kontinuierlichen Dreiecks Streifens interpretiert. Es gibt einen speziellen Indexwert, der den Wunsch darstellt, eine Diskontinuität im Strip zu haben, den Ausschneide Index Wert. Diese Enumeration listet die unterstützten Ausschneide Werte auf.  |
| [**D3D12_INDIRECT_ARGUMENT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_indirect_argument_type). Gibt den Typ des indirekten Parameters an.  |
| [**D3D12_INPUT_CLASSIFICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_input_classification). Gibt den Typ der Daten an, die in einem Eingabe Slot enthalten sind. |
| [**D3D12_LIFETIME_STATE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_lifetime_state). Definiert Konstanten, die den Lebensdauer Zustand eines Objekts angeben, das mit der Lebensdauer verfolgt wird. |
| [**D3D12_LOGIC_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_logic_op). Gibt logische Vorgänge an, die für ein Renderziel konfiguriert werden sollen. |
| [**D3D12_MEASUREMENTS_ACTION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_measurements_action). Definiert Konstanten, die angeben, was mit den Ergebnissen der früheren workloadinstrumentation geschehen soll. |
| [**D3D12_MEMORY_POOL**](/windows/win32/api/d3d12/ne-d3d12-d3d12_memory_pool). Gibt den Speicherpool für den Heap an. |
| [**D3D12_META_COMMAND_PARAMETER_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_flags). Definiert Konstanten, die die Flags für einen Parameter für einen Meta-Befehl angeben. Werte können bitweise oder gleich sein. |
| [**D3D12_META_COMMAND_PARAMETER_STAGE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_stage). Definiert Konstanten, die die Stufe eines Parameters für einen Meta-Befehl angeben. |
| [**D3D12_META_COMMAND_PARAMETER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_type). Definiert Konstanten, die den Datentyp eines Parameters für einen Meta-Befehl angeben. |
| [**D3D12_MULTIPLE_FENCE_WAIT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multiple_fence_wait_flags). Gibt mehrere warte Flags für mehrere Zäune an. |
| [**D3D12_MULTISAMPLE_QUALITY_LEVELS_FLAG**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags). Gibt Optionen zum Bestimmen der Qualitätsstufen an.  |
| [**D3D12_PIPELINE_STATE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags). Flags zum Steuern des Pipeline Zustands.  |
| [**D3D12_PIPELINE_STATE_SUBOBJECT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type). Gibt den Typ eines untergeordneten Objekts in einer Beschreibung des Pipeline Zustandsdaten Stroms an. |
| [**D3D12_PREDICATION_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_predication_op). Gibt den anzuwendenden prädikationsvorgang an.  |
| [**D3D12_PRIMITIVE_TOPOLOGY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type). Gibt an, wie die Pipeline Geometry-oder Hull-Shader-Eingabe primitive interpretiert. |
| [**D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_programmable_sample_positions_tier). Gibt die Ebene der Unterstützung für programmierbare Beispiel Positionen an, die vom Adapter angeboten werden. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_resource_session_flags). Definiert Konstanten, die geschützte ressourcensitzungsflags angeben. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_resource_session_support_flags). Definiert Konstanten, die die Unterstützung geschützter Ressourcen Sitzungen angeben. |
| [**D3D12_PROTECTED_SESSION_STATUS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_session_status). Definiert Konstanten, die den Status der geschützten Sitzung angeben. |
| [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type). Gibt den Typ des zu erstellenden Abfrage Heaps an. |
| [**D3D12_QUERY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type). Gibt den Typ der Abfrage an. |
| [**D3D12_RAY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_ray_flags). Flags, die an die [**traceray**](./traceray-function.md) -Funktion übergeben werden, um Transparenz, Vererbung und frühe Ausgabeverhalten zu überschreiben. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BUILD_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_build_flags). Gibt Flags für den Build einer Raytracing-Beschleunigungs Struktur an. Verwenden Sie einen Wert aus dieser Enumeration mit der [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) -Struktur, die Eingaben für den Buildvorgang der Beschleunigungs Struktur bereitstellt. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_copy_mode). Gibt den Typ des Kopiervorgangs an, der beim Aufrufen von [**copyraytracingaccelerationstructure**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-copyraytracingaccelerationstructure)ausgeführt wird. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_type). Gibt den Typ der Beschleunigungs Struktur an, die nach Buildinformationen abgerufen werden kann, die mit Aufrufen von " [**emitraytracingaccelerationstructurepostbuildinfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo) " und " [**buildraytracingaccelerationstructure**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure)" abgerufen werden können. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_type). Gibt den Typ einer Raytracing-Beschleunigungs Struktur an. |
| [**D3D12_RAYTRACING_GEOMETRY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_flags). Gibt Flags für die Raytracing-Geometrie in einer [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc) Struktur an. |
| [**D3D12_RAYTRACING_GEOMETRY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_type). Gibt den für Raytracing verwendeten Geometry-Typ an. Verwenden Sie einen Wert aus dieser Enumeration, um den Geometry-Typ in einem [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc)anzugeben. |
| [**D3D12_RAYTRACING_INSTANCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_instance_flags). Flags für eine Raytracing-Beschleunigungs Struktur Instanz. Diese Flags können verwendet werden, um [**D3D12_RAYTRACING_GEOMETRY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_flags) für einzelne Instanzen zu überschreiben. |
| [**D3D12_RAYTRACING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_tier). Gibt die Ebene der Unterstützung für die Ray-Ablauf Verfolgung auf dem Grafikgerät an. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_beginning_access_type). Gibt den Typ des Zugriffs an, den eine Anwendung an die angegebene Ressource (n) beim Übergang in einen renderdurchlauf erhält. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_ending_access_type). Gibt den Zugriffstyp an, der einer Anwendung beim Übergang aus einem renderdurchlauf für die angegebene Ressource (n) erteilt wird. |
| [**D3D12_RENDER_PASS_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_flags). Gibt die Art des Renderpass an; beispielsweise, ob es sich um eine Unterbrechung oder einen fortgesetzten renderdurchlauf handelt. |
| [**D3D12_RESIDENCY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_residency_flags). Wird mit der enqueuemakeresident-Funktion verwendet, um auszuwählen, wie die Residenz Vorgänge bei Überschreitung des Arbeitsspeicher Budgets fortgesetzt werden. |
| [**D3D12_RESIDENCY_PRIORITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_residency_priority). Gibt umfassende Residenz-Prioritäts Behälter an, die für die schnelle Einrichtung eines Anwendungs Prioritäts Schemas |
| [**D3D12_RESOLVE_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resolve_mode). Gibt einen Auflösungs Vorgang an. |
| [**D3D12_RESOURCE_BARRIER_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags). Flags zum Festlegen von Ressourcen Barrieren aufteilen.  |
| [**D3D12_RESOURCE_BARRIER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_type). Gibt einen Typ von Ressourcen Barriere an (Übergang in der Ressourcenverwendung). |
| [**D3D12_RESOURCE_BINDING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_binding_tier). Gibt die Ebene der verwendeten Ressourcen Bindung an.  |
| [**D3D12_RESOURCE_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension). Identifiziert den Typ der verwendeten Ressource. |
| [**D3D12_RESOURCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_flags). Gibt Optionen für die Arbeit mit Ressourcen an.  |
| [**D3D12_RESOURCE_HEAP_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_heap_tier). Gibt an, welche Ressourcen Heap Ebene von Hardware und Treiber unterstützt wird.  |
| [**D3D12_RESOURCE_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states). Gibt den Zustand einer Ressource an, die angibt, wie die Ressource verwendet wird.  |
| [**D3D12_ROOT_DESCRIPTOR_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags). Gibt die Volatilität der Daten an, auf die durch Deskriptoren in einer Stamm Signatur 1,1-Beschreibung verwiesen wird. Dadurch können einige Treiber Optimierungen aktiviert werden. |
| [**D3D12_ROOT_PARAMETER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_parameter_type). Gibt den Typ des Stamm Signatur Slots an.  |
| [**D3D12_ROOT_SIGNATURE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_signature_flags). Gibt Optionen für das Layout der Stamm Signatur an.  |
| [**D3D12_RTV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_rtv_dimension). Identifiziert den Typ der Ressource, die als Renderziel angezeigt werden soll. |
| [**D3D12_SHADER_CACHE_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_cache_support_flags). Beschreibt die Ebene der Unterstützung für das Shader-Caching im aktuellen Grafiktreiber. |
| [**D3D12_SHADER_COMPONENT_MAPPING**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_component_mapping). Gibt an, wie der Arbeitsspeicher durch eine Shader-Ressourcen Ansicht (SRV) weitergeleitet wird.  |
| [**D3D12_SHADER_MIN_PRECISION_SUPPORT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_min_precision_support). Beschreibt die unterstützten mindestgenauigkeits Optionen für Shader im aktuellen Grafiktreiber.  |
| [**D3D12_SHADER_VISIBILITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_visibility). Gibt die Shader an, die auf den Inhalt eines angegebenen Stamm Signatur Slots zugreifen können. |
| [**D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shared_resource_compatibility_tier). Definiert Konstanten, die eine API-übergreifende Freigabe Unterstützung angeben. |
| [**D3D12_SRV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_srv_dimension). Gibt den Typ der Ressource an, die als Shaderressource angezeigt wird. |
| [**D3D12_STATIC_BORDER_COLOR**](/windows/win32/api/d3d12/ne-d3d12-d3d12_static_border_color). Gibt die Rahmenfarbe für einen statischen Sampler an.  |
| [**D3D12_STENCIL_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_stencil_op). Gibt die Schablonen Vorgänge an, die während des Tests der tiefen Schablone ausgeführt werden können. |
| [**D3D12_TEXTURE_ADDRESS_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_address_mode). Identifiziert eine Technik zum Auflösen von Texturkoordinaten, die sich außerhalb der Grenzen einer Textur befinden.  |
| [**D3D12_TEXTURE_COPY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_copy_type). Gibt an, welche Art von Textur Kopie durchgeführt werden soll. |
| [**D3D12_TEXTURE_LAYOUT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_layout). Gibt Textur Layout-Optionen an.  |
| [**D3D12_TILE_COPY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_copy_flags). Gibt an, wie eine Kachel kopiert wird.  |
| [**D3D12_TILE_MAPPING_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_mapping_flags). Gibt an, wie ein Kachel Zuordnungs Vorgang durchgeführt wird.  |
| [**D3D12_TILE_RANGE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_range_flags). Gibt einen Bereich von Kachel Zuordnungen an.  |
| [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier). Gibt die Ebene an, mit der die gekachelten Ressourcen unterstützt werden.  |
| [**D3D12_UAV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_uav_dimension). Identifiziert Optionen für ungeordnete Zugriffs Ansichten. |
| [**D3D12_VIEW_INSTANCING_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_view_instancing_flags). Gibt Optionen für das Anzeigen der Instanziierung an. |
| [**D3D12_VIEW_INSTANCING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_view_instancing_tier). Gibt die Ebene an, auf der die Ansichts Instanziierung unterstützt wird. |
| [**D3D12_WRITEBUFFERIMMEDIATE_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_writebufferimmediate_mode). Gibt den Modus an, der von einem **Write-bufferimmediate** -Vorgang verwendet wird. |

## <a name="related-topics"></a>Zugehörige Themen

* [Core-Referenz](direct3d-12-core-reference.md)
* [Direct3D 12-Referenz](direct3d-12-reference.md)