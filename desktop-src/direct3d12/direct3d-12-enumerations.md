---
title: Core-Enumerationen
description: Die folgenden Enumerationen werden in d3d12.h deklariert.
ms.assetid: 76E76C85-128E-4F0E-9711-C72C4CF6C835
ms.localizationpriority: low
ms.topic: article
ms.date: 09/19/2019
ms.openlocfilehash: 31cac62c8dfa6b1126d8ff2a7c134490c0c58038
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436225"
---
# <a name="core-enumerations"></a>Core-Enumerationen

Die folgenden Enumerationen werden in d3d12.h deklariert.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema und Beschreibung |
|-|
| [**D3D_ROOT_SIGNATURE_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version). Gibt die Version des Stammsignaturlayouts an. |
| [**D3D_SHADER_MODEL**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model). Gibt ein Shadermodell an. |
| [**D3D12_AUTO_BREADCRUMB_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_auto_breadcrumb_op). Definiert Konstanten, die Render-/Compute-GPU-Vorgänge angeben. |
| [**D3D12_BACKGROUND_PROCESSING_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_background_processing_mode). Definiert Konstanten, die eine Ebene der dynamischen Optimierung angeben, die auf GPU-Arbeit angewendet werden soll, die anschließend übermittelt wird. |
| [**D3D12_BLEND**](/windows/win32/api/d3d12/ne-d3d12-d3d12_blend). Gibt Überblendfaktoren an, die Werte für den Pixel-Shader und das Renderziel modulieren. |
| [**D3D12_BLEND_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_blend_op). Gibt RGB- oder Alphamischungsvorgänge an. |
| [**D3D12_BUFFER_SRV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags). Gibt an, wie eine Pufferressource angezeigt wird. |
| [**D3D12_BUFFER_UAV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags). Identifiziert Ungeordnete Zugriffsansichtsoptionen für eine Pufferressource. |
| [**D3D12_CLEAR_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_clear_flags). Gibt an, was aus der Tiefen-Schablonenansicht zu löschen ist. |
| [**D3D12_COLOR_WRITE_ENABLE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_color_write_enable). Gibt an, welche Komponenten der einzelnen Pixel eines Renderziels während des Mischens beschreibbar sind. |
| [**D3D12_COMMAND_LIST_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_support_flags). Wird verwendet, um zu bestimmen, welche Arten von Befehlslisten verschiedene Vorgänge unterstützen können. |
| [**D3D12_COMMAND_LIST_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type). Gibt den Typ einer Befehlsliste an. |
| [**D3D12_COMMAND_QUEUE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_queue_flags). Gibt Flags an, die beim Erstellen einer Befehlswarteschlange verwendet werden sollen. |
| [**D3D12_COMMAND_QUEUE_PRIORITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_queue_priority). Definiert Prioritätsstufen für eine Befehlswarteschlange. |
| [**D3D12_COMPARISON_FUNC**](/windows/win32/api/d3d12/ne-d3d12-d3d12_comparison_func). Gibt Vergleichsoptionen an. |
| [**D3D12_CONSERVATIVE_RASTERIZATION_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode). Gibt an, ob die konservative Rasterung ein- oder ausgeschaltet ist. |
| [**D3D12_CONSERVATIVE_RASTERIZATION_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_tier). Identifiziert die Ebene der konservativen Rasterung. |
| [**D3D12_CPU_PAGE_PROPERTY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cpu_page_property). Gibt die CPU-Seiteneigenschaften für den Heap an. |
| [**D3D12_CROSS_NODE_SHARING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier). Gibt die Ebene der Freigabe zwischen Knoten eines Adapters an, z. B. Ebene 1 Emuliert, Ebene 1 oder Ebene 2.  |
| [**D3D12_CULL_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cull_mode). Gibt an, dass Dreiecke mit einer bestimmten Richtung nicht gezeichnet werden. |
| [**D3D12_DEBUG_DEVICE_PARAMETER_TYPE**](/windows/win32/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type). Gibt den Datentyp des Arbeitsspeichers an, auf den der *pData-Parameter* von [**ID3D12DebugDevice1::SetDebugParameter**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter) und [**ID3D12DebugDevice1::GetDebugParameter**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter)verweist. |
| [**D3D12_DEPTH_WRITE_MASK**](/windows/win32/api/d3d12/ne-d3d12-d3d12_depth_write_mask). Identifiziert den Teil eines Tiefen-Schablonenpuffers zum Schreiben von Tiefendaten. |
| [**D3D12_DESCRIPTOR_HEAP_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags). Gibt Optionen für einen Heap an. |
| [**D3D12_DESCRIPTOR_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type). Gibt einen Deskriptor-Heaptyp an.  |
| [**D3D12_DESCRIPTOR_RANGE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags). Gibt die Flüchtigkeit sowohl von Deskriptoren als auch der Daten an, auf die sie in einer Beschreibung der Stammsignatur 1.1 verweisen, die einige Treiberoptimierungen ermöglichen kann. |
| [**D3D12_DESCRIPTOR_RANGE_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_type). Gibt einen Bereich an, sodass dieser Bereich beispielsweise in einem Eintrag anstatt in 100 deklariert werden kann, wenn ein Teil einer Deskriptortabelle über 100 Shader-Ressourcensichten (SRVs) verfügt.  |
| [**D3D12_DRED_ALLOCATION_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_allocation_type). Definiert Konstanten, die Render-/Compute-GPU-Vorgänge angeben. |
| [**D3D12_DRED_ENABLEMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_enablement). Definiert Konstanten (die von der [ID3D12DeviceRemovedExtendedDataSettings-Schnittstelle](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings)verwendet werden), die angeben, wie einzelne DRED-Features (Device Removed Extended Data) aktiviert werden. |
| [**D3D12_DRED_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_flags). Definiert Konstanten, die in der D3D12_DEVICE_REMOVED_EXTENDED_DATA [verwendet werden,](/windows/win32/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data) um Steuerungsflags für die Direct3D-Runtime anzugeben. |
| [**D3D12_DRED_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_version). Definiert Konstanten, die eine Version von Device Removed Extended Data (DRED) angeben, die von der D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA [wird.](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_device_removed_extended_data) |
| [**D3D12_DSV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dsv_dimension). Gibt den Zugriff auf eine Ressource an, die in einer Tiefen-Schablonenansicht verwendet wird. |
| [**D3D12_DSV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dsv_flags). Gibt Optionen für die Tiefen-Schablonenansicht an. |
| [**D3D12_FEATURE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature). Direct3D 12-Featureoptionen, die vom aktuellen Grafiktreiber unterstützt werden.  |
| [**D3D12_FENCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags). Gibt Fence-Optionen an.  |
| [**D3D12_FILL_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fill_mode). Gibt den Füllmodus an, der beim Rendern von Dreiecken verwendet werden soll. |
| [**D3D12_FILTER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter). Gibt Filteroptionen während der Texturstichprobe an. |
| [**D3D12_FILTER_REDUCTION_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter_reduction_type). Gibt den Typ der Filterverringerung an.  |
| [**D3D12_FILTER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter_type). Gibt den Typ der Vergrößerungs- oder Minification-Samplerfilter an.  |
| [**D3D12_FORMAT_SUPPORT1**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support1). Gibt Ressourcen an, die für ein bereitgestelltes Format unterstützt werden. |
| [**D3D12_FORMAT_SUPPORT2**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support2). Gibt an, welche ungeordneten Ressourcenoptionen für ein bereitgestelltes Format unterstützt werden. |
| [**D3D12_GRAPHICS_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_graphics_states). Definiert Flags, die Zustände im Zusammenhang mit einer Grafikbefehlsliste angeben. Werte können bitweise OR'd zusammen sein. |
| [**D3D12_HEAP_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags). Gibt Heapoptionen an, z. B. ob der Heap Texturen enthalten kann und ob Ressourcen adapterübergreifend freigegeben werden.  |
| [**D3D12_HEAP_SERIALIZATION_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_serialization_tier). Definiert Konstanten, die Heapserialisierungsunterstützung angeben. |
| [**D3D12_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type). Gibt den Heaptyp an. Bei einem residenten Speicher befinden sich Heaps in einem bestimmten physischen Speicherpool mit bestimmten CPU-Cacheeigenschaften.  |
| [**D3D12_INDEX_BUFFER_STRIP_CUT_VALUE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value). Bei Verwendung einer primitiven Topologie mit Dreiecksstreifen werden Scheitelpunktpositionen als Scheitelpunkte eines kontinuierlichen Dreiecksstreifens interpretiert. Es gibt einen speziellen Indexwert, der den Wunsch darstellt, eine Diskontinuität im Strip, den Schnittindexwert, zu haben. Diese Enum listet die unterstützten Ausschneidewerte auf.  |
| [**D3D12_INDIRECT_ARGUMENT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_indirect_argument_type). Gibt den Typ des indirekten Parameters an.  |
| [**D3D12_INPUT_CLASSIFICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_input_classification). Identifiziert den Typ der in einem Eingabeslot enthaltenen Daten. |
| [**D3D12_LIFETIME_STATE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_lifetime_state). Definiert Konstanten, die den Lebensdauerzustand eines Lebensdauerverfolgungsobjekts angeben. |
| [**D3D12_LOGIC_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_logic_op). Gibt logische Vorgänge an, die für ein Renderziel konfiguriert werden. |
| [**D3D12_MEASUREMENTS_ACTION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_measurements_action). Definiert Konstanten, die angeben, was mit den Ergebnissen der früheren Workloadinstrumentierung erfolgen soll. |
| [**D3D12_MEMORY_POOL**](/windows/win32/api/d3d12/ne-d3d12-d3d12_memory_pool). Gibt den Speicherpool für den Heap an. |
| [**D3D12_MESH_SHADER_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_mesh_shader_tier). Definiert Konstanten, die Gitternetz- und Verstärkungs-Shaderunterstützung angeben. |
| [**D3D12_META_COMMAND_PARAMETER_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_flags). Definiert Konstanten, die die Flags für einen Parameter für einen Metabefehl angeben. Werte können bitweise OR'd zusammen sein. |
| [**D3D12_META_COMMAND_PARAMETER_STAGE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_stage). Definiert Konstanten, die die Phase eines Parameters für einen Metabefehl angeben. |
| [**D3D12_META_COMMAND_PARAMETER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_type). Definiert Konstanten, die den Datentyp eines Parameters für einen Metabefehl angeben. |
| [**D3D12_MULTIPLE_FENCE_WAIT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multiple_fence_wait_flags). Gibt mehrere Warteflags für mehrere Fences an. |
| [**D3D12_MULTISAMPLE_QUALITY_LEVELS_FLAG**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags). Gibt Optionen zum Bestimmen von Qualitätsstufen an.  |
| [**D3D12_PIPELINE_STATE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags). Flags zum Steuern des Pipelinezustands.  |
| [**D3D12_PIPELINE_STATE_SUBOBJECT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type). Gibt den Typ eines Unterobjekts in einer Pipelinezustandsstreambeschreibung an. |
| [**D3D12_PREDICATION_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_predication_op). Gibt den anzuwendenden Prädication-Vorgang an.  |
| [**D3D12_PRIMITIVE_TOPOLOGY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type). Gibt an, wie die Pipeline eingabeprimitive Geometrie- oder Hüllen-Shadereingaben interpretiert. |
| [**D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_programmable_sample_positions_tier). Gibt den Grad der Unterstützung für programmierbare Beispielpositionen an, die vom Adapter angeboten werden. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_resource_session_flags). Definiert Konstanten, die Sitzungsflags für geschützte Ressourcen angeben. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_resource_session_support_flags). Definiert Konstanten, die unterstützung für geschützte Ressourcensitzung angeben. |
| [**D3D12_PROTECTED_SESSION_STATUS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_session_status). Definiert Konstanten, die den Status der geschützten Sitzung angeben. |
| [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type). Gibt den Typ des zu erstellenden Abfragehaps an. |
| [**D3D12_QUERY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type). Gibt den Typ der Abfrage an. |
| [**D3D12_RAY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_ray_flags). Flags, die an die [**TraceRay-Funktion übergeben**](./traceray-function.md) werden, um Transparenz, Culling und frühes Verhalten zu überschreiben. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BUILD_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_build_flags). Gibt Flags für den Aufbau einer Raytracingbeschleunigungsstruktur an. Verwenden Sie einen Wert aus dieser Enumeration mit [**der**](/windows/win32/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS-Struktur, die Eingaben für den Beschleunigungsstruktur-Buildvorgang bietet. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_copy_mode). Gibt den Typ des Kopiervorgang an, der beim Aufrufen von [**CopyRaytracingAccelerationStructure ausgeführt wird.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-copyraytracingaccelerationstructure) |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_type). Gibt den Typ der Informationen zur Beschleunigungsstruktur nach dem Build an, die mit Aufrufen von [**EmitRaytracingAccelerationStructurePostbuildInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo) und [**BuildRaytracingAccelerationStructure abgerufen werden können.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure) |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_type). Gibt den Typ einer Raytracingbeschleunigungsstruktur an. |
| [**D3D12_RAYTRACING_GEOMETRY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_flags). Gibt Flags für die Raytracinggeometrie in [**einer**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc) D3D12_RAYTRACING_GEOMETRY_DESC an. |
| [**D3D12_RAYTRACING_GEOMETRY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_type). Gibt den Typ der Geometrie an, die für das Raytracing verwendet wird. Verwenden Sie einen Wert aus dieser Enumeration, [](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc)um den Geometrietyp in einer -D3D12_RAYTRACING_GEOMETRY_DESC. |
| [**D3D12_RAYTRACING_INSTANCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_instance_flags). Flags für eine Instanz der Raytracingbeschleunigungsstruktur. Diese Flags können verwendet werden, um die D3D12_RAYTRACING_GEOMETRY_FLAGS [**einzelnen**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_flags) Instanzen zu überschreiben. |
| [**D3D12_RAYTRACING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_tier). Gibt den Grad der Unterstützung der Ray-Ablaufverfolgung auf dem Grafikgerät an. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_beginning_access_type). Gibt den Zugriffstyp an, den eine Anwendung den angegebenen Ressourcen beim Übergang in einen Renderpass erhält. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_ending_access_type). Gibt den Zugriffstyp an, den eine Anwendung den angegebenen Ressourcen beim Übergang aus einem Renderpass erhält. |
| [**D3D12_RENDER_PASS_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_flags). Gibt die Art des Renderpasses an. z. B. ob es sich um einen angehaltenen oder einen fortsetzenden Renderpass handelt. |
| [**D3D12_RESIDENCY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_residency_flags). Wird mit der EnqueueMakeResident-Funktion verwendet, um zu wählen, wie Residencyvorgänge bei Überschreitung des Arbeitsspeicherbudgets fortgesetzt werden. |
| [**D3D12_RESIDENCY_PRIORITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_residency_priority). Gibt allgemeine Buckets für DieResidenzpriorität an, die für die schnelle Einrichtung eines Anwendungsprioritätsschemas nützlich sind. |
| [**D3D12_RESOLVE_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resolve_mode). Gibt einen Auflösungsvorgang an. |
| [**D3D12_RESOURCE_BARRIER_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags). Flags zum Festlegen von Barrieren für geteilte Ressourcen.  |
| [**D3D12_RESOURCE_BARRIER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_type). Gibt einen Typ der Ressourcenbarriere (Übergang bei der Ressourcennutzung) an. |
| [**D3D12_RESOURCE_BINDING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_binding_tier). Identifiziert die Ebene der verwendeten Ressourcenbindung.  |
| [**D3D12_RESOURCE_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension). Gibt den Typ der verwendeten Ressource an. |
| [**D3D12_RESOURCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_flags). Gibt Optionen für die Arbeit mit Ressourcen an.  |
| [**D3D12_RESOURCE_HEAP_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_heap_tier). Gibt an, welche Ressourcenhapebene die Hardware- und Treiberunterstützung unterstützt.  |
| [**D3D12_RESOURCE_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states). Gibt den Zustand einer Ressource in Bezug auf die Verwendung der Ressource an.  |
| [**D3D12_ROOT_DESCRIPTOR_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags). Gibt die Flüchtigkeit der Daten an, auf die von Deskriptoren in einer Beschreibung der Stammsignatur 1.1 verwiesen wird, die einige Treiberoptimierungen ermöglichen kann. |
| [**D3D12_ROOT_PARAMETER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_parameter_type). Gibt den Typ des Stammsignaturslots an.  |
| [**D3D12_ROOT_SIGNATURE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_signature_flags). Gibt Optionen für das Stammsignaturlayout an.  |
| [**D3D12_RTV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_rtv_dimension). Identifiziert den Typ der Ressource, die als Renderziel angezeigt werden soll. |
| [**D3D12_SAMPLER_FEEDBACK_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_sampler_feedback_tier). Definiert Konstanten, die Feedbackunterstützung für Sampler angeben. |
| [**D3D12_SHADER_CACHE_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_cache_support_flags). Beschreibt den Grad der Unterstützung für das Shaderzwischenspeichern im aktuellen Grafiktreiber. |
| [**D3D12_SHADER_COMPONENT_MAPPING**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_component_mapping). Gibt an, wie Arbeitsspeicher von einer Shaderressourcenansicht (SRV) geroutet wird.  |
| [**D3D12_SHADER_MIN_PRECISION_SUPPORT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_min_precision_support). Beschreibt die Minimalgenauigkeitsunterstützungsoptionen für Shader im aktuellen Grafiktreiber.  |
| [**D3D12_SHADER_VISIBILITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_visibility). Gibt die Shader an, die auf den Inhalt eines angegebenen Stammsignaturslots zugreifen können. |
| [**D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shared_resource_compatibility_tier). Definiert Konstanten, die eine API-übergreifende Freigabeunterstützungsebene angeben. |
| [**D3D12_SRV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_srv_dimension). Identifiziert den Typ der Ressource, die als Shaderressource angezeigt wird. |
| [**D3D12_STATIC_BORDER_COLOR**](/windows/win32/api/d3d12/ne-d3d12-d3d12_static_border_color). Gibt die Rahmenfarbe für einen statischen Sampler an.  |
| [**D3D12_STENCIL_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_stencil_op). Identifiziert die Schablonenvorgänge, die während tiefen schablonenbasierten Tests ausgeführt werden können. |
| [**D3D12_TEXTURE_ADDRESS_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_address_mode). Identifiziert eine Technik zum Auflösen von Texturkoordinaten, die sich außerhalb der Grenzen einer Textur befinden.  |
| [**D3D12_TEXTURE_COPY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_copy_type). Gibt an, welcher Texturkopiertyp stattfinden soll. |
| [**D3D12_TEXTURE_LAYOUT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_layout). Gibt Texturlayoutoptionen an.  |
| [**D3D12_TILE_COPY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_copy_flags). Gibt an, wie eine Kachel kopiert wird.  |
| [**D3D12_TILE_MAPPING_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_mapping_flags). Gibt an, wie ein Kachelzuordnungsvorgang durchgeführt wird.  |
| [**D3D12_TILE_RANGE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_range_flags). Gibt einen Bereich von Kachelzuordnungen an.  |
| [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier). Gibt die Ebene an, auf der gekachelte Ressourcen unterstützt werden.  |
| [**D3D12_UAV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_uav_dimension). Identifiziert ungeordnete Zugriffsansichtsoptionen. |
| [**D3D12_VIEW_INSTANCING_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_view_instancing_flags). Gibt Optionen für die Ansichtsinstancing an. |
| [**D3D12_VIEW_INSTANCING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_view_instancing_tier). Gibt die Ebene an, auf der die Ansichtsinstancierung unterstützt wird. |
| [**D3D12_WAVE_MMA_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_wave_mma_tier). Definiert Konstanten, die eine Ebene der Unterstützung für WaveMMA-Vorgänge (wave_matrix) angeben. |
| [**D3D12_WRITEBUFFERIMMEDIATE_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_writebufferimmediate_mode). Gibt den Modus an, der von einem **WriteBufferImmediate-Vorgang verwendet** wird. |

## <a name="related-topics"></a>Zugehörige Themen

* [Core-Referenz](direct3d-12-core-reference.md)
* [Referenz zu Direct3D 12](direct3d-12-reference.md)
