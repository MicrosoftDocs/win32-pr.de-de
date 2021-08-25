---
description: Medientypkonvertierungen
ms.assetid: 6aee18b8-79b1-47fb-816f-d1c2c77b3a03
title: Medientypkonvertierungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aacb4b7209ec96493c7b32c9de15ecf55071d7fb2861eda86f6f38fed8566e71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827470"
---
# <a name="media-type-conversions"></a>Medientypkonvertierungen

Gelegentlich ist es erforderlich, zwischen Media Foundation Medientypen und den älteren Medientypstrukturen aus DirectShow oder dem Windows Media Format SDK zu konvertieren.

### <a name="from-a-format-structure-to-a-media-foundation-type"></a>Von einer Formatstruktur zu einem Media Foundation Typ

Die folgenden Funktionen initialisieren einen Media Foundation Medientyp aus einer Formatstruktur. Diese Funktionen sind auch nützlich, wenn ein Datenstrom oder ein Dateiheader eine Formatstruktur enthält. Beispielsweise enthält der Dateiheader für WAVE-Audiodateien eine [**WAVEFORMATEX-Struktur.**](/previous-versions/dd757713(v=vs.85))



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
<td><a href="/windows/win32/api/strmif/ns-strmif-am_media_type"><strong>AM_MEDIA_TYPE</strong></a> (DirectShow)<br/> <a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type"><strong>DMO_MEDIA_TYPE</strong></a> (DirectX-Medienobjekte) <br/> <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type"><strong>WM_MEDIA_TYPE</strong></a> (Windows Media Format SDK) <br/>
<blockquote>
[!Note]<br />
Diese Strukturen sind gleichwertig.
</blockquote>
<br/> <br/></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromammediatype"><strong>MFInitMediaTypeFromAMMediaType</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader"><strong>BITMAPINFOHEADER</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatevideomediatypefrombitmapinfoheaderex"><strong>MFCreateVideoMediaTypeFromBitMapInfoHeaderEx</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat"><strong>MFVIDEOFORMAT</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommfvideoformat"><strong>MFInitMediaTypeFromMFVideoFormat</strong></a></td>
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
<td><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader"><strong>VIDEOINFOHEADER</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader"><strong>MFInitMediaTypeFromVideoInfoHeader</strong></a></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/dd757713(v=vs.85)"><strong>WAVEFORMATEX</strong></a> oder <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)"> <strong>WAVEFORMATEXTENSIBLE</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex"><strong>MFInitMediaTypeFromWaveFormatEx</strong></a></td>
</tr>
</tbody>
</table>



 

### <a name="from-a-media-foundation-type-to-a-format-structure"></a>Von einem Media Foundation zu einer Formatstruktur

Die folgenden Funktionen erstellen oder initialisieren eine Formatstruktur aus einem Media Foundation Medientyp.



| Funktion                                                                             | Zielstruktur                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BESCHRIFTUNGstyp::GetRepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation)            | [**AM \_ \_MEDIENTYP,**](/windows/win32/api/strmif/ns-strmif-am_media_type) [**MFVIDEOFORMAT,**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)oder [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) |
| [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype)     | [**\_ \_ AM-MEDIENTYP**](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |
| [**MFCreateMFVideoFormatFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemfvideoformatfrommfmediatype) | [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat)                                                                                                                                              |
| [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype)   | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) oder [ **WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))                                                                                    |
| [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype)         | [**\_ \_ AM-MEDIENTYP**](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |



 

## <a name="format-mappings"></a>Formatzuordnungen

In den folgenden Tabellen sind die Media Foundation aufgeführt, die verschiedenen Formatstrukturen entsprechen. Nicht alle diese Attribute können direkt übersetzt werden. Um Konvertierungen durchzuführen, sollten Sie die im vorherigen Abschnitt aufgeführten Funktionen verwenden. diese Tabellen werden hauptsächlich als Referenz bereitgestellt.

### <a name="am_media_type"></a>\_ \_ AM-MEDIENTYP



| Member                   | attribute                                                                            |
|--------------------------|--------------------------------------------------------------------------------------|
| **bTemporalCompression** | [**MF \_ MT \_ ALL \_ SAMPLES \_ INDEPENDENT**](mf-mt-all-samples-independent-attribute.md) |
| **bFixedSizeSamples**    | [**BEISPIELE FÜR MF \_ MT \_ MIT FESTER \_ \_ GRÖßE**](mf-mt-fixed-size-samples-attribute.md)           |
| **lSampleSize**          | [**MF \_ \_ MT-STICHPROBENGRÖßE \_**](mf-mt-sample-size-attribute.md)                          |



 

### <a name="waveformatex-waveformatextensible"></a>WAVEFORMATEX, WAVEFORMATEXTENSIBLE



| Member                  | attribute                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **wFormatTag**          | [**MF \_ \_ MT-UNTERTYP**](mf-mt-subtype-attribute.md)<br/> Wenn **wFormatTag** WAVE \_ FORMAT \_ EXTENSIBLE ist, befindet sich der Untertyp im **SubFormat-Member.**<br/> |
| **nChannels**           | [**MF \_ MT AUDIO \_ \_ \_ NUM-KANÄLE**](mf-mt-audio-num-channels-attribute.md)                                                                                                |
| **nSamplesPerSec**      | [**MF \_ \_ MT-AUDIOBEISPIELE \_ \_ PRO \_ SEKUNDE**](mf-mt-audio-samples-per-second-attribute.md)                                                                                   |
| **nAvgBytesPerSec**     | [**MF \_ MT \_ AUDIO \_ AVG \_ BYTES \_ PER \_ SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md)                                                                              |
| **nBlockAlign**         | [**MF MT AUDIO BLOCK ALIGNMENT (MF \_ \_ MT-AUDIOBLOCKAUSRICHTUNG) \_ \_**](mf-mt-audio-block-alignment-attribute.md)                                                                                          |
| **wBitsPerSample**      | [**MF \_ \_ MT-AUDIOBITS \_ \_ PRO \_ BEISPIEL**](mf-mt-audio-bits-per-sample-attribute.md)                                                                                         |
| **wValidBitsPerSample** | [**GÜLTIGE MF \_ \_ MT-AUDIOBITS \_ \_ PRO \_ \_ BEISPIEL**](mf-mt-audio-valid-bits-per-sample-attribute.md)                                                                            |
| **wSamplesPerBlock**    | [**MF \_ \_ MT-AUDIOBEISPIELE \_ \_ PRO \_ BLOCK**](mf-mt-audio-samples-per-block-attribute.md)                                                                                     |
| **dwChannelMask**       | [**MF \_ MT \_ AUDIO \_ CHANNEL \_ MASK**](mf-mt-audio-channel-mask-attribute.md)                                                                                                |
| **SubFormat**           | [**MF \_ \_ MT-UNTERTYP**](mf-mt-subtype-attribute.md)                                                                                                                        |
| Zusätzliche Daten              | [**MF \_ \_ MT-BENUTZERDATEN \_**](mf-mt-user-data-attribute.md)                                                                                                                   |



 

### <a name="videoinfoheader-videoinfoheader2"></a>VIDEOINFOHEADER, VIDEOINFOHEADER2



| Member                                         | attribute                                                                                                                                                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwBitRate**                                  | [**MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md)                                                                                                                                                                                      |
| **dwBitErrorRate**                             | [**MF \_ MT \_ AVG \_ BIT \_ ERROR \_ RATE**](mf-mt-avg-bit-error-rate-attribute.md)                                                                                                                                                                      |
| **AvgTimePerFrame**                            | [**MF \_ MT \_ FRAME \_ RATE;**](mf-mt-frame-rate-attribute.md)Verwenden Sie [**MFAverageTimePerFrameToFrameRate,**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) um diesen Wert zu berechnen.                                                                             |
| **dwInterlaceFlags**                           | [**MF \_ MT \_ INTERLACE-MODUS \_**](mf-mt-interlace-mode-attribute.md)                                                                                                                                                                                |
| **dwCopyProtectFlags**                         | Keine definierte Entsprechung                                                                                                                                                                                                                            |
| **dwPictAspectRatioX**, **dwPictAspectRatioY** | [**MF \_ MT \_ PIXEL \_ ASPECT \_ RATIO;**](mf-mt-pixel-aspect-ratio-attribute.md)muss das Bild-Seitenverhältnis in das Bild-Seitenverhältnis konvertieren.                                                                                                      |
| **dwControlFlags**                             | [**MF \_ MT \_ \_ PAD-STEUERELEMENTFLAGS \_**](mf-mt-pad-control-flags-attribute.md). Wenn das **FLAG AMCONTROL \_ COLORINFO \_ PRESENT** vorhanden ist, legen Sie die erweiterten Farbattribute fest, die unter [Erweiterte Farbinformationen beschrieben werden.](extended-color-information.md) |
| **bmiHeader.biWidth**, **bmiHeader.biHeight**  | [**MF \_ MT \_ FRAME \_ SIZE**](mf-mt-frame-size-attribute.md)                                                                                                                                                                                        |
| **bmiHeader.biBitCount**                       | Implizit im Untertyp ([**MF \_ MT \_ SUBTYPE**](mf-mt-subtype-attribute.md)).                                                                                                                                                                    |
| **bmiHeader.biCompression**                    | Implizit im Untertyp.                                                                                                                                                                                                                         |
| **bmiHeader.biSizeImage**                      | [**MF \_ \_ MT-STICHPROBENGRÖßE \_**](mf-mt-sample-size-attribute.md)                                                                                                                                                                                      |
| Paletteninformationen                            | [**MF \_ MT \_ PALETTE**](mf-mt-palette-attribute.md)                                                                                                                                                                                               |



 

Die folgenden Attribute können aus der [**VIDEOINFOHEADER-**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) oder [**VIDEOINFOHEADER2-Struktur**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) abgeleitet werden, erfordern jedoch auch kenntnisse der Formatdetails. Beispielsweise haben verschiedene YUV-Formate unterschiedliche Anforderungen.

-   [**MF \_ MT \_ DEFAULT \_ STRIDE**](mf-mt-default-stride-attribute.md)
-   [**MF \_ MT \_ MINIMUM \_ DISPLAY \_ APERTURE**](mf-mt-minimum-display-aperture-attribute.md)
-   [**MF \_ MT \_ PAN \_ SCAN \_ APERTURE**](mf-mt-pan-scan-aperture-attribute.md)

### <a name="mpeg1videoinfo"></a>MPEG1VIDEOINFO



| Member                                   | attribute                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------|
| **dwStartTimeCode**                      | [**MF \_ MT \_ MPEG \_ START \_ TIME \_ CODE**](mf-mt-mpeg-start-time-code-attribute.md) |
| **bSequenceHeader**                      | [**MF \_ MT \_ MPEG \_ SEQUENCE \_ HEADER**](mf-mt-mpeg-sequence-header-attribute.md)  |
| **biXPelsPerMeter**, **biYPelsPerMeter** | [**MF \_ MT PIXEL \_ \_ \_ SEITENVERHÄLTNIS**](mf-mt-pixel-aspect-ratio-attribute.md)      |



 

### <a name="mpeg2videoinfo"></a>MPEG2VIDEOINFO



| Member               | attribute                                                                       |
|----------------------|---------------------------------------------------------------------------------|
| **dwStartTimeCode**  | [**MF \_ MT \_ MPEG \_ START \_ TIME \_ CODE**](mf-mt-mpeg-start-time-code-attribute.md) |
| **dwSequenceHeader** | [**MF \_ MT \_ MPEG \_ SEQUENCE \_ HEADER**](mf-mt-mpeg-sequence-header-attribute.md)  |
| **dwProfile**        | [**MF \_ MT \_ \_ MPEG2-PROFIL**](mf-mt-mpeg2-profile-attribute.md)                 |
| **dwLevel**          | [**MF \_ MT \_ MPEG2 \_ LEVEL**](mf-mt-mpeg2-level-attribute.md)                     |
| **dwFlags**          | [**MF \_ MT \_ \_ MPEG2-FLAGS**](mf-mt-mpeg2-flags-attribute.md)                     |



 

## <a name="examples"></a>Beispiele

Der folgende Code füllt eine [**BITMAPINFOHEADER-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) aus einem Videomedientyp aus. Beachten Sie, dass bei diesen Konvertierungen einige der Formatinformationen (Interlacing, Framerate, erweiterte Farbdaten) verloren geht. Dies kann jedoch hilfreich sein, wenn Sie z. B. eine Bitmap aus einem Videoframe speichern.


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

 

 
