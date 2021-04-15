---
description: Dieser Artikel enthält allgemeine Anleitungen für die Verwendung der Direct3D 12-Video-APIs.
ms.assetid: ''
title: Direct3D 12-Video Übersicht
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: b21587f2784b34131da9c050655b6f3fbe43582d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524563"
---
# <a name="direct3d-12-video-overview"></a>Direct3D 12-Video Übersicht

Dieser Artikel enthält allgemeine Anleitungen für die Verwendung der Direct3D 12-Video-APIs.

## <a name="about-direct3d-12-video"></a>Info zu Direct3D 12-Video

Die Videoschnittstelle Direct3D 12 bietet eine neue Möglichkeit für apps, Video Decodierung und-Prozess zu implementieren. Die Direct3D 12-Schnittstelle unterscheidet sich von der vorherigen Direct3D 11-Schnittstelle, da Sie für die Konsistenz mit den Direct3D 12-Prinzipien und-Stil konzipiert wurde, darunter die folgenden:

- Entwicklern mehr Kontrolle verschaffen
 - Zuordnung von Hardware zugreif baren Arbeitsspeicher
 - CPU-Threads zum generieren & Befehle zum Senden
   - Unabhängige Generierung und Übermittlung
   - Nicht blockierend
 - Planen der Hardware Arbeit
- Behandelt vorhandene Funktionen, einschließlich der meisten Direct3D 11-Videofunktionen, aber gleichzeitig die Einfachheit und Benutzerfreundlichkeit zu berücksichtigen.
- Leistung und Leistung von Haupt Direct3D 12 Anwendungen gleich oder besser als Direct3D 11
- Konsistenz mit anderen Direct3D 12-APIs
- Interoperabilität mit vorhandenen Grafik-APIs


## <a name="video-decoding"></a>Video Decodierung

In den folgenden Abschnitten werden einige der Aufgaben beschrieben, die bei der Implementierung von Direct3D 12-Video Decodierung beteiligt sind

### <a name="query-for-decoding-capabilities"></a>Abfrage der Decodierungs Funktionen

Wenden Sie sich an [ID3D12VideoDevice:: checkfeaturesupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) , um die Support Details für Direct3D 12-Video Decodierungs Vorgänge zu überprüfen. Übergeben Sie einen Wert aus der [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) -Enumeration, um das Feature anzugeben, für das Sie Support Informationen anfordern.

### <a name="create-the-video-decoder"></a>Erstellen des Video-Decoders

Rufen Sie [ID3D12VideoDevice:: createvideodecoder](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoder) auf, um eine Instanz der [ID3D12VideoDecoder](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecoder) -Schnittstelle zu erstellen. Der Decoder behält den Zustand einer decodiersitzung bei, einschließlich Verweis bezogener Daten, z. b. Bewegungsvektoren.  Im Fall einer Änderung der Auflösung oder einer Änderung von [maxdecodepicturebuffercount](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decoder_heap_desc) wird das Decoder-Objekt neu erstellt. Die Breite und die Höhe des Decodierungs Modus geben die systemeigene streamauflösung vor jeder Skala an.  Die DPB-Anzahl (Maximum Decode Image Buffer) gibt die größte DPB-Anzahl an, die verwendet werden kann, ohne dass der Video Decoder neu erstellt werden kann.

Der Decoder kann verwendet werden, um Befehle aus mehreren Befehlslisten aufzuzeichnen, kann jedoch nur jeweils einer Befehlsliste zugeordnet werden.  Die Anwendung ist für die Synchronisierung des Zugriffs auf den Decoder verantwortlich.

### <a name="create-the-video-decoder-heap"></a>Erstellen des Video Decoder-Heaps 

Rufen Sie [ID3D12VideoDevice:: createvideodecoderheap](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoderheap) auf, um eine Instanz der [ID3D12VideoDecoderHeap](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecoderheap) -Schnittstelle zu erstellen. Dieses Objekt enthält die von der Auflösung abhängigen Treiber Ressourcen und den Status.

### <a name="decoding-a-frame"></a>Decodieren eines Frames

Alle Eingabe-und Ausgabeparameter für die Video Verarbeitungsvorgänge werden in einer Eingabeparameter Struktur, [D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_input_stream_arguments)und einer Ausgabeparameter Struktur, [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments), angeordnet.
Die Anwendung verwaltet die Verweis Rahmen und muss daher die Verweis Rahmen für jeden Decodierungs Vorgang festlegen.
Wenn die Befehlsliste ordnungsgemäß aufgezeichnet wird, können Sie [ID3D12CommandQueue:: executecommandlists](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) in der Video Befehls Warteschlange aufrufen, um die Frame-Decodierung an die GPU zu übermitteln.


### <a name="enabling-decoder-output-conversions"></a>Aktivieren von Decoder-Ausgabe Konvertierungen
Wenn der Decoder die Konvertierung unterstützt, aktivieren Sie die gewünschten Konvertierungen, indem Sie die [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments) Struktur ordnungsgemäß ausfüllen. Das Format und die Auflösungen der gewünschten Ausgabe im Vergleich zur systemeigenen Ausgabe des Decoders werden über den Unterschied in den Farbräumen und Auflösungen kommuniziert, die in den Konvertierungs Parametern angegeben werden.

##  <a name="querying-decoding-status"></a>Decodierungs Status wird abgefragt 
Verwenden Sie die Methoden [ID3D12VideoDecodeCommandList:: beginquery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-beginquery) und [ID3D12VideoDecodeCommandList:: endquery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-endquery) , um den Status des Decodierungs Vorgangs abzufragen.

Die [D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_query_data_video_decode_statistics) Struktur wird verwendet, um die Video-Decodierung von Statistiken zu beschreiben. Zum Abrufen einer Instanz dieser Struktur wird [ID3D12VideoDecodeCommandList:: endquery](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-endquery)aufgerufen, wobei der Heap-Abfragetyp Wert [D3D12_QUERY_TYPE_VIDEO_DECODE_STATISTIC](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type)übergeben wird. Beachten Sie, dass diese Abfrage nicht [ID3D12VideoDecodeCommandList:: beginquery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-beginquery)verwendet.

## <a name="video-processing"></a>Video Verarbeitung

Direct3D 12-Video-APIs sind eine optimierte Herangehensweise an die Videoverarbeitung und eliminieren Features von Direct3D 11, die nicht häufig verwendet wurden, und Entfernen von Funktionsprüfungen für Features, die Geräte übergreifend obligatorisch sind. Der enumerationsprozess für die Videoverarbeitung wird entfernt. Verwenden Sie stattdessen [ID3D12VideoDevice:: checkfeaturesupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) , mit dem eine APP die Funktionen des Video Prozessors identifizieren kann. Die gewünschten Videos, Interlace, Stereoformate und Raten werden als Eingabe für **checkfeaturesupport** bereitgestellt.

### <a name="removed-capabilities"></a>Entfernte Funktionen

Die folgenden Funktionen von Direct3D 11 werden in der Direct3D 12-Videoverarbeitung nicht unterstützt:
- Benutzerdefinierte Tarife.  Stattdessen wird während der [ID3D12VideoProcessCommandList::P rocess Frames](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist-processframes) -Befehls Aufzeichnung eine Eingabe-und eine Ausgabe Rate angegeben.
- Jetzt stehen nur noch zwei Deinterlacing-Modi zur Verfügung: [Bob](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_deinterlace_flags) und [Custom](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_deinterlace_flags). Andere Modi wurden entfernt. Benutzer definiert ist ein hochwertiger deinterlacingmodus, der vom Hardwarehersteller bereitgestellt wird.
- Alle optionalen Stereoformate in [D3D11_VIDEO_PROCESSOR_STEREO_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_stereo_caps) werden nicht mehr unterstützt. Stattdessen sind " [Nono](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format)", " [Horizontal](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format)", " [vertikal](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format)" und " [separat](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format) " für alle Hardware Geräte obligatorisch, wenn Stereo unterstützt wird.
- Es gibt keine Entsprechung für [D3D11_VIDEO_PROCESSOR_FORMAT_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_format_caps) oder [D3D11_VIDEO_PROCESSOR_AUTO_STREAM_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_auto_stream_caps). Stattdessen sind Eingabe-und Ausgabeformate Argumente für die Erstellung des Video Prozessors, und zu diesem Zeitpunkt sollte bekannt sein, ob der Videoprozessor den Vorgang mit dem angegebenen Format ausführen kann oder nicht. Der [D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAGS](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_auto_processing_flags) wird verwendet, um anzugeben, ob Funktionen zur automatischen Verarbeitung verfügbar sind.
- Es gibt keine Entsprechung für [D3D11_VIDEO_PROCESSOR_CAPS_LEGACY](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_feature_caps).
- Es gibt keine Entsprechung für [D3D11_VIDEO_PROCESSOR_CAPS_CONSTRICTION](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_feature_caps).
- Bei der Umstellung von Stereo in Mono geht davon aus, dass die Baseline-Sicht 0 ist.
- Die Direct3D 12-Videoverarbeitung unterstützt das Umrechnen von Mono in Stereo nicht, und es gibt keine Unterstützung für Mono-Offset. 


### <a name="creating-a-video-processor"></a>Erstellen eines Video Prozessors

Rufen Sie [ID3D12VideoDevice:: kreatevideoprocessor](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideoprocessor) auf, um eine Instanz des [ID3D12VideoProcessor](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videoprocessor)-Objekts zu erstellen. Der Videoprozessor hält den Status für eine Video Verarbeitungs Sitzung, einschließlich erforderlicher Zwischenspeicher, zwischen gespeicherter Verarbeitungsdaten oder anderem temporärer Arbeitsbereich. Die Argumente für die Erstellung des Video Prozessors geben an, welche Vorgänge ausgeführt werden oder unter [ID3D12VideoProcessCommandList1::P rocessframes1](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist1-processframes1) Time verfügbar sind.  Treiber Zuordnungen zum Ausführen des Video Verarbeitungsvorgangs (z. b. Vermittler) werden zum Zeitpunkt der Erstellung des Video Prozessors zugeordnet.  Verwenden Sie [D3D12_FEATURE_VIDEO_PROCESSOR_SIZE](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) , um die Zuordnungs Größe des Video Prozessors im Voraus zu bestimmen.

Der Videoprozessor kann nur dazu verwendet werden, Befehle aus mehreren Befehlslisten aufzuzeichnen, aber nur jeweils einer Befehlsliste zugeordnet zu werden.  Die Anwendung ist für die Synchronisierung des Zugriffs auf den Videoprozessor verantwortlich.  Die Anwendung muss auch Video Verarbeitungs Befehle für den videoprokoessor in der Reihenfolge aufzeichnen, in der Sie auf der GPU ausgeführt werden.

Alle Eingabe-und Ausgabe Argumente für die Video Verarbeitungsvorgänge werden in einer Eingabe Argument Struktur, [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments)und einer Ausgabe Argument Struktur, [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_arguments), angeordnet. Die Anwendung muss [ID3D12VideoProcessCommandList::P rocess Frames](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist-processframes) aufzurufen, um den auszuführenden Video Verarbeitungsvorgang aufzuzeichnen. 

Wenn die Befehlsliste aufgezeichnet wird, können Sie [ID3D12CommandQueue:: executecommandlists](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) in der Video Befehls Warteschlange aufrufen, um die Frame-Verarbeitung an die GPU zu übermitteln.


## <a name="tiers"></a>Ebenen

Das Video Direct3D 12 definiert Ebenen, die die Funktionen von Hardware Geräten gruppieren, sodass die APP weniger Codepfade für die Vielfalt der Hardware aufweisen kann. Die Ebenen werden mit der [D3D12_VIDEO_DECODE_TIER](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_decode_tier) -Enumeration angegeben.

Auf allen Ebenen steht Folgendes zur Verfügung:

- Es ist nicht erforderlich, dass Decoder bei der Auflösung geändert werden. Bei einer Auflösungs Änderung muss nur der Decoder-Heap neu erstellt werden.
- Alle Referenzrahmen werden von der APP verwaltet. Dies ermöglicht dem System, Arbeitsspeicher zu sparen, da wir nicht die maximale Anzahl von dpds zum Erstellungs Zeitpunkt des Decoders in einigen Tarifen zuordnen müssen und apps Flexibilität bei der Behebung von Szenarios für die Lösung bieten.

Beachten Sie, dass die Ebenen Supersets sind. Eine APP kann sich für Ebene 1 entscheiden und nicht die Features höherer Ebene verwenden, die zulässig sind, aber möglicherweise keine optimale Leistung bieten. Weitere Informationen zu den Funktionen, die unterschiedlichen Ebenen zugeordnet sind, finden Sie unter [D3D12_VIDEO_DECODE_TIER](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_decode_tier).

## <a name="reference-frames"></a>Verweis Rahmen

Mit Direct3D 12 Video werden Verweis Rahmen explizit übermittelt. Dies ermöglicht eine deutliche Verwendung eines Arrays von Texturen oder Textur Arrays, wenn wir Frames dekodieren. Es ist nicht erforderlich, dass die APP genau dasselbe Ressourcen handle übergibt, wenn Sie als Verweis verwendet wird. Es kann beispielsweise entscheiden, eine Ressource in eine andere Ressource zu kopieren und dann die Kopie anstelle der ursprünglichen zu übergeben. Die DXVA *refframelist* -und *currpic* -Indizes werden vom Treiber weiterhin verwendet, um relevante Daten für jeden decodierten Frame zu speichern.


## <a name="directx-12-fences"></a>DirectX 12-Zäune

In DirectX 12 ist die APP für die Synchronisierung des Zugriffs auf die Puffer verantwortlich. Beim Decodieren ist es erforderlich, dass den Eingabe Puffern und den Ausgabe Puffern Zäune hinzugefügt werden. Jedem Fence ist ein Wert zugeordnet, der für die Synchronisierung der CPU und der Hardware-Engines verwendet wird. Weitere Informationen finden Sie unter [Verwenden von Ressourcen Barrieren zum Synchronisieren von Ressourcen Zuständen in Direct3D 12](/windows/desktop/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12).

Eine typische-Implementierung verfügt über einen Fence für jeden Eingabepuffer. Im Fall von Eingabe Puffern ist es möglich, dass der Puffer verfügbar ist, bevor der gesamte Decodierungs Prozess abgeschlossen ist. Das System ignoriert diesen Fall und geht davon aus, dass der Eingabepuffer verfügbar ist, wenn die Decodierung abgeschlossen ist.
Eine Implementierung verfügt in der Regel auch über einen Fence für jeden Ausgabepuffer. Beim Senden der Ausgabe an den Compositor ist beispielsweise ein Fence erforderlich, der signalisiert wird, wenn diese Darstellung des Frames schließlich abgeschlossen wird, und gibt an, dass die Ausgabe wieder für den Decoder verfügbar ist.


## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>
[Direct3D 12-Video-APIs](direct3d-12-video-apis.md) 
 [Media Foundation-Programmier Handbuch](media-foundation-programming-guide.md)
</dt> </dl>

 

 
