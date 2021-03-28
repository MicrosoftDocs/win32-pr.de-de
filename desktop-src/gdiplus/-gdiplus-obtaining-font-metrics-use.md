---
description: 'Die FontFamily-Klasse stellt die folgenden Methoden bereit, die verschiedene Metriken für eine bestimmte Kombination aus Familie und Stil abrufen:'
ms.assetid: 3be485d0-9e0d-43e0-813e-668102ebc010
title: Abrufen von Schriftart Metriken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800fcee7dd1729a6fd5e59bb5dd636af89670776
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041713"
---
# <a name="obtaining-font-metrics"></a>Abrufen von Schriftart Metriken

Die [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) -Klasse stellt die folgenden Methoden bereit, die verschiedene Metriken für eine bestimmte Kombination aus Familie und Stil abrufen:

-   [**FontFamily:: GetEmHeight**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight)(FontStyle)
-   [**FontFamily:: GetCellAscent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcellascent)(FontStyle)
-   [**FontFamily:: GetCellDescent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent)(FontStyle)
-   [**FontFamily:: GetLineSpacing(**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getlinespacing)FontStyle)

Die von diesen Methoden zurückgegebenen Zahlen sind in Schriftart Entwurfs Einheiten, sodass Sie unabhängig von der Größe und den Einheiten eines bestimmten [**Schriftart**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) Objekts sind.

In der folgenden Abbildung sind die Aufstiege, der Abstieg und der Zeilenabstand dargestellt.

![Diagramm von zwei Zeichen in angrenzenden Zeilen, das Zellen Aufstieg, den Zell Abstieg und den Zeilenabstand anzeigt](images/fontstext7a.png)

Im folgenden Beispiel werden die Metriken für den regulären Stil der Arial-Schriftfamilie angezeigt. Der Code erstellt auch ein [**Schriftart**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) Objekt (basierend auf der Arial-Familie) mit einer Größe von 16 Pixel und zeigt die Metriken (in Pixel) für das jeweilige **Schriftart** Objekt an.


```
#define INFO_STRING_SIZE 100  // one line of output including null terminator
WCHAR infoString[INFO_STRING_SIZE] = L"";
UINT  ascent;                 // font family ascent in design units
REAL  ascentPixel;            // ascent converted to pixels
UINT  descent;                // font family descent in design units
REAL  descentPixel;           // descent converted to pixels
UINT  lineSpacing;            // font family line spacing in design units
REAL  lineSpacingPixel;       // line spacing converted to pixels
                       
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 16, FontStyleRegular, UnitPixel);
PointF       pointF(10.0f, 10.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 0));

// Display the font size in pixels.
StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE, 
   L"font.GetSize() returns %f.", font.GetSize());

graphics.DrawString(
   infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0);

// Display the font family em height in design units.
StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE, 
   L"fontFamily.GetEmHeight() returns %d.", 
   fontFamily.GetEmHeight(FontStyleRegular));

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down two lines.
pointF.Y += 2.0f * font.GetHeight(0.0f);

// Display the ascent in design units and pixels.
ascent = fontFamily.GetCellAscent(FontStyleRegular);

// 14.484375 = 16.0 * 1854 / 2048
ascentPixel = 
   font.GetSize() * ascent / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString,
   INFO_STRING_SIZE,
   L"The ascent is %d design units, %f pixels.",
   ascent, 
   ascentPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0f);

// Display the descent in design units and pixels.
descent = fontFamily.GetCellDescent(FontStyleRegular);

// 3.390625 = 16.0 * 434 / 2048
descentPixel = 
   font.GetSize() * descent / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE,
   L"The descent is %d design units, %f pixels.",
   descent, 
   descentPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0f);

// Display the line spacing in design units and pixels.
lineSpacing = fontFamily.GetLineSpacing(FontStyleRegular);

// 18.398438 = 16.0 * 2355 / 2048
lineSpacingPixel = 
   font.GetSize() * lineSpacing / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE,
   L"The line spacing is %d design units, %f pixels.",
   lineSpacing, 
   lineSpacingPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);
            
```



Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes.

![Screenshot eines Fensters mit Text, der die Schriftgröße und-Höhe angibt, und die Steigung, den Abstieg und den Zeilenabstand](images/fontstext8.png)

Beachten Sie die ersten beiden Zeilen der Ausgabe in der obigen Abbildung. Das [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) -Objekt gibt eine Größe von 16 zurück, und das [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) -Objekt gibt die EM-Höhe von 2.048 zurück. Diese beiden Zahlen (16 und 2.048) sind der Schlüssel für die Typumwandlung zwischen Schriftart Entwurfs Einheiten und den Einheiten (in diesem Fall Pixel) des **Schriftart** Objekts.

Beispielsweise können Sie den Aufstieg wie folgt von Entwurfs Einheiten in Pixel konvertieren:

![Gleichung, bei der 1854-Entwurfs Einheiten um 16 Pixel dividiert durch 2048-Entwurfs Einheiten, gleich 14,484375 Pixel, multipliziert werden.](images/fontstext9.png)

Der vorangehende Code positioniert Text vertikal, indem der *y* -Datenmember eines [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) -Objekts festgelegt wird. Die y-Koordinate wird von `font.GetHeight(0.0f)` für jede neue Textzeile um erweitert. Die [**Schriftart:: GetHeight**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-getheight(inreal)) -Methode eines [**Schriftart**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) Objekts gibt den Zeilenabstand (in Pixel) für das jeweilige **Schriftart** Objekt zurück. In diesem Beispiel ist die Zahl, die von **Font:: GetHeight** zurückgegeben wird, 18,398438. Beachten Sie, dass dies mit der Zahl übereinstimmt, die durch die Umstellung der Metrik für den Zeilenabstand in Pixel erreicht wird.

 

 
