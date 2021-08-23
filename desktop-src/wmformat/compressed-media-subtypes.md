---
title: Komprimierte Medienuntertypen
description: Komprimierte Medienuntertypen
ms.assetid: 0ed6b4e8-6450-4484-90d6-efa2f9101782
keywords:
- Windows Medienformat-SDK, Medientypen
- Advanced Systems Format (ASF), Medientypen
- ASF (Advanced Systems Format), Medientypen
- Windows Medienformat-SDK, komprimierte Medienuntertypen
- Advanced Systems Format (ASF), komprimierte Medienuntertypen
- ASF (Advanced Systems Format), komprimierte Medienuntertypen
- Medientypen,komprimierte Medienuntertypen
- Komprimierte Medienuntertypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f231c9c8ff666c11d3fb3bf101dc3b43c1cd2ff90ca3a28ca1af0113fe8fccd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548090"
---
# <a name="compressed-media-subtypes"></a>Komprimierte Medienuntertypen

In der folgenden Tabelle sind die Untertypen komprimierter Medien aufgeführt. Diese Typen werden verwendet, um komprimierte Datenströme in einer Datei zu identifizieren. Wenn Sie einen Video- oder Audiostream konfigurieren, verwenden Sie in der Regel diese Typen.



| Untertyp "Komprimierte Medien"          | Beschreibung                                                                                                                                                                                                                                                                                 |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMMEDIASUBTYPE \_ ACELPnet          | Audio codiert mit dem Sipro Labs ACELP-Codec. Bei diesem Audio handelt es sich normalerweise um Sprachdaten. (Wird für die Codierung nicht mehr unterstützt.)                                                                                                                                                                       |
| WMMEDIASUBTYPE \_ MP43              | Video codiert durch den Microsoft MPEG 4-Codec Version 3. Dieser Codec wird nicht mehr vom Windows Media Format SDK unterstützt. Wenn dieser Codec bereits auf einem Computer installiert ist, wird dieser Codec durch die Installation des Windows Media Format SDK oder des Weiterverteilungspakets auf einem Computer nicht entfernt. |
| WMMEDIASUBTYPE \_ MP4S              | Video codiert mit dem ISO MPEG 4-Codec Version 1.                                                                                                                                                                                                                                         |
| WMMEDIASUBTYPE \_ \_ MPEG2-VIDEO      | Video codiert nach MPEG 2-Spezifikationen.                                                                                                                                                                                                                                                     |
| WMMEDIASUBTYPE \_ MSS1              | Video codiert mit dem Windows Media Screen-Codec, Version 1.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ MSS2              | Video codiert mit dem Windows Media Video 9 Screen-Codec.                                                                                                                                                                                                                                  |
| WMMEDIASUBTYPE \_ WMVP              | Video codiert mit dem Windows Media Video 9-Bildcodec zum Transformieren von Bitmaps und Dateidaten in einen Videostream.                                                                                                                                                                     |
| WMMEDIASUBTYPE \_ WVP2              | Video codiert mit dem Windows Media Video 9 Image v2-Codec.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMAudio \_ Lossless | Audio codiert mit dem Windows Media Audio 9 Lossless Codec oder dem Windows Media Audio 9.1-Codec.                                                                                                                                                                                           |
| WMMEDIASUBTYPE \_ WMAudioV2         | Audio codiert mit dem Windows Media Audio-Codec Version 2. Dieser Wert ist identisch mit WMMEDIASUBTYPE \_ WMAudioV7 und WMMEDIASUBTYPE WMAudioV8, da die Bitstreams für diese \_ Codecversionen kompatibel sind.                                                                             |
| WMMEDIASUBTYPE \_ WMAudioV7         | Audio codiert mit dem Windows Media Audio-Codec, Version 7. Dieser Wert ist identisch mit WMMEDIASUBTYPE \_ WMAudioV2 und WMMEDIASUBTYPE WMAudioV8, da die Bitstreams für diese \_ Codecversionen kompatibel sind.                                                                             |
| WMMEDIASUBTYPE \_ WMAudioV8         | Audio codiert mit dem Windows Media Audio 8-Codec, dem Windows Media Audio 9-Codec oder dem Windows Media Audio 9.1-Codec. Dieser Wert ist identisch mit WMMEDIASUBTYPE \_ WMAudioV2 und WMMEDIASUBTYPE WMAudioV7, da die Bitstreams für diese \_ Codecversionen kompatibel sind.              |
| WMMEDIASUBTYPE \_ WMAudioV9         | Audio codiert mit dem Windows Media Audio 9-Professional codec oder dem Windows Media Audio 9.1-Professional Codec.                                                                                                                                                                          |
| WMMEDIASUBTYPE \_ M4S2              | Video codiert mit dem ISO MPEG4 v1.1-Codec.                                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMSP1             | Audio codiert mit dem Windows Media Audio 9 Voice-Codec.                                                                                                                                                                                                                                   |
| WMMEDIASUBTYPE \_ WMV1              | Video codiert mit dem Windows Media Video-Codec, Version 7.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMV2              | Video codiert mit dem Windows Media Video 8-Codec.                                                                                                                                                                                                                                        |
| WMMEDIASUBTYPE \_ WMV3              | Video codiert mit dem Windows Media Video 9-Codec.                                                                                                                                                                                                                                        |
| WMMEDIASUBTYPE \_ WMVA              | Video codiert mit der Version des Windows Media Video 9 Advanced Profile-Codecs, der mit dem Windows Media Format 9 Series SDK veröffentlicht wurde.                                                                                                                                           |
| WMMEDIASUBTYPE \_ WVC1              | Video codiert mit der Version des Windows Media Video 9 Advanced Profile-Codecs, der mit dem Windows Media Format 11 SDK veröffentlicht wurde. Dieser Untertyp identifiziert einen Bitstream, der mit dem SMPTE VC-1-Standard kompatibel ist.                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Medientypbezeichner**](media-type-identifiers.md)
</dt> <dt>

[**Medientypen**](media-types.md)
</dt> <dt>

[**Unkomprimierte Medienuntertypen**](uncompressed-media-subtypes.md)
</dt> </dl>

 

 




