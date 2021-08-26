---
description: Dieser Abschnitt enthält Referenzinformationen zu den Microsoft Direct3D 12-Video-API-Strukturen.
ms.assetid: ''
title: Direct3D 12 Video-Strukturen
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: 945bb3f32a72cab437939e45a0b9691cbde70ef32acf7b08afd2580ff4a4259b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958750"
---
# <a name="direct3d-12-video-structures"></a>Direct3D 12 Video-Strukturen

Dieser Abschnitt enthält Referenzinformationen zu den Microsoft Direct3D 12-Video-API-Strukturen.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema                                                                                | Beschreibung                                                                                              |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support)  | Ruft die Liste der unterstützten Profile ab.|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_formats)  | Ruft die Liste der unterstützten Formate ab.|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_HISTOGRAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_histogram)  | Stellt Daten für Aufrufe von ID3D12VideoDevice::CheckFeatureSupport zur D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM.|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles)  | Ruft die Liste der unterstützten Profile ab.|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_support)  | Ruft Unterstützungsinformationen für die Videodecodierung ab.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_COUNT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_count)  | Ruft die Anzahl der Videoerweiterungsbefehle ab.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETER_COUNT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_parameter_count)  | Ruft die unterstützte Anzahl von Parametern für die angegebene Parameterphase ab.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETERS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_parameters)  | Ruft die Liste der Befehlsparameter der Videoerweiterung für die angegebene Parameterphase ab.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_SIZE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_size)  | Überprüft die Zuordnungsgröße eines Videoerweiterungsbefehls.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_support)  | Ruft die Unterstützung von Videoerweiterungsbefehlen mithilfe von befehlsdefinierten Eingabe- und Ausgabestrukturen ab.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMANDS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_commands)  | Ruft die Liste der Videoerweiterungsbefehle vom Treiber ab.|
| [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator)  | Stellt Daten für Aufrufe von ID3D12VideoDevice::CheckFeatureSupport zur D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR. Ruft die Bewegungsschätzungsfunktionen für einen Videoencoder ab.|
| [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR_PROTECTED_RESOURCES](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator_protected_resources)  | Stellt Daten für Aufrufe von ID3D12VideoDevice::CheckFeatureSupport zur D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR_PROTECTED_RESOURCES. Ruft die Unterstützung der geschützten Ressourcen für die Schätzung von Videobewegungen ab.|
| [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR_SIZE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator_size)  | Beschreibt die Zuordnungsgröße eines Videobewegungs-Estimator-Heaps.|
| [D3D12_FEATURE_DATA_VIDEO_PROCESS_MAX_INPUT_STREAMS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_process_max_input_streams)  | Ruft die maximale Anzahl aktivierter Eingabestreams ab, die vom Videoprozessor unterstützt werden.|
| [D3D12_FEATURE_DATA_VIDEO_PROCESS_REFERENCE_INFO](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_process_reference_info)  | Ruft die Anzahl der vergangenen und zukünftigen Referenzframes ab, die für den angegebenen Deinterlacemodus, Filter, die Geschwindigkeitskonvertierung oder die automatische Verarbeitung erforderlich sind.|
| [D3D12_FEATURE_DATA_VIDEO_PROCESS_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_process_support)  | Stellt Daten für Aufrufe von ID3D12VideoDevice::CheckFeatureSupport zur D3D12_FEATURE_VIDEO_PROCESS_SUPPORT.|
| [D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_query_data_video_decode_statistics)  | Stellt Daten für eine Videodecodierungsstatistikabfrage dar, die durch Aufrufen von ID3D12VideoDecodeCommandList::EndQuery aufgerufen wird.|
| [D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_INPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_resolve_video_motion_vector_heap_input)  | Stellt Eingabedaten für Aufrufe von ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap zur Auswahl.|
| [D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_OUTPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_resolve_video_motion_vector_heap_output)  | Empfängt Ausgabedaten von Aufrufen von ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap.|
| [D3D12_RESOURCE_COORDINATE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_resource_coordinate)  | Beschreibt die Koordinaten einer Ressource.|
| [D3D12_VIDEO_DECODER_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decoder_desc)  | Beschreibt einen ID3D12VideoDecoder.|
| [D3D12_VIDEO_DECODER_HEAP_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decoder_heap_desc)  | Beschreibt einen ID3D12VideoDecoderHeap.|
| [D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_compressed_bitstream)  | Stellt einen komprimierten Bitstream dar, aus dem das Video decodiert wird.|
| [D3D12_VIDEO_DECODE_CONFIGURATION](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_configuration)  | Beschreibt die Konfiguration für einen Videodecoder.|
| [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments)  | Gibt die Parameter für die Decodierung der Ausgabekonvertierung an.|
| [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS1](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments1)  | Gibt die Parameter für die Decodierung der Ausgabekonvertierung an.|
| [D3D12_VIDEO_DECODE_FRAME_ARGUMENT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_frame_argument)  | Stellt die Decodierungsparameter für einen Frame dar.|
| [D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_input_stream_arguments)  | Gibt die Parameter für den Eingabestream für einen Videodecodierungsvorgang an.|
| [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram)  | Stellt den Histogrammausgabepuffer für eine einzelne Komponente dar.|
| [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments)  | Gibt die Parameter für den Ausgabestream für einen Videodecodierungsvorgang an.|
| [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1)  | Gibt die Parameter für den Ausgabestream für einen Videodecodierungsvorgang an.|
| [D3D12_VIDEO_DECODE_REFERENCE_FRAMES](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_reference_frames)  | Enthält die Liste der Referenzframes für den aktuellen Decodierungsvorgang.|
| [D3D12_VIDEO_DECODE_SUB_SAMPLE_MAPPING_BLOCK](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_sub_sample_mapping_block)  | Definiert die Verschlüsselungs-Bytezuordnung von Unterbeispielen für die Videodecodierung.|
| [D3D12_VIDEO_EXTENSION_COMMAND_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_extension_command_desc)  | Beschreibt einen Videoerweiterungsbefehl.|
| [D3D12_VIDEO_EXTENSION_COMMAND_INFO](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_extension_command_info)  | Beschreibt einen Videoerweiterungsbefehl.|
| [D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_INFO](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_extension_command_parameter_info)  | Beschreibt einen Befehlsparameter für die Videoerweiterung.|
| [D3D12_VIDEO_FORMAT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_format)  | Definiert die Kombination aus Pixelformat und Farbraum für eine Ressourceninhaltsbeschreibung.|
| [D3D12_VIDEO_MOTION_ESTIMATOR_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_desc)  | Beschreibt einen ID3D12VideoMotionEstimator. Übergeben Sie diese Struktur an ID3D12VideoDevice1::CreateVideoMotionEstimator, um eine Instanz von ID3D12VideoMotionEstimator zu erstellen.|
| [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input)  | Stellt Eingabedaten für Aufrufe von ID3D12VideoEncodeCommandList::EstimateMotion zur Auswahl.|
| [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output)  | Empfängt Ausgabedaten von Aufrufen von ID3D12VideoEncodeCommandList::EstimateMotion.|
| [D3D12_VIDEO_MOTION_VECTOR_HEAP_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_vector_heap_desc)  | Beschreibt eine ID3D12VideoMotionEstimatorHeap. Übergeben Sie diese Struktur an ID3D12VideoDevice1::CreateVideoMotionEstimatorHeap, um eine Instanz von ID3D12VideoMotionEstimatorHeap zu erstellen.|
| [D3D12_VIDEO_PROCESS_ALPHA_BLENDING](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_alpha_blending)  | Gibt Alphablendingparameter für die Videoverarbeitung an.|
| [D3D12_VIDEO_PROCESS_FILTER_RANGE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_filter_range)  | Definiert den Bereich der unterstützten Werte für einen Bildfilter.|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream)  | Enthält Eingabeinformationen für die Blend-Funktionalität des Videoprozessors.|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments)  | Gibt Eingabestreamargumente für einen Eingabestream an, der an ID3D12VideoCommandList::P rocessFrames übergeben wird.|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc)  | Gibt die Parameter für den Eingabestream für einen Videoprozessvorgang an.|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM_RATE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_rate)  | Stellt Informationen zur Datenstromrate bereit.|
| [D3D12_VIDEO_PROCESS_LUMA_KEY](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_luma_key)  | Gibt die Einstellungen an, die für luma keying verwendet werden.|
| [D3D12_VIDEO_PROCESS_OUTPUT_STREAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream)  | Stellt den Ausgabestream für Videoverarbeitungsbefehle dar.|
| [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_arguments)  | Gibt Ausgabestreamargumente für die Ausgabe an, die an ID3D12VideoCommandList::P rocessFrames übergeben wird.|
| [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc)  | Gibt Ausgabestreamargumente für die Ausgabe an, die an ID3D12VideoProcessCommandList::P rocessFrames übergeben wird.|
| [D3D12_VIDEO_PROCESS_REFERENCE_SET](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_reference_set)  | Enthält die Verweisframes, die für die Videoverarbeitung erforderlich sind.|
| [D3D12_VIDEO_PROCESS_TRANSFORM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_transform)  | Gibt Transformationsparameter für die Videoverarbeitung an.|
| [D3D12_VIDEO_SAMPLE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_sample)  | Beschreibt die Breite, Höhe, das Format und den Farbraum eines Bildpuffers.|
| [D3D12_VIDEO_SCALE_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_scale_support)  | Beschreibt den unterstützten Skalierungsbereich von Ausgabegrößen für eine Videoskalierung.|
| [D3D12_VIDEO_SIZE_RANGE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_size_range)  | Beschreibt den Bereich der unterstützten Größen für einen Videoskalierer.|



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 12 Video-APIs](direct3d-12-video-apis.md)
</dt> </dl>

 

 



