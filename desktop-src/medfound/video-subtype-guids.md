---
description: Die folgenden Video-Untertyp-GUIDs sind in der Header Datei "mfapi. h" definiert. Um den Untertyp anzugeben, legen Sie das \_ Attribut "MF MT \_ SubType" für den Medientyp fest.
ms.assetid: 7dfd85e6-936e-4b78-a2cb-a5d59153e1c4
title: Video Untertyp-GUIDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38829480aed7372496fc196cc6c55d781b672a2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528556"
---
# <a name="video-subtype-guids"></a>Video Untertyp-GUIDs

Die folgenden Video-Untertyp-GUIDs sind in der Header Datei "mfapi. h" definiert. Um den Untertyp anzugeben, legen Sie das Attribut " [**MF \_ MT \_ SubType**](mf-mt-subtype-attribute.md) " für den Medientyp fest.

Wenn diese Untertypen verwendet werden, legen Sie das-Attribut des [MF- \_ \_ Haupt \_ Typs](mf-mt-major-type-attribute.md) auf **mfmediatype- \_ Video** fest.

-   [Nicht komprimierte RGB-Formate](#uncompressed-rgb-formats)
-   [YUV-Formate: 8-Bit und palettisiert](#yuv-formats-8-bit-and-palettized)
-   [YUV-Formate: 10-Bit und 16-Bit](#yuv-formats-10-bit-and-16-bit)
-   [Formate für Leuchtkraft und Tiefe](#luminance-and-depth-formats)
-   [Codierte Video Typen](#encoded-video-types)
-   [Erstellen von Untertyp-GUIDs aus fourccs-und D3DFORMAT-Werten](#creating-subtype-guids-from-fourccs-and-d3dformat-values)
-   [Zugehörige Themen](#related-topics)

## <a name="uncompressed-rgb-formats"></a>Nicht komprimierte RGB-Formate



| GUID                             | Beschreibung                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------|
| **MF-Format \_ RGB8**          | RGB, 8 Bits pro Pixel (BPP). (Gleiches Arbeitsspeicher Layout wie **D3DFMT \_ P8**.)                            |
| **MF-Format \_ RGB555**        | RGB 555, 16 bpp. (Gleiches Arbeitsspeicher Layout wie **D3DFMT \_ X1R5G5B5**.)                                  |
| **MF-Format \_ RGB565**        | RGB 565, 16 bpp. (Gleiches Arbeitsspeicher Layout wie **D3DFMT \_ R5G6B5**.)                                    |
| **MF-Format \_ RGB24**         | RGB, 24 bpp.                                                                                    |
| **MF-Format \_ RGB32**         | RGB, 32 bpp.                                                                                    |
| **MF-Format \_ ARGB32**        | RGB, 32 bpp mit Alphakanal.                                                                 |
| **MF-Format \_ A2R10G10B10**   | RGB, 10 BPP für jede Farbe und 2 BPP für Alpha. (Gleiches Arbeitsspeicher Layout wie **D3DFMT \_ A2B10G10R10**) |
| **MF-Format \_ A16B16G16R16F** | RGB, 16 bpp mit Alphakanal. (Gleiches Arbeitsspeicher Layout wie **D3DFMT \_ A16B16G16R16F**)               |



 

> [!Note]  
> Diese Untertypen stimmen nicht mit den untergeordneten RGB-typguids überein, die in vorherigen sdken wie z. b. DirectShow verwendet wurden.

 

## <a name="yuv-formats-8-bit-and-palettized"></a>YUV-Formate: 8-Bit und palettisiert



| GUID                    | Format | Stichproben | Gepackt oder planare | Bits pro Kanal |
|-------------------------|--------|----------|------------------|------------------|
| **MF-Format \_ AI44** | AI44   | 4:4:4    | Stop           | Das Paletten       |
| **MF-Format ( \_ ayuv)** | Ayuv   | 4:4:4    | Stop           | 8                |
| **MF-Format \_ I420** | I420   | 4:2:0    | Planare           | 8                |
| **MF-Format ( \_ IYUV)** | IYUV   | 4:2:0    | Planare           | 8                |
| **MF-Format \_ NV11** | NV11   | 4:1:1    | Planare           | 8                |
| **MF-Format \_ NV12** | NV12   | 4:2:0    | Planare           | 8                |
| **MF-Format ( \_ UYVY)** | UYVY   | 4:2:2    | Stop           | 8                |
| **MF-Format \_ im y41p** | Im y41p   | 4:1:1    | Stop           | 8                |
| **MF-Format \_ Y41T** | Y41T   | 4:1:1    | Stop           | 8                |
| **MF-Format \_ Y42T** | Y42T   | 4:2:2    | Stop           | 8                |
| **MF-Format \_ im YUY2** | Im YUY2   | 4:2:2    | Stop           | 8                |
| **MF-Format \_ YVU9** | YVU9   | 8:4:4    | Planare           | 9                |
| **MF-Format \_ YV12** | YV12   | 4:2:0    | Planare           | 8                |
| **Mfvideoformat \_ yvyu** | Im yvyu   | 4:2:2    | Stop           | 8                |



 

Die empfohlenen YUV-Formate werden im Thema [Empfohlene 8-Bit-YUV-Formate für Video Rendering](recommended-8-bit-yuv-formats-for-video-rendering.md)ausführlich beschrieben.

> [!Note]  
> I420 und IYUV verfügen über das gleiche Layout im Arbeitsspeicher, Ihnen werden jedoch unterschiedliche typguids zugewiesen. Die Untertyp-GUIDs entsprechen den FourCC-Codes ' I420 ' und ' IYUV '; Weitere Informationen finden Sie im [Video fourccs](video-fourccs.md) .

 

## <a name="yuv-formats-10-bit-and-16-bit"></a>YUV-Formate: 10-Bit und 16-Bit



| GUID                    | Format | Stichproben | Gepackt oder planare | Bits pro Kanal |
|-------------------------|--------|----------|------------------|------------------|
| **MF-Format \_ P010** | P010   | 4:2:0    | Planare           | 10               |
| **MF-Format \_ P016** | P016   | 4:2:0    | Planare           | 16               |
| **MF-Format \_ P210** | P210   | 4:2:2    | Planare           | 10               |
| **MF-Format \_ P216** | P216   | 4:2:2    | Planare           | 16               |
| **MF-Format \_ V210** | v210   | 4:2:2    | Stop           | 10               |
| **MF-Format \_ v216** | v216   | 4:2:2    | Stop           | 16               |
| **MF-Format \_ v410** | v40    | 4:4:4    | Stop           | 10               |
| **MF-Format \_ Y210** | Y210   | 4:2:2    | Stop           | 10               |
| **MF-Format \_ Y216** | Y216   | 4:2:2    | Stop           | 16               |
| **MF-Format \_ Y410** | Y40    | 4:4:4    | Stop           | 10               |
| **MF-Format \_ Y416** | Y416   | 4:4:4    | Stop           | 16               |



 

Weitere Informationen zu diesen Formaten finden Sie unter [10-Bit-und 16-Bit-YUV-Video Formate](10-bit-and-16-bit-yuv-video-formats.md).

## <a name="luminance-and-depth-formats"></a>Formate für Leuchtkraft und Tiefe



| GUID                   | Beschreibung                                                          |
|------------------------|----------------------------------------------------------------------|
| **MF-Format- \_ L8**  | nur 8-Bit-Leuchtkraft. (BPP). (Gleiches Arbeitsspeicher Layout wie **D3DFMT \_ L8**.) |
| **MF-Format \_ L16** | nur 16-Bit-Leuchtkraft. (Gleiches Arbeitsspeicher Layout wie **D3DFMT \_ L16**.)      |
| **MF-Format \_ D16** | 16-Bit-z-Puffer Tiefe. (Gleiches Arbeitsspeicher Layout wie **D3DFMT \_ D16**.)      |



 

## <a name="encoded-video-types"></a>Codierte Video Typen



| GUID                        | FOURCC         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                 |
|-----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MF-Format \_ DV25**     | 'dv25'         | DVCPro 25 (525-60 oder 625-50).                                                                                                                                                                                                                                                                               |
| **MF-Format \_ DV50**     | 'dv50'         | DVCPRO 50 (525-60 oder 625-50).                                                                                                                                                                                                                                                                               |
| **MF-Format ( \_ DVC)**      | DVC         | DVC/DV-Video.                                                                                                                                                                                                                                                                                               |
| **MF-Format \_ DVH1**     | 'dvh1'         | DVCPRO 100 (1080/60i, 1080/50i oder 720/60p).                                                                                                                                                                                                                                                                |
| **MF-Format ( \_ dvhd)**     | "dvhd"         | HD-dvcr (1125-60 oder 1250-50).                                                                                                                                                                                                                                                                               |
| **MF-Format ( \_ DVSD)**     | "DVSD"         | SDL-dvcr (525-60 oder 625-50).                                                                                                                                                                                                                                                                                |
| **MF-Format \_ dvsl**     | "dvsl"         | SD-dvcr (525-60 oder 625-50).                                                                                                                                                                                                                                                                                 |
| **MF-Format \_ H263**     | 'H263'         | H. 263-Video.                                                                                                                                                                                                                                                                                                |
| **MF-Format \_ H264**     | H264         | H. 264-Video.<br/> Medien Beispiele enthalten H. 264-bitstreamdaten mit Start Codes, die überlappende SPS/PPS verfügen. Jedes Beispiel enthält ein umfassendes Bild, entweder ein Feld oder einen Frame.<br/>                                                                                                       |
| **MF-Format \_ H265**     | 'H265'         | H. 265-Video.                                                                                                                                                                                                                                                                                                |
| **MF-Format \_ H264 \_ es** | Nicht verfügbar | H. 264-elementare Datenstrom.<br/> Dieser Medientyp ist mit dem **MF-Format \_ H264** identisch, mit dem Unterschied, dass die Medien Beispiele einen fragmentierten H. 264-Bitstream enthalten. Jedes Beispiel kann ein partielles Bild enthalten. mehrere komplette Bilder; oder ein oder mehrere vollständige Bilder und ein partielles Bild.<br/>           |
| **MF-Format \_ hevc**     | HEVC         | Das hevc-Hauptprofil und das Hauptprofil Profil.<br/> Jedes Beispiel enthält ein umfassendes Bild.<br/> Wird in Windows 8.1 und höher unterstützt. Das Hauptprofil von hevc und das Hauptprofil für die Bild Profile. <br/>                                                              |
| **MF-Format \_ hevc \_ es** | "HEVs"         | Dieser Medientyp ist mit **MF-Format \_ hevc** identisch, mit dem Unterschied, dass die Medien Beispiele einen fragmentierten hevc-Bitstream enthalten. Jedes Beispiel kann ein partielles Bild enthalten. mehrere komplette Bilder; oder ein oder mehrere vollständige Bilder und ein partielles Bild.<br/> Wird in Windows 8.1 und höher unterstützt.<br/> |
| **MF-Format \_ M4S2**     | X 4s2 '         | MPEG-4 Part 2-Video.                                                                                                                                                                                                                                                                                        |
| **MF-Format ( \_ mjpg)**     | "Mjpg"         | Motion JPEG.                                                                                                                                                                                                                                                                                                |
| **MF-Format \_ MP43**     | 'MP43'         | Microsoft MPEG 4 Codec Version 3. Dieser Codec wird nicht mehr unterstützt.                                                                                                                                                                                                                                        |
| **MF-Format \_ MP4 Bitrate**     | MP4 Bitrate         | ISO MPEG 4 Codec Version 1.                                                                                                                                                                                                                                                                                 |
| **MF-Format \_ MP4V**     | MP4V         | MPEG-4 Part 2-Video.                                                                                                                                                                                                                                                                                        |
| **MF-Format ( \_ MPEG2)**    | Nicht verfügbar | MPEG-2-Video. (Entspricht dem **\_ \_ Video mediasubtype MPEG2** in DirectShow.)                                                                                                                                                                                                                                 |
| **MF-Format \_ VP80**     | 'MPG1'         | VP8-Video.                                                                                                                                                                                                                                                                                                  |
| **MF-Format \_ VP90**     | 'MPG1'         | VP9-Video.                                                                                                                                                                                                                                                                                                  |
| **MF-Format \_ MPG1**     | 'MPG1'         | MPEG-1-Video.                                                                                                                                                                                                                                                                                               |
| **MF-Format \_ MSS1**     | 'MSS1'         | Windows Media-Bildschirm Codec Version 1.                                                                                                                                                                                                                                                                       |
| **MF-Format \_ MSS2**     | 'MSS2'         | Windows Media Video 9-Bildschirm Codec.                                                                                                                                                                                                                                                                         |
| **MF-Format \_ WMV1**     | 'WMV1'         | Windows Media Video Codec Version 7.                                                                                                                                                                                                                                                                        |
| **MF-Format \_ WMV2**     | 'WMV2'         | Windows Media Video 8-Codec.                                                                                                                                                                                                                                                                                |
| **MF-Format \_ WMV3**     | 'WMV3'         | Windows Media Video 9-Codec.                                                                                                                                                                                                                                                                                |
| **MF-Format \_ WVC1**     | 'WVC1'         | SMPTE 421m ("VC-1").                                                                                                                                                                                                                                                                                        |
| **MF-Format \_ 420o**     | "420o"         | 8-Bit pro Kanal planare YUV 4:2:0 Video.                                                                                                                                                                                                                                                                   |
| **MF-Format \_ AV1**     | 'AV01'         | AV1-Video.                                                                                                                                                                                                                                                                                                |



 

## <a name="creating-subtype-guids-from-fourccs-and-d3dformat-values"></a>Erstellen von Untertyp-GUIDs aus fourccs-und D3DFORMAT-Werten

Video Formate werden häufig durch fourccs-oder **D3DFORMAT** -Werte dargestellt. Ein Bereich von GUIDs ist für die Darstellung dieser Werte als Untertypen reserviert. Diese GUIDs verfügen über das Format `XXXXXXXX-0000-0010-8000-00AA00389B71` , wobei `XXXXXXXX` der 4-Byte-FourCC-Code oder **D3DFORMAT** -Wert ist.

Wenn einem Videoformat ein FourCC-oder **D3DFORMAT** -Wert zugeordnet ist, können Sie die entsprechende Untertyp-GUID wie folgt erstellen: beginnen Sie mit der Konstanten **MF Videoformat- \_ Basis** , und ersetzen Sie das erste **DWORD** der GUID durch das Video FourCC oder den **D3DFORMAT** -Wert. Zu diesem Zweck können Sie das [**\_ \_ GUID-Makro "MediaType" definieren**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) .

> [!Note]  
> DirectShow verwendet dieses System auch für die meisten Video Untertypen, jedoch nicht für nicht komprimierte RGB-Formate. Aus diesem Grund stimmen die RGB-Untertypen in DirectShow nicht mit den RGB-Untertypen in Media Foundation.

 

Die **D3DFORMAT** -Enumeration wird in der Header Datei d3d9types. h definiert. In der folgenden Tabelle werden die gängigsten nicht komprimierten RGB-Formate und der entsprechende **D3DFORMAT** -Wert angezeigt.



| RGB-Format                                                              | **D3DFORMAT** -Wert     |
|-------------------------------------------------------------------------|-------------------------|
| 32-Bit-RGB                                                              | **D3DFMT \_ X8R8G8B8**    |
| 32-Bit RGB mit Alphakanal                                           | **D3DFMT \_ A8R8G8B8**    |
| 24-Bit-RGB                                                              | **D3DFMT \_ R8G8B8**      |
| RGB 555 (16-Bit RGB)                                                    | **D3DFMT \_ X1R5G5B5**    |
| RGB 555 mit Alphakanal                                              | **D3DFMT \_ A4R4G4B4**    |
| RGB 565 (16-Bit RGB)                                                    | **D3DFMT \_ R5G6B5**      |
| 8-Bit-palettisierte RGB                                                    | **D3DFMT \_ P8**          |
| A2 R10 G10 B10 (32-Bit RGB mit Alphakanal, 10 Bits pro RGB-Kanal) | **D3DFMT \_ A2R10G10B10** |
| A2 B10 G10 (32-Bit RGB mit Alphakanal, 10 Bits pro RGB-Kanal) | **D3DFMT \_ A2B10G10R10** |
| nur 8-Bit-Leuchtkraft.                                                   | **D3DFMT \_ L8**          |
| nur 16-Bit-Leuchtkraft.                                                  | **D3DFMT \_ L16**         |
| 16-Bit-z-Puffer Tiefe                                                   | **D3DFMT \_ D16**         |



 

Weitere Informationen zu fourccs finden Sie unter [Video fourccs](video-fourccs.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientyp-GUIDs](media-type-guids.md)
</dt> <dt>

[**MF- \_ MT- \_ Untertyp**](mf-mt-subtype-attribute.md)
</dt> <dt>

[Medientypen](media-types.md)
</dt> <dt>

[Video Medientypen](video-media-types.md)
</dt> </dl>

 

 




