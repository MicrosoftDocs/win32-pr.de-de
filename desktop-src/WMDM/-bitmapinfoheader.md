---
title: _BITMAPINFOHEADER Struktur
description: Die \_ BITMAPINFOHEADER-Struktur definiert das Format eines Videoframes.
ms.assetid: 394b8ded-81db-4ad3-8cf7-086f1e832771
keywords:
- _BITMAPINFOHEADER Struktur von Windows Media Geräte-Manager
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
ms.openlocfilehash: 5f2d0da3d05fe050f32d5a35bbbe7de558e1c4962fa84a958855b2960e343942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586884"
---
# <a name="_bitmapinfoheader-structure"></a>\_BITMAPINFOHEADER-Struktur

Die **\_ BITMAPINFOHEADER-Struktur** definiert das Format eines Videoframes.

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

**biSize**
</dt> <dd>

Gibt die Anzahl der Bytes an, die für die -Struktur erforderlich sind.

</dd> <dt>

**biWidth**
</dt> <dd>

Gibt die Breite der Bitmap in Pixel an.

</dd> <dt>

**biHeight**
</dt> <dd>

Gibt die Höhe der Bitmap in Pixel an. Wenn **biHeight** positiv ist, ist die Bitmap ein DIB von unten nach oben, und der Ursprung ist die untere linke Ecke. Wenn **biHeight** negativ ist, ist die Bitmap ein DIB von oben nach unten, und ihr Ursprung ist die linke obere Ecke. Wenn **biHeight** negativ ist und ein DIB von oben nach unten anzeigt, muss **biCompression** entweder BI \_ RGB oder BI \_ BITFIELDS sein. DiBs von oben nach unten können nicht komprimiert werden.

</dd> <dt>

**Doppeldecker**
</dt> <dd>

Gibt die Anzahl der Ebenen für das Zielgerät an. Dieser Wert muss auf 1 festgelegt werden.

</dd> <dt>

**biBitCount**
</dt> <dd>

Gibt die Anzahl der Bits pro Pixel an. Das **biBitCount-Element** der **BITMAPINFOHEADER-Struktur** bestimmt die Anzahl der Bits, die jedes Pixel definieren, und die maximale Anzahl von Farben in der Bitmap. Dieser Member muss einer der folgenden Werte sein.



| Wert | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Die Bitmap ist monocolore, und der bmiColors-Member enthält zwei Einträge. Jedes Bit im Bitmaparray stellt ein Pixel dar. Wenn das Bit klar ist, wird das Pixel mit der Farbe des ersten Eintrags in der Tabelle bmiColors angezeigt. wenn das Bit festgelegt ist, hat das Pixel die Farbe des zweiten Eintrags in der Tabelle.                                                                                                                                                                                                                                                                                                        |
| 2     | Die Bitmap verfügt über vier mögliche Farbwerte.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 4     | Die Bitmap hat maximal 16 Farben, und das bmiColors-Element enthält bis zu 16 Einträge. Jedes Pixel in der Bitmap wird durch einen 4-Bit-Index in der Farbtabelle dargestellt. Wenn das erste Byte in der Bitmap beispielsweise 0x1F ist, stellt das Byte zwei Pixel dar. Das erste Pixel enthält die Farbe im zweiten Tabelleneintrag, und das zweite Pixel enthält die Farbe im 16. Tabelleneintrag.                                                                                                                                                                                                                 |
| 8     | Die Bitmap hat maximal 256 Farben, und das bmiColors-Element enthält bis zu 256 Einträge. In diesem Fall stellt jedes Byte im Array ein einzelnes Pixel dar.                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 16    | Die Bitmap hat maximal 2^16 Farben. Wenn der biCompression-Member von BITMAPINFOHEADER BI \_ RGB ist, ist der bmiColors-Member **NULL.** Jedes WORD im Bitmaparray stellt ein einzelnes Pixel dar. Die relativen Intensitäten von Rot, Grün und Blau werden für jede Farbkomponente mit 5 Bits dargestellt. Der Wert für blau ist in den am wenigsten signifikanten 5 Bits, gefolgt von jeweils 5 Bits für Grün und Rot. Das wichtigste Bit wird nicht verwendet. Die bmiColors-Farbtabelle wird zum Optimieren von Farben verwendet, die auf palettenbasierten Geräten verwendet werden, und muss die Anzahl der Einträge enthalten, die vom biClrUsed-Member angegeben werden. |
| 24    | Die Bitmap hat maximal 2^24 Farben, und der bmiColors-Member ist **NULL.** Jedes 3-Byte-Triplet im Bitmaparray stellt die relativen Intensitäten von Blau, Grün bzw. Rot für ein Pixel dar. Die bmiColors-Farbtabelle wird zum Optimieren von Farben verwendet, die auf palettenbasierten Geräten verwendet werden, und muss die Anzahl der Einträge enthalten, die vom biClrUsed-Member angegeben werden.                                                                                                                                                                                                                                     |
| 32    | Die Bitmap hat maximal 2^32 Farben. Wenn der biCompression-Member BI \_ RGB ist, ist der bmiColors-Member **NULL.** Jedes DWORD im Bitmaparray stellt die relativen Intensitäten von Blau, Grün und Rot für ein Pixel dar. Das hohe Byte in jedem DWORD wird nicht verwendet. Die bmiColors-Farbtabelle wird zum Optimieren von Farben verwendet, die auf palettenbasierten Geräten verwendet werden, und muss die Anzahl der Einträge enthalten, die vom biClrUsed-Member angegeben werden.                                                                                                                                                                 |



 

</dd> <dt>

**biCompression**
</dt> <dd>

Gibt den Komprimierungstyp für eine komprimierte Bottom-Up-Bitmap an (DIBs von oben nach unten können nicht komprimiert werden). Dieser Member kann einer der folgenden Werte sein.



| Wert         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BI \_ RGB       | Ein nicht komprimiertes Format.                                                                                                                                                                                                                                                                                            |
| BI \_ BITFIELDS | Gibt an, dass die Bitmap nicht komprimiert ist und dass die Farbtabelle aus drei DWORD-Farbmasken besteht, die die rote, grüne bzw. blaue Komponente jedes Pixels angeben. Dies ist gültig, wenn sie mit 16-bpp- und 32-bpp-Bitmaps verwendet wird. Dieser Wert ist in Microsoft Windows CE Version 2.0 und höher gültig. |



 

</dd> <dt>

**biSizeImage**
</dt> <dd>

Gibt die Größe des Bilds in Bytes an. Dies kann für BI RGB-Bitmaps auf 0 (null) festgelegt \_ werden.

</dd> <dt>

**biXPelsPerMeter**
</dt> <dd>

Gibt die horizontale Auflösung des Zielgeräts für die Bitmap in Pixel pro Verbrauchseinheit an. Eine Anwendung kann diesen Wert verwenden, um eine Bitmap aus einer Ressourcengruppe auszuwählen, die den Merkmalen des aktuellen Geräts am besten entspricht.

</dd> <dt>

**biYPelsPerMeter**
</dt> <dd>

Gibt die vertikale Auflösung des Zielgeräts für die Bitmap in Pixel pro Meter an.

</dd> <dt>

**biClrUsed**
</dt> <dd>

Gibt die Anzahl der Farbindizes in der Farbtabelle an, die tatsächlich von der Bitmap verwendet werden. Wenn dieser Wert 0 (null) ist, verwendet die Bitmap die maximale Anzahl von Farben, die dem Wert des **biBitCount-Elements** für den von **biCompression** angegebenen Komprimierungsmodus entsprechen.

</dd> <dt>

**biClrImportant**
</dt> <dd>

Gibt die Anzahl der Farbindizes an, die zum Anzeigen der Bitmap erforderlich sind. Wenn dieser Wert 0 (null) ist, sind alle Farben erforderlich.

Wenn biClrUsed ungleich null ist und das biBitCount-Element kleiner als 16 ist, gibt das biClrUsed-Element die tatsächliche Anzahl von Farben an, auf die die Grafik-Engine oder der Gerätetreiber zugreift. Wenn biBitCount 16 oder höher ist, gibt das biClrUsed-Element die Größe der Farbtabelle an, die zum Optimieren der Leistung der Systemfarbpaletten verwendet wird. Wenn biBitCount gleich 16 oder 32 ist, beginnt die optimale Farbpalette unmittelbar nach den drei DWORD-Masken.

Wenn die Bitmap eine gepackte Bitmap ist (eine Bitmap, in der das Bitmaparray unmittelbar der \_ BITMAPINFOHEADER-Struktur folgt und auf die ein einzelner Zeiger verweist), muss das biClrUsed-Element entweder 0 (null) oder die tatsächliche Größe der Farbtabelle sein.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur ist in einer **\_ VIDEOINFOHEADER-Struktur** enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](structures.md)
</dt> <dt>

[**\_VIDEOINFOHEADER**](-videoinfoheader.md)
</dt> </dl>

 

 





