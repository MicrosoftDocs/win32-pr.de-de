---
description: Der MPEG4 Part 2-Video Decoder decodiert Videostreams, die entsprechend dem MPEG4-Teil 2-Standard codiert wurden.
ms.assetid: 56e32d3c-9bd0-41fe-bb22-e4ff37b7cc5c
title: MPEG-4 Part 2-Video Decoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 777e6144684c799eb58f75afd4811ccc8871a46b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215031"
---
# <a name="mpeg-4-part-2-video-decoder"></a>MPEG-4 Part 2-Video Decoder

Der MPEG4 Part 2-Video Decoder decodiert Videostreams, die entsprechend dem MPEG4-Teil 2-Standard codiert wurden.

Sie können eine Instanz des Video-Decoders von MPEG4 Part 2 erstellen, indem Sie **CoCreateInstance** aufrufen. Verwenden Sie die Klassen-ID **CLSID \_ CMpeg4sDecMediaObject**, um eine Instanz des Decoders zu erstellen, der sich als DirectX Media Object (DMO) verhält. Verwenden Sie die Klassen-ID **CLSID \_ CMpeg4sDecMFT**, um eine istance des Decoders zu erstellen, der sich als Media Foundation Transformation (MFT) verhält.

## <a name="input-types"></a>Eingabetypen

Der MPEG4 Part 2-Video Decoder unterstützt die folgenden Eingabemedien Typen.

-   Mediasubtype \_ M4S2
-   Mediasubtype \_ m4s2
-   Mediasubtype \_ MP4V
-   Mediasubtype \_ MP4V
-   Mediasubtype \_ MP4 Bitrate (veraltet)
-   Mediasubtype \_ MP4 Bitrate (veraltet)

## <a name="output-types"></a>Ausgabetypen

Der MPEG4 Part 2-Video Decoder unterstützt die folgenden Ausgabemedien-Untertypen, wenn er als DMO fungiert.

-   Mediasubtype \_ YV12
-   Mediasubtype \_ NV12
-   Mediasubtype \_ im YUY2
-   mediasubtype \_ UYVY
-   mediasubtype \_ yvyu
-   Mediasubtype \_ NV11
-   Mediasubtype \_ RGB32
-   Mediasubtype \_ RGB24
-   Mediasubtype \_ RGB565
-   Mediasubtype \_ RGB555
-   Mediasubtype \_ RGB8

Der MPEG4 Part 2-Video Decoder unterstützt die folgenden Ausgabemedien-Untertypen, wenn er als MFT fungiert.

-   Mediasubtype \_ NV12
-   Mediasubtype \_ YV12

## <a name="formats"></a>Formate

Der MPEG4 Part 2-Video Decoder akzeptiert die folgenden Formate.

-   [**Videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)
-   [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (VIH2)
-   [**MF-Info**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoinfo)
-   [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (nur der VIH2-Teil des Headers wird verwendet.)

## <a name="interfaces-for-the-dmo"></a>Schnittstellen für den DMO

Wenn Sie eine Instanz des Video-Decoders von MPEG4 Part 2 als DMO erstellen, macht der Decoder die folgenden Schnittstellen verfügbar.

-   [**Imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**Icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi)

Sie können eine [**imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) -Schnittstelle abrufen, indem Sie **CoCreateInstance** aufrufen, und Sie können eine [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle abrufen, indem Sie **QueryInterface** aufrufen.

## <a name="interfaces-for-the-mft"></a>Schnittstellen für die MFT

Wenn Sie eine Instanz des Video-Decoders der Komponente "MPEG2 Part 2" als MFT erstellen, macht der Decoder die folgenden Schnittstellen verfügbar.

-   [**IMF-Transformation**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**Imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**IMF-Empfehlung**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**Imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**Imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)

Sie können einen Zeiger auf die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle abrufen, indem Sie **CoCreateInstance** aufrufen, und Sie können einen Zeiger auf die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle abrufen, indem Sie [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)aufrufen. Sie können einen Zeiger auf die [**imfqualityempfehlung**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise) -oder [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2) -Schnittstelle abrufen, indem Sie **QueryInterface** auf der MFT aufrufen. Sie können einen Zeiger auf die [**imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) -oder [**imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) -Schnittstelle abrufen, indem Sie [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) aufrufen und den Dienst-ID **MF- \_ Raten \_ Steuerungs \_ Dienst** übergeben.

## <a name="profiles-and-levels"></a>Profile und Ebenen

Die MPEG4-Spezifikation definiert mehrere Profile, von denen jede die Tools angibt, mit denen ein Encoder einen codierten Datenstrom generieren kann. Der MPEG4 part2-Video Decoder unterstützt zwei dieser Profile: einfaches visuelles Profil und erweitertes einfaches Profil. Das heißt, der MPEG4 Part 2-Video Decoder kann Datenströme decodieren, die entweder entsprechend dem einfachen visuellen Profil oder dem erweiterten einfachen Profil codiert wurden.

Das einfache visuelle Profil unterstützt die grundlegende Übertragung von Video mit niedriger Bitrate im progressiven Modus. Es werden nur interne und Vorhersage Bilder unterstützt. Außerdem wird der kurzheader Modus unterstützt, der abwärts mit dem H. 263 Baseline-Profil kompatibel ist. Ab Windows 10 unterstützt der MPEG-4 Part 2-Video Decoder auch h. 263v2 (h. 263 +), der benutzerdefinierte Bildgrößen unterstützt.

Das erweiterte einfache Profil unterstützt alle Tools des einfachen visuellen Profils und unterstützt zusätzlich Zeilen Sprung Video, B-Frames, Quarter-PEL-Bewegungskompensation, zusätzliche Quantisierungs Tabellen und globale Bewegungs Kompensierung.

Die MPEG4-Spezifikation definiert auch mehrere Ebenen, von denen jede Einschränkungen für den von einem Encoder generierten Ausgabestream angibt.

In der folgenden Tabelle sind die Profile und Ebenen zusammen mit den typischen Lösungen aufgeführt, die vom MPEG4 Part 2-Video Decoder unterstützt werden.



| Profil         | Ebene | Typische Lösung |
|-----------------|-------|--------------------|
| Einfaches visuelles Element   | 0     | 176 x 144          |
| Einfaches visuelles Element   | 1     | 176 x 144          |
| Einfaches visuelles Element   | 2     | 352 x 288          |
| Einfaches visuelles Element   | 3     | 352 x 288          |
| Simplevisual    | 4a    | 640 x 480          |
| Einfaches visuelles Element   | 5     | 720 x 576          |
| Erweiterte einfache | 0     | 176 x 144          |
| Erweiterte einfache | 1     | 176 x 144          |
| Erweiterte einfache | 2     | 352 x 288          |
| Erweiterte einfache | 3     | 352 x 288          |
| Erweiterte einfache | 3b    | 352 x 288          |
| Erweiterte einfache | 4     | 352 x 756          |
| Erweiterte einfache | 5     | 720 x 576          |



 

Weitere Informationen zu Profilen und Ebenen finden Sie in der "MPEG4 Part 2"-Spezifikation (ISO/IEC 14496-2): Informationstechnologie-Codieren von audiovisuellen Objekten--Teil 2: Visual.

## <a name="decoder-properties"></a>Decoder-Eigenschaften

Verwenden Sie die [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle oder die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle, um die Eigenschaften des Video-Decoders von MPEG4 Part 2 festzulegen.

Der MPEG4 Part 2-Video Decoder unterstützt die folgenden Eigenschaften.



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
<td>Gibt den Energie Stand an.<br/> <dl> Windows 7.<br />
Nur Schreibzugriff.<br />
</dl></td>
<td>100</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avdecvideothumbnailgenerationmode-property"><strong>CODECAPI_AVDecVideoThumbnailGenerationMode</strong></a></td>
<td>Gibt den Modus für die Miniatur Generierung an.<br/> <dl> Windows 7.<br />
Nur Schreibzugriff.<br />
</dl></td>
<td><strong>VARIANT_FALSE</strong></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Die global eindeutigen Bezeichner (GUIDs) für RGB-Medien Untertypen unterscheiden sich abhängig davon, ob ein Decoder als DMO oder MFT fungiert. Die GUIDs für nicht-RGB-Medien Untertypen sind identisch, unabhängig davon, ob ein Decoder als DMO oder MFT fungiert. Informationen zu den GUIDs, die Medien Untertypen darstellen, finden Sie unter [Medientypen](media-types.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MP4SDecd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> </dl>

 

 
