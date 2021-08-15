---
description: Der MPEG4 Part 2 Video-Decoder decodiert Videostreams, die gemäß dem MPEG4 Part 2-Standard codiert wurden.
ms.assetid: 56e32d3c-9bd0-41fe-bb22-e4ff37b7cc5c
title: MPEG-4 Part 2 Video Decoder (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847e5be8c506e534c42962ecf6b0037a2ecb2f184c9c47fa92981fa32fd55422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973019"
---
# <a name="mpeg-4-part-2-video-decoder"></a>MPEG-4 Part 2 Video Decoder

Der MPEG4 Part 2 Video-Decoder decodiert Videostreams, die gemäß dem MPEG4 Part 2-Standard codiert wurden.

Sie können eine Instanz des MPEG4 Part 2 Video-Decoders erstellen, indem Sie **CoCreateInstance** aufrufen. Verwenden Sie den Klassenbezeichner **CLSID \_ CMpeg4sDecMediaObject,** um eine Instanz des Decoders zu erstellen, die sich als DirectX-Medienobjekt (DMO) verhält. Verwenden Sie den Klassenbezeichner **CLSID \_ CMpeg4sDecMFT,** um einen Decoder zu erstellen, der sich als Media Foundation Transform (MFT) verhält.

## <a name="input-types"></a>Eingabetypen

Der MPEG4 Part 2 Video-Decoder unterstützt die folgenden Eingabemedientypen.

-   MEDIASUBTYPE \_ M4S2
-   MEDIASUBTYPE \_ m4s2
-   MEDIASUBTYPE \_ MP4V
-   MEDIASUBTYPE \_ mp4v
-   MEDIASUBTYPE \_ MP4S (veraltet)
-   MEDIASUBTYPE \_ mp4s (veraltet)

## <a name="output-types"></a>Ausgabetypen

Der MPEG4 Part 2 Video-Decoder unterstützt die folgenden Ausgabemedienuntertypen, wenn er als DMO fungiert.

-   MEDIASUBTYPE \_ YV12
-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ YVYO
-   MEDIASUBTYPE \_ NV11
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

Der MPEG4 Part 2 Video-Decoder unterstützt die folgenden Ausgabemedienuntertypen, wenn er als MFT fungiert.

-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YV12

## <a name="formats"></a>Formate

Der MPEG4 Part 2 Video-Decoder akzeptiert die folgenden Formate.

-   [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)
-   [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (VIH2)
-   [**MFVideoInfo**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoinfo)
-   [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (Nur der VIH2-Teil des Headers wird verwendet.)

## <a name="interfaces-for-the-dmo"></a>Schnittstellen für die DMO

Wenn Sie eine Instanz des MPEG4 Part 2 Video-Decoders als DMO erstellen, macht der Decoder die folgenden Schnittstellen verfügbar.

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)

Sie können eine [**IMediaObject-Schnittstelle**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) abrufen, indem **Sie CoCreateInstance** aufrufen, und Sie können eine [**ICodecAPI-Schnittstelle**](/windows/win32/api/strmif/nn-strmif-icodecapi) abrufen, indem Sie **QueryInterface** aufrufen.

## <a name="interfaces-for-the-mft"></a>Schnittstellen für MFT

Wenn Sie eine Instanz des MPEG2 Part 2 Video-Decoders als MFT erstellen, macht der Decoder die folgenden Schnittstellen verfügbar.

-   [**ÜBERTRANSFORM**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**ATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**HAPQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**HAPQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**THICKNESSRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**1000000000**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)

Sie können einen Zeiger auf die [**INTERFACESTransform-Schnittstelle**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) abrufen, indem Sie **CoCreateInstance** aufrufen, und Sie können einen Zeiger auf die [**INTERFACESAttributes-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) abrufen, indem [**Sie DENTRANSFORM::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)aufrufen. Sie können einen Zeiger auf die [**SCHNITTSTELLE "POINTERQualityAdvise"**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise) oder [**"POINTERQualityAdvise2"**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2) abrufen, indem Sie **QueryInterface** für den MFT aufrufen. Sie können einen Zeiger auf die [**INTERFACESRateControl-**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) oder [**DIETRATESupport-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) abrufen, indem Sie [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) aufrufen und den Dienstbezeichner **MF RATE CONTROL \_ \_ \_ SERVICE** übergeben.

## <a name="profiles-and-levels"></a>Profile und Ebenen

Die MPEG4-Spezifikation definiert mehrere Profile, von denen jedes die Tools angibt, die ein Encoder zum Generieren eines codierten Streams verwenden kann. Der MPEG4 Part2 Video Decoder unterstützt zwei dieser Profile: Einfaches visuelles Profil und Erweitertes einfaches Profil. Anders ausgedrückt: Der MPEG4 Part 2 Video-Decoder kann Streams decodieren, die entweder gemäß dem einfachen visuellen Profil oder dem erweiterten einfachen Profil codiert wurden.

Das einfache visuelle Profil unterstützt die einfache Übertragung von Videos mit niedriger Bitrate im progressiven Modus. Es unterstützt nur Intra- und Prediction-Bilder. Es unterstützt auch den kurzen Headermodus, der abwärtskompatibel mit dem H.263-Baselineprofil ist. Ab Windows 10 unterstützt der MPEG-4 Part 2 Video Decoder auch H.263v2 (H.263+), der benutzerdefinierte Bildgrößen unterstützt.

Advanced Simple Profile unterstützt alle Tools des einfachen visuellen Profils und darüber hinaus Videointerlacing, B-Frames, Quarter-Motion-Kompensierung, zusätzliche Quantisierungstabellen und globale Bewegungskompensierung.

Die MPEG4-Spezifikation definiert auch mehrere Ebenen, von denen jede Einschränkungen für den von einem Encoder generierten Ausgabestream angibt.

Die folgende Tabelle zeigt die Profile und Ebenen sowie typische Auflösungen, die vom MPEG4 Part 2 Video-Decoder unterstützt werden.



| Profil         | Ebene | Typische Auflösung |
|-----------------|-------|--------------------|
| Einfaches Visual   | 0     | 176 x 144          |
| Einfaches Visual   | 1     | 176 x 144          |
| Einfaches Visual   | 2     | 352 x 288          |
| Einfaches Visual   | 3     | 352 x 288          |
| SimpleVisual    | 4a    | 640 x 480          |
| Einfaches Visual   | 5     | 720 x 576          |
| Advanced Simple | 0     | 176 x 144          |
| Advanced Simple | 1     | 176 x 144          |
| Advanced Simple | 2     | 352 x 288          |
| Advanced Simple | 3     | 352 x 288          |
| Advanced Simple | 3b    | 352 x 288          |
| Advanced Simple | 4     | 352 x 756          |
| Advanced Simple | 5     | 720 x 576          |



 

Weitere Informationen zu Profilen und Ebenen finden Sie in der MPEG4 Part 2-Spezifikation (ISO/IEC 14496-2): Information technology -- Coding of audio-visual objects -- Part 2: Visual.

## <a name="decoder-properties"></a>Decodereigenschaften

Um Eigenschaften für den MPEG4 Part 2 Video-Decoder festzulegen, verwenden Sie die [**ICodecAPI-Schnittstelle**](/windows/win32/api/strmif/nn-strmif-icodecapi) oder die [**INTERFACESAttributes-Schnittstelle.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

Der MPEG4 Part 2 Video-Decoder unterstützt die folgenden Eigenschaften.



<table>
<thead>
<tr class="header">
<th>Eigenschaft</th>
<th>BESCHREIBUNG</th>
<th>Standardwert</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avdecvideoswpowerlevel-property"><strong>CODECAPI_AVDecVideoSWPowerLevel</strong></a></td>
<td>Gibt die Leistungsstufe an.<br/> <dl> Windows 7.<br />
Nur Schreibzugriff.<br />
</dl></td>
<td>100</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avdecvideothumbnailgenerationmode-property"><strong>CODECAPI_AVDecVideoThumbnailGenerationMode</strong></a></td>
<td>Gibt den Miniaturansichtsgenerierungsmodus an.<br/> <dl> Windows 7.<br />
Nur Schreibzugriff.<br />
</dl></td>
<td><strong>VARIANT_FALSE</strong></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Hinweise

Die GUIDs (Globally Unique Identifiers) für RGB-Medienuntertypen unterscheiden sich je nachdem, ob ein Decoder als DMO oder MFT fungiert. Die GUIDs für Nicht-RGB-Medienuntertypen sind identisch, unabhängig davon, ob ein Decoder als DMO oder MFT fungiert. Informationen zu den GUIDs, die Medienuntertypen darstellen, finden Sie unter [Medientypen.](media-types.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MP4SDecd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> </dl>

 

 
