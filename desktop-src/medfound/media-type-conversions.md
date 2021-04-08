---
description: Medientyp Konvertierungen
ms.assetid: 6aee18b8-79b1-47fb-816f-d1c2c77b3a03
title: Medientyp Konvertierungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3a72e74439251f9661e0ff27166c504e47c238
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761466"
---
# <a name="media-type-conversions"></a>Medientyp Konvertierungen

Gelegentlich ist es erforderlich, zwischen Media Foundation Medientypen und den älteren Medientyp Strukturen aus DirectShow oder dem Windows Media Format SDK zu konvertieren.

### <a name="from-a-format-structure-to-a-media-foundation-type"></a>Von einer Format Struktur zu einem Media Foundation-Typ

Die folgenden Funktionen initialisieren einen Media Foundation Medientyp aus einer Format Struktur. Diese Funktionen sind auch nützlich, wenn ein Datenstrom oder ein Dateiheader eine Format Struktur enthält. Der Dateiheader für Wave-Audiodateien enthält z. b. eine [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Zu konvertierende Struktur</th>
<th>Funktion</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/strmif/ns-strmif-am_media_type"><strong>AM_MEDIA_TYPE</strong></a> (DirectShow)<br/> <a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type"><strong>DMO_MEDIA_TYPE</strong></a> (DirectX-Medienobjekte) <br/> <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type"><strong>WM_MEDIA_TYPE</strong></a> (Windows Media-Format-SDK) <br/>
<blockquote>
[!Note]<br />
Diese Strukturen sind gleichwertig.
</blockquote>
<br/> <br/></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromammediatype"><strong>Mfinitmediatypfromammediatype</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader"><strong>BITMAPINFOHEADER</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatevideomediatypefrombitmapinfoheaderex"><strong>Mfkreatevideomediatypeer frombitmapinfoheaderex</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat"><strong>MF-Format</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommfvideoformat"><strong>Mfinitmediatypfrommf-Format</strong></a></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo"><strong>MPEG1VIDEOINFO</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg1videoinfo"><strong>MFInitMediaTypeFromMPEG1VideoInfo</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo"><strong>MPEG2VIDEOINFO</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg2videoinfo"><strong>MFInitMediaTypeFromMPEG2VideoInfo</strong></a></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2"><strong>VIDEOINFOHEADER2</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader2"><strong>MFInitMediaTypeFromVideoInfoHeader2</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader"><strong>Videoinfoheader</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader"><strong>Mfinitmediatypeer fromvideoinfoheader</strong></a></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/dd757713(v=vs.85)"><strong>WaveFormatEx</strong></a> oder <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)"> <strong>WAVEFORMATEXTENSIBLE</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex"><strong>Mfinitmediatypeer fromwaveformatex</strong></a></td>
</tr>
</tbody>
</table>



 

### <a name="from-a-media-foundation-type-to-a-format-structure"></a>Von einem Media Foundation-Typ in eine Format Struktur

Die folgenden Funktionen erstellen oder initialisieren eine Format Struktur aus einem Media Foundation Medientyp.



| Funktion                                                                             | Zielstruktur                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMF MediaType:: getrepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation)            | [**Am \_ \_Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type), [**MF-Format**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat), [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)oder [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) |
| [**MF | ateammediatypfrommf**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype)     | [**AM \_ - \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |
| [**MF createmf videoformatfrommf**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemfvideoformatfrommfmediatype) | [**MF-Format**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat)                                                                                                                                              |
| [**MF | atewaveformatexfrommf MediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype)   | [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) oder [ **WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))                                                                                    |
| [**Mfinitammediatypammediatype**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype)         | [**AM \_ - \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |



 

## <a name="format-mappings"></a>Format Zuordnungen

In den folgenden Tabellen sind die Media Foundation Attribute aufgeführt, die verschiedenen Format Strukturen entsprechen. Nicht alle diese Attribute können direkt übersetzt werden. Zum Durchführen von Konvertierungen sollten Sie die im vorherigen Abschnitt aufgeführten Funktionen verwenden. Diese Tabellen werden hauptsächlich zur Referenz bereitgestellt.

### <a name="am_media_type"></a>AM \_ - \_ Medientyp



| Member                   | attribute                                                                            |
|--------------------------|--------------------------------------------------------------------------------------|
| **btemporalcompression** | [**\_ \_ alle \_ Beispiele \_ unabhängig von MF**](mf-mt-all-samples-independent-attribute.md) |
| **bfixedsizesamples**    | [**\_Beispiele für \_ die \_ große Größe \_ von MF MT**](mf-mt-fixed-size-samples-attribute.md)           |
| **lsamplesize**          | [**Größe des MF-MT-Beispiels \_ \_ \_**](mf-mt-sample-size-attribute.md)                          |



 

### <a name="waveformatex-waveformatextensible"></a>WaveFormatEx, WAVEFORMATEXTENSIBLE



| Member                  | attribute                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **wformattag**          | [**MF- \_ MT- \_ Untertyp**](mf-mt-subtype-attribute.md)<br/> Wenn es sich bei **wformattag** um ein \_ erweiterbares Wave-Format handelt \_ , befindet sich der Untertyp im **unter formatmember** .<br/> |
| **nchannels**           | [**MF \_ \_ -MT- \_ audionum- \_ Kanäle**](mf-mt-audio-num-channels-attribute.md)                                                                                                |
| **nsamplespersec**      | [**MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde**](mf-mt-audio-samples-per-second-attribute.md)                                                                                   |
| **navgbytespersec**     | [**MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde**](mf-mt-audio-avg-bytes-per-second-attribute.md)                                                                              |
| **nBlockAlign**         | [**MF \_ \_ -MT- \_ Audioblock \_ Ausrichtung**](mf-mt-audio-block-alignment-attribute.md)                                                                                          |
| **wbitspersample**      | [**MF \_ \_ -MT- \_ audiobits \_ pro \_ Beispiel**](mf-mt-audio-bits-per-sample-attribute.md)                                                                                         |
| **wvalidbitspersample** | [**zulässige \_ \_ \_ \_ Bits \_ pro \_ Beispiel für MF-MT-Audiodaten**](mf-mt-audio-valid-bits-per-sample-attribute.md)                                                                            |
| **wsamplesperblock**    | [**MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Block**](mf-mt-audio-samples-per-block-attribute.md)                                                                                     |
| **dwchannelmask**       | [**MF \_ \_ -MT \_ - \_ audiokanalmaske**](mf-mt-audio-channel-mask-attribute.md)                                                                                                |
| **Unter Formattyp**           | [**MF- \_ MT- \_ Untertyp**](mf-mt-subtype-attribute.md)                                                                                                                        |
| Zusätzliche Daten              | [**\_ \_ Benutzer \_ Daten für MF-MT**](mf-mt-user-data-attribute.md)                                                                                                                   |



 

### <a name="videoinfoheader-videoinfoheader2"></a>Videoinfoheader, VIDEOINFOHEADER2



| Member                                         | attribute                                                                                                                                                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwbitrate**                                  | [**MF-mittlere mittlere \_ \_ \_ Bitrate**](mf-mt-avg-bitrate-attribute.md)                                                                                                                                                                                      |
| **dwbiterrorrate**                             | [**durchschnittliche \_ \_ \_ \_ Fehler \_ Rate des MF-MT-Durchschnittl.**](mf-mt-avg-bit-error-rate-attribute.md)                                                                                                                                                                      |
| **Avgtimeperframe**                            | [**MF \_ MT- \_ Frame \_ Rate**](mf-mt-frame-rate-attribute.md); verwenden Sie [**mfaveragetimeperframetframerate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) , um diesen Wert zu berechnen.                                                                             |
| **dwinterlaceflags**                           | [**MF- \_ MT- \_ Interlace- \_ Modus**](mf-mt-interlace-mode-attribute.md)                                                                                                                                                                                |
| **dwcopyprotectflags**                         | Kein definiertes Äquivalent                                                                                                                                                                                                                            |
| **dwpictaspectratiox**, **dwpictaspectratijen** | [**MF \_ \_ \_ Seiten \_**](mf-mt-pixel-aspect-ratio-attribute.md)Verhältnis des MT-Pixels; muss zwischen Bildseiten Verhältnis und Bildseiten Verhältnis konvertieren.                                                                                                      |
| **dwcontrolflags**                             | [**MF \_ MT- \_ Pad- \_ \_ steuerungflags**](mf-mt-pad-control-flags-attribute.md). Wenn das **amcontrol \_ colorinfo \_ Present** -Flag vorhanden ist, legen Sie die erweiterten Farb Attribute fest, die unter [Erweiterte Farbinformationen](extended-color-information.md)beschrieben werden. |
| **bmiheader. biwidth**, **bmiheader. biheight**  | [**MF- \_ MT- \_ Frame \_ Größe**](mf-mt-frame-size-attribute.md)                                                                                                                                                                                        |
| **bmiheader. biBitCount**                       | Implizit im Untertyp ([**MF \_ MT- \_ Untertyp**](mf-mt-subtype-attribute.md)).                                                                                                                                                                    |
| **bmiheader. bicompression**                    | Implizit im Untertyp.                                                                                                                                                                                                                         |
| **bmiheader. bisizeimage**                      | [**Größe des MF-MT-Beispiels \_ \_ \_**](mf-mt-sample-size-attribute.md)                                                                                                                                                                                      |
| Paletteninformationen                            | [**MF- \_ MT- \_ Palette**](mf-mt-palette-attribute.md)                                                                                                                                                                                               |



 

Die folgenden Attribute können aus der [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -oder [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Struktur abgeleitet werden, erfordern jedoch auch einige Kenntnisse der Format Details. Beispielsweise weisen verschiedene YUV-Formate unterschiedliche Stride-Anforderungen auf.

-   [**MF- \_ MT- \_ Standard \_ Schritt**](mf-mt-default-stride-attribute.md)
-   [**minimale Anzahl von MF- \_ MT- \_ \_ anzeigen \_**](mf-mt-minimum-display-aperture-attribute.md)
-   [**MF- \_ MT- \_ Schwenken- \_ Überprüfung \_**](mf-mt-pan-scan-aperture-attribute.md)

### <a name="mpeg1videoinfo"></a>MPEG1VIDEOINFO



| Member                                   | attribute                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------|
| **dwstarttimecode**                      | [**Code der MF- \_ \_ MPEG- \_ \_ Startzeit \_**](mf-mt-mpeg-start-time-code-attribute.md) |
| **bsequenceheader**                      | [**MF- \_ MT- \_ MPEG- \_ Sequenz \_ Header**](mf-mt-mpeg-sequence-header-attribute.md)  |
| **bixpelspermeter**, **biypelspermeter** | [**Verhältnis der MF- \_ MT- \_ Pixel \_ Seite \_**](mf-mt-pixel-aspect-ratio-attribute.md)      |



 

### <a name="mpeg2videoinfo"></a>MPEG2VIDEOINFO



| Member               | attribute                                                                       |
|----------------------|---------------------------------------------------------------------------------|
| **dwstarttimecode**  | [**Code der MF- \_ \_ MPEG- \_ \_ Startzeit \_**](mf-mt-mpeg-start-time-code-attribute.md) |
| **dwsequenceheader** | [**MF- \_ MT- \_ MPEG- \_ Sequenz \_ Header**](mf-mt-mpeg-sequence-header-attribute.md)  |
| **dwprofile**        | [**MF- \_ MT- \_ MPEG2- \_ Profil**](mf-mt-mpeg2-profile-attribute.md)                 |
| **dwlevel**          | [**MF- \_ MT- \_ \_ Ebene**](mf-mt-mpeg2-level-attribute.md)                     |
| **dwFlags**          | [**MF- \_ MT- \_ MPEG2- \_ Flags**](mf-mt-mpeg2-flags-attribute.md)                     |



 

## <a name="examples"></a>Beispiele

Der folgende Code füllt eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur aus einem Video Medientyp auf. Beachten Sie, dass diese Konvertierungen einige der Formatinformationen (Interlacing, Framerate, erweiterte Farbdaten) verlieren. Dies kann jedoch nützlich sein, wenn Sie beispielsweise eine Bitmap aus einem Videoframe speichern.


```C++
#include <dshow.h>
#include <dvdmedia.h>

// Converts a video type to a BITMAPINFO structure.
// The caller must free the structure by calling CoTaskMemFree.

// Note that this conversion loses some format information, including 
// interlacing, and frame rate.

HRESULT GetBitmapInfoHeaderFromMFMediaType(
    IMFMediaType *pType,            // Pointer to the media type.
    BITMAPINFOHEADER **ppBmih,      // Receives a pointer to the structure. 
    DWORD *pcbSize)                 // Receives the size of the structure.
{
    *ppBmih = NULL;
    *pcbSize = 0;

    GUID majorType = GUID_NULL;
    AM_MEDIA_TYPE *pmt = NULL;
    DWORD cbSize = 0;
    DWORD cbOffset = 0;
    BITMAPINFOHEADER *pBMIH = NULL;

    // Verify that this is a video type.
    HRESULT hr = pType->GetMajorType(&majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    if (majorType != MFMediaType_Video)
    {
        hr = MF_E_INVALIDMEDIATYPE;
        goto done;
    }

    hr = pType->GetRepresentation(AM_MEDIA_TYPE_REPRESENTATION, (void**)&pmt);
    if (FAILED(hr))
    {
        goto done;
    }

    if (pmt->formattype == FORMAT_VideoInfo)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER,bmiHeader));
    }
    else if (pmt->formattype == FORMAT_VideoInfo2)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER2,bmiHeader));
    }
    else
    {
        hr = MF_E_INVALIDMEDIATYPE; // Unsupported format type.
        goto done;
    }

    if (pmt->cbFormat - cbOffset < sizeof(BITMAPINFOHEADER))
    {
        hr = E_UNEXPECTED; // Bad format size. 
        goto done;
    }

    cbSize = pmt->cbFormat - cbOffset;

    pBMIH = (BITMAPINFOHEADER*)CoTaskMemAlloc(cbSize);
    if (pBMIH == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }
    
    CopyMemory(pBMIH, pmt->pbFormat + cbOffset, cbSize);
    
    *ppBmih = pBMIH;
    *pcbSize = cbSize;

done:
    if (pmt)
    {
        pType->FreeRepresentation(AM_MEDIA_TYPE_REPRESENTATION, pmt);
    }
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medientypen](media-types.md)
</dt> </dl>

 

 
