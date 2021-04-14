---
description: Mit diesem Filter wird das Video MPEG-1, MPEG-2, H. 264 decodiert.
ms.assetid: d8195c3a-97ac-4ad1-a097-18878c8fda6f
title: Microsoft MPEG-2-Video Decoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8460b5b554fffc8f0dd8679810e5ef3f42bcb004
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392429"
---
# <a name="microsoft-mpeg-2-video-decoder"></a>Microsoft MPEG-2-Video Decoder

Mit diesem Filter wird das Video MPEG-1, MPEG-2, H. 264 decodiert.

> [!Note]  
> Das Decodieren von H. 264-Video erfordert Windows 7.

 

> [!Note]  
> Dieser Filter wird auf IA-64-basierten Plattformen nicht unterstützt.

 

In der Registrierung lautet der Anzeige Name dieses Filters "Microsoft DTV-DVD Video Decoder".



Filter Informationen

Filter Schnittstellen

[**Iamdecodercaps**](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps)<br/> [**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**Icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

Eingabe-PIN-Medientypen

Video Eingabe-PIN:

-   MediaType \_ DVD- \_ verschlüsseltes \_ Paket, mediasubtype \_ MPEG2- \_ Video
-   MediaType \_ MPEG2- \_ , mediasubtype \_ MPEG2- \_ Video
-   MediaType \_ Video, mediasubtype \_ MPEG1Packet
-   MediaType \_ Video, mediasubtype \_ MPEG1Payload
-   MediaType- \_ Video, mediasubtype \_ MPEG2- \_ Video

Teilbild-Eingabe-PIN:<br/>

-   MediaType \_ DVD- \_ verschlüsseltes \_ Paket, mediasubtype \_ DVD- \_ subbild

Ab Windows 7 unterstützt die Videoeingabe-PIN auch die folgenden Eingabetypen:<br/>

-   **MediaType \_ Video**, **mediasubtype \_ AVC1**
-   **MediaType \_ Video**, **mediasubtype \_ H264**
-   **MediaType \_ Video**, **mediasubtype \_ H264**
-   **MediaType \_ Video**, **mediasubtype \_ X264**
-   **MediaType \_ Video**, **mediasubtype \_ x264**

Weitere Informationen finden Sie unter [H. 264-Video Typen](h-264-video-types.md) . Der Eingabe Medientyp kann sich dynamisch zwischen den Typen "MPEG2" und "H. 264" ändern.<br/>

PIN-Eingabeschnittstellen

[**Icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [**"Ikspropertyset"**](ikspropertyset.md)<br/> [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IMF Sample Protection**](/windows/win32/api/mfidl/nn-mfidl-imfsampleprotection)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**Iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Ausgabe-PIN-Medientypen

Video Ausgabe-PIN:

-   MediaType- \_ Video, DXVA \_ ModeMPEG2 \_ A (DXVA 1,0)
-   MediaType- \_ Video, DXVA \_ ModeMPEG2 \_ C (DXVA 1,0)
-   MediaType \_ Video, mediasubtype \_ I420 (Software Decodierung oder DXVA 2.0)
-   MediaType \_ Video, mediasubtype \_ NV12 (Software Decodierung oder DXVA 2.0)
-   MediaType \_ Video, mediasubtype \_ im YUY2 (Software Decodierung oder DXVA 2.0)
-   MediaType \_ Video, mediasubtype \_ IMC3 (nur DXVA 2.0)
-   MediaType \_ Video, mediasubtype \_ IMC4 (nur DXVA 2.0)
-   MediaType \_ Video, mediasubtype \_ S340 (nur DXVA 2.0)
-   MediaType \_ Video, mediasubtype \_ YV12 (nur DXVA 2.0)

Zeilen-21-Ausgabe-PIN:<br/>

-   MediaType \_ AUXLine21Data, mediasubtype \_ Line21 \_ goppacket

Ausgabepin für Teilbild:<br/>

-   MediaType \_ Video, mediasubtype \_ AI44
-   MediaType \_ Video, mediasubtype \_ ARGB32
-   MediaType \_ Video, mediasubtype \_ ARGB4444
-   MediaType- \_ Video, mediasubtype \_ ayuv

PIN-Schnittstellen

[**Iamvideoacceleratornotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (nur Videoausgabe-PIN)<br/> [**"Ikspropertyset"**](ikspropertyset.md)<br/> [**Imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**Iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> [**Ivpconfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig)<br/>

CLSID Filtern

**CLSID \_ CMPEG2VidDecoderDS** (in wmcodecdsp. h definiert)

Ausführbare Datei

msmpeg2vdec.dll

[Verdienst](merit.md)

**Verdienst \_ NORMAL** -1

[Filter Kategorie](filter-categories.md)

**CLSID \_ legacyamfiltercategory**



 

## <a name="remarks"></a>Bemerkungen

Dieser Filter verfügt über zwei Eingabe Pins und drei Ausgabe Pins.

Eingabe Pins:

-   Videoeingang
-   Teil Bild Eingabe

Ausgabe Pins:

-   Videoausgang
-   Zeile-21-Ausgabe
-   Teil Bild Ausgabe

Der Filter erstellt nicht die Ausgabe-PIN für das Teil Bild, es sei denn, die Videoeingabe-PIN ist mit einem MediaType-Dateityp mit **\_ DVD \_ verschlüsselt \_** .

### <a name="mpeg-12-support"></a>MPEG-1/2-Unterstützung

Für MPEG-1 und MPEG-2 unterstützt der Decoder die folgenden Formate:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Profile/Ebenen</td>
<td>Eine beliebige Kombination der folgenden Profile und Ebenen:<br/>
<ul>
<li>Profile: einfach, Main</li>
<li>Ebenen: niedrig, Main, hoch, hoch 1440</li>
</ul></td>
</tr>
<tr class="even">
<td>Chroma-Formate</td>
<td>4:2:0 Chroma</td>
</tr>
<tr class="odd">
<td>Maximale Auflösung</td>
<td>1920 × 1088 Pixel</td>
</tr>
<tr class="even">
<td>DXVA</td>
<td>Der Decoder unterstützt die DirectX-Video Beschleunigung (DXVA) Version 1 und Version 2.</td>
</tr>
</tbody>
</table>



 

Der Decoder unterstützt keine skalierbaren Bitstreams. Die Eingabe muss ein grundlegender Videostream sein.

Der Decoder unterstützt keine 4:2:2 Chroma-Formate.

### <a name="h264-support"></a>H. 264-Unterstützung

Für H. 264 unterstützt der Decoder die folgenden Formate:



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Profile/Ebenen    | Baseline, Main und High Profile, bis zu Ebene 5,1. (Ausführliche Informationen finden Sie in der ITU-T H. 264-Spezifikation.)                                                                                                                                                                          |
| Chroma-Formate     | 4:2:0 Chroma oder Monochrom                                                                                                                                                                                                                                                |
| Minimale Auflösung | 48 × 48 Pixel                                                                                                                                                                                                                                                            |
| Maximale Auflösung | 1920 × 1088 Pixel                                                                                                                                                                                                                                                        |
| DXVA               | Der Decoder unterstützt DXVA Version 2, aber nicht DXVA Version 1. DXVA-Decodierung wird nur für Haupt kompatible Bitstreams, Main und High Profile unterstützt. (Haupt-kompatible Baseline-Bitstreams werden als **Profil \_ IDC**= 66 und **eingeschränkter \_ set1- \_ Flag**= 1 definiert.) |



 

Der Decoder bietet keine Unterstützung für die Technologie zum Filmen von Folien.

Weitere Informationen zu den h. 264-Medientypen finden Sie unter [h. 264-Video Typen](h-264-video-types.md).

### <a name="codec-properties"></a>Codec-Eigenschaften

Die Eingabe-Pins unterstützen die folgenden Eigenschaften Sätze über " [**ikspropertyset**](ikspropertyset.md)":

-   [**Eigenschaften Satz für den DVD-Kopierschutz**](dvd-copy-protection-property-set.md)
-   [**Eigenschaft des DVD-Teil Bilds**](dvd-subpicture-property-set.md) (nur unter Bild-PIN)

Die Eingabe-Pins unterstützen die folgenden Eigenschaften über [**icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Eigenschaft                                                                  | Erforderlich      |
|---------------------------------------------------------------------------|---------------|
| [**Avdeccommoninputformat**](avdeccommoninputformat-property.md)         | Windows Vista |
| [**Avdecvideoinputscantype**](avdecvideoinputscantype-property.md)       | Windows Vista |
| [**Avdecvideopixelaspectratio**](avdecvideopixelaspectratio-property.md) | Windows Vista |



 

Der Filter unterstützt die folgenden Eigenschaften über [**icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Eigenschaft                                                                                | Erforderlich      |
|-----------------------------------------------------------------------------------------|---------------|
| [**Avdecmmcssclass**](avdecmmcss-property.md)                                          | Windows Vista |
| [**Avdecvideoacceleration \_ H264**](avdecvideoacceleration-h264-property.md)            | Windows 7     |
| [**Avdecvideoacceleration- \_ MPEG2**](avdecvideoacceleration-mpeg2-property.md)          | Windows 7     |
| [**Avdecvideodroppicwithmissingref**](avdecvideodroppicwithmissingref-property.md)     | Windows 7     |
| [**Avdecvideofastdecodemode**](avdecvideofastdecodemode.md)                            | Windows 7     |
| [**Avdecvideoimagesize**](avdecvideoimagesize.md)                                      | Windows 7     |
| [**Avdecvideosoftwaredeingeterlacemode**](avdecvideosoftwaredeinterlacemode-property.md) | Windows 7     |
| [**Avdecvideothumbnailgenerationmode**](avdecvideothumbnailgenerationmode-property.md) | Windows 7     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                                                                     |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[**DVD-Medientypen**](dvd-media-types.md)
</dt> <dt>

[H. 264-Video Typen](h-264-video-types.md)
</dt> </dl>

 

 
