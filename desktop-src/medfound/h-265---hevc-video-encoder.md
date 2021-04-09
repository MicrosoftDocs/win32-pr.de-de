---
description: Der Video Encoder Media Foundation H. 265 ist eine Media Foundation Transformation, die das Codieren von Inhalten in das H. 265/hevc-Format unterstützt.
ms.assetid: 790CFB39-6FC0-432D-A434-5262C30EABF4
title: H. 265/hevc-Video Encoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015295792a72f3250c47389192586dbc00566858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959193"
---
# <a name="h265--hevc-video-encoder"></a>H. 265/hevc-Video Encoder

Der Video Encoder Media Foundation H. 265 ist eine [Media Foundation Transformation](media-foundation-transforms.md) , die das Codieren von Inhalten in das H. 265/hevc-Format unterstützt. Der Encoder unterstützt die folgenden Profile:

-   Profil: Main

Der H. 265-Video Encoder macht die folgenden Schnittstellen verfügbar:

-   [**Icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMF-Transformation**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a>Eingabetypen

Der Eingabe Medientyp muss einen der folgenden Untertypen aufweisen:

-   **MF-Format ( \_ IYUV)**
-   **MF-Format \_ NV12**
-   **MF-Format \_ im YUY2**
-   **MF-Format \_ YV12**

Weitere Informationen zu diesen Untertypen finden Sie unter [Video Untertyp-GUIDs](video-subtype-guids.md).

Der Ausgabetyp muss vor dem Eingabetyp festgelegt werden. Bis der Ausgabetyp festgelegt ist, gibt die [**IMF Transform:: setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) -Methode des Encoders einen **\_ \_ \_ \_ nicht \_ festgelegten MF E-Transformationstyp** zurück.

## <a name="output-types"></a>Ausgabetypen

Der Encoder unterstützt einen einzelnen Ausgabe Untertyp:

-   **MF-Format \_ H265**

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
<td>Video Untertyp. Muss <strong>MFVideoFormat_HEVC</strong>werden.</td>
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
<td><a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a></td>
<td>H. 265-Codierungs Profil.<br/> Die unterstützten Werte sind: <br/>
<ul>
<li><strong>eAVEncH265VProfile_Main_420_8</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></td>
<td>Gibt die Ebene des codierten Videos an. Weitere Informationen zu den Einschränkungen für Profile und Ebenen finden Sie in Anhang A von ITU-T H. 265.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></td>
<td>Dies ist optional. Gibt das Pixel Seitenverhältnis an. Der Standardwert ist 1:1.</td>
</tr>
</tbody>
</table>



 

Nachdem der Ausgabetyp festgelegt wurde, aktualisiert der Video Encoder den Typ durch Hinzufügen des [**MF \_ MT-MPEG- \_ \_ Sequenz \_ Header**](mf-mt-mpeg-sequence-header-attribute.md) Attributs. Dieses Attribut enthält den Sequence-Header.

## <a name="supported-imftransform-methods"></a>Unterstützte IMF Transform-Methoden

Die folgenden Methoden der [**IMF Transform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle werden für den H. 265/hevc-Encoder unterstützt:

-   [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)
-   [**Getinputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)
-   [**Getinputcurrenttype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)
-   [**Getinputstatus**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstatus)
-   [**Getinputstreaminfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)
-   [**Getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)
-   [**Getoutputcurrenttype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)
-   [**Getoutputstatus**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus)
-   [**Getoutputstreaminfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)
-   [**Getstreamcount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount)
-   [**Getstreamlimits**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits)
-   [**ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
-   [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)
-   [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)
-   [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
-   [**"Ttinputtype"**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)
-   [**Setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
-   [**Setoutputbounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds)

Alle anderen [**IMF Transform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Methoden geben den Fehler E \_ notimpl zurück.

## <a name="supported-icodecapi-methods"></a>Unterstützte icodecapi-Methoden

Die folgenden Methoden der [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle werden für den H. 265/hevc-Encoder unterstützt:

-   [**IsSupported**](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)
-   [**GetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [**Getparameterrange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [**GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)

Alle anderen [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Methoden geben den Fehler E \_ notimpl zurück.

## <a name="codec-properties"></a>Codec-Eigenschaften

Der H. 265-Encoder implementiert die [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle zum Festlegen von Codierungs Parametern. Die folgenden Eigenschaften werden unterstützt:

Die Codec-Anforderungen für die HCK Encoder-Zertifizierung finden Sie weiter unten im Abschnitt **Certified Hardware Encoder** .



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
<td><a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a></td>
<td>Legt den Raten Steuerungs Modus fest. Unterstützte Modi:<br/>
<ul>
<li><strong>eAVEncCommonRateControlMode_CBR</strong></li>
<li><strong>eAVEncCommonRateControlMode_Quality</strong></li>
</ul>
Wenn andere Modi angegeben werden, wird die <strong>eAVEncCommonRateControlMode_CBR</strong> Raten Steuerung verwendet.<br/> Dies ist ein VT_UI4 Wert.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></td>
<td>Legt die durchschnittliche Bitrate für den codierten Bitstream in Bits pro Sekunde fest. <br/> Der gültige Bereich ist [1... 2 ³ ² – 1]. <br/> Dies ist ein VT_UI4 Wert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></td>
<td>Legt die Puffergröße in Bytes für die Konstante Bitrate (CBR)-Codierung fest.<br/> Der gültige Bereich ist [1... 2 ³ ² – 1]. <br/> Dies ist ein VT_UI4 Wert.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></td>
<td>Legt die maximale Bitrate für Raten Steuerungs Modi fest, die eine Spitzen Bitrate zulassen. <br/> Der gültige Bereich ist [1... 2 ³ ² – 1]. <br/> Dies ist ein VT_UI4 Wert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></td>
<td>Legt die Anzahl von Bildern von einem GOP-Header auf den nächsten fest, einschließlich des führenden Ankers, jedoch nicht des folgenden. <br/> Der gültige Bereich ist [0... 2 ³ ² – 1]. Wenn der Wert NULL ist, wählt der Encoder die GOP-Größe aus. Der Standardwert ist 0 (null). <br/> Dies ist ein VT_UI4 Wert.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></td>
<td>Aktiviert oder deaktiviert den Modus mit niedriger Latenz. <br/> Dies ist ein VT_BOOL Wert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></td>
<td>Legt den Kompromiss der Qualität/Geschwindigkeit fest. Dieser Wert wirkt sich darauf aus, wie der Encoder verschiedene Codierungs Vorgänge ausführt, z. b. Motion Compensation. Bei höheren Komplexitätsstufen führt der Encoder langsamer aus, erzeugt aber eine bessere Qualität mit derselben Bitrate. <br/> Der gültige Bereich ist 0 – 100. Intern wird dieser Wert einem kleineren Satz von Qualitäts-und Geschwindigkeitsstufen zugeordnet, der vom Encoder unterstützt wird.<br/> Dies ist ein VT_UI4 Wert.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></td>
<td>Zwingt den Encoder, den nächsten Frame als Keyframe zu codieren.<br/> Dies ist ein VT_UI4 Wert.<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></td>
<td>Wenn diese Eigenschaft festgelegt wird, bewirkt dies, dass der Encoder das angegebene QP verwendet, um den nächsten Frame und alle nachfolgenden Frames zu codieren, bis ein neues QP angegeben wird. <br/> Gültiger Bereich: 0 – 51, inklusiv <br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></td>
<td>Mit dieser Eigenschaft wird ein Grenzwert für den minimalen QP festgelegt, der vom Encoder während der CBR-Ratecontrol verwendet werden kann.<br/> Dies ist ein VT_UI4 Wert.<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a></td>
<td>Mit dieser Eigenschaft wird ein Grenzwert für die maximale Anzahl von QP festgelegt, die der Encoder während der CBR-Ratecontrol verwenden kann.<br/> Dies ist ein VT_UI4 Wert.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a></td>
<td>Legt fest, ob es sich bei dem Inhalt um Vollbildvideos handelt, im Gegensatz zu Bildschirm Inhalten, die möglicherweise ein kleineres Videofenster enthalten oder überhaupt kein Video enthalten.<br/> Dies ist ein VT_UI4 Wert.<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></td>
<td>Legt die Anzahl von Threads fest, die verwendet werden, um den Komprimierungs Vorgang auszuführen. Der Encoder teilt den Frame in Kacheln auf, sodass die Anzahl der Threads der Anzahl der Kacheln gleicht.<br/>
<ul>
<li>Die Anzahl der logischen Prozessoren. Die Anzahl der Threads muss kleiner oder gleich der Anzahl der logischen Prozessoren sein.</li>
<li>Die Größe des Frames. Die Größe einer Kachel muss größer oder gleich 265x 64 Pixel sein.</li>
<li>Parität: Die Anzahl der Threads muss ein geraden Wert sein. Wenn der angegebene Wert ungerade ist, wird der nächste niedrigere gleich Wert verwendet.</li>
</ul>
Dies ist ein VT_UI4 Wert.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="certified-hardware-encoder"></a>Zertifizierter Hardware Encoder

Wenn ein zertifizierter Hardware Encoder vorhanden ist, wird er in der Regel anstelle des Eingangsbox System Encoders für Media Foundation bezogenen Szenarios verwendet. Zertifizierte Encoder sind erforderlich, um einen bestimmten Satz von **icodecapi** -Eigenschaften zu unterstützen, und können optional einen anderen Satz von Eigenschaften unterstützen. Der Zertifizierungsprozess sollte sicherstellen, dass die erforderlichen Eigenschaften ordnungsgemäß unterstützt werden, und, wenn eine optionale Eigenschaft unterstützt wird, dass Sie ebenfalls ordnungsgemäß unterstützt wird.

Im folgenden finden Sie die erforderlichen und optionalen **icodecapi** -Eigenschaften für Encoder zum übergeben der HCK Encoder-Zertifizierung.

-   [Codecapi \_ avenccommonratecontrolmode](../directshow/avenccommonratecontrolmode-property.md)
-   [Codecapi \_ avenccommonquality](../directshow/avenccommonquality-property.md)
-   [Codecapi \_ avenccommonmeanbitrate](../directshow/avenccommonmeanbitrate-property.md)
-   [Codecapi \_ avenccommonbuffersize](../directshow/avenccommonbuffersize-property.md)
-   [Codecapi \_ avencmpvgopsize](../directshow/avencmpvgopsize-property.md)
-   [Codecapi \_ avencvideoencodeqp](codecapi-avencvideoencodeqp.md)
-   [Codecapi \_ avencvideoforcekeyframe](codecapi-avencvideoforcekeyframe.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                |
| DLL<br/>                      | <dl> <dt>Mfh265enc.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> </dl>

 

 
