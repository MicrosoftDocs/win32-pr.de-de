---
description: Beschreibt entsprechende Direct3D 12-Video-APIs zu früheren Versionen.
ms.assetid: ''
title: Siehe Migrieren zu Direct3D 12 (Video).
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: 56af5ba7845db5e1d4bfeac280cae9235f47ebe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344849"
---
# <a name="migrating-to-direct3d-12-video"></a>Siehe Migrieren zu Direct3D 12 (Video).

In diesem Artikel werden die Direct3D 12-Video-APIs beschrieben, die zum Implementieren der in früheren Versionen verfügbaren Features verwendet werden. Um die Leistung und die Benutzerfreundlichkeit der Video Features mit der höchsten Priorität zu verbessern, werden einige Features von Direct3D 11 in Direct3D 12 vollständig oder teilweise nicht unterstützt. 

Beachten Sie, dass zwar die meisten Features von Direct3D 11 in Direct3D 12 verfügbar sind, sich das API-Design jedoch geändert hat, sodass es in vielen Fällen nicht zu einer Zuordnung von APIs zwischen den beiden API-Sätzen kommt. Die folgenden Tabellen sollen Sie auf die relevantesten APIs in Direct3D 12 für jede Direct3D 11-API verweisen, aber die Art und Weise, in der Sie die neuen APIs verwenden, kann sich erheblich unterscheiden. Beispiel:

- Zum Decodieren eines Video Frame verwendet die Direct3D 11-Video-APIs Aufrufe von [decoderbeginframe](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe), [getdecoderbuffer](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer), [submitdecoderbuffers](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers)und [decoderendframe](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe). Bei Direct3D 12 wird eine einzelne Methode verwendet,  [ID3D12VideoDecodeCommandList::D ecodeframe](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe).
- Bei der Videoverarbeitung stellte Direct3D 11 einzelne Methoden zum Festlegen der verschiedenen Konfigurationswerte bereit, wie z. b. [videoprocess orsetoutputcolorspace](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputcolorspace) und [videoprocesorsetoutputalphafillmode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputalphafillmode). In Direct3D 12 werden diese Werte festgelegt, wenn der Videoprozessor erstellt wird, im Aufrufen von [ID3D12VideoDevice:: Erstellungs Videoprozessor](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideoprocessor)oder bei der Verarbeitung des Frames mit einem Aufrufen von [ID3D12VideoProcessCommandList1::P rocessframes1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist1-processframes1).





## <a name="id3d11videocontext"></a>ID3D11VideoContext
Bietet die Videofunktionen eines Direct3D 11-Geräts, einschließlich Video Decodierung, Videoverarbeitung, GPU-basierter Inhalts Schutz und Verschlüsselung/Entschlüsselung von Videos. Diese Funktion ist für Direct3D 12 teilweise implementiert.


| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [Konfigurieren von reauthentiinitiedchannel](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel) | Nicht implementiert |
| [Decoderbeginframe](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe)| [ID3D12VideoDecodeCommandList::D "Ecode Frame](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe)", "  [D3D12_VIDEO_DECODE_FRAME_ARGUMENT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_frame_argument)", " [D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_compressed_bitstream) [D3D12_VIDEO_DECODE_REFERENCE_FRAMES](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_reference_frames) |
| [Decoderendframe](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe) | [ID3D12VideoDecodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videodecodecommandlist) |
| [Decoderextension](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderextension) | Nicht implementiert. |
| [Decryptionblt](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)  | Nicht implementiert. |
| [Verschlüsselungsblt](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt) | Nicht implementiert. |
| [Finishsessionkeyrefresh](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh) | Nicht implementiert. |
| [Getdecoderbuffer](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) | Nicht implementiert. Komprimierte Puffer werden in Direct3D 12 von der APP verwaltet. |
| [Getencryptionbltkey](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey) | Nicht implementiert. | 
| [Aushandateauthentichanedchannelkeyexchange](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-negotiateauthenticatedchannelkeyexchange) | Nicht implementiert. |
| [Aushandatecryptosessionkeyexchange](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-negotiatecryptosessionkeyexchange) | Nicht implementiert. |
| [Queryauthentiinitiedchannel](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-queryauthenticatedchannel) | Nicht implementiert. |
| [Releasedecoderbuffer](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer) | Nicht implementiert. Komprimierte Puffer werden in Direct3D 12 von der APP verwaltet. |
| [Starungessionkeyrefresh](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh) | Nicht implementiert |
| [Submitdecoderbuffers](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers) | [ID3D12VideoDecodeCommandList::D "Ecode Frame"](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe) |
| [Videoprocess orblt](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt) | [ID3D12VideoProcessCommandList1::P rocessframes1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist1-processframes1) |
| [Videoprocess orgetoutputalphafillmode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputalphafillmode) [videoprocess orsetoutputalphafillmode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputalphafillmode) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. Alphafillmode](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [Videoprocess orgetoutputbackgroundcolor](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputbackgroundcolor) [videoprocess orsetoutputbackgroundcolor](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputbackgroundcolor) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. Background Color](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc)  |
| [Videoprocesorgetoutputcolorspace](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputcolorspace) [videoprocess orsetoutputcolorspace](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputcolorspace) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. Colorspace](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc)  |
| [Videoprocess orgetoutput\striction](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputconstriction) [videoprocess orsetoutput\striction](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputconstriction) | Nicht implementiert. Software DRM wird nicht unterstützt. |
| [Videoprocess orgetoutputextension](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputextension) [videoprocess orsetoutputextension](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputextension) | Nicht implementiert. |
| [Videoprocess orgetoutputstereomode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputstereomode) [videoprocess orsetoutputstereomode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputstereomode) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. Enablestereo](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [Videoprocess orgetoutputtargetrect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputtargetrect) [videoprocess orsetoutputtargetrect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputtargetrect) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS. Targetrechteck](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_arguments) |
| [Videoprocess orgetstreamalpha](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamalpha) [videoprocess-setstreamalpha](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamalpha)  | [D3D12_VIDEO_PROCESS_ALPHA_BLENDING. Alpha](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_alpha_blending) |
| [Videoprocess orgetstreamautoprocessingmode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamautoprocessingmode) [videoprocess orsetstreamautoprocessingmode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamautoprocessingmode) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC. Enableautoprocessing](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [Videoprocesorgetstreamcolorspace](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamcolorspace) [videoprocesorsetstreamcolorspace](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamcolorspace) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Colorspace](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [Videoprocess orgetstreamdestrect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamdestrect) [videoprocess orsetstreamdestrect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamdestrect) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Destinationrechteck](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [Videoprocess orgetstreamextension](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamextension) [videoprocbilorsetstreamextension](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamextension) | Nicht implementiert. |
| [Videoprocess orgetstreamfilter](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamfilter) [videoprocmeorsetstreamfilter](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamfilter) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Filterflags](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [Videoprocess orgetstreamframeformat](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamframeformat) [videoprocess orsetstreamframeformat](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamframeformat) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Ges](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [Videoprocess orgetstreamlumakey](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamlumakey) [videoprocess orsetstreamlumakey](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamlumakey) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Lumakey](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [Videoprocess orgetstreamoutputrate](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamoutputrate) [videoprocess orsetstreamoutputrate](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamoutputrate) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. FrameRate](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [VideoProcessorGetStreamPalette](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreampalette) [VideoProcessorSetStreamPalette](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreampalette) | Nicht implementiert |
| [Videoprocesorgetstreampixelaspectratio](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreampixelaspectratio) [videoprocesorsetstreampixelaspectratio](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreampixelaspectratio) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Sin](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |
| [Videoprocess orgetstreamrotation](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamrotation) [videoprocess-setstreamrotation](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamrotation) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Sin](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |
| [Videoprocmeorgetstreamsourcerect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamsourcerect) [videoprocess orsetstreamsourcerect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamsourcerect) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Sin](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |
| [Videoprocooorgetstreamstereoformat](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamstereoformat) [videoprocess-setstreamstereoformat](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamstereoformat) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Sin](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |

## <a name="id3d11videocontext1"></a>ID3D11VideoContext1

Bietet erweiterte Videofunktionen eines Direct3D 11-Geräts, einschließlich Hardware-DRM, Verbesserungen der Oberflächen Auslastung und mehr Video Verarbeitungsfunktionen. Diese Funktion wird für Direct3D 12 über neue Schnittstellen implementiert.


| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| Checkcryptosessionstatus | TBD | 
| [Decoderenabledownsampling](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) | [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments) |
| [Decoderupdatedownsampling](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-decoderenabledownsampling) | [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments) |
| [Getdatafornetwhardwarekey](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-getdatafornewhardwarekey) | TBD |
| [SubmitDecoderBuffers1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-submitdecoderbuffers1) | [ID3D12VideoDecodeCommandList::D "Ecode Frame"](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe) |
| [Videoprocess orgetverhalverhalhinweise](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetbehaviorhints) | TBD |
| [VideoProcessorGetOutputColorSpace1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetoutputcolorspace1) [VideoProcessorSetOutputColorSpace1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetoutputcolorspace1) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. Colorspace](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [Videoprocmeorgetoutputshaderusage](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetoutputshaderusage) [videoprocess orsetoutputshaderusage](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetoutputshaderusage) | TBD |
| [VideoProcessorGetStreamColorSpace1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetstreamcolorspace1) [VideoProcessorSetStreamColorSpace1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetstreamcolorspace1) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC. Colorspace](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [Videoprocess orgetstreammirror](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetstreammirror) [videoprocess-setstreammirror](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetstreammirror) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Sin](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |

## <a name="id3d11videodecoder"></a>ID3D11VideoDecoder

Stellt einen Hardware beschleunigten Video Decoder für Direct3D 11 dar. Dies ist eine Wrapper Schnittstelle um [ID3D11VideoContext](/windows/win32/api/d3d11/nn-d3d11-id3d11videocontext) , die die tatsächliche Decodierungs Funktionalität verfügbar macht. Es ist keine entsprechende API für Direct3D 12-Video vorhanden.


## <a name="id3d11videodecoderoutputview"></a>ID3D11VideoDecoderOutputView

Gibt die Ausgabe Oberflächen an, auf die während der Video Decodierung zugegriffen werden kann. In Direct3D 12 verwendet die [ID3D12VideoProcessor](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoprocessor) -Schnittstelle [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) -Objekte direkt.

## <a name="id3d11videodevice"></a>ID3D11VideoDevice

Bietet die videodecodierungs-und Video Verarbeitungsfunktionen eines Direct3D 11-Geräts. Dies ist der Haupteinstiegspunkt zum Erstellen des Video Decoder-Geräts und der Kryptografiesitzung sowie für die Videoverarbeitung,-Funktionen,-Profile usw. Diese Funktion ist für Direct3D 12 teilweise implementiert.


| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [Checkcryptokeyexchange](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-checkcryptokeyexchange) | Nicht implementiert. |
| [Checkvideodecoderformat](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-checkvideodecoderformat) | [D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_formats) |
| ["Kreateauthentiinitiedchannel"](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel) | Nicht implementiert. |
| ["Deecryp"-Sitzung](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) | Nicht implementiert. |
| [Createvideodecoder](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) | [ID3D12VideoDevice:: createvideodecoder](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoder)  [ID3D12VideoDevice:: createvideodecoderheap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoderheap) |
| [Createvideodecoderoutputview](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview) | [ID3D12Texture2D](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) |
| ["Kreatevideoprocessor"](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor) | [ID3D12VideoDevice:: kreatevideoprocessor](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideoprocessor)  |
| ["Kreatevideoprocess"-erator](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessorenumerator) | – |
| ["Kreatevideoprocess orinputview"](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessorinputview) | [ID3D12Texture2D](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) |
| ["Kreatevideoprocess oroutputview"](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessoroutputview) | [ID3D12Texture2D](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) |
| [Getcontentschutzcaps](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getcontentprotectioncaps) | TBD
| [Getvideodecoderconfig](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfig) | In Direct3D 12 wird nur der VLD-Modus unterstützt. [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles) [D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_formats) |
| [Getvideodecoderconfigcount](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfigcount) | – |
| [Getvideodecoderprofile](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile) | [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles) |
| [Getvideodecoderprofilecount](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofilecount) | [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES. Profil Anzahl](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles) |
| [SetPrivateData](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-setprivatedata) | [ID3D12Object:: setprivatedata](/windows/win32/api/d3d12/nf-d3d12-id3d12object-setprivatedata) |
| [SetPrivateDataInterface](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-setprivatedatainterface) | [ID3D12Object:: setprivatedatainterface](/windows/win32/api/d3d12/nf-d3d12-id3d12object-setprivatedatainterface) |

## <a name="id3d11videodevice1"></a>ID3D11VideoDevice1

Bietet erweiterte Video-Decodierung und Video Verarbeitungsfunktionen eines Direct3D 11-Geräts, einschließlich mehr Erweiterungen, Hardware-DRM-Dateien, Decodieren von Downsampling, Video Decoder-Funktionen usw. Diese Funktion ist für Direct3D 12 implementiert.

| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [Checkvideodecoderdownsampling](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-checkvideodecoderdownsampling) | [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support) |
| [Getcryptosessionprivatedatasize](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-getcryptosessionprivatedatasize) | TBD |
| [Getvideodecodercaps](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-getvideodecodercaps) | [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support) |
| [RecommendVideoDecoderDownsampleParameters](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-recommendvideodecoderdownsampleparameters) | [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support) |


## <a name="id3d11videoprocessor"></a>ID3D11VideoProcessor

Stellt einen Videoprozessor für Direct3D 11 dar. Diese Funktionalität ist für Direct3D 12 in den [ID3D12VideoProcessor](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoprocessor) implementiert.

| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [GetContentDesc](/windows/win32/api/d3d11/nf-d3d11-id3d11videoprocessor-getcontentdesc)| Nicht implementiert |
| [Getrateconversioncaps](/windows/win32/api/d3d11/nf-d3d11-id3d11videoprocessor-getrateconversioncaps) | Nicht implementiert |


## <a name="id3d11videoprocessorenumerator-and-id3d11videoprocessorenumerator1"></a>ID3D11VideoProcessorEnumerator und ID3D11VideoProcessorEnumerator1

Listet die Videoprozessor Funktionen eines Direct3D 11-Geräts auf.
In Direct3D 12 wird die enumerationsfunktionalität durch [ID3D12VideoDevice:: checkfeaturesupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport)ersetzt. 

##  <a name="id3d11videoprocessorinputview"></a>ID3D11VideoProcessorInputView

Identifiziert die Eingabe Oberflächen, auf die während der Videoverarbeitung zugegriffen werden kann.
In Direct3D 12 wird dies durch ID3D12Texture2D ersetzt.

##  <a name="id3d11videoprocessoroutputview"></a>ID3D11VideoProcessorOutputView

Gibt die Ausgabe Oberflächen an, auf die während der Videoverarbeitung zugegriffen werden kann.
In Direct3D 12 wird dies durch ID3D12Texture2D ersetzt.

## <a name="id3d11authenticatedchannel"></a>ID3D11AuthenticatedChannel

Stellt einen sicheren Kommunikationskanal mit dem Grafiktreiber oder der Microsoft Direct3D-Laufzeit bereit. Diese Funktion ist für Direct3D 12-Video nicht implementiert.

##  <a name="id3d11cryptosession"></a>ID3D11CryptoSession

Stellt eine Kryptografiesitzung dar. Wird für Software-und Hardware-DRM-Szenarien verwendet. Es ist keine entsprechende öffentliche API für Direct3D 12-Video vorhanden.

## <a name="related-topics"></a>Zugehörige Themen

[Direct3D 12-Video-APIs](direct3d-12-video-apis.md)


 

 




