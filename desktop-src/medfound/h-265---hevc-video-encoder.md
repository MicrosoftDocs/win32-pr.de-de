---
description: Der Media Foundation H.265-Videoencoder ist eine Media Foundation Transform, die die Codierung von Inhalten im H.265/HEVC-Format unterstützt.
ms.assetid: 790CFB39-6FC0-432D-A434-5262C30EABF4
title: H.265/HEVC Video Encoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b95eee96d3313df2604919883cf631b0aef999f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467487"
---
# <a name="h265--hevc-video-encoder"></a>H.265/HEVC Video Encoder

Der Media Foundation H.265-Videoencoder ist eine [Media Foundation Transform,](media-foundation-transforms.md) die die Codierung von Inhalten im H.265/HEVC-Format unterstützt. Der Encoder unterstützt die folgenden Profile:

-   Profil: Main

Der H.265-Videoencoder macht die folgenden Schnittstellen verfügbar:

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**ERWEITERETransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a>Eingabetypen

Der Eingabemedientyp muss einen der folgenden Untertypen aufweisen:

-   **MFVideoFormat \_ IYUV**
-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ YUY2**
-   **MFVideoFormat \_ YV12**

Weitere Informationen zu diesen Untertypen finden Sie unter [Video-Untertyp-GUIDs.](video-subtype-guids.md)

Der Ausgabetyp muss vor dem Eingabetyp festgelegt werden. Bis der Ausgabetyp festgelegt ist, gibt die [**ENCODERTRANSFORM::SetInputType-Methode**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) **MF E TRANSFORM TYPE NOT \_ \_ \_ \_ \_ SET** zurück.

## <a name="output-types"></a>Ausgabetypen

Der Encoder unterstützt einen einzelnen Ausgabeuntertyp:

-   **MFVideoFormat \_ H265**

Legen Sie die folgenden Attribute für den Ausgabemedientyp fest.




| Attribut | BESCHREIBUNG | 
|-----------|-------------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Haupttyp. Muss <strong>MFMediaType_Video</strong>sein. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Videountertyp. Muss <strong>MFVideoFormat_HEVC</strong>sein. | 
| <a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a> | Durchschnittliche codierte Bitrate in Bits pro Sekunde. Muss größer sein als Null. | 
| <a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a> | Bildrate. | 
| <a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a> | Framegröße. | 
| <a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a> | Interlace-Modus. | 
| <a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a> | H.265-Codierungsprofil.<br /> Die unterstützten Werte sind: <br /><ul><li><strong>eAVEncH265VProfile_Main_420_8</strong></li></ul> | 
| <a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a> | Gibt die Ebene des codierten Videos an. Weitere Informationen zu Profil- und Ebeneneinschränkungen finden Sie in Anhang A von ITU-T H.265.<br /> | 
| <a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a> | Optional. Gibt das Pixel-Seitenverhältnis an. Der Standardwert ist 1:1. | 




 

Nachdem der Ausgabetyp festgelegt wurde, aktualisiert der Videoencoder den Typ durch Hinzufügen des [**MF MT MPEG SEQUENCE \_ \_ \_ HEADER-Attributs. \_**](mf-mt-mpeg-sequence-header-attribute.md) Dieses Attribut enthält den Sequenzheader.

## <a name="supported-imftransform-methods"></a>Unterstützte SUPPORTEDTRANSFORM-Methoden

Die folgenden Methoden der [**INTERFACESTransform-Schnittstelle**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) werden für den H.265/HEVC-Encoder unterstützt:

-   [**Getattributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)
-   [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)
-   [**GetInputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)
-   [**GetInputStatus**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstatus)
-   [**GetInputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)
-   [**GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)
-   [**GetOutputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)
-   [**GetOutputStatus**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus)
-   [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)
-   [**GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount)
-   [**GetStreamLimits**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits)
-   [**ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
-   [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)
-   [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)
-   [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
-   [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)
-   [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
-   [**SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds)

Alle anderen [**METHODEN VOM FORMATTRANSFORM**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) geben den Fehler E \_ NOTIMPL zurück.

## <a name="supported-icodecapi-methods"></a>Unterstützte ICodecAPI-Methoden

Die folgenden Methoden der [**ICodecAPI-Schnittstelle**](/windows/win32/api/strmif/nn-strmif-icodecapi) werden für den H.265/HEVC-Encoder unterstützt:

-   [**Issupported**](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)
-   [**GetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [**GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [**GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)

Alle anderen [**ICodecAPI-Methoden**](/windows/win32/api/strmif/nn-strmif-icodecapi) geben den Fehler E \_ NOTIMPL zurück.

## <a name="codec-properties"></a>Codeceigenschaften

Der H.265-Encoder implementiert die [**ICodecAPI-Schnittstelle**](/windows/win32/api/strmif/nn-strmif-icodecapi) zum Festlegen von Codierungsparametern. Sie unterstützt die folgenden Eigenschaften.

Die Codecanforderungen für die HCK-Encoderzertifizierung finden Sie weiter unten im Abschnitt **Zertifizierter Hardwareencoder.**




| Eigenschaft | BESCHREIBUNG | 
|----------|-------------|
| <a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a> | Legt den Ratensteuerungsmodus fest. Unterstützte Modi:<br /><ul><li><strong>eAVEncCommonRateControlMode_CBR</strong></li><li><strong>eAVEncCommonRateControlMode_Quality</strong></li></ul>Wenn andere Modi angegeben werden, wird die <strong>eAVEncCommonRateControlMode_CBR</strong> Ratensteuerung verwendet.<br /> Dies ist ein VT_UI4 Wert.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> | Legt die durchschnittliche Bitrate für den codierten Bitstream in Bits pro Sekunde fest. <br /> Der gültige Bereich ist [1 ... 2 quadratisch–1]. <br /> Dies ist ein VT_UI4 Wert.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a> | Legt die Puffergröße für die CBR-Codierung (Constant Bit Rate) in Bytes fest.<br /> Der gültige Bereich ist [1 ... 2präsent–1]. <br /> Dies ist ein VT_UI4 Wert.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a> | Legt die maximale Bitrate für Ratensteuerungsmodi fest, die eine Spitzenbitrate zulassen. <br /> Der gültige Bereich ist [1 ... 2präsent–1]. <br /> Dies ist ein VT_UI4 Wert.<br /> | 
| <a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a> | Legt die Anzahl der Bilder von einem GOP-Header auf den nächsten fest, einschließlich des führenden Ankers, aber nicht des folgenden. <br /> Der gültige Bereich ist [0 ... 2 quadratisch–1]. Bei 0 (null) wählt der Encoder die GOP-Größe aus. Der Standardwert ist 0 (null). <br /> Dies ist ein VT_UI4 Wert.<br /> | 
| <a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a> | Aktiviert oder deaktiviert den Modus mit niedriger Latenz. <br /> Dies ist ein VT_BOOL Wert.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a> | Legt den Qualitäts-/Geschwindigkeits-Kompromiss fest. Dieser Wert wirkt sich darauf aus, wie der Encoder verschiedene Codierungsvorgänge ausführt, z. B. die Bewegungskompensierung. Bei höheren Komplexitätsgraden wird der Encoder langsamer ausgeführt, erzeugt aber eine bessere Qualität mit der gleichen Bitrate. <br /> Der gültige Bereich ist 0 bis 100. Intern wird dieser Wert einem kleineren Satz von Qualitäts-/Geschwindigkeitsstufen zugeordnet, die vom Encoder unterstützt werden.<br /> Dies ist ein VT_UI4 Wert.<br /> | 
| <a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a> | Erzwingt, dass der Encoder den nächsten Frame als Keyframe codt.<br /> Dies ist ein VT_UI4 Wert.<br /> | 
| <a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a> | Wenn diese Eigenschaft festgelegt ist, bewirkt dies, dass der Encoder den angegebenen QP verwendet, um den nächsten Frame und alle nachfolgenden Frames zu codieren, bis ein neuer QP angegeben wird. <br /> Gültiger Bereich: 0–51, einschließlich <br /> | 
| <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> | Diese Eigenschaft legt einen Grenzwert für die minimale QP fest, die der Encoder während cbr ratecontrol verwenden kann.<br /> Dies ist ein VT_UI4 Wert.<br /> | 
| <a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a> | Diese Eigenschaft legt einen Grenzwert für die maximale QP fest, die der Encoder während cbr ratecontrol verwenden kann.<br /> Dies ist ein VT_UI4 Wert.<br /> | 
| <a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a> | Legt fest, ob es sich bei den Inhalten um Vollbildvideos handelt, im Gegensatz zu Bildschirminhalten, die möglicherweise ein kleineres Videofenster oder gar kein Video enthalten.<br /> Dies ist ein VT_UI4 Wert.<br /> | 
| <a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a> | Legt die Anzahl der Threads fest, die zum Ausführen des Komprimierungsvorgangs verwendet werden. Der Encoder teilt den Rahmen in Kacheln auf, sodass die Anzahl der Threads der Anzahl der Kacheln entspricht.<br /><ul><li>Die Anzahl der logischen Prozessoren. Die Anzahl der Threads muss kleiner oder gleich der Anzahl logischer Prozessoren sein.</li><li>Die Größe des Rahmens. Die Größe einer Kachel muss größer oder gleich 265 x 64 Pixel sein.</li><li>Parität: Die Anzahl der Threads muss ein gerader Wert sein. Wenn der angegebene Wert ungerade ist, wird der nächstuntere gerade Wert verwendet.</li></ul>Dies ist ein VT_UI4 Wert.<br /> | 




 

## <a name="certified-hardware-encoder"></a>Zertifizierter Hardwareencoder

Wenn ein zertifizierter Hardwareencoder vorhanden ist, wird er in der Regel anstelle des Inbox-Systemencoders für Media Foundation zugehörigen Szenarien verwendet. Zertifizierte Encoder sind erforderlich, um einen bestimmten Satz von **ICodecAPI-Eigenschaften** zu unterstützen, und können optional einen anderen Satz von Eigenschaften unterstützen. Der Zertifizierungsprozess sollte sicherstellen, dass die erforderlichen Eigenschaften ordnungsgemäß unterstützt werden. Wenn eine optionale Eigenschaft unterstützt wird, sollten sie auch ordnungsgemäß unterstützt werden.

Im Folgenden sind die erforderlichen und optionalen **ICodecAPI-Eigenschaften** für Encoder aufgeführt, um die HCK-Encoderzertifizierung zu bestehen.

-   [CODECAPI \_ AVEncCommonRateControlMode](../directshow/avenccommonratecontrolmode-property.md)
-   [CODECAPI \_ AVEncCommonQuality](../directshow/avenccommonquality-property.md)
-   [CODECAPI \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)
-   [CODECAPI \_ AVEncCommonBufferSize](../directshow/avenccommonbuffersize-property.md)
-   [CODECAPI \_ AVEncMPVGOPSize](../directshow/avencmpvgopsize-property.md)
-   [CODECAPI \_ AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md)
-   [CODECAPI \_ AVEncVideoForceKeyFrame](codecapi-avencvideoforcekeyframe.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                |
| DLL<br/>                      | <dl> <dt>Mfh265enc.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> </dl>

 

 
