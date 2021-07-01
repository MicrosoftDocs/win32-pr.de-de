---
description: Die folgenden Untertypen definieren nicht komprimierte RGB-Formate ohne Alphakanal.
ms.assetid: 49c91c8c-6889-48c6-8fa5-84929c03d951
title: Unkomprimierte RGB-Videountertypen (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f149786c32c0734492179e2d3e75e5a7d7df969
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119245"
---
# <a name="uncompressed-rgb-video-subtypes"></a>Unkomprimierte RGB-Videountertypen

Die folgenden Untertypen definieren nicht komprimierte RGB-Formate ohne Alphakanal.



| Konstante                                                                                                                                                                        | Beschreibung                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------|
| <span id="MEDIASUBTYPE_RGB1"></span><span id="mediasubtype_rgb1"></span><dl> <dt>**MEDIASUBTYPE \_ RGB1**</dt> </dl>       | RGB, 1 Bit pro Pixel (bpp), palettisiert<br/> |
| <span id="MEDIASUBTYPE_RGB4"></span><span id="mediasubtype_rgb4"></span><dl> <dt>**MEDIASUBTYPE \_ RGB4**</dt> </dl>       | RGB, 4 BPP, palettisiert<br/>                 |
| <span id="MEDIASUBTYPE_RGB8"></span><span id="mediasubtype_rgb8"></span><dl> <dt>**MEDIASUBTYPE \_ RGB8**</dt> </dl>       | RGB, 8 bpp, palettisiert<br/>                 |
| <span id="MEDIASUBTYPE_RGB555"></span><span id="mediasubtype_rgb555"></span><dl> <dt>**MEDIASUBTYPE \_ RGB555**</dt> </dl> | RGB 555, 16 BPP<br/>                        |
| <span id="MEDIASUBTYPE_RGB565"></span><span id="mediasubtype_rgb565"></span><dl> <dt>**MEDIASUBTYPE \_ RGB565**</dt> </dl> | RGB 565, 16 BPP<br/>                        |
| <span id="MEDIASUBTYPE_RGB24"></span><span id="mediasubtype_rgb24"></span><dl> <dt>**MEDIASUBTYPE \_ RGB24**</dt> </dl>    | RGB, 24 bpp<br/>                            |
| <span id="MEDIASUBTYPE_RGB32"></span><span id="mediasubtype_rgb32"></span><dl> <dt>**MEDIASUBTYPE \_ RGB32**</dt> </dl>    | RGB, 32 bpp<br/>                            |



Die folgenden Untertypen definieren nicht komprimierte RGB-Formate mit Alphakanal.



| Konstante                                                                                                                                                                                       | Beschreibung                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| <span id="MEDIASUBTYPE_ARGB1555"></span><span id="mediasubtype_argb1555"></span><dl> <dt>**MEDIASUBTYPE \_ ARGB1555**</dt> </dl>          | RGB 555 mit Alphakanal<br/>                                                    |
| <span id="MEDIASUBTYPE_ARGB32"></span><span id="mediasubtype_argb32"></span><dl> <dt>**MEDIASUBTYPE \_ ARGB32**</dt> </dl>                | RGB 32 mit Alphakanal<br/>                                                     |
| <span id="MEDIASUBTYPE_ARGB4444"></span><span id="mediasubtype_argb4444"></span><dl> <dt>**MEDIASUBTYPE \_ ARGB4444**</dt> </dl>          | 16-Bit RGB mit Alphakanal; 4 Bits pro Kanal<br/>                             |
| <span id="MEDIASUBTYPE_A2R10G10B10"></span><span id="mediasubtype_a2r10g10b10"></span><dl> <dt>**MEDIASUBTYPE \_ A2R10G10B10**</dt> </dl> | 32-Bit RGB mit Alphakanal; 10 Bits pro RGB-Kanal plus 2 Bits für Alpha.<br/> |
| <span id="MEDIASUBTYPE_A2B10G10R10"></span><span id="mediasubtype_a2b10g10r10"></span><dl> <dt>**MEDIASUBTYPE \_ A2B10G10R10**</dt> </dl> | 32-Bit-BGR mit Alphakanal; 10 Bits pro BGR-Kanal plus 2 Bits für Alpha.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei palettierten Formaten wird die Farbe jedes Pixels als Index in einer Palette angegeben. Die Palette muss im Formatblock gemäß der [**BITMAPINFOHEADER-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) enthalten sein. Bei nicht palettierten Formaten wird die Farbe jedes Pixels direkt angegeben. Das Speicherlayout hängt von der Bittiefe ab:

-   RGB 555 verwendet das folgende Speicherlayout:
    ```C++
    High-order byte:    Low-order byte: 
    X R R R R R G G     G G G B B B B B 

    X = Don't care, R = Red, G = Green, B = Blue
    ```

    

-   RGB 565 verwendet das folgende Speicherlayout:
    ```C++
    High-order byte:    Low-order byte: 
    R R R R R G G G     G G G B B B B B 
    ```

    

-   Für RGB 24 ist jedes Pixel ein [**RGBTRIPLE.**](/windows/win32/api/wingdi/ns-wingdi-rgbtriple) Jede Farbe ist ein Byte mit einem Wert von 0 bis einschließlich 255. Das Speicherlayout ist:

    |       | Layout     | Layout      | Layout     |
    |-------|------|-------|-----|
    | **Byte**  | 0    | 1     | 2   |
    | **Wert** | Blau | Grün | Red |

    

     

-   Für RGB 32 ist jedes Pixel ein **RGBQUAD.** Jede Farbe ist ein Byte mit einem Wert von 0 bis einschließlich 255. Das Speicherlayout ist: 

    |       | Layout     | Layout      | Layout     | Layout |
    |-------|------|-------|-----|---------------------|
    | **Byte**  | 0    | 1     | 2   | 3                   |
    | **Wert** | Blau | Grün | Red | Alpha oder Keine Sorge |

    

     

    Wenn der Untertyp MEDIASUBTYPE \_ ARGB32 ist, enthält Byte 3 einen Wert für den Alphakanal. Wenn der Untertyp MEDIASUBTYPE \_ RGB32 ist, sollte Byte 3 ignoriert werden.

-   A2R10G10B10 verwendet das folgende Layout: 

    |       | Layout     | Layout      | Layout     | Layout |
    |-------|-------|---------|---------|---------|
    | **Bit**   | 0–9 | 10 – 19 | 20 - 29 | 30 - 31 |
    | **Wert** | Blau  | Grün   | Red     | Alpha   |

    

     

-   A2B10G10R10 verwendet das folgende Layout: 

    |       | Layout     | Layout      | Layout     | Layout |
    |-------|-------|---------|---------|---------|
    | **Bit**   | 0–9 | 10 – 19 | 20 - 29 | 30 - 31 |
    | **Wert** | Red   | Grün   | Blau    | Alpha   |

    

     

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videountertypen](video-subtypes.md)
</dt> <dt>

[Arbeiten mit Videoframes](working-with-video-frames.md)
</dt> </dl>

 

 
