---
description: 'Der Video Encoder Microsoft Media Foundation H. 264 ist eine Media Foundation Transformation, die die folgenden H. 264-Profile unterstützt:'
ms.assetid: 4d4c768f-b76a-40ca-8736-2f592a4f4cc4
title: H. 264-Video Encoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5631239e9db0ddf078848bc3c4a04282e7e79990
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348478"
---
# <a name="h264-video-encoder"></a>H. 264-Video Encoder

Der Video Encoder Microsoft Media Foundation H. 264 ist eine [Media Foundation Transformation](media-foundation-transforms.md) , die die folgenden H. 264-Profile unterstützt:

-   Basis Linien Profil
-   Profil: Main
-   Hohes Profil (erfordert Windows 8)

Der H. 264-Video Encoder macht die folgenden Schnittstellen verfügbar:

-   [**Icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMF-Transformation**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a>Eingabetypen

Der Eingabe Medientyp muss einen der folgenden Untertypen aufweisen:

-   **MFVideoFormat_I420**
-   **MFVideoFormat_IYUV**
-   **MFVideoFormat_NV12**
-   **MFVideoFormat_YUY2**
-   **MFVideoFormat_YV12**

Weitere Informationen zu diesen Untertypen finden Sie unter [Video Untertyp-GUIDs](video-subtype-guids.md).

Der Ausgabetyp muss vor dem Eingabetyp festgelegt werden. Bis der Ausgabetyp festgelegt ist, gibt die [**IMF Transform:: setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) -Methode des Encoders **MF_E_TRANSFORM_TYPE_NOT_SET** zurück.

## <a name="output-types"></a>Ausgabetypen

Der Encoder unterstützt einen einzelnen Ausgabe Untertyp:

-   **MFVideoFormat_H264**

Legen Sie die folgenden Attribute für den Ausgabe Medientyp fest.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></td>
<td>Der Haupttyp. Muss <strong>MFMediaType_Video</strong>werden.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></td>
<td>Video Untertyp. Muss <strong>MFVideoFormat_H264</strong>werden.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></td>
<td>Die durchschnittliche codierte Bitrate in Bits pro Sekunde. Muss größer sein als Null.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></td>
<td>Die Framerate.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></td>
<td>Frame Größe.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></td>
<td>Interlace-Modus.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a></td>
<td>H. 264-Codierungs Profil.<br/> Die unterstützten Werte sind:<br/>
<ul>
<li><strong>eAVEncH264VProfile_Base</strong> (Standard)</li>
<li><strong>eAVEncH264VProfile_Main</strong></li>
<li><strong>eAVEncH264VProfile_High</strong> (erfordert Windows 8)</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></td>
<td>Dies ist optional. Gibt die H. 264-Codierungs Ebene an.<br/> Der Standardwert ist – 1 und gibt an, dass der Encoder die Codierungs Ebene auswählt.<br/> Es wird empfohlen, die Ebene nicht im Medientyp festzulegen, und der Encoder kann die Ebene auswählen. Der Encoder kann die richtige Ebene für einen bestimmten Videostream ableiten, wobei die Format Einschränkungen und die Merkmale des Videos berücksichtigt werden. Weitere Informationen zu den Einschränkungen für Profile und Ebenen finden Sie in Anhang A von ITU-T H. 264.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></td>
<td>Dies ist optional. Gibt das Pixel Seitenverhältnis an. Der Standardwert ist 1:1.</td>
</tr>
</tbody>
</table>



 

Nachdem der Ausgabetyp festgelegt wurde, aktualisiert der Video Encoder den Typ durch Hinzufügen des [**MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) Attributs. Dieses Attribut enthält den Sequence-Header.

## <a name="codec-properties"></a>Codec-Eigenschaften

Der H. 264-Encoder implementiert die [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle zum Festlegen von Codierungs Parametern. Die folgenden Eigenschaften werden unterstützt:

Die Codec-Anforderungen für die HCK Encoder-Zertifizierung finden Sie weiter unten im Abschnitt **Certified Hardware Encoder** .

Die folgenden Eigenschaften werden in Windows 7 unterstützt.



| Eigenschaft                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CODECAPI_AVEncCommonRateControlMode**](../directshow/avenccommonratecontrolmode-property.md) | Legt den Raten Steuerungs Modus fest. Siehe Hinweise. Der Standardmodus ist die eingeschränkte variablenbitrate (VBR).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**CODECAPI_AVEncCommonQuality**](../directshow/avenccommonquality-property.md)                 | Legt die Qualitätsstufe fest. Diese Eigenschaft wird angewendet, wenn der Raten Steuerungs Modus Qualitäts basierte VBR (**eAVEncCommonRateControlMode_Quality**) ist. Der gültige Bereich ist 1 – 100. Der Standardwert ist 70. <br/> Um diesen Parameter festzulegen, legen Sie die-Eigenschaft vor dem Aufrufen von [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)fest. <br/> Wenn Sie diesen Parameter in Windows 7 festlegen möchten, legen Sie die-Eigenschaft vor dem Aufrufen von [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)fest. Der Encoder ignoriert Änderungen, nachdem der Ausgabetyp festgelegt wurde. <br/> In Windows 8 kann diese Eigenschaft während der Codierung jederzeit festgelegt werden. Änderungen werden ab dem nächsten Eingabe Rahmen angewendet. <br/> Intern konvertiert der Encoder diese Eigenschaft in einen [avencvideoencodeqp](codecapi-avencvideoencodeqp.md) -Wert. <br/> |



 

Die folgenden Eigenschaften erfordern Windows 8.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Eigenschaft</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a></td>
<td>Legt den adaptiven Codierungs Modus fest. Der H. 264-Encoder unterstützt die folgenden Modi in Windows 8:
<ul>
<li><strong>eAVEncAdaptiveMode_None</strong>. Keine adaptive Codierung. (Standardeinstellung)</li>
<li><strong>eAVEncAdaptiveMode_FrameRate</strong>. Ändern Sie die Framerate adaptiv.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></td>
<td>Legt die Puffergröße in Bytes für die Konstante Bitrate (CBR)-Codierung fest.<br/> Der gültige Bereich ist [1... 2 ³ ² – 1]. <br/> Erfordert Windows 8. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></td>
<td>Gibt bei eingeschränkter VBR-Codierung die Rate an, mit der der &quot; Leaky-Bucket &quot; in Bits pro Sekunde entladen wird. Diese Eigenschaft wird angewendet, wenn der Raten Steuerungs Modus <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>ist. <br/> Der gültige Bereich ist [1... 2 ³ ² – 1]. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></td>
<td>Legt die durchschnittliche Bitrate für den codierten Bitstream in Bits pro Sekunde fest. Diese Eigenschaft wird ignoriert, wenn der Raten Steuerungs Modus <strong>eAVEncCommonRateControlMode_Quality</strong>ist. <br/> Der gültige Bereich ist [1... 2 ³ ² – 1]. <br/> In CBR und uneingeschränkten VBR-Modi bestimmt die durchschnittliche Bitrate die endgültige Größe der Datei. Im CBR-Modus ist die durchschnittliche Bitrate auch die Rate, mit der komprimierte Bits aus dem &quot; Leaky-Bucket entladen werden. &quot; (Weitere Informationen finden Sie unter das unkomprimierte <a href="the-leaky-bucket-buffer-model.md">Bucket-Puffer Modell</a>.) <br/> In Windows 7 wird die durchschnittliche Bitrate durch das <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> -Attribut für den Medientyp angegeben. <br/> In Windows 8 können Sie die durchschnittliche Bitrate entweder mithilfe des <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> -Attributs oder der <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> -Eigenschaft festlegen. Wenn beide festgelegt sind, CODECAPI_AVEncCommonMeanBitRate überschreibt. In Windows 8 können Sie die durchschnittliche Bitrate während der Codierung festlegen. Wenn sich die Bitrate ändert, verwendet der Encoder Adaptive Codierung.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></td>
<td>Legt den Kompromiss der Qualität/Geschwindigkeit fest. Gültiger Bereich:
<ul>
<li>0 – 33: geringe Komplexität</li>
<li>34 – 66: mittlere Komplexität (Standard)</li>
<li>67 – 100: hohe Komplexität</li>
</ul>
<br/> Dieser Wert wirkt sich darauf aus, wie der Encoder verschiedene Codierungs Vorgänge ausführt, z. b. Motion Compensation. Bei höheren Komplexitätsstufen führt der Encoder langsamer aus, erzeugt aber eine bessere Qualität mit derselben Bitrate.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a></td>
<td>Aktiviert oder deaktiviert CABAC (Kontext Adaptive binäre binäre Codierung) für die H. 264-Entropie Codierung. Der Standardwert ist <strong>VARIANT_FALSE</strong>. <br/> CABAC wird nicht für Basis Linien Profile verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a></td>
<td>Legt den Wert <strong>seq_parameter_set_id</strong> in der SPS-nal-Einheit des H. 264-Bitstreams fest. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a></td>
<td>Legt die maximale Anzahl aufeinander folgender B-Frames im ausgabebitstream fest. Gültige Werte sind:
<ul>
<li>0: keine Rahmen (Standard) verwenden.</li>
<li>1: Verwenden Sie einen B-Frame.</li>
<li>2: Verwenden Sie zwei B-Frames.</li>
</ul>
Um diesen Parameter festzulegen, legen Sie die-Eigenschaft vor dem Aufrufen von <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>imftransform:: setoutputtype</strong></a>fest. <br/> Für das Basis Linien Profil ist die Anzahl der B-Frames immer 0 (null). Der Encoder überschreibt Werte ungleich 0 (null).<br/> Wenn diese Eigenschaft bei anderen H. 264-Profilen ungleich 0 (null) ist, ist das Codierungs Muster ibbpbbp, wobei die maximale Anzahl aufeinander folgender B-Frames gleich <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a>ist. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></td>
<td>Legt die Anzahl von Bildern von einem GOP-Header auf den nächsten fest, einschließlich des führenden Ankers, jedoch nicht des folgenden. <br/> Der gültige Bereich ist [0... 2 ³ ² – 1]. Wenn der Wert NULL ist, wählt der Encoder die GOP-Größe aus. Der Standardwert ist 0 (null). <br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></td>
<td>Legt die Anzahl von Arbeitsthreads fest, die von einem Encoder verwendet werden.<br/> Der gültige Bereich ist 0 – 16. Wenn der Wert NULL ist, wählt der Encoder die Anzahl der Threads aus. <br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a></td>
<td>Gibt den Typ von Videoinhalten an.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></td>
<td>Gültiger Bereich: 16 – 51. Der Standardwert ist 24. <br/> Diese Eigenschaft wird angewendet, wenn der Raten Steuerungs Modus <strong>eAVEncCommonRateControlMode_Quality</strong>ist. <br/> Diese Eigenschaft konfiguriert die gleiche Codierungs Einstellung wie " <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>rrccommonquality</strong></a>". Mithilfe von " <a href="codecapi-avencvideoencodeqp.md">avencvideoencodeqp</a> " kann die Anwendung den Wert von QP jedoch direkt angeben. Wenn beide Eigenschaften festgelegt sind, überschreibt der Wert von avencvideoencodeqp. <br/> Der Standardwert von 24 entspricht dem Standardwert 70 für die Einstellung " <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>avenccommonquality</strong></a> ".<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></td>
<td>Zwingt den Encoder, den nächsten Frame als Keyframe zu codieren.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></td>
<td>Gültiger Bereich: 0 – 51. Der Standardwert ist 0. <br/> Diese Eigenschaft gilt für alle Raten Steuerungs Modi. Der Encoder sollte nicht einen QP-Wert enthalten, der niedriger ist als der Wert, der durch die <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> -Eigenschaft angegeben wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></td>
<td>Aktiviert oder deaktiviert den Modus mit niedriger Latenz. Weitere Informationen finden Sie &quot; im Abschnitt "Hinweise" unter Multithreading &quot; .<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Der Encoder unterstützt die folgenden Modi für die Raten Steuerung.



| Mode                                  | Konstante                                            | BESCHREIBUNG                                                                                                                                                                                                                                         |
|---------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Konstante Bitrate (CBR)               | **eAVEncCommonRateControlMode_CBR**                | Der Encoder versucht, eine Konstante Bitrate mithilfe eines "Leaky Bucket"-Modells zu erzielen. Die Zielbitrate wird durch die [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) -Eigenschaft angegeben. <br/> Erfordert Windows 8. <br/> |
| Bitrate der eingeschränkten Variablen (VBR)   | **eAVEncCommonRateControlMode_PeakConstrainedVBR** | Der Encoder verwendet ein "Leaky Bucket"-Modell mit einer Spitzen Bitrate. Die Ausgleichs Rate für den Leaky-Bucket wird durch die [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) -Eigenschaft angegeben. <br/> Erfordert Windows 8. <br/>     |
| Qualitäts basierte Variable Bitrate (VBR) | **eAVEncCommonRateControlMode_Quality**            | Der Encoder versucht, eine Konstante Qualitätsstufe zu erreichen, die von der Eigenschaft " [**avenccommonquality**](../directshow/avenccommonquality-property.md) " angegeben wird.                                                                                                           |
| Nicht eingeschränkter VBR                     | **eAVEncCommonRateControlMode_UnconstrainedVBR**   | Der Encoder versucht, die Ziel Bitrate zu erreichen, die vom [**MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) -Attribut im Ausgabe Medientyp angegeben wird. Dies ist der Standardmodus.                                                              |



 

Für CBR und eingeschränkte VBR-Modi ist Windows 8 erforderlich.

In Windows 8 legt der Encoder die folgenden Attribute auf den Ausgabe Beispielen fest:

-   [MFSampleExtension_DecodeTimestamp](mfsampleextension-decodetimestamp.md)
-   [MFSampleExtension_VideoEncodePictureType](mfsampleextension-videoencodepicturetype.md)
-   [MFSampleExtension_VideoEncodeQP](mfsampleextension-videoencodeqp.md)

> [!Note]  
> In einer früheren Version der Dokumentation wurde fälschlicherweise angegeben, dass der Encoder auf Windows Server 2008 R2 unterstützt wird.

 

### <a name="multithreading"></a>Multithreading

In Windows 8 unterstützt der Encoder zwei Codierungs Modi:

-   **Slice-Codierung.** In diesem Modus werden Slices parallel codiert. Jeder Slice wird in einem anderen Thread codiert. Dieser Modus weist eine geringe Latenzzeit auf, da ein einzelnes Bild parallel codiert wird. Dieser Ansatz wird jedoch nicht skaliert, wenn die Anzahl der Kerne zunimmt, weil die Anzahl der Slices durch die Anzahl der Makroblock Zeilen im Eingabebild begrenzt ist.
-   **Multiframe-Codierung.** In diesem Modus akzeptiert der Encoder mehrere Frames der Eingabe und codiert Sie parallel. Dieser Modus wird in einer Umgebung mit mehreren Kernen besser skaliert, führt jedoch zu einer höheren Latenz.

Der Encoder verwendet standardmäßig die Slice-Codierung, um die Latenz zu minimieren Legen Sie die [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) -Eigenschaft auf **VARIANT_FALSE** fest, um die Multi-Frame-Codierung zu aktivieren.

Legen Sie die [CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) -Eigenschaft fest, um die Anzahl von Arbeitsthreads festzulegen, die vom Encoder verwendet werden.

In Windows 7 verwendet der Encoder immer die Slice-Codierung.

### <a name="certified-hardware-encoder"></a>Zertifizierter Hardware Encoder

Wenn ein zertifizierter Hardware Encoder vorhanden ist, wird er in der Regel anstelle des Eingangsbox System Encoders für Media Foundation bezogenen Szenarios verwendet. Zertifizierte Encoder sind erforderlich, um einen bestimmten Satz von **icodecapi** -Eigenschaften zu unterstützen, und können optional einen anderen Satz von Eigenschaften unterstützen. Der Zertifizierungsprozess sollte sicherstellen, dass die erforderlichen Eigenschaften ordnungsgemäß unterstützt werden, und, wenn eine optionale Eigenschaft unterstützt wird, dass Sie ebenfalls ordnungsgemäß unterstützt wird.

Im folgenden finden Sie die erforderlichen und optionalen **icodecapi** -Eigenschaften für Encoder zum übergeben der HCK Encoder-Zertifizierung.

Die folgenden Eigenschaften von Windows 8 und Windows 8.1 **icodecapi** sind erforderlich:

-   [CODECAPI_AVEncCommonRateControlMode](../directshow/avenccommonratecontrolmode-property.md)
-   [CODECAPI_AVEncCommonQuality](../directshow/avenccommonquality-property.md)
-   [CODECAPI_AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md)
-   [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)
-   [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md)
-   [CODECAPI_AVEncCommonBufferSize](../directshow/avenccommonbuffersize-property.md)
-   [CODECAPI_AVEncMPVGOPSize](../directshow/avencmpvgopsize-property.md)
-   [CODECAPI_AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md)
-   [CODECAPI_AVEncVideoForceKeyFrame](codecapi-avencvideoforcekeyframe.md)

Die folgenden Windows 8.1 **icodecapi** -Eigenschaften sind optional, werden jedoch in HCK getestet, sofern dies unterstützt wird.

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

Die folgenden Eigenschaften von Windows 8 und Windows 8.1 **icodecapi** sind optional, werden aber in HCK getestet, sofern dies unterstützt wird.

-   [CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (statisch)
-   [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md)

Die folgenden **icodecapi** -Eigenschaften sind optional. Sie werden nicht in HCK getestet.

-   [CODECAPI_AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                |
| DLL<br/>                      | <dl> <dt>Mfh264enc.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[MPEG-4-Unterstützung in Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Unterstützte Medienformate in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Video Medientypen](video-media-types.md)
</dt> </dl>

 

 
