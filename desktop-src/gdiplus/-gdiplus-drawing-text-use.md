---
description: Sie können die DrawString-Methode der Grafikklasse verwenden, um Text an einer angegebenen Position oder innerhalb eines angegebenen Rechtecks zu zeichnen.
ms.assetid: a873c132-f232-4144-bcc3-ca200055074c
title: Zeichnen von Text (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e16ed49a5ab92380b42ed3316346ac547f95be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131348"
---
# <a name="drawing-text-gdi"></a>Zeichnen von Text (GDI+)

Sie können die [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) -Methode der [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse verwenden, um Text an einer angegebenen Position oder innerhalb eines angegebenen Rechtecks zu zeichnen.

-   [Zeichnen von Text an einer angegebenen Position](#drawing-text-at-a-specified-location)
-   [Zeichnen von Text in einem Rechteck](#drawing-text-in-a-rectangle)

## <a name="drawing-text-at-a-specified-location"></a>Zeichnen von Text an einer angegebenen Position

Zum Zeichnen von Text an einer angegebenen Position benötigen Sie [**Grafiken**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)-, [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font)-, [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf)-und [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) -Objekte.

Im folgenden Beispiel wird die Zeichenfolge "Hello" an Position (30, 10) gezeichnet. Die Schriftfamilie ist Times New Roman. Die Schriftart, bei der es sich um einen einzelnen Member der Schriftfamilie handelt, ist Times New Roman, die Größe 24 Pixel, regulärer Stil. Angenommen, die **Grafik** ist ein vorhandenes [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt.

```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
PointF      pointF(30.0f, 10.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(L"Hello", -1, &font, pointF, &solidBrush);

```

Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes.

![Screenshot eines kleinen Fensters mit dem Text "Hello"](images/fontstext1.png)

Im vorherigen Beispiel erhält der [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) -Konstruktor eine Zeichenfolge, die die Schriftfamilie identifiziert. Die Adresse des **FontFamily** -Objekts wird als erstes Argument an den [**Schriftart**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) -Konstruktor übergeben. Das zweite Argument, das an den **Schriftart** -Konstruktor übergeben wird, gibt die Größe der Schriftart an, gemessen in Einheiten, die vom vierten Argument angegeben werden. Das dritte Argument gibt den Stil der Schriftart an (regulär, Fett, kursiv usw.).

Die [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) -Methode empfängt fünf Argumente. Das erste Argument ist die Zeichenfolge, die gezeichnet werden soll, und das zweite Argument ist die Länge (in Zeichen, nicht Bytes) dieser Zeichenfolge. Wenn die Zeichenfolge NULL-terminiert ist, können Sie – 1 als Länge übergeben. Das dritte Argument ist die Adresse des zuvor erstellten [**Schriftart**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) Objekts. Das vierte Argument ist ein [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) -Objekt, das die Koordinaten der linken oberen Ecke der Zeichenfolge enthält. Das fünfte Argument ist die Adresse eines [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) -Objekts, das zum Ausfüllen der Zeichen der Zeichenfolge verwendet wird.

## <a name="drawing-text-in-a-rectangle"></a>Zeichnen von Text in einem Rechteck

Eine der [**DrawString**](https://www.bing.com/search?q=**DrawString**) -Methoden der [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse verfügt über einen *RectF* -Parameter. Indem Sie diese **DrawString** -Methode aufrufen, können Sie Text zeichnen, der in einem angegebenen Rechteck umbrochen wird. Zum Zeichnen von Text in einem Rechteck benötigen Sie **Grafiken**, [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)-, [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font)-, [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf)-und [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) -Objekte.

Im folgenden Beispiel wird ein Rechteck mit der oberen linken Ecke (30, 10), der Breite 100 und der Höhe 122 erstellt. Anschließend zeichnet der Code eine Zeichenfolge innerhalb dieses Rechtecks. Die Zeichenfolge ist auf das Rechteck beschränkt und wird so umschlossen, dass einzelne Wörter nicht beschädigt werden.

```
WCHAR string[] = 
   L"Draw text in a rectangle by passing a RectF to the DrawString method.";

FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 12, FontStyleBold, UnitPoint);
RectF        rectF(30.0f, 10.0f, 100.0f, 122.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(string, -1, &font, rectF, NULL, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
```

Die folgende Abbildung zeigt den im Rechteck gezeichneten Text.

![Screenshot eines kleinen Fensters mit einem Winkel, in dem der erste Teil eines Satzes angezeigt wird](images/fontstext2.png)

Im vorherigen Beispiel ist das vierte Argument, das an die [**DrawString**](https://www.bing.com/search?q=**DrawString**) -Methode übermittelt wurde, ein [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf) -Objekt, das das umgebende Rechteck für den Text angibt. Der fünfte Parameter weist den Typ [**StringFormat**](/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)auf – das Argument ist **null** , da keine besondere Zeichen folgen Formatierung erforderlich ist.
