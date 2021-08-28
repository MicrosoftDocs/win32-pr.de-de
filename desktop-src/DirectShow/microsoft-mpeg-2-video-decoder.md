---
description: Dieser Filter decodiert MPEG-1,MPEG-2, H.264-Video.
ms.assetid: d8195c3a-97ac-4ad1-a097-18878c8fda6f
title: Microsoft MPEG-2 Video Decoder (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4afdd9609124ba1057f597c4b7a907654c62a321
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982193"
---
# <a name="microsoft-mpeg-2-video-decoder"></a>Microsoft MPEG-2-Videodecoder

Dieser Filter decodiert MPEG-1,MPEG-2, H.264-Video.

> [!Note]  
> Die Decodierung von H.264-Videos erfordert Windows 7.

 

> [!Note]  
> Dieser Filter wird auf IA-64-basierten Plattformen nicht unterstützt.

 

In der Registrierung lautet der Anzeigename dieses Filters "Microsoft DTV-DVD Video Decoder".



Filterinformationen

Filterschnittstellen

[**IAMDecoderCaps**](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps)<br/> [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

Eingabepinmedientypen

Videoeingabepin:

-   MEDIATYPE \_ DVD \_ ENCRYPTED \_ PACK, MEDIASUBTYPE \_ MPEG2 \_ VIDEO
-   MEDIATYPE \_ MPEG2 \_ PES, MEDIASUBTYPE \_ MPEG2 \_ VIDEO
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ MPEG1Packet
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ MPEG1Payload
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ MPEG2 \_ VIDEO

Eingabepin für Unteraufdrückung:<br/>

-   MEDIATYPE \_ DVD \_ ENCRYPTED \_ PACK, MEDIASUBTYPE \_ DVD \_ SUBPICTURE

Ab Windows 7 unterstützt der Videoeingabepin auch die folgenden Eingabetypen:<br/>

-   **MEDIATYPE \_ Video,** **MEDIASUBTYPE \_ AVC1**
-   **MEDIATYPE \_ Video,** **MEDIASUBTYPE \_ H264**
-   **MEDIATYPE \_ Video,** **MEDIASUBTYPE \_ h264**
-   **MEDIATYPE \_ Video,** **MEDIASUBTYPE \_ X264**
-   **MEDIATYPE \_ Video,** **MEDIASUBTYPE \_ x264**

Weitere Informationen finden Sie unter [H.264-Videotypen.](h-264-video-types.md) Der Eingabemedientyp kann sich dynamisch zwischen MPEG2- und H.264-Typen ändern.<br/>

Eingabe-Pin-Schnittstellen

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**KONSenssampleProtection**](/windows/win32/api/mfidl/nn-mfidl-imfsampleprotection)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Medientypen des Ausgabepins

Videoausgabe-PIN:

-   MEDIATYPE \_ Video, DXVA \_ ModeMPEG2 \_ A (DXVA 1.0)
-   MEDIATYPE \_ Video, DXVA \_ ModeMPEG2 \_ C (DXVA 1.0)
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ I420 (Softwaredecode oder DXVA2.0)
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ NV12 (Softwaredecode oder DXVA2.0)
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ YUY2 (Softwaredecode oder DXVA2.0)
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ IMC3 (nur DXVA2.0)
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ IMC4 (nur DXVA2.0)
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ S340 (nur DXVA2.0)
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ YV12 (nur DXVA2.0)

Zeilen-21-Ausgabepin:<br/>

-   MEDIATYPE \_ AUXLine21Data, MEDIASUBTYPE \_ Line21 \_ GOPPacket

Ausgabepin für Unterausdrückung:<br/>

-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ AI44
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ ARGB32
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ ARGB4444
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ AYUV

Ausgabe-Pin-Schnittstellen

[**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (nur Videoausgabe-PIN)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig)<br/>

Filtern von CLSID

**CLSID \_ CMPEG2VidDecoderDS** (definiert in wmcodecdsp.h)

Ausführbare Datei

msmpeg2vdec.dll

[Verdienst](merit.md)

**VERERZUNG \_ NORMAL** – 1

[Filterkategorie](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Bemerkungen

Dieser Filter verfügt über zwei Eingabepins und drei Ausgabepins.

Eingabepins:

-   Videoeingang
-   Eingabe der Unterausdrückung

Ausgabepins:

-   Videoausgang
-   Line-21-Ausgabe
-   Subpicture-Ausgabe

Der Filter erstellt den Bildausgabepin nur dann, wenn der Videoeingabepin mit einem **MEDIATYPE \_ DVD ENCRYPTED \_ \_ PACK-Medientyp** verbunden ist.

### <a name="mpeg-12-support"></a>MPEG-1/2-Unterstützung

Für MPEG-1 und MPEG-2 unterstützt der Decoder die folgenden Formate:




| Bezeichnung | Wert |
|--------|-------|
| Profile/Ebenen | Eine beliebige Kombination der folgenden Profile und Ebenen:<br /><ul><li>Profile: Simple, Main</li><li>Ebenen: Niedrig, Haupt, Hoch, Hoch 1440</li></ul> | 
| Formatformat | 4:2:0 Uhr | 
| Maximale Auflösung | 1920 × 1088 Pixel | 
| DXVA | Der Decoder unterstützt DirectX Video Acceleration (DXVA) Version 1 und Version 2. | 




 

Der Decoder unterstützt keine skalierbaren Bitstreams. Die Eingabe muss ein elementarer Videostream sein.

Der Decoder unterstützt keine 4:2:2-Formatformate.

### <a name="h264-support"></a>H.264-Unterstützung

Für H.264 unterstützt der Decoder die folgenden Formate:



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Profile/Ebenen    | Baseline-, Main- und High-Profile bis Ebene 5.1. (Weitere Informationen finden Sie unter ITU-T H.264-Spezifikation.)                                                                                                                                                                          |
| Formatformat "Format"     | 4:2:0 monofarbig oder monofarbig                                                                                                                                                                                                                                                |
| Minimale Auflösung | 48 × 48 Pixel                                                                                                                                                                                                                                                            |
| Maximale Auflösung | 1920 × 1088 Pixel                                                                                                                                                                                                                                                        |
| DXVA               | Der Decoder unterstützt DXVA Version 2, aber nicht DXVA Version 1. DXVA-Decodierung wird nur für Main-kompatible Baseline-, Main- und High Profile-Bitstreams unterstützt. (Main-kompatible Baselinebitstreams sind als Profil **\_ idc**=66 und **constrained \_ set1 \_ flag**=1 definiert.) |



 

Der Decoder unterstützt keine Film grain-Technologie.

Informationen zu den H.264-Medientypen finden Sie unter [H.264-Videotypen.](h-264-video-types.md)

### <a name="codec-properties"></a>Codec-Eigenschaften

Die Eingabepins unterstützen die folgenden Eigenschaftensätze über [**IKsPropertySet:**](ikspropertyset.md)

-   [**DVD Copy Protection-Eigenschaftensatz**](dvd-copy-protection-property-set.md)
-   [**DVD Subpicture Property Set**](dvd-subpicture-property-set.md) (nur Subpicture Pin)

Die Eingabepins unterstützen die folgenden Eigenschaften über [**ICodecAPI:**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)



| Eigenschaft                                                                  | Erforderlich      |
|---------------------------------------------------------------------------|---------------|
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md)         | Windows Vista |
| [**AVDecVideoInputScanType**](avdecvideoinputscantype-property.md)       | Windows Vista |
| [**AVDecVideoPixelAspectRatio**](avdecvideopixelaspectratio-property.md) | Windows Vista |



 

Der Filter unterstützt die folgenden Eigenschaften über [**ICodecAPI:**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)



| Eigenschaft                                                                                | Erforderlich      |
|-----------------------------------------------------------------------------------------|---------------|
| [**AVDecMmcssClass**](avdecmmcss-property.md)                                          | Windows Vista |
| [**AVDecVideoAcceleration \_ H264**](avdecvideoacceleration-h264-property.md)            | Windows 7     |
| [**AVDecVideoAcceleration \_ MPEG2**](avdecvideoacceleration-mpeg2-property.md)          | Windows 7     |
| [**AVDecVideoDropPicWithMissingRef**](avdecvideodroppicwithmissingref-property.md)     | Windows 7     |
| [**AVDecVideoFastDecodeMode**](avdecvideofastdecodemode.md)                            | Windows 7     |
| [**AVDecVideoImageSize**](avdecvideoimagesize.md)                                      | Windows 7     |
| [**AVDecVideoSoftwareDeinterlaceMode**](avdecvideosoftwaredeinterlacemode-property.md) | Windows 7     |
| [**AVDecVideoThumbnailGenerationMode**](avdecvideothumbnailgenerationmode-property.md) | Windows 7     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                                                                     |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[**DVD-Medientypen**](dvd-media-types.md)
</dt> <dt>

[H.264-Videotypen](h-264-video-types.md)
</dt> </dl>

 

 
