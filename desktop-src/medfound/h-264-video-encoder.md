---
description: 'Der Microsoft Media Foundation H.264-Videoencoder ist eine Media Foundation-Transformation, die die folgenden H.264-Profile unterstützt:'
ms.assetid: 4d4c768f-b76a-40ca-8736-2f592a4f4cc4
title: H.264 Video Encoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 875974c53be265fbcace8cf99e2bdd78d69cdda5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467527"
---
# <a name="h264-video-encoder"></a>H.264 Video Encoder

Der Microsoft Media Foundation H.264-Videoencoder ist eine [Media Foundation-Transformation,](media-foundation-transforms.md) die die folgenden H.264-Profile unterstützt:

-   Baselineprofil
-   Profil: Main
-   Hohes Profil (erfordert Windows 8)

Der H.264-Videoencoder macht die folgenden Schnittstellen verfügbar:

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**ÜBERTRANSFORM**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a>Eingabetypen

Der Eingabemedientyp muss einen der folgenden Untertypen aufweisen:

-   **MFVideoFormat_I420**
-   **MFVideoFormat_IYUV**
-   **MFVideoFormat_NV12**
-   **MFVideoFormat_YUY2**
-   **MFVideoFormat_YV12**

Weitere Informationen zu diesen Untertypen finden Sie unter [Video-Untertyp-GUIDs.](video-subtype-guids.md)

Der Ausgabetyp muss vor dem Eingabetyp festgelegt werden. Bis der Ausgabetyp festgelegt ist, gibt die [**ENCODER-Methode "ENCODERTransform::SetInputType"**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) **MF_E_TRANSFORM_TYPE_NOT_SET** zurück.

## <a name="output-types"></a>Ausgabetypen

Der Encoder unterstützt einen einzelnen Ausgabeuntertyp:

-   **MFVideoFormat_H264**

Legen Sie die folgenden Attribute für den Ausgabemedientyp fest.




| Attribut | BESCHREIBUNG | 
|-----------|-------------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Haupttyp. Muss <strong>MFMediaType_Video</strong>sein. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Videountertyp. Muss <strong>MFVideoFormat_H264</strong>sein. | 
| <a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a> | Durchschnittliche codierte Bitrate in Bits pro Sekunde. Muss größer sein als Null. | 
| <a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a> | Bildrate. | 
| <a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a> | Framegröße. | 
| <a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a> | Interlace-Modus. | 
| <a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a> | H.264-Codierungsprofil.<br /> Die unterstützten Werte sind:<br /><ul><li><strong>eAVEncH264VProfile_Base</strong> (Standard)</li><li><strong>eAVEncH264VProfile_Main</strong></li><li><strong>eAVEncH264VProfile_High</strong> (erfordert Windows 8)</li></ul> | 
| <a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a> | Optional. Gibt die H.264-Codierungsebene an.<br /> Der Standardwert ist –1 und gibt an, dass der Encoder die Codierungsebene auswählt.<br /> Es wird empfohlen, die Ebene im Medientyp nicht festzulegen und dem Encoder das Auswählen der Ebene zu erlauben. Der Encoder kann die richtige Ebene für einen bestimmten Videostream ableiten, wobei die Formateinschränkungen und die Merkmale des Videos berücksichtigt werden. Weitere Informationen zu Profil- und Ebeneneinschränkungen finden Sie in Anhang A von ITU-T H.264.<br /> | 
| <a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a> | Optional. Gibt das Pixelseitenverhältnis an. Der Standardwert ist 1:1. | 




 

Nachdem der Ausgabetyp festgelegt wurde, aktualisiert der Videoencoder den Typ, indem er das [**attribut MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) hinzufügt. Dieses Attribut enthält den Sequenzheader.

## <a name="codec-properties"></a>Codeceigenschaften

Der H.264-Encoder implementiert die [**ICodecAPI-Schnittstelle**](/windows/win32/api/strmif/nn-strmif-icodecapi) zum Festlegen von Codierungsparametern. Sie unterstützt die folgenden Eigenschaften.

Die Codecanforderungen für die HCK-Encoderzertifizierung finden Sie weiter unten im Abschnitt **Zertifizierter Hardwareencoder.**

Die folgenden Eigenschaften werden in Windows 7 unterstützt.



| Eigenschaft                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CODECAPI_AVEncCommonRateControlMode**](../directshow/avenccommonratecontrolmode-property.md) | Legt den Ratensteuerungsmodus fest. Siehe Hinweise. Der Standardmodus ist eine nicht eingeschränkte variable Bitrate (VBR).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**CODECAPI_AVEncCommonQuality**](../directshow/avenccommonquality-property.md)                 | Legt die Qualitätsstufe fest. Diese Eigenschaft gilt, wenn der Ratensteuerungsmodus qualitätsbasierte VBR **(eAVEncCommonRateControlMode_Quality**) ist. Der gültige Bereich ist 1 bis 100. Der Standardwert ist 70. <br/> Um diesen Parameter festzulegen, legen Sie die -Eigenschaft fest, bevor Sie [**ÜBERTRANSFORM::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)aufrufen. <br/> Um diesen Parameter in Windows 7 festzulegen, legen Sie die -Eigenschaft fest, bevor Sie [**DENTRANSFORM::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)aufrufen. Der Encoder ignoriert Änderungen, nachdem der Ausgabetyp festgelegt wurde. <br/> In Windows 8 kann diese Eigenschaft jederzeit während der Codierung festgelegt werden. Änderungen werden ab dem nächsten Eingaberahmen angewendet. <br/> Intern konvertiert der Encoder diese Eigenschaft in einen [AVEncVideoEncodeQP-Wert.](codecapi-avencvideoencodeqp.md) <br/> |



 

Die folgenden Eigenschaften erfordern Windows 8.




| Eigenschaft | BESCHREIBUNG | 
|----------|-------------|
| <a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a> | Legt den adaptiven Codierungsmodus fest. Der H.264-Encoder unterstützt die folgenden Modi in Windows 8:<ul><li><strong>eAVEncAdaptiveMode_None</strong>. Keine adaptive Codierung. (Standardeinstellung)</li><li><strong>eAVEncAdaptiveMode_FrameRate</strong>. Ändern Sie die Bildfrequenz adaptive.</li></ul><br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a> | Legt die Puffergröße für die CBR-Codierung (Constant Bit Rate) in Bytes fest.<br /> Der gültige Bereich ist [1 ... 2präsent–1]. <br /> Erfordert Windows 8. <br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a> | Gibt für die eingeschränkte VBR-Codierung die Rate an, mit der der "leaky bucket" in Bits pro Sekunde entladen wird. Diese Eigenschaft wird angewendet, wenn der Ratensteuerungsmodus <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>ist. <br /> Der gültige Bereich ist [1 ... 2präsent–1]. <br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> | Legt die durchschnittliche Bitrate für den codierten Bitstream in Bits pro Sekunde fest. Diese Eigenschaft wird ignoriert, wenn der Ratensteuerungsmodus <strong>eAVEncCommonRateControlMode_Quality</strong>ist. <br /> Der gültige Bereich ist [1 ... 2präsent–1]. <br /> In CBR- und uneingeschränkten VBR-Modi bestimmt die durchschnittliche Bitrate die endgültige Größe der Datei. Im CBR-Modus ist die durchschnittliche Bitrate auch die Rate, mit der komprimierte Bits aus dem "leaky bucket" entladen werden. (Weitere Informationen finden Sie unter <a href="the-leaky-bucket-buffer-model.md">The Leaky Bucket Buffer Model</a>.) <br /> In Windows 7 wird die durchschnittliche Bitrate vom <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE-Attribut</a> für den Medientyp angegeben. <br /> In Windows 8 können Sie die durchschnittliche Bitrate entweder mit dem <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE-Attribut</a> oder der <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate-Eigenschaft</a> festlegen. Wenn beide festgelegt sind, CODECAPI_AVEncCommonMeanBitRate Außerkraftsetzungen. In Windows 8 können Sie die durchschnittliche Bitrate während der Codierung festlegen. Wenn sich die Bitrate ändert, verwendet der Encoder adaptive Codierung.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a> | Legt den Qualitäts-/Geschwindigkeits-Kompromiss fest. Gültiger Bereich:<ul><li>0–33: Geringe Komplexität</li><li>34–66: Mittlere Komplexität (Standard)</li><li>67–100: Hohe Komplexität</li></ul><br /> Dieser Wert wirkt sich darauf aus, wie der Encoder verschiedene Codierungsvorgänge ausführt, z. B. die Bewegungskompensierung. Bei höheren Komplexitätsgraden wird der Encoder langsamer ausgeführt, erzeugt aber eine bessere Qualität mit der gleichen Bitrate.<br /> | 
| <a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a> | Aktiviert oder deaktiviert CABAC (kontext adaptive binäre arithmetische Codierung) für die H.264-Entropiecodierung. Der Standardwert ist <strong>VARIANT_FALSE</strong>. <br /> CABAC wird nicht für Baselineprofile verwendet.<br /> | 
| <a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a> | Legt den Wert von <strong>seq_parameter_set_id</strong> in der SPS-NAL-Einheit des H.264-Bitstreams fest. <br /> | 
| <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a> | Legt die maximale Anzahl aufeinanderfolgender B-Frames im Ausgabebitstream fest. Gültige Werte sind:<ul><li>0: Verwenden Sie keine B-Frames (Standard).</li><li>1: Verwenden Sie einen B-Frame.</li><li>2: Verwenden Sie zwei B-Frames.</li></ul>Um diesen Parameter festzulegen, legen Sie die -Eigenschaft fest, bevor Sie <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>ÜBERTRANSFORM::SetOutputType</strong></a>aufrufen. <br /> Für Baselineprofil ist die Anzahl von B-Frames immer 0 (null). Der Encoder überschreibt Werte ungleich 0 (null).<br /> Wenn diese Eigenschaft für andere H.264-Profile ungleich 0 (null) ist, lautet das Codierungsmuster IBBPBBP, wobei die maximale Anzahl aufeinanderfolgender B-Frames <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">gleich CODECAPI_AVEncMPVDefaultBPictureCount</a>ist. <br /> | 
| <a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a> | Legt die Anzahl der Bilder von einem GOP-Header auf den nächsten fest, einschließlich des führenden Ankers, aber nicht des folgenden. <br /> Der gültige Bereich ist [0 ... 2 quadratisch–1]. Bei 0 (null) wählt der Encoder die GOP-Größe aus. Der Standardwert ist 0 (null). <br /> | 
| <a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a> | Legt die Anzahl von Arbeitsthreads fest, die von einem Encoder verwendet werden.<br /> Der gültige Bereich ist 0 bis 16. Bei 0 (null) wählt der Encoder die Anzahl der Threads aus. <br /> | 
| <a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a> | Gibt den Typ des Videoinhalts an.<br /> | 
| <a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a> | Gültiger Bereich: 16–51. Der Standardwert ist 24. <br /> Diese Eigenschaft wird angewendet, wenn der Ratensteuerungsmodus <strong>eAVEncCommonRateControlMode_Quality</strong>ist. <br /> Diese Eigenschaft konfiguriert die gleiche Codierungseinstellung wie <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality.</strong></a> <a href="codecapi-avencvideoencodeqp.md">AvEncVideoEncodeQP</a> ermöglicht der Anwendung jedoch, den Wert von QP direkt anzugeben. Wenn beide Eigenschaften festgelegt sind, überschreibt AVEncVideoEncodeQP. <br /> Der Standardwert 24 entspricht dem Standardwert 70 für die <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>EINSTELLUNG AVEncCommonQuality.</strong></a><br /> | 
| <a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a> | Erzwingt, dass der Encoder den nächsten Frame als Keyframe codt.<br /> | 
| <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> | Gültiger Bereich: 0 bis 51. Der Standardwert ist 0. <br /> Diese Eigenschaft gilt für alle Ratensteuerungsmodi. Der Encoder sollte keinen QP-Wert erzeugen, der niedriger ist als der von der <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP-Eigenschaft</a> angegebene Wert.<br /> | 
| <a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a> | Aktiviert oder deaktiviert den Modus mit niedriger Latenz. Siehe "Multithreading" im Abschnitt "Hinweise".<br /> | 




 

## <a name="remarks"></a>Hinweise

Der Encoder unterstützt die folgenden Ratensteuerungsmodi.



| Modus                                  | Konstante                                            | BESCHREIBUNG                                                                                                                                                                                                                                         |
|---------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Konstante Bitrate (CBR)               | **eAVEncCommonRateControlMode_CBR**                | Der Encoder versucht, eine konstante Bitrate zu erreichen, indem er ein "leaky bucket"-Modell verwendet. Die Zielbitrate wird von der [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) -Eigenschaft angegeben. <br/> Erfordert Windows 8. <br/> |
| Eingeschränkte variable Bitrate (VBR)   | **eAVEncCommonRateControlMode_PeakConstrainedVBR** | Der Encoder verwendet ein "leaky bucket"-Modell mit einer Spitzenbitrate. Die Entleerungsrate für den Bucket "Leaky" wird durch die [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) -Eigenschaft angegeben. <br/> Erfordert Windows 8. <br/>     |
| Qualitätsbasierte variable Bitrate (VBR) | **eAVEncCommonRateControlMode_Quality**            | Der Encoder versucht, eine konstante Qualitätsstufe zu erreichen, die von der [**AVEncCommonQuality-Eigenschaft**](../directshow/avenccommonquality-property.md) angegeben wird.                                                                                                           |
| Nicht eingeschränkte VBR                     | **eAVEncCommonRateControlMode_UnconstrainedVBR**   | Der Encoder versucht, die vom [**MF_MT_AVG_BITRATE-Attribut**](mf-mt-avg-bitrate-attribute.md) im Ausgabemedientyp angegebene Zielbitrate zu erreichen. Dies ist der Standardmodus.                                                              |



 

CBR- und eingeschränkte VBR-Modi erfordern Windows 8.

In Windows 8 legt der Encoder die folgenden Attribute für die Ausgabebeispiele fest:

-   [MFSampleExtension_DecodeTimestamp](mfsampleextension-decodetimestamp.md)
-   [MFSampleExtension_VideoEncodePictureType](mfsampleextension-videoencodepicturetype.md)
-   [MFSampleExtension_VideoEncodeQP](mfsampleextension-videoencodeqp.md)

> [!Note]  
> In einer früheren Version der Dokumentation wurde fälschlicherweise angegeben, dass der Encoder auf Windows Server 2008 R2 unterstützt wird.

 

### <a name="multithreading"></a>Multithreading

In Windows 8 unterstützt der Encoder zwei Codierungsmodi:

-   **Slicecodierung.** In diesem Modus werden Slices parallel codiert. Jeder Slice wird in einem anderen Thread codiert. Dieser Modus weist eine geringe Latenz auf, da ein einzelnes Bild parallel codiert wird. Dieser Ansatz wird jedoch nicht skaliert, wenn die Anzahl der Kerne zunimmt, da die Anzahl der Slices durch die Anzahl der Makroblockzeilen im Eingabebild begrenzt wird.
-   **Multiframecodierung.** In diesem Modus akzeptiert der Encoder mehrere Eingabeframes und codiert sie parallel. Dieser Modus wird in einer Umgebung mit mehreren Kernen besser skaliert, führt jedoch zu einer größeren Latenz.

Der Encoder verwendet standardmäßig Slicecodierung, um die Latenz zu minimieren. Um die Multiframecodierung zu aktivieren, legen Sie die [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) -Eigenschaft auf **VARIANT_FALSE** fest.

Um die Anzahl der vom Encoder verwendeten Arbeitsthreads festzulegen, legen Sie die [eigenschaft CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) fest.

In Windows 7 verwendet der Encoder immer Slicecodierung.

### <a name="certified-hardware-encoder"></a>Zertifizierter Hardwareencoder

Wenn ein zertifizierter Hardwareencoder vorhanden ist, wird er in der Regel anstelle des Inbox-Systemencoders für Media Foundation zugehörigen Szenarien verwendet. Zertifizierte Encoder sind erforderlich, um einen bestimmten Satz von **ICodecAPI-Eigenschaften** zu unterstützen, und können optional einen anderen Satz von Eigenschaften unterstützen. Der Zertifizierungsprozess sollte sicherstellen, dass die erforderlichen Eigenschaften ordnungsgemäß unterstützt werden. Wenn eine optionale Eigenschaft unterstützt wird, sollten sie auch ordnungsgemäß unterstützt werden.

Im Folgenden werden die erforderlichen und optionalen **ICodecAPI-Eigenschaften** für Encoder aufgeführt, um die HCK-Encoderzertifizierung zu bestehen.

Die folgenden Windows 8 und Windows 8.1 **ICodecAPI-Eigenschaften** sind erforderlich:

-   [CODECAPI_AVEncCommonRateControlMode](../directshow/avenccommonratecontrolmode-property.md)
-   [CODECAPI_AVEncCommonQuality](../directshow/avenccommonquality-property.md)
-   [CODECAPI_AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md)
-   [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)
-   [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md)
-   [CODECAPI_AVEncCommonBufferSize](../directshow/avenccommonbuffersize-property.md)
-   [CODECAPI_AVEncMPVGOPSize](../directshow/avencmpvgopsize-property.md)
-   [CODECAPI_AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md)
-   [CODECAPI_AVEncVideoForceKeyFrame](codecapi-avencvideoforcekeyframe.md)

Die folgenden Windows 8.1 **ICodecAPI-Eigenschaften** sind optional, werden jedoch in HCK getestet, sofern unterstützt.

-   [CODECAPI_AVEncVideoMinQP](codecapi-avencvideominqp.md)
-   [CODECAPI_AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md)
-   [CODECAPI_AVEncVideoMarkLTRFrame](codecapi-avencvideomarkltrframe.md)
-   [CODECAPI_AVEncVideoUseLTRFrame](codecapi-avencvideouseltrframe.md)
-   [CODECAPI_AVEncVideoEncodeFrameTypeQP](codecapi-avencvideoencodeframetypeqp.md)
-   [CODECAPI_AVEncSliceControlMode](codecapi-avencslicecontrolmode.md)
-   [CODECAPI_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md)
-   [CODECAPI_AVEncVideoMaxNumRefFrame](codecapi-avencvideomaxnumrefframe.md)
-   [CODECAPI_AVEncVideoMeanAbsoluteDifference](codecapi-avencvideomeanabsolutedifference.md)
-   [CODECAPI_AVEncVideoMaxQP](codecapi-avencvideomaxqp.md)
-   [CODECAPI_AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md)
-   [CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (dynamisch)
-   [CODECAPI_AVEncH264CABACEnable](codecapi-avench264cabacenable.md)

Die folgenden Windows 8 und Windows 8.1 **ICodecAPI-Eigenschaften** sind optional, werden jedoch in HCK getestet, sofern unterstützt.

-   [CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (statisch)
-   [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md)

Die folgenden **ICodecAPI-Eigenschaften** sind optional. Sie werden in HCK nicht getestet.

-   [CODECAPI_AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                |
| DLL<br/>                      | <dl> <dt>Mfh264enc.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[MPEG-4-Unterstützung in Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Unterstützte Medienformate in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Videomedientypen](video-media-types.md)
</dt> </dl>

 

 
