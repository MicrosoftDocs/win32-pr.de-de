---
title: _BITMAPINFOHEADER Struktur
description: Die \_ BITMAPINFOHEADER-Struktur definiert das Format eines Video Frames.
ms.assetid: 394b8ded-81db-4ad3-8cf7-086f1e832771
keywords:
- _BITMAPINFOHEADER Struktur von Windows-Medien Device Manager
topic_type:
- apiref
api_name:
- _BITMAPINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481c80b6d209e0da8d00ef06d88392504bcae8e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362076"
---
# <a name="_bitmapinfoheader-structure"></a>\_BITMAPINFOHEADER-Struktur

Die **\_ BITMAPINFOHEADER** -Struktur definiert das Format eines Video Frames.

## <a name="syntax"></a>Syntax


```C++
typedef struct _tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} _BITMAPINFOHEADER;
```



## <a name="members"></a>Member

<dl> <dt>

**bisize**
</dt> <dd>

Gibt die Anzahl der Bytes an, die für die Struktur erforderlich sind.

</dd> <dt>

**biwidth**
</dt> <dd>

Gibt die Breite der Bitmap in Pixel an.

</dd> <dt>

**biheight**
</dt> <dd>

Gibt die Höhe der Bitmap in Pixel an. Wenn **biheight** positiv ist, ist die Bitmap ein Bottom-up-DIB, und der Ursprung ist die untere linke Ecke. Wenn **biheight** negativ ist, ist die Bitmap eine Top-Down-DIB, und Ihr Ursprung ist die linke obere Ecke. Wenn **biheight** auf einen negativen Wert festgelegt ist, der einen Top-Down-DIB anzeigt, muss die **bikomprimierung** entweder BI \_ RGB oder BI- \_ Bitfields sein Top-Down-Disb können nicht komprimiert werden.

</dd> <dt>

**zwei Ebenen**
</dt> <dd>

Gibt die Anzahl der Ebenen für das Zielgerät an. Dieser Wert muss auf 1 festgelegt werden.

</dd> <dt>

**biBitCount**
</dt> <dd>

Gibt die Anzahl der Bits pro Pixel an. Der **biBitCount** -Member der **BITMAPINFOHEADER** -Struktur bestimmt die Anzahl der Bits, die jedes Pixel definieren, sowie die maximale Anzahl von Farben in der Bitmap. Dieser Member muss einen der folgenden Werte aufweisen.



| Wert | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Die Bitmap ist Monochrom und der bmicolors-Member enthält zwei Einträge. Jedes Bit im Bitmap-Array stellt ein Pixel dar. Wenn das Bit eindeutig ist, wird das Pixel mit der Farbe des ersten Eintrags in der Tabelle bmicolors angezeigt. Wenn das-Bit festgelegt ist, hat das Pixel die Farbe des zweiten Eintrags in der Tabelle.                                                                                                                                                                                                                                                                                                        |
| 2     | Die Bitmap verfügt über vier mögliche Farbwerte.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 4     | Die Bitmap hat maximal 16 Farben, und der bmicolors-Member enthält bis zu 16 Einträge. Jedes Pixel in der Bitmap wird durch einen 4-Bit-Index in der Farbtabelle dargestellt. Wenn das erste Byte in der Bitmap z. b. 0x1F ist, stellt das Byte zwei Pixel dar. Das erste Pixel enthält die Farbe im zweiten Tabelleneintrag, und das zweite Pixel enthält die Farbe in der zehnten Tabelle.                                                                                                                                                                                                                 |
| 8     | Die Bitmap hat maximal 256 Farben, und der bmicolors-Member enthält bis zu 256 Einträge. In diesem Fall stellt jedes Byte im Array ein einzelnes Pixel dar.                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 16    | Die Bitmap hat maximal 2 ^ 16 Farben. Wenn der bicompression-Member von BITMAPINFOHEADER BI \_ RGB ist, ist der bmicolors-Member **null**. Jedes Wort im bitmaparray stellt ein einzelnes Pixel dar. Die relativen Intensitäten von rot, grün und blau werden für jede Farbkomponente mit 5 Bits dargestellt. Der Wert für blau liegt in den geringsten 5 Bits, gefolgt von 5 Bits für Grün und rot. Das signifikanteste Bit wird nicht verwendet. Die Farbtabelle bmicolors dient zum Optimieren von Farben, die auf palettenbasierten Geräten verwendet werden, und muss die Anzahl der Einträge enthalten, die vom biclrused-Member angegeben werden. |
| 24    | Die Bitmap hat maximal 2 ^ 24 Farben, und der bmicolors-Member ist **null**. Jede 3-Byte-Zahl im Bitmap-Array stellt die relativen Intensitäten von blau, grün und rot für ein Pixel dar. Die Farbtabelle bmicolors dient zum Optimieren von Farben, die auf palettenbasierten Geräten verwendet werden, und muss die Anzahl der Einträge enthalten, die vom biclrused-Member angegeben werden.                                                                                                                                                                                                                                     |
| 32    | Die Bitmap hat maximal 2 ^ 32 Farben. Wenn der bicompression-Member BI \_ RGB ist, ist der bmicolors-Member **null**. Jedes DWORD im Bitmap-Array stellt die relativen Intensitäten von blau, grün und rot für ein Pixel dar. Das hohe Byte in jedem DWORD wird nicht verwendet. Die Farbtabelle bmicolors dient zum Optimieren von Farben, die auf palettenbasierten Geräten verwendet werden, und muss die Anzahl der Einträge enthalten, die vom biclrused-Member angegeben werden.                                                                                                                                                                 |



 

</dd> <dt>

**bikomprimierung**
</dt> <dd>

Gibt den Komprimierungstyp für eine komprimierte Bottom-up-Bitmap an (Top-Down-Disb können nicht komprimiert werden). Dieser Member kann einen der folgenden Werte aufweisen.



| Wert         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BI \_ RGB       | Ein unkomprimiertes Format.                                                                                                                                                                                                                                                                                            |
| BI- \_ Bitfields | Gibt an, dass die Bitmap nicht komprimiert ist und dass die Farbtabelle aus drei DWORD-Farb Masken besteht, die jeweils die roten, grünen und blauen Komponenten der einzelnen Pixel angeben. Dies ist gültig bei Verwendung mit 16-bpp-und 32-bpp-Bitmaps. Dieser Wert ist in Microsoft Windows CE Version 2,0 und höher gültig. |



 

</dd> <dt>

**bisizeimage**
</dt> <dd>

Gibt die Größe des Bilds in Bytes an. Dieser Wert kann für BI RGB-Bitmaps auf 0 (null) festgelegt werden \_ .

</dd> <dt>

**bixpelspermeter**
</dt> <dd>

Gibt die horizontale Auflösung des Zielgeräts für die Bitmap in Pixel pro Meter an. Mit diesem Wert kann eine Anwendung eine Bitmap aus einer Ressourcengruppe auswählen, die den Merkmalen des aktuellen Geräts am besten entspricht.

</dd> <dt>

**biypelspermeter**
</dt> <dd>

Gibt die vertikale Auflösung des Zielgeräts für die Bitmap in Pixel pro Meter an.

</dd> <dt>

**biclrused**
</dt> <dd>

Gibt die Anzahl der Farbindizes in der Farbtabelle an, die tatsächlich von der Bitmap verwendet werden. Wenn dieser Wert 0 (null) ist, verwendet die Bitmap die maximale Anzahl von Farben, die dem Wert des **biBitCount** -Members für den durch die **bikomprimierung** angegebenen Komprimierungs Modus entspricht.

</dd> <dt>

**biclrimportant**
</dt> <dd>

Gibt die Anzahl der für die Anzeige der Bitmap erforderlichen Farbindizes an. Wenn dieser Wert 0 (null) ist, sind alle Farben erforderlich.

Wenn der biclrused-Wert ungleich 0 (null) und der biBitCount-Member kleiner als 16 ist, gibt der biclrused-Member die tatsächliche Anzahl der Farben an, auf die das Grafik Modul oder der Gerätetreiber zugreift Wenn biBitCount 16 oder größer ist, gibt der biclrused-Member die Größe der Farbtabelle an, die zum Optimieren der Leistung der System Farbpaletten verwendet wird. Wenn biBitCount gleich 16 oder 32 ist, beginnt die optimale Farbpalette unmittelbar nach den drei DWORD-Masken.

Wenn es sich bei der Bitmap um eine gepackte Bitmap handelt (eine Bitmap, in der das bitmaparray unmittelbar auf die \_ BITMAPINFOHEADER-Struktur folgt und von einem einzelnen Zeiger referenziert wird), muss der biclrused-Member entweder 0 (null) oder die tatsächliche Größe der Farbtabelle aufweisen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur ist in einer **\_ videoinfoheader** -Struktur enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](structures.md)
</dt> <dt>

[**\_Videoinfoheader**](-videoinfoheader.md)
</dt> </dl>

 

 





