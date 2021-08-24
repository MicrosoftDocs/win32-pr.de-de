---
description: Beschreibt die unterstützten Bilddateiformate. Beschreibungen dieser Formate finden Sie unter Hinweise.
ms.assetid: 245a0052-f156-44ad-ab46-3677a818167e
title: D3DXIMAGE_FILEFORMAT-Enumeration (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_FILEFORMAT
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: 715b9f0f6d8c56153d51c9c19b70ba253e508619229f52201a28f23c1902d26e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123166"
---
# <a name="d3dximage_fileformat-enumeration"></a>D3DXIMAGE \_ FILEFORMAT-Enumeration

Beschreibt die unterstützten Bilddateiformate. Beschreibungen dieser Formate finden Sie unter Hinweise.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXIMAGE_FILEFORMAT { 
  D3DXIFF_BMP          = 0,
  D3DXIFF_JPG          = 1,
  D3DXIFF_TGA          = 2,
  D3DXIFF_PNG          = 3,
  D3DXIFF_DDS          = 4,
  D3DXIFF_PPM          = 5,
  D3DXIFF_DIB          = 6,
  D3DXIFF_HDR          = 7,
  D3DXIFF_PFM          = 8,
  D3DXIFF_FORCE_DWORD  = 0x7fffffff
} D3DXIMAGE_FILEFORMAT, *LPD3DXIMAGE_FILEFORMAT;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DXIFF_BMP"></span><span id="d3dxiff_bmp"></span>**D3DXIFF \_ BMP**
</dt> <dd>

Windows BMP-Dateiformat (Bitmap).

</dd> <dt>

<span id="D3DXIFF_JPG"></span><span id="d3dxiff_jpg"></span>**D3DXIFF \_ JPG**
</dt> <dd>

Jpeg-Komprimiertes Dateiformat (Joint Jpgs Experts Group).

</dd> <dt>

<span id="D3DXIFF_TGA"></span><span id="d3dxiff_tga"></span>**D3DXIFF \_ TGA**
</dt> <dd>

Truevision-Bilddateiformat (Targa oder TGA).

</dd> <dt>

<span id="D3DXIFF_PNG"></span><span id="d3dxiff_png"></span>**D3DXIFF \_ PNG**
</dt> <dd>

Portable Network Graphics(PNG)-Dateiformat.

</dd> <dt>

<span id="D3DXIFF_DDS"></span><span id="d3dxiff_dds"></span>**D3DXIFF \_ DDS**
</dt> <dd>

DDS-Dateiformat (DirectDraw Surface).

</dd> <dt>

<span id="D3DXIFF_PPM"></span><span id="d3dxiff_ppm"></span>**D3DXIFF \_ PPM**
</dt> <dd>

Portable Pixmap-Dateiformat (PPM).

</dd> <dt>

<span id="D3DXIFF_DIB"></span><span id="d3dxiff_dib"></span>**D3DXIFF \_ DIB**
</dt> <dd>

Windows DiB-Dateiformat (Device-Independent Bitmap).

</dd> <dt>

<span id="D3DXIFF_HDR"></span><span id="d3dxiff_hdr"></span>**D3DXIFF \_ HDR**
</dt> <dd>

HDR-Dateiformat (High Dynamic Range).

</dd> <dt>

<span id="D3DXIFF_PFM"></span><span id="d3dxiff_pfm"></span>**D3DXIFF \_ PFM**
</dt> <dd>

Portables Float map-Dateiformat.

</dd> <dt>

<span id="D3DXIFF_FORCE_DWORD"></span><span id="d3dxiff_force_dword"></span>**D3DXIFF \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration in eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Funktionen, die mit D3DXLoadxxx beginnen, unterstützen alle aufgeführten Formate. Funktionen, die mit D3DXSavexxx beginnen, unterstützen alle aufgeführten Formate mit Ausnahme der Formate Truevision (.tga) und portable Pixmap (.ppm).

In der folgenden Tabelle sind die verfügbaren Eingabe- und Ausgabeformate aufgeführt.



| Dateierweiterung | Beschreibung                                                                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BMP           | Windows Bitmapformat. Enthält einen Header, der die Auflösung des Geräts beschreibt, auf dem das Pixelrechteck erstellt wurde, die Abmessungen des Rechtecks, die Größe des Arrays von Bits, eine logische Palette und ein Array von Bits, das die Beziehung zwischen Pixeln im Bitmapbild und Einträgen in der logischen Palette definiert. |
| .dds           | DirectDraw Surface-Dateiformat. Speichert Texturen, Volumentexturen und kubische Umgebungskarten mit oder ohne Mipmapebenen und mit oder ohne Pixelkomprimierung. Weitere Informationen finden Sie unter [DDS](../direct3ddds/dx-graphics-dds.md).                                                                                                                                       |
| DIB           | Windows Dib. Enthält ein Array von Bits in Kombination mit Strukturen, die Breite und Höhe des Bitmapbilds, das Farbformat des Geräts, auf dem das Bild erstellt wurde, und die Auflösung des Geräts angeben, das zum Erstellen dieses Bilds verwendet wird.                                                                                                              |
| HDR           | HDR-Format. Codiert jedes Pixel als RGBE-32-Bit-Farbe mit 8 Bits Mantisse für Rot, Grün und Blau und einem freigegebenen 8-Bit-Exponenten. Jeder Kanal wird separat mit RLE (Run-Length Encoding) komprimiert.                                                                                                                                       |
| .jpg           | JPEG-Standard. Gibt die variable Komprimierung von 24-Bit-RGB-Farb- und 8-Bit-TIFF-Bilddokumentdateien (Gray Scale Tagged Image File Format) an.                                                                                                                                                                                                       |
| PFM           | Portables Float-Kartenformat. Ein unformatiertes Gleitkommabildformat ohne Komprimierung. Der Dateiheader gibt Bildbreite, Höhe, Monocolore oder Farbe sowie die Wortreihenfolge des Computers an. Pixeldaten werden als 32-Bit-Gleitkommawerte gespeichert, wobei 3 Werte pro Pixel für Farbe und ein Wert pro Pixel für Monocolore angegeben sind.                                |
| .png           | PNG-Format. Ein nicht proprietäres Bitmapformat mit verlustfreier Komprimierung.                                                                                                                                                                                                                                                                            |
| .ppm           | Portables Pixmap-Format. Ein binäres oder ASCII-Dateiformat für Farbbilder, das Bildhöhe und -breite sowie den maximalen Farbkomponentenwert enthält.                                                                                                                                                                                                 |
| .tga           | Targa- oder Truevision-Grafikadapterformat. Unterstützt Tiefen von 8, 15, 16, 24 und 32 Bit, einschließlich grauer 8-Bit-Skala, und enthält optionale Farbpalettendaten, Bildursprungs- und Größendaten (x, y) sowie Pixeldaten.                                                                                                                               |



 

Weitere Informationen zu einigen dieser Formate finden Sie unter [Bitmaptypen.](../gdiplus/-gdiplus-types-of-bitmaps-about.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9tex.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
