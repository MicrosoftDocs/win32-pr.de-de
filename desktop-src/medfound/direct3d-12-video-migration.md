---
description: Beschreibt äquivalente Direct3D 12-Video-APIs zu früheren Versionen.
ms.assetid: ''
title: Siehe Migrieren zu Direct3D 12 (Video).
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: 4004c35c21d9d6c67c0af3f9413521cf845437cddbc2ce245c3da495ed3daca5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777420"
---
# <a name="migrating-to-direct3d-12-video"></a>Siehe Migrieren zu Direct3D 12 (Video).

In diesem Artikel werden die Direct3D 12-Video-APIs beschrieben, die zum Implementieren von Features verwendet werden, die in früheren Versionen verfügbar sind. Um die Leistung und Nutzbarkeit der Videofeatures mit der höchsten Priorität zu verbessern, werden einige Features von Direct3D 11 in Direct3D 12 vollständig oder teilweise nicht unterstützt. 

Beachten Sie, dass zwar die meisten Features von Direct3D 11 in Direct3D 12 verfügbar sind, das API-Design jedoch geändert wurde, sodass es in vielen Fällen keine 1:1-Zuordnung von APIs zwischen den beiden API-Sätzen gibt. Die folgenden Tabellen sollen Sie auf die relevantesten APIs in Direct3D 12 für jede Direct3D 11-API verweisen, aber die Verwendung der neuen APIs kann sich erheblich unterscheiden. Beispiel:

- Zum Decodieren eines Videoframes verwenden die Direct3D 11-Video-APIs Aufrufe von [DecoderBeginFrame,](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) [GetDecoderBuffer,](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) [SubmitDecoderBuffers](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers)und [DecoderEndFrame](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe). Bei Direct3D 12 wird eine einzelne Methode verwendet: [ID3D12VideoDecodeCommandList::D ecodeFrame.](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe)
- Für die Videoverarbeitung stellte Direct3D 11 einzelne Methoden zum Festlegen der verschiedenen Konfigurationswerte bereit, z. B. [VideoProcessorSetOutputColorSpace](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputcolorspace) und [VideoProcessorSetOutputAlphaFillMode.](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputalphafillmode) In Direct3D 12 werden diese Werte festgelegt, wenn der Videoprozessor erstellt wird, beim Aufruf von [ID3D12VideoDevice::CreateVideoProcessor](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideoprocessor)oder wenn der Frame mit einem Aufruf von [ID3D12VideoProcessCommandList1::P rocessFrames1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist1-processframes1)verarbeitet wird.





## <a name="id3d11videocontext"></a>ID3D11VideoContext
Stellt die Videofunktionen eines Direct3D 11-Geräts bereit, einschließlich Videodecodierung, Videoverarbeitung, GPU-basierter Inhaltsschutz und Videoverschlüsselung/-entschlüsselung. Diese Funktionalität ist teilweise für Direct3D 12 implementiert.


| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [ConfigureAuthenticatedChannel](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel) | Nicht implementiert |
| [DecoderBeginFrame](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe)| [ID3D12VideoDecodeCommandList::D ecodeFrame](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe),  [D3D12_VIDEO_DECODE_FRAME_ARGUMENT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_frame_argument), [D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_compressed_bitstream), [D3D12_VIDEO_DECODE_REFERENCE_FRAMES](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_reference_frames) |
| [DecoderEndFrame](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe) | [ID3D12VideoDecodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videodecodecommandlist) |
| [DecoderExtension](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderextension) | Nicht implementiert. |
| [DecryptionBlt](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)  | Nicht implementiert. |
| [EncryptionBlt](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt) | Nicht implementiert. |
| [FinishSessionKeyRefresh](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh) | Nicht implementiert. |
| [GetDecoderBuffer](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) | Nicht implementiert. Komprimierte Puffer werden in Direct3D 12 von der App verwaltet. |
| [GetEncryptionBltKey](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey) | Nicht implementiert. | 
| [NegotiateAuthenticatedChannelKeyExchange](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-negotiateauthenticatedchannelkeyexchange) | Nicht implementiert. |
| [NegotiateCryptoSessionKeyExchange](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-negotiatecryptosessionkeyexchange) | Nicht implementiert. |
| [QueryAuthenticatedChannel](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-queryauthenticatedchannel) | Nicht implementiert. |
| [ReleaseDecoderBuffer](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer) | Nicht implementiert. Komprimierte Puffer werden in Direct3D 12 von der App verwaltet. |
| [StartSessionKeyRefresh](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh) | Nicht implementiert |
| [SubmitDecoderBuffers](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers) | [ID3D12VideoDecodeCommandList::D ecodeFrame](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe) |
| [VideoProcessorBlt](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt) | [ID3D12VideoProcessCommandList1::P rocessFrames1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist1-processframes1) |
| [VideoProcessorGetOutputAlphaFillMode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputalphafillmode) [VideoProcessorSetOutputAlphaFillMode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputalphafillmode) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. AlphaFillMode](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [VideoProcessorGetOutputBackgroundColor](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputbackgroundcolor) [VideoProcessorSetOutputBackgroundColor](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputbackgroundcolor) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. Backgroundcolor](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc)  |
| [VideoProcessorGetOutputColorSpace](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputcolorspace) [VideoProcessorSetOutputColorSpace](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputcolorspace) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. Farbraum](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc)  |
| [VideoProcessorGetOutputConstriction](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputconstriction) [VideoProcessorSetOutputConstriction](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputconstriction) | Nicht implementiert. Software-DRM wird nicht unterstützt. |
| [VideoProcessorGetOutputExtension](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputextension) [VideoProcessorSetOutputExtension](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputextension) | Nicht implementiert. |
| [VideoProcessorGetOutputStereoMode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputstereomode) [VideoProcessorSetOutputStereoMode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputstereomode) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. EnableStereo](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [VideoProcessorGetOutputTargetRect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputtargetrect) [VideoProcessorSetOutputTargetRect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputtargetrect) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS. TargetRectangle](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_arguments) |
| [VideoProcessorGetStreamAlpha](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamalpha) [VideoProcessorSetStreamAlpha](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamalpha)  | [D3D12_VIDEO_PROCESS_ALPHA_BLENDING. Alpha](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_alpha_blending) |
| [VideoProcessorGetStreamAutoProcessingMode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamautoprocessingmode) [VideoProcessorSetStreamAutoProcessingMode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamautoprocessingmode) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC. EnableAutoProcessing](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [VideoProcessorGetStreamColorSpace](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamcolorspace) [VideoProcessorSetStreamColorSpace](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamcolorspace) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Farbraum](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [VideoProcessorGetStreamDestRect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamdestrect) [VideoProcessorSetStreamDestRect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamdestrect) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. DestinationRectangle](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [VideoProcessorGetStreamExtension](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamextension) [VideoProcessorSetStreamExtension](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamextension) | Nicht implementiert. |
| [VideoProcessorGetStreamFilter](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamfilter) [VideoProcessorSetStreamFilter](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamfilter) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. FilterFlags](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [VideoProcessorGetStreamFrameFormat](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamframeformat) [VideoProcessorSetStreamFrameFormat](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamframeformat) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Format](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [VideoProcessorGetStreamLumaKey](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamlumakey) [VideoProcessorSetStreamLumaKey](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamlumakey) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. LumaKey](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [VideoProcessorGetStreamOutputRate](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamoutputrate) [VideoProcessorSetStreamOutputRate](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamoutputrate) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. FrameRate](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [VideoProcessorGetStreamPalette](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreampalette) [VideoProcessorSetStreamPalette](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreampalette) | Nicht implementiert |
| [VideoProcessorGetStreamPixelAspectRatio](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreampixelaspectratio) [VideoProcessorSetStreamPixelAspectRatio](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreampixelaspectratio) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Verwandeln](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |
| [VideoProcessorGetStreamRotation](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamrotation) [VideoProcessorSetStreamRotation](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamrotation) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Verwandeln](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |
| [VideoProcessorGetStreamSourceRect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamsourcerect) [VideoProcessorSetStreamSourceRect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamsourcerect) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Verwandeln](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |
| [VideoProcessorGetStreamStereoFormat](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamstereoformat) [VideoProcessorSetStreamStereoFormat](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamstereoformat) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Verwandeln](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |

## <a name="id3d11videocontext1"></a>ID3D11VideoContext1

Bietet erweiterte Videofunktionen eines Direct3D 11-Geräts, einschließlich Hardware-DRM, Verbesserungen der Oberflächennutzung und mehr Videoverarbeitungsfunktionen. Diese Funktionalität wird für Direct3D 12 über neue Schnittstellen implementiert.


| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| CheckCryptoSessionStatus | TBD | 
| [DecoderEnableDownsampling](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) | [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments) |
| [DecoderUpdateDownsampling](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-decoderenabledownsampling) | [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments) |
| [GetDataForNewHardwareKey](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-getdatafornewhardwarekey) | TBD |
| [SubmitDecoderBuffers1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-submitdecoderbuffers1) | [ID3D12VideoDecodeCommandList::D ecodeFrame](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe) |
| [VideoProcessorGetBehaviorHints](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetbehaviorhints) | TBD |
| [VideoProcessorGetOutputColorSpace1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetoutputcolorspace1) [VideoProcessorSetOutputColorSpace1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetoutputcolorspace1) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. Farbraum](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [VideoProcessorGetOutputShaderUsage](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetoutputshaderusage) [VideoProcessorSetOutputShaderUsage](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetoutputshaderusage) | TBD |
| [VideoProcessorGetStreamColorSpace1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetstreamcolorspace1) [VideoProcessorSetStreamColorSpace1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetstreamcolorspace1) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC. Farbraum](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [VideoProcessorGetStreamMirror](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetstreammirror) [VideoProcessorSetStreamMirror](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetstreammirror) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Verwandeln](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |

## <a name="id3d11videodecoder"></a>ID3D11VideoDecoder

Stellt einen hardwarebeschleunigten Videodecoder für Direct3D 11 dar. Dies ist eine Wrapperschnittstelle um [ID3D11VideoContext,](/windows/win32/api/d3d11/nn-d3d11-id3d11videocontext) die die eigentliche Decodierungsfunktion verfügbar macht. Es gibt keine entsprechende API für Direct3D 12-Videos.


## <a name="id3d11videodecoderoutputview"></a>ID3D11VideoDecoderOutputView

Identifiziert die Ausgabeoberflächen, auf die während der Videodecodierung zugegriffen werden kann. In Direct3D 12 verwendet die [ID3D12VideoProcessor-Schnittstelle](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoprocessor) [ID3D12Resource-Objekte](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) direkt.

## <a name="id3d11videodevice"></a>ID3D11VideoDevice

Stellt die Videodecodierungs- und Videoverarbeitungsfunktionen eines Direct3D 11-Geräts bereit. Dies ist der Haupteinstiegspunkt zum Erstellen des Videodecodergeräts und der Krypto-Sitzung sowie für die Videoverarbeitung, Funktionen, Profile usw. Diese Funktionalität ist teilweise für Direct3D 12 implementiert.


| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [CheckCryptoKeyExchange](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-checkcryptokeyexchange) | Nicht implementiert. |
| [CheckVideoDecoderFormat](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-checkvideodecoderformat) | [D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_formats) |
| [CreateAuthenticatedChannel](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel) | Nicht implementiert. |
| [CreateCryptoSession](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) | Nicht implementiert. |
| [CreateVideoDecoder](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) | [ID3D12VideoDevice::CreateVideoDecoder](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoder)  [ID3D12VideoDevice::CreateVideoDecoderHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoderheap) |
| [CreateVideoDecoderOutputView](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview) | [ID3D12Texture2D](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) |
| [CreateVideoProcessor](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor) | [ID3D12VideoDevice::CreateVideoProcessor](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideoprocessor)  |
| [CreateVideoProcessorEnumerator](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessorenumerator) | Nicht zutreffend |
| [CreateVideoProcessorInputView](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessorinputview) | [ID3D12Texture2D](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) |
| [CreateVideoProcessorOutputView](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessoroutputview) | [ID3D12Texture2D](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) |
| [GetContentProtectionCaps](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getcontentprotectioncaps) | TBD
| [GetVideoDecoderConfig](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfig) | In Direct3D 12 wird nur der VLD-Modus unterstützt. [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles) [D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_formats) |
| [GetVideoDecoderConfigCount](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfigcount) | Nicht zutreffend |
| [GetVideoDecoderProfile](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile) | [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles) |
| [GetVideoDecoderProfileCount](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofilecount) | [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES. ProfileCount](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles) |
| [SetPrivateData](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-setprivatedata) | [ID3D12Object::SetPrivateData](/windows/win32/api/d3d12/nf-d3d12-id3d12object-setprivatedata) |
| [SetPrivateDataInterface](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-setprivatedatainterface) | [ID3D12Object::SetPrivateDataInterface](/windows/win32/api/d3d12/nf-d3d12-id3d12object-setprivatedatainterface) |

## <a name="id3d11videodevice1"></a>ID3D11VideoDevice1

Bietet erweiterte Videodecodierungs- und Videoverarbeitungsfunktionen eines Direct3D 11-Geräts, einschließlich mehr Erweiterungen, Hardware-DRM, Decodierungs-Downsampling, Videodecoderfunktionen usw. Diese Funktionalität wird für Direct3D 12 implementiert.

| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [CheckVideoDecoderDownsampling](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-checkvideodecoderdownsampling) | [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support) |
| [GetCryptoSessionPrivateDataSize](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-getcryptosessionprivatedatasize) | TBD |
| [GetVideoDecoderCaps](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-getvideodecodercaps) | [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support) |
| [RecommendVideoDecoderDownsampleParameters](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-recommendvideodecoderdownsampleparameters) | [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support) |


## <a name="id3d11videoprocessor"></a>ID3D11VideoProcessor

Stellt einen Videoprozessor für Direct3D 11 dar. Diese Funktion wird für Direct3D 12 im [ID3D12VideoProcessor implementiert.](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoprocessor)

| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [GetContentDesc](/windows/win32/api/d3d11/nf-d3d11-id3d11videoprocessor-getcontentdesc)| Nicht implementiert |
| [GetRateConversionCaps](/windows/win32/api/d3d11/nf-d3d11-id3d11videoprocessor-getrateconversioncaps) | Nicht implementiert |


## <a name="id3d11videoprocessorenumerator-and-id3d11videoprocessorenumerator1"></a>ID3D11VideoProcessorEnumerator und ID3D11VideoProcessorEnumerator1

Enumeriert die Videoprozessorfunktionen eines Direct3D 11-Geräts.
In Direct3D 12 wird die Enumerationsfunktion durch [ID3D12VideoDevice::CheckFeatureSupport ersetzt.](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) 

##  <a name="id3d11videoprocessorinputview"></a>ID3D11VideoProcessorInputView

Identifiziert die Eingabeoberflächen, auf die während der Videoverarbeitung zugegriffen werden kann.
In Direct3D 12 wird dies durch ID3D12Texture2D ersetzt.

##  <a name="id3d11videoprocessoroutputview"></a>ID3D11VideoProcessorOutputView

Identifiziert die Ausgabeoberflächen, auf die während der Videoverarbeitung zugegriffen werden kann.
In Direct3D 12 wird dies durch ID3D12Texture2D ersetzt.

## <a name="id3d11authenticatedchannel"></a>ID3D11AuthenticatedChannel

Stellt einen sicheren Kommunikationskanal mit dem Grafiktreiber oder der Microsoft Direct3D-Runtime zur Verfügung. Diese Funktionalität ist für Direct3D 12-Videos nicht implementiert.

##  <a name="id3d11cryptosession"></a>ID3D11CryptoSession

Stellt eine kryptografische Sitzung dar. Wird für DRM-Szenarien mit Software und Hardware verwendet. Es gibt keine entsprechende öffentliche API für Direct3D 12-Videos.

## <a name="related-topics"></a>Zugehörige Themen

[Direct3D 12-Video-APIs](direct3d-12-video-apis.md)


 

 




