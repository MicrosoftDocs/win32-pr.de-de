---
description: Dieser Artikel enthält allgemeine Anleitungen für die Verwendung der Direct3D 12-Video-APIs.
ms.assetid: ''
title: Direct3D 12 Video Overview
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: 561ceba8a3110d6aa7e9a336430c0a14ddb45bc5707c650588a08c391cd65863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828320"
---
# <a name="direct3d-12-video-overview"></a>Direct3D 12 Video Overview

Dieser Artikel enthält allgemeine Anleitungen für die Verwendung der Direct3D 12-Video-APIs.

## <a name="about-direct3d-12-video"></a>Video zu Direct3D 12

Die Direct3D 12-Videoschnittstelle bietet Apps eine neue Möglichkeit zum Implementieren der Videodecodierung und -verarbeitung. Die Direct3D 12-Schnittstelle ist anders als die vorherige Direct3D 11-Schnittstelle, da sie mit den Prinzipien und dem Stil von Direct3D 12 konsistent ist, die Folgendes enthalten:

- Entwicklern mehr Kontrolle geben
 - Zuordnung von Hardwarespeicher, auf den zugegriffen werden kann
 - CPU-Threads zum Generieren von & Übermitteln von Befehlen
   - Unabhängige Generierung und Übermittlung
   - Nicht blockierend
 - Planen der Hardwarearbeit
- Behandelt vorhandene Funktionen, einschließlich der meisten Direct3D 11-Videofunktionen, aber gleichzeitig wird die Einfachheit und Benutzerfreundlichkeit im Hinterkopf behalten.
- Leistung und Leistung von Direct3D 12-Hauptanwendungen, die gleich oder besser als Direct3D 11 sind
- Konsistenz mit anderen Direct3D 12-APIs
- Interoperabilität mit vorhandenen Grafik-APIs


## <a name="video-decoding"></a>Videodecodierung

In den folgenden Abschnitten werden einige der Aufgaben beschrieben, die bei der Implementierung der Direct3D 12-Videodecodierung beteiligt sind.

### <a name="query-for-decoding-capabilities"></a>Abfragen von Decodierungsfunktionen

Rufen [Sie ID3D12VideoDevice::CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) auf, um die Supportdetails für Direct3D 12-Videodecodierungsvorgänge zu überprüfen. Übergeben Sie einen Wert aus [der](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) D3D12_FEATURE_VIDEO -Enumeration, um das Feature anzugeben, für das Sie Supportinformationen anfordern.

### <a name="create-the-video-decoder"></a>Erstellen des Videodecoders

Rufen [Sie ID3D12VideoDevice::CreateVideoDecoder](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoder) auf, um eine Instanz der [ID3D12VideoDecoder-Schnittstelle zu](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecoder) erstellen. Der Decoder enthält den Zustand für eine Decodierungssitzung, einschließlich referenzbezogener Daten wie Bewegungsvektoren.  Bei einer Auflösungsänderung oder [einer MaxDecodePictureBufferCount-Änderung](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decoder_heap_desc) wird das Decoderobjekt neu erstellt. Die Decodierungsbreite und -höhe geben die native Streamauflösung vor jeder Skala an.  Die maximale Anzahl von DPB-Dateien (Decode Picture Buffer) gibt die größte DPB-Anzahl an, die verwendet werden kann, ohne den Videodecoder neu zu spezifizieren.

Der Decoder kann zum Aufzeichnen von Befehlen aus mehreren Befehlslisten verwendet werden, kann aber nur einer Befehlsliste gleichzeitig zugeordnet werden.  Die Anwendung ist für die Synchronisierung des Zugriffs auf den Decoder verantwortlich.

### <a name="create-the-video-decoder-heap"></a>Erstellen des Videodecoder-Heaps 

Rufen [Sie ID3D12VideoDevice::CreateVideoDecoderHeap](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoderheap) auf, um eine Instanz der [ID3D12VideoDecoderHeap-Schnittstelle zu](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecoderheap) erstellen. Dieses Objekt enthält die auflösungsabhängigen Treiberressourcen und den Zustand.

### <a name="decoding-a-frame"></a>Decodieren eines Frames

Alle Eingabe- und Ausgabeparameter für die Videoverarbeitungsvorgänge sind in einer Eingabeparameterstruktur [,](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_input_stream_arguments)D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS und einer Ausgabeparameterstruktur, D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS. [](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments)
Die Anwendung verwaltet die Referenzframes und muss daher die Referenzframes für jeden Decodierungsvorgang festlegen.
Wenn die Befehlsliste ordnungsgemäß aufgezeichnet ist, rufen Sie [ID3D12CommandQueue::ExecuteCommandLists](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) in der Videobefehlswarteschlange auf, um die Framedecodierung an die GPU zu übermitteln.


### <a name="enabling-decoder-output-conversions"></a>Aktivieren von Decoderausgabekonvertierungen
Wenn der Decoder die Konvertierung unterstützt, aktivieren Sie die [](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments) gewünschten Konvertierungen, indem Sie die D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS auffüllen. Das Format und die Auflösungen der gewünschten Ausgabe im Vergleich zur nativen Ausgabe des Decoders werden über den Unterschied im Farbraum und in den Auflösungen kommuniziert, die in den Konvertierungsparametern angegeben sind.

##  <a name="querying-decoding-status"></a>Abfragen des Decodierungsstatus 
Verwenden Sie die Methoden [ID3D12VideoDecodeCommandList::BeginQuery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-beginquery) und [ID3D12VideoDecodeCommandList::EndQuery,](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-endquery) um den Status des Decodierungsvorgang abfragt.

Die [D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS-Struktur](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_query_data_video_decode_statistics) wird verwendet, um Statistiken zur Videodecodierung zu beschreiben. Um eine Instanz dieser Struktur zu erhalten, rufen Sie [ID3D12VideoDecodeCommandList::EndQuery](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-endquery)auf, und übergeben Sie den Wert des Heapabfragetyps [D3D12_QUERY_TYPE_VIDEO_DECODE_STATISTIC](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type). Beachten Sie, dass diese Abfrage [id3D12VideoDecodeCommandList::BeginQuery nicht verwendet.](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-beginquery)

## <a name="video-processing"></a>Videoverarbeitung

Direct3D 12-Video-APIs verwenden einen optimierten Ansatz für die Videoverarbeitung, wodurch Features von Direct3D 11 entfernt werden, die nicht häufig verwendet wurden, und Funktionsprüfungen für Features entfernt werden, die geräteübergreifend obligatorisch sind. Der Enumerationsprozess für die Videoverarbeitung wird entfernt. Rufen Sie stattdessen [ID3D12VideoDevice::CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) auf, wodurch eine App die Funktionen des Videoprozessors identifizieren kann. Die gewünschten Video-, Interlace-, Stereoformate und -raten werden als Eingabe für **CheckFeatureSupport bereitgestellt.**

### <a name="removed-capabilities"></a>Entfernte Funktionen

Die folgenden Funktionen von Direct3D 11 werden in der Direct3D 12-Videoverarbeitung nicht unterstützt:
- Benutzerdefinierte Raten.  Stattdessen wird während der Aufzeichnung des [Befehls ID3D12VideoProcessCommandList::P rocessFrames eine Eingabe- und Ausgaberate](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist-processframes) angegeben.
- Es sind jetzt nur zwei Deinterlacingmodi verfügbar: [BOB](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_deinterlace_flags) und [CUSTOM](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_deinterlace_flags). Andere Modi wurden entfernt. CUSTOM ist ein qualitativ hochwertiger Deinterlacingmodus, der vom Hardwareanbieter bereitgestellt wird.
- Alle optionalen Stereoformate in [D3D11_VIDEO_PROCESSOR_STEREO_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_stereo_caps) werden nicht mehr unterstützt. Stattdessen sind [nichto,](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format) [horizontal,](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format) [vertikal](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format)und [separat](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format) für alle Hardwaregeräte obligatorisch, wenn Stereo unterstützt wird.
- Es gibt keine Entsprechung für [D3D11_VIDEO_PROCESSOR_FORMAT_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_format_caps) oder [D3D11_VIDEO_PROCESSOR_AUTO_STREAM_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_auto_stream_caps). Stattdessen sind Eingabe- und Ausgabeformate Argumente für die Erstellung des Videoprozessors. Zu diesem Zeitpunkt sollte bekannt sein, ob der Videoprozessor den Vorgang mit dem angegebenen Format ausführen kann oder nicht. Der [D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAGS](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_auto_processing_flags) wird verwendet, um anzugeben, ob Funktionen für die automatische Verarbeitung verfügbar sind.
- Es gibt keine Entsprechung für [D3D11_VIDEO_PROCESSOR_CAPS_LEGACY.](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_feature_caps)
- Es gibt keine Entsprechung für [D3D11_VIDEO_PROCESSOR_CAPS_CONSTRICTION.](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_feature_caps)
- Bei der Konvertierung von Stereo in Mono wird davon ausgegangen, dass die Baselineansicht 0 ist.
- Die Direct3D 12-Videoverarbeitung unterstützt die Konvertierung von Mono in Stereo nicht, und mono-Offset wird nicht unterstützt. 


### <a name="creating-a-video-processor"></a>Erstellen eines Videoprozessors

Rufen [Sie ID3D12VideoDevice::CreateVideoProcessor](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideoprocessor) auf, um eine Instanz von [ID3D12VideoProcessor zu erstellen.](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videoprocessor) Der Videoprozessor enthält den Zustand für eine Videoverarbeitungssitzung, einschließlich des erforderlichen Zwischenspeichers, zwischengespeicherter Verarbeitungsdaten oder eines anderen temporären Arbeitsraums. Die Argumente für die Videoprozessorerstellung geben an, welche Vorgänge ausgeführt werden oder unter [ID3D12VideoProcessCommandList1::P rocessFrames1 verfügbar](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist1-processframes1) sind.  Treiberzuordnungen zum Ausführen des Videoprozessvorgangs (z. B. Zwischenabbildungen) werden zum Zeitpunkt der Videoprozessorerstellung zugeordnet.  Verwenden [D3D12_FEATURE_VIDEO_PROCESSOR_SIZE,](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) um die Zuordnungsgröße des Videoprozessors im Voraus zu bestimmen.

Der Videoprozessor kann nur zum Aufzeichnen von Befehlen aus mehreren Befehlslisten verwendet werden, kann aber nur einer Befehlsliste gleichzeitig zugeordnet sein.  Die Anwendung ist für die Synchronisierung des Zugriffs auf den Videoprozessor verantwortlich.  Die Anwendung muss auch Videoverarbeitungsbefehle für den Videoprocoessor in der Reihenfolge aufzeichnen, in der sie auf der GPU ausgeführt werden.

Alle Eingabe- und Ausgabeargumente für die Videoverarbeitungsvorgänge [](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments)sind in einer Eingabeargumentstruktur, D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS und einer Ausgabeargumentstruktur, D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS. [](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_arguments) Die Anwendung muss [ID3D12VideoProcessCommandList::P rocessFrames](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist-processframes) aufrufen, um den auszuführenden Videoverarbeitungsvorgang aufzeichnen zu können. 

Wenn die Befehlsliste aufgezeichnet wird, rufen Sie [ID3D12CommandQueue::ExecuteCommandLists](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) in der Videobefehlswarteschlange auf, um die Frameverarbeitung an die GPU zu übermitteln.


## <a name="tiers"></a>Ebenen

Direct3D 12-Video definiert Ebenen, die die Funktionen von Hardwaregeräten gruppiert, sodass die App weniger Codepfade für die Vielzahl von Hardware bieten kann. Die Ebenen werden mit der [-Enumeration](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_decode_tier) D3D12_VIDEO_DECODE_TIER angegeben.

In allen Ebenen ist Folgendes verfügbar:

- Es ist nicht notwendig, decoder-Neugestaltung bei Auflösungsänderungen vorzunehmen. Nur der Decoderhap muss bei einer Auflösungsänderung neu erstellt werden.
- Alle Referenzframes werden von der App verwaltet. Dadurch kann das System Arbeitsspeicher sparen, da wir zum Zeitpunkt der Decodererstellung in einigen Ebenen nicht die maximale Anzahl von DPBs zuordnen müssen, und bietet Apps Flexibilität bei der Lösungswechselszenarios.

Beachten Sie, dass es sich bei den Ebenen um Oberstufen handelt. Eine App entscheidet sich möglicherweise für Ebene 1 und verwendet nicht die Funktionen auf höherer Ebene, die zwar zulässig sind, aber möglicherweise keine optimale Leistung bieten. Weitere Informationen zu den Funktionen, die verschiedenen Ebenen zugeordnet sind, finden Sie [unter D3D12_VIDEO_DECODE_TIER](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_decode_tier).

## <a name="reference-frames"></a>Referenzframes

Mit Direct3D 12-Video werden Verweisframes explizit übergeben. Dies ermöglicht eine klare Verwendung von Texturenarrays oder Texturarrays beim Decodieren von Frames. Die App muss nicht genau dasselbe Ressourcenhand handle übergeben, wenn sie als Verweis verwendet wird. Sie kann z. B. entscheiden, eine Ressource in eine andere zu kopieren und dann die Kopie anstelle der ursprünglichen zu übergeben. Die *DXVA-RefFrameList-* *und CurrPic-Indizes* werden weiterhin vom Treiber verwendet, um relevante Daten für jeden decodierten Frame zu speichern.


## <a name="directx-12-fences"></a>DirectX 12 Fences

In DirectX 12 ist die App für die Synchronisierung des Zugriffs auf ihre Puffer verantwortlich. Für den Decodierungsfall müssen den Eingabepuffern und den Ausgabepuffern Fences hinzugefügt werden. Jedem Fence ist ein Wert zugeordnet und wird für die Synchronisierung der CPU und der Hardware-Engines verwendet. Weitere Informationen finden Sie unter [Verwenden von Ressourcenbarrieren zum Synchronisieren von Ressourcenzuständen in Direct3D 12](/windows/desktop/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12).

Eine typische Implementierung hat einen Fence für jeden Eingabepuffer. Bei Eingabepuffern ist es möglich, dass der Puffer verfügbar ist, bevor der gesamte Decodierungsprozess abgeschlossen ist. Das System ignoriert diesen Fall und geht davon aus, dass der Eingabepuffer verfügbar ist, wenn die Decodierung abgeschlossen ist.
Eine Implementierung verfügt in der Regel auch über einen Fence für jeden Ausgabepuffer. Im Fall des Sendens der Ausgabe an den Compositor wird beispielsweise ein Fence benötigt, der signalisiert wird, wenn diese Darstellung dieses Frames schließlich abgeschlossen ist, was angibt, dass die Ausgabe wieder für den Decoder verfügbar ist.


## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>
[Direct3D 12 Video-APIs](direct3d-12-video-apis.md) 
 [Media Foundation Programmierhandbuch](media-foundation-programming-guide.md)
</dt> </dl>

 

 
