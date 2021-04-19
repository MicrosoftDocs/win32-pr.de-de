---
description: Die folgenden Untertypen definieren unkomprimierte RGB-Formate ohne Alphakanal.
ms.assetid: 49c91c8c-6889-48c6-8fa5-84929c03d951
title: Unkomprimierte RGB-Video Untertypen (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e04237a61fa91f4fe648dcb7743c893604adbe7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369201"
---
# <a name="uncompressed-rgb-video-subtypes"></a>Unkomprimierte RGB-Video Untertypen

Die folgenden Untertypen definieren unkomprimierte RGB-Formate ohne Alphakanal.



| Konstante                                                                                                                                                                        | BESCHREIBUNG                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------|
| <span id="MEDIASUBTYPE_RGB1"></span><span id="mediasubtype_rgb1"></span><dl> <dt>**Mediasubtype \_ RGB1**</dt> </dl>       | RGB, 1 Bit pro Pixel (BPP), palettisiert<br/> |
| <span id="MEDIASUBTYPE_RGB4"></span><span id="mediasubtype_rgb4"></span><dl> <dt>**Mediasubtype \_ RGB4**</dt> </dl>       | RGB, 4 bpp, palettisiert<br/>                 |
| <span id="MEDIASUBTYPE_RGB8"></span><span id="mediasubtype_rgb8"></span><dl> <dt>**Mediasubtype \_ RGB8**</dt> </dl>       | RGB, 8 bpp, palettisiert<br/>                 |
| <span id="MEDIASUBTYPE_RGB555"></span><span id="mediasubtype_rgb555"></span><dl> <dt>**Mediasubtype \_ RGB555**</dt> </dl> | RGB 555, 16 bpp<br/>                        |
| <span id="MEDIASUBTYPE_RGB565"></span><span id="mediasubtype_rgb565"></span><dl> <dt>**Mediasubtype \_ RGB565**</dt> </dl> | RGB 565, 16 bpp<br/>                        |
| <span id="MEDIASUBTYPE_RGB24"></span><span id="mediasubtype_rgb24"></span><dl> <dt>**Mediasubtype \_ RGB24**</dt> </dl>    | RGB, 24 bpp<br/>                            |
| <span id="MEDIASUBTYPE_RGB32"></span><span id="mediasubtype_rgb32"></span><dl> <dt>**Mediasubtype \_ RGB32**</dt> </dl>    | RGB, 32 bpp<br/>                            |



Die folgenden Untertypen definieren unkomprimierte RGB-Formate mit dem Alphakanal.



| Konstante                                                                                                                                                                                       | BESCHREIBUNG                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| <span id="MEDIASUBTYPE_ARGB1555"></span><span id="mediasubtype_argb1555"></span><dl> <dt>**Mediasubtype \_ ARGB1555**</dt> </dl>          | RGB 555 mit Alphakanal<br/>                                                    |
| <span id="MEDIASUBTYPE_ARGB32"></span><span id="mediasubtype_argb32"></span><dl> <dt>**Mediasubtype \_ ARGB32**</dt> </dl>                | RGB 32 mit Alphakanal<br/>                                                     |
| <span id="MEDIASUBTYPE_ARGB4444"></span><span id="mediasubtype_argb4444"></span><dl> <dt>**Mediasubtype \_ ARGB4444**</dt> </dl>          | 16-Bit-RGB mit Alphakanal; 4 Bits pro Kanal<br/>                             |
| <span id="MEDIASUBTYPE_A2R10G10B10"></span><span id="mediasubtype_a2r10g10b10"></span><dl> <dt>**Mediasubtype \_ A2R10G10B10**</dt> </dl> | 32-Bit RGB mit Alphakanal; 10 Bits pro RGB-Kanal plus 2 Bits für Alpha.<br/> |
| <span id="MEDIASUBTYPE_A2B10G10R10"></span><span id="mediasubtype_a2b10g10r10"></span><dl> <dt>**Mediasubtype \_ A2B10G10R10**</dt> </dl> | 32-Bit-BGR mit Alphakanal; 10 Bits pro BGR-Kanal plus 2 Bits für Alpha.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei Paletten-Formaten wird die Farbe jedes Pixels als Index in einer Palette angegeben. Die Palette muss im Format Block nach der [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur enthalten sein. Bei nicht palettierten Formaten wird die Farbe jedes Pixels direkt angegeben. das Speicher Layout hängt von der Bittiefe ab:

-   RGB 555 verwendet das folgende Arbeitsspeicher Layout:
    ```C++
    High-order byte:    Low-order byte: 
    X R R R R R G G     G G G B B B B B 

    X = Don't care, R = Red, G = Green, B = Blue
    ```

    

-   RGB 565 verwendet das folgende Arbeitsspeicher Layout:
    ```C++
    High-order byte:    Low-order byte: 
    R R R R R G G G     G G G B B B B B 
    ```

    

-   Bei RGB 24 ist jedes Pixel ein [**rgbtriple**](/windows/win32/api/wingdi/ns-wingdi-rgbtriple). Jede Farbe ist ein Byte mit einem Wert zwischen 0 und 255 (einschließlich). Das Speicher Layout ist: 

    |       |      |       |     |
    |-------|------|-------|-----|
    | Byte  | 0    | 1     | 2   |
    | Wert | Blau | Grün | Red |

    

     

-   Bei RGB 32 ist jedes Pixel ein **rgbquad**. Jede Farbe ist ein Byte mit einem Wert zwischen 0 und 255 (einschließlich). Das Speicher Layout ist: 

    |       |      |       |     |                     |
    |-------|------|-------|-----|---------------------|
    | Byte  | 0    | 1     | 2   | 3                   |
    | Wert | Blau | Grün | Red | Alpha oder nicht wichtig |

    

     

    Wenn der Untertyp mediasubtype \_ ARGB32 ist, enthält Byte 3 einen Wert für den Alphakanal. Wenn der Untertyp mediasubtype \_ RGB32 ist, sollte Byte 3 ignoriert werden.

-   A2R10G10B10 verwendet das folgende Layout: 

    |       |       |         |         |         |
    |-------|-------|---------|---------|---------|
    | bit   | 0–9 | 10 – 19 | 20 - 29 | 30 - 31 |
    | Wert | Blau  | Grün   | Red     | Alpha   |

    

     

-   A2B10G10R10 verwendet das folgende Layout: 

    |       |       |         |         |         |
    |-------|-------|---------|---------|---------|
    | bit   | 0–9 | 10 – 19 | 20 - 29 | 30 - 31 |
    | Wert | Red   | Grün   | Blau    | Alpha   |

    

     

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video Untertypen](video-subtypes.md)
</dt> <dt>

[Arbeiten mit Video Frames](working-with-video-frames.md)
</dt> </dl>

 

 
