---
title: Komprimierte Medien Untertypen
description: Komprimierte Medien Untertypen
ms.assetid: 0ed6b4e8-6450-4484-90d6-efa2f9101782
keywords:
- Windows Media-Format-SDK, Medientypen
- Advanced Systems Format (ASF), Medientypen
- ASF (Advanced Systems Format), Medientypen
- Windows Media-Format-SDK, komprimierte Medien Untertypen
- Advanced Systems Format (ASF), komprimierte Medien Untertypen
- ASF (Advanced Systems Format), komprimierte Medien Untertypen
- Medientypen, komprimierte Medien Untertypen
- komprimierte Medien Untertypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d92d192d04257f0375a618dda05aa97fd3f344b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100646"
---
# <a name="compressed-media-subtypes"></a>Komprimierte Medien Untertypen

In der folgenden Tabelle sind die Untertypen für komprimierte Medien aufgeführt. Diese Typen werden verwendet, um komprimierte Datenströme in einer Datei zu identifizieren. Wenn Sie ein Video oder einen Audiostream konfigurieren, werden diese Typen in der Regel verwendet.



| Komprimierter Medien Untertyp          | BESCHREIBUNG                                                                                                                                                                                                                                                                                 |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Wmmediasubtype- \_ acelpnet          | Das mit dem Sipro Labs-ACELP-Codec codierte Audiodaten. Diese Audiodaten sind normalerweise Sprach Daten. (Wird nicht mehr für die Codierung unterstützt.)                                                                                                                                                                       |
| Wmmediasubtype \_ MP43              | Video, das vom Microsoft MPEG 4-Codec Version 3 codiert wurde. Dieser Codec wird vom Windows Media-Format-SDK nicht mehr unterstützt. Wenn dieser Codec bereits auf einem Computer installiert ist, wird dieser Codec nicht durch die Installation des Windows Media-Format-SDKs oder des Verteilungs Pakets auf einem Computer entfernt. |
| Wmmediasubtype \_ MP4 Bitrate              | Video, das mit dem ISO MPEG 4-Codec Version 1 codiert ist.                                                                                                                                                                                                                                         |
| Wmmediasubtype- \_ MPEG2- \_ Video      | Video, das in MPEG 2-Spezifikationen codiert ist.                                                                                                                                                                                                                                                     |
| Wmmediasubtype \_ MSS1              | Video, das mit dem Windows Media-Bildschirm Codec Version 1 codiert ist.                                                                                                                                                                                                                                |
| Wmmediasubtype \_ MSS2              | Video, das mit dem Windows Media Video 9-Bildschirm Codec codiert ist.                                                                                                                                                                                                                                  |
| wmmediasubtype \_ wmvp              | Video, das mit dem Bild Codec Windows Media Video 9 codiert ist, um Bitmaps und Decodierungs Daten in einen Videostream umzuwandeln.                                                                                                                                                                     |
| Wmmediasubtype \_ WVP2              | Das mit dem Windows Media Video 9-Abbild v2-Codec codierte Video.                                                                                                                                                                                                                                |
| Wmmediasubtype \_ \_ wmaudioverlust Verlust | Audiodaten, die mit dem Windows Media Audio 9-Codec oder dem Windows Media Audio 9,1-Codec codiert sind.                                                                                                                                                                                           |
| Wmmediasubtype \_ WMAudioV2         | Das mit der Windows Media Audio Codec-Version 2 codierte Audiodatei. Dieser Wert ist identisch mit wmmediasubtype \_ WMAudioV7 und wmmediasubtype \_ WMAudioV8, da die Bitstreams für diese Codec-Versionen kompatibel sind.                                                                             |
| Wmmediasubtype \_ WMAudioV7         | Das mit dem Windows Media Audio Codec Version 7 codierte Audiodatei. Dieser Wert ist identisch mit wmmediasubtype \_ WMAudioV2 und wmmediasubtype \_ WMAudioV8, da die Bitstreams für diese Codec-Versionen kompatibel sind.                                                                             |
| Wmmediasubtype \_ WMAudioV8         | Das mit dem Windows Media Audio 8-Codec codierte Audiodaten, der Windows Media Audio 9-Codec oder der Windows Media Audio 9,1-Codec. Dieser Wert ist identisch mit wmmediasubtype \_ WMAudioV2 und wmmediasubtype \_ WMAudioV7, da die Bitstreams für diese Codec-Versionen kompatibel sind.              |
| Wmmediasubtype \_ WMAudioV9         | Audiocodierung mit dem Windows Media Audio 9 Professional-Codec oder dem Windows Media Audio 9,1 Professional-Codec.                                                                                                                                                                          |
| Wmmediasubtype \_ M4S2              | Video, das mit dem ISO MPEG4 v 1.1-Codec codiert ist.                                                                                                                                                                                                                                                |
| Wmmediasubtype \_ WMSP1             | Das mit dem Sprach Codec Windows Media Audio 9 codierte Audiodaten.                                                                                                                                                                                                                                   |
| Wmmediasubtype \_ WMV1              | Video, das mit dem Windows Media Video Codec Version 7 codiert ist.                                                                                                                                                                                                                                |
| Wmmediasubtype \_ WMV2              | Das mit dem Windows Media Video 8-Codec codierte Video.                                                                                                                                                                                                                                        |
| Wmmediasubtype \_ WMV3              | Das mit dem Windows Media Video 9-Codec codierte Video.                                                                                                                                                                                                                                        |
| wmmediasubtype \_ wmva              | Video, das mit der Version von Windows Media Video 9 Advanced Profile Codec codiert ist, die mit dem SDK der Windows Media-Serie 9 veröffentlicht wurde.                                                                                                                                           |
| Wmmediasubtype \_ WVC1              | Video, das mit der Version von Windows Media Video 9 Advanced Profile Codec codiert ist, die mit dem SDK für Windows Media-Format 11 veröffentlicht wurde. Dieser Untertyp identifiziert einen Bitstream, der mit dem SMPTE VC-1-Standard kompatibel ist.                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Medientyp-IDs**](media-type-identifiers.md)
</dt> <dt>

[**Medientypen**](media-types.md)
</dt> <dt>

[**Nicht komprimierte Medien Untertypen**](uncompressed-media-subtypes.md)
</dt> </dl>

 

 




