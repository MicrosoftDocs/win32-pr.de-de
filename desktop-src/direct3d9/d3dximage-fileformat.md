---
description: Beschreibt die unterstützten Bild Dateiformate. Beschreibungen dieser Formate finden Sie unter "Hinweise".
ms.assetid: 245a0052-f156-44ad-ab46-3677a818167e
title: D3DXIMAGE_FILEFORMAT-Enumeration (D3dx9tex. h)
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
ms.openlocfilehash: 3b1195e7503ff32e92cdbafde941b811dcf86427
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354827"
---
# <a name="d3dximage_fileformat-enumeration"></a>D3DXIMAGE \_ FileFormat-Enumeration

Beschreibt die unterstützten Bild Dateiformate. Beschreibungen dieser Formate finden Sie unter "Hinweise".

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

Windows-Bitmap-Dateiformat (BMP).

</dd> <dt>

<span id="D3DXIFF_JPG"></span><span id="d3dxiff_jpg"></span>**D3DXIFF \_ JPG**
</dt> <dd>

Komprimiertes Dateiformat für eine gemeinsame Photographics Experts Group (JPEG).

</dd> <dt>

<span id="D3DXIFF_TGA"></span><span id="d3dxiff_tga"></span>**D3DXIFF- \_ TGA**
</dt> <dd>

Bild Dateiformat Truevision (Targa, TGA).

</dd> <dt>

<span id="D3DXIFF_PNG"></span><span id="d3dxiff_png"></span>**D3DXIFF \_ PNG**
</dt> <dd>

Das Dateiformat Portable Network Graphics (PNG).

</dd> <dt>

<span id="D3DXIFF_DDS"></span><span id="d3dxiff_dds"></span>**D3DXIFF- \_ DDS**
</dt> <dd>

Das DDS-Dateiformat (DirectDraw Surface).

</dd> <dt>

<span id="D3DXIFF_PPM"></span><span id="d3dxiff_ppm"></span>**D3DXIFF \_ ppm**
</dt> <dd>

Dateiformat für Portable pixmap (ppm).

</dd> <dt>

<span id="D3DXIFF_DIB"></span><span id="d3dxiff_dib"></span>**D3DXIFF \_ DIB**
</dt> <dd>

Windows-DIB-Dateiformat (geräteunabhängige Bitmap).

</dd> <dt>

<span id="D3DXIFF_HDR"></span><span id="d3dxiff_hdr"></span>**D3DXIFF \_ HDR**
</dt> <dd>

Das HDR-Dateiformat (High Dynamic Range).

</dd> <dt>

<span id="D3DXIFF_PFM"></span><span id="d3dxiff_pfm"></span>**D3DXIFF \_ PFM**
</dt> <dd>

Portable float-Kartendatei Format.

</dd> <dt>

<span id="D3DXIFF_FORCE_DWORD"></span><span id="d3dxiff_force_dword"></span>**D3DXIFF \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Funktionen, die mit D3DXLoadxxx beginnen, unterstützen alle aufgeführten Formate. Funktionen, die mit D3DXSavexxx beginnen, unterstützen alle aufgeführten Formate, ausgenommen die Formate Truevision (. TGA) und Portable pixmap (. ppm).

In der folgenden Tabelle sind die verfügbaren Eingabe-und Ausgabeformate aufgeführt.



| Dateierweiterung | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BMP           | Windows-Bitmap-Format. Enthält einen Header, der die Auflösung des Geräts, auf dem das Rechteck von Pixeln erstellt wurde, die Abmessungen des Rechtecks, die Größe des Bits-Arrays, eine logische Palette und ein Array von Bits beschreibt, das die Beziehung zwischen Pixeln im bitzugeordneten Bild und Einträgen in der logischen Palette definiert. |
| .dds           | Format der DirectDraw-Oberflächen Datei. Speichert Texturen, volumetexturen und kubische Umgebungs Zuordnungen mit oder ohne MipMap-Ebenen und mit oder ohne Pixel Komprimierung. Siehe [DDS](../direct3ddds/dx-graphics-dds.md).                                                                                                                                       |
| DIB           | Windows DIB. Enthält ein Array von Bits in Kombination mit Strukturen, die die Breite und Höhe des bitzugeordneten Bilds, das Farb Format des Geräts, auf dem das Image erstellt wurde, und die Auflösung des Geräts angeben, das zum Erstellen des Bilds verwendet wurde.                                                                                                              |
| . HDR           | HDR-Format. Codiert jedes Pixel als RGBE-32-Bit-Farbe mit 8 Bits der Mantisse für Rot, grün und blau und einem freigegebenen 8-Bit-Exponenten. Jeder Kanal wird separat mit der Lauf Zeit Codierung (Run-Length Encoding, RLE) komprimiert.                                                                                                                                       |
| .jpg           | JPEG-Standard. Gibt die Variablen Komprimierung von 24-Bit-RGB-Farb-und 8-Bit-Bilddokument Dateien mit Graustufen Tagged Image File Format (TIFF) an.                                                                                                                                                                                                       |
| . PFM           | Portable float-Kartenformat. Ein unformatierte Gleit Komma Bildformat ohne Komprimierung. Der Dateiheader gibt Bildbreite, Höhe, monochrome oder Farbe und die Reihenfolge des Computers an. Pixel Daten werden als 32-Bit-Gleit Komma Werte mit drei Werten pro Pixel für Farbe und einem Wert pro Pixel für monochrome gespeichert.                                |
| .png           | PNG-Format. Ein nicht proprietäres Bitmap-Format, das die Verlust lose Komprimierung verwendet.                                                                                                                                                                                                                                                                            |
| . ppm           | Portables Pixmap-Format. Ein Binär-oder ASCII-Dateiformat für Farbbilder, das Bild Höhe und-Breite sowie den Wert der maximalen Farbkomponente enthält.                                                                                                                                                                                                 |
| .tga           | Format für das Targa-oder Truevision-Grafik Adapter. Unterstützt Tiefen von 8, 15, 16, 24 und 32 Bits, einschließlich der 8-Bit-Grau Skala, und enthält optionale Farb Palettendaten, Bild (x, y) Ursprungs-und Größendaten sowie Pixeldaten.                                                                                                                               |



 

Weitere Informationen zu einigen dieser Formate finden Sie unter [Typen von Bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9tex. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
