---
description: Der Video Decoder Media Foundation H. 264 ist eine Media Foundation Transformation, die die Decodierung von Baseline, Main und High Profile bis zu Ebene 5,1 unterstützt.
ms.assetid: 783a3618-981a-4573-9e9e-ebf5eeb75d06
title: H. 264-Video Decoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75c4713b1a4e36d1ba085b2239c24ca0f6e4fae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484054"
---
# <a name="h264-video-decoder"></a>H. 264-Video Decoder

Der Video Decoder Media Foundation H. 264 ist eine [Media Foundation Transformation](media-foundation-transforms.md) , die die Decodierung von Baseline, Main und High Profile bis zu Ebene 5,1 unterstützt.

Der H. 264-Video Decoder macht die folgenden Schnittstellen verfügbar.

-   [**Icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) (unterstützt in Windows 8)
-   [**IMF-Dienst**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMF-Empfehlung**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**Imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**Imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**Imfrealtimeclient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMF-Transformation**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

Führen Sie eine der folgenden Aktionen aus, um eine Instanz des Decoders zu erstellen:

-   Ruft die [**mftenum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) -oder [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion auf.
-   [**Cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)aufrufen. Die CLSID für den Decoder ist **CLSID \_ CMSH264DecoderMFT**, deklariert in wmcodecdsp. h.

## <a name="input-types"></a>Eingabetypen

Der Eingabetyp muss mindestens die beiden folgenden Attribute enthalten:



| Attribut                                                 | BESCHREIBUNG                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**Haupt-Typ des MF- \_ MT \_ \_**](mf-mt-major-type-attribute.md) | **MF MediaType- \_ Video**                                                                        |
| [**MF- \_ MT- \_ Untertyp**](mf-mt-subtype-attribute.md)        | [MF-Format \_ H264 oder](video-subtype-guids.md) MF-Format \_ H264 \_ es |



 

Wenn der Eingabetyp nur diese beiden Attribute enthält, bietet der Decoder einen Standard Ausgabetyp an, der als Platzhalter fungiert. Wenn der Decoder genügend Eingabe Beispiele empfängt, um einen Ausgabe Rahmen zu schaffen, signalisiert er eine Formatänderung, indem er die **Änderung von MF \_ E \_ Transform \_ \_ Stream** von [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)zurückgibt. Ausführliche Informationen zur Behandlung von Formatänderungen finden Sie in der **ProcessOutput** -Dokumentation.

Um eine anfängliche Formatänderung zu vermeiden, geben Sie so viele Informationen wie möglich im Eingabetyp an, einschließlich:



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
<td><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></td>
<td>Die Framerate.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></td>
<td>Frame Dimensionen.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></td>
<td>Interlace-Modus.
<blockquote>
[!Note]<br />
In H. 264-Video kann sich die damit-Struktur dynamisch ändern, sodass der empfohlene Wert dieses Attributs <strong>MFVideoInterlace_MixedInterlaceOrProgressive</strong>ist. Interlace-Informationen im Video-elementaren Stream haben Vorrang vor dem Medientyp. Weitere Informationen finden Sie unter <a href="video-interlacing.md">Video Interlacing</a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></td>
<td>Pixel Seitenverhältnis.</td>
</tr>
</tbody>
</table>



 

Der Eingabetyp muss vor dem Ausgabetyp festgelegt werden. Bis der Eingabetyp festgelegt ist, gibt die [**IMF Transform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) -Methode des Encoders einen **\_ \_ \_ \_ nicht \_ festgelegten MF E-Transformationstyp** zurück.

## <a name="output-types"></a>Ausgabetypen

Der Decoder unterstützt die folgenden Ausgabe Untertypen:

-   **MF-Format \_ I420**
-   **MF-Format ( \_ IYUV)**
-   **MF-Format \_ NV12**
-   **MF-Format \_ im YUY2**
-   **MF-Format \_ YV12**

Weitere Informationen zu diesen Untertypen finden Sie unter [Video Untertyp-GUIDs](video-subtype-guids.md).

## <a name="transform-attributes"></a>Transformations Attribute

Der H. 264-Decoder implementiert die [**IMF Transform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) -Methode. Anwendungen können diese Methode verwenden, um die folgenden Attribute zu erhalten oder festzulegen.



| Attribut                                                                                       | BESCHREIBUNG                                                                                |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [Codecapi \_ avdecvideoacceleration \_ H264](../directshow/avdecvideoacceleration-h264-property.md)            | Aktiviert oder deaktiviert die Hardwarebeschleunigung.                                                 |
| [Codecapi \_ avdecvideothumbnailgenerationmode](../directshow/avdecvideothumbnailgenerationmode-property.md) | Aktiviert oder deaktiviert den Miniatur Ansichts Generierungs Modus.                                             |
| [MF \_ sa \_ D3D \_](mf-sa-d3d-aware-attribute.md)                                             | Gibt an, dass der Decoder die DirectX-Video Beschleunigung (DXVA) unterstützt. Als schreibgeschützt behandeln. |



 

In Windows 8 unterstützt der H. 264-Decoder auch die folgenden Attribute.



| Attribut                                                                                                     | BESCHREIBUNG                                                                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Codecapi \_ avlowlatencymode](codecapi-avlowlatencymode.md)                                                   | Aktiviert oder deaktiviert den Decodierungs Modus mit niedriger Latenz.                                                              |
| [Codecapi \_ avdecnumworkerthreads](codecapi-avdecnumworkerthreads.md)                                         | Legt die Anzahl von Arbeitsthreads fest, die vom Decoder verwendet werden.                                                      |
| [Codecapi \_ avdecvideomaxcodedwidth](codecapi-avdecvideomaxcodedwidth.md)                                     | Legt die maximale Bildbreite fest, die der Decoder als Eingabetyp akzeptiert.                               |
| [Codecapi \_ avdecvideomaxcodedheight](codecapi-avdecvideomaxcodedheight.md)                                   | Legt die maximale Bildhöhe fest, die der Decoder als Eingabetyp akzeptiert.                              |
| [\_Anzahl der \_ minimalen \_ Ausgabe \_ Beispiele \_ für MF-SA](mf-sa-minimum-output-sample-count.md)                               | Gibt die maximale Anzahl von Ausgabe Beispielen an.                                                             |
| [MFT- \_ Decoder macht \_ \_ Ausgabe \_ Typen \_ in \_ nativer \_ Reihenfolge verfügbar.](mft-decoder-expose-output-types-in-native-order.md) | Gibt an, ob ein Decoder vor anderen Formaten IYUV/I420-Ausgabetypen (für die Transcodierung geeignet) verfügbar macht. |



 

In Windows 8 unterstützt der H. 264-Decoder die [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle. Diese Schnittstelle bietet eine alternativate-API zum Festlegen der folgenden Codec-Eigenschaften.

-   [Codecapi \_ avdecvideomaxcodedwidth](codecapi-avdecvideomaxcodedwidth.md)
-   [Codecapi \_ avdecvideoacceleration \_ H264](../directshow/avdecvideoacceleration-h264-property.md)
-   [Codecapi \_ avdecvideomaxcodedheight](codecapi-avdecvideomaxcodedheight.md)
-   [Codecapi \_ avdecvideomaxcodedwidth](codecapi-avdecvideomaxcodedwidth.md)
-   [Codecapi \_ avdecvideothumbnailgenerationmode](../directshow/avdecvideothumbnailgenerationmode-property.md)

## <a name="format-constraints"></a>Format Einschränkungen

Der Decoder unterstützt die folgenden Formate:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Profile/Ebenen</td>
<td>Baseline, Main und High Profile, bis zu Ebene 5,1. (Ausführliche Informationen finden Sie in der ITU-T H. 264-Spezifikation.)</td>
</tr>
<tr class="even">
<td>Chroma-Formate</td>
<td>4:2:0 Chroma oder Monochrom</td>
</tr>
<tr class="odd">
<td>Minimale Auflösung</td>
<td>48 × 48 Pixel</td>
</tr>
<tr class="even">
<td>Maximale Auflösung</td>
<td>4096 × 2304 Pixel<br/> Die maximale garantierte Auflösung der DXVA-Beschleunigung beträgt 1920 × 1088 Pixel. bei höherer Auflösung erfolgt die Decodierung mit DXVA, wenn Sie von der zugrunde liegenden Hardware unterstützt wird. andernfalls erfolgt die Decodierung mit Software.<br/>
<blockquote>
[!Note]<br />
In Windows 7 ist die maximal unterstützte Auflösung 1920 × 1088 Pixel für die Software-und DXVA-Decodierung.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td>DXVA</td>
<td>Der Decoder unterstützt DXVA Version 2, aber nicht DXVA Version 1. DXVA-Decodierung wird nur für Haupt kompatible Bitstreams, Main und High Profile unterstützt. (Haupt-kompatible Baseline-Bitstreams werden als <strong>profile_idc</strong>= 66 und <strong>constrained_set1_flag</strong>= 1 definiert.)</td>
</tr>
</tbody>
</table>



 

Eingabedaten müssen dem Anhang B ISO/IEC 14496-10 entsprechen. Die Daten müssen die Start Codes enthalten. Der Decoder überspringt bytes, bis ein gültiger Sequenz Parametersatz (SPS) und ein Bildparameter Satz (PPS) im Bytestream gefunden werden.

Der Decoder bietet keine Unterstützung für die Technologie zum Filmen von Folien.

> [!Note]  
> In einer früheren Version der Dokumentation wurde fälschlicherweise angegeben, dass der Decoder auf Windows Server 2008 R2 unterstützt wird.

 

Wenn die Ergänzung zum Platt Form Update für Windows Vista installiert ist, steht der H. 264-Video Decoder unter Windows Vista zur Verfügung. der Zugriff auf Windows Vista ist jedoch nur mithilfe des [Quell Readers](source-reader.md)möglich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                  |
| DLL<br/>                      | <dl> <dt>Msmpeg2vdec.dll</dt> </dl> |



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

 

 
