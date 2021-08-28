---
description: Sie können die DrawString-Methode der Graphics-Klasse verwenden, um Text an einer angegebenen Position oder innerhalb eines angegebenen Rechtecks zu zeichnen.
ms.assetid: a873c132-f232-4144-bcc3-ca200055074c
title: Zeichnen von Text (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31591d62198bc6ff72cdd7cce0d8ab515dc0e96011457b5bccd601a59ee0293f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115040"
---
# <a name="drawing-text-gdi"></a>Zeichnen von Text (GDI+)

Sie können die [DrawString-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) der [**Graphics-Klasse**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) verwenden, um Text an einer angegebenen Position oder innerhalb eines angegebenen Rechtecks zu zeichnen.

-   [Zeichnen von Text an einer angegebenen Position](#drawing-text-at-a-specified-location)
-   [Zeichnen von Text in einem Rechteck](#drawing-text-in-a-rectangle)

## <a name="drawing-text-at-a-specified-location"></a>Zeichnen von Text an einer angegebenen Position

Um Text an einer angegebenen Position zu zeichnen, benötigen Sie [**Grafik-,**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) [**FontFamily-,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) [**Font-,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) [**PointF-**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf)und [**Brush-Objekte.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush)

Im folgenden Beispiel wird die Zeichenfolge "Hello" am Speicherort (30, 10) zeichnet. Die Schriftfamilie ist Times New Roman. Die Schriftart, die ein einzelnes Element der Schriftfamilie ist, ist Times New Roman, Größe 24 Pixel, regulärer Stil. Angenommen, **Grafik** ist ein vorhandenes [**Graphics-Objekt.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)

```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
PointF      pointF(30.0f, 10.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(L"Hello", -1, &font, pointF, &solidBrush);

```

Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes.

![Screenshot eines kleinen Fensters mit dem Text "hello"](images/fontstext1.png)

Im vorherigen Beispiel empfängt der [**FontFamily-Konstruktor**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) eine Zeichenfolge, die die Schriftfamilie identifiziert. Die Adresse des **FontFamily-Objekts** wird als erstes Argument an den [**Font-Konstruktor**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) übergeben. Das zweite Argument, das an den **Font-Konstruktor** übergeben wird, gibt die Größe der Schriftart an, die in Einheiten gemessen wird, die vom vierten Argument angegeben werden. Das dritte Argument gibt den Stil (normal, fett, kursiv usw.) der Schriftart an.

Die [DrawString-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) empfängt fünf Argumente. Das erste Argument ist die zu zeichnende Zeichenfolge, und das zweite Argument ist die Länge (in Zeichen, nicht in Bytes) dieser Zeichenfolge. Wenn die Zeichenfolge NULL-terminiert ist, können Sie –1 für die Länge übergeben. Das dritte Argument ist die Adresse des [**Font-Objekts,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) das zuvor erstellt wurde. Das vierte Argument ist ein [**PointF-Objekt,**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) das die Koordinaten der oberen linken Ecke der Zeichenfolge enthält. Das fünfte Argument ist die Adresse eines [**SolidBrush-Objekts,**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) das zum Füllen der Zeichen der Zeichenfolge verwendet wird.

## <a name="drawing-text-in-a-rectangle"></a>Zeichnen von Text in einem Rechteck

Eine der [**DrawString-Methoden**](https://www.bing.com/search?q=**DrawString**) der [**Graphics-Klasse**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) verfügt über einen *RectF-Parameter.* Durch Aufrufen dieser **DrawString-Methode** können Sie Text zeichnen, der in einem angegebenen Rechteck umbrochen wird. Um Text in einem Rechteck zu zeichnen, benötigen Sie **Graphics-,** [**FontFamily-,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) [**Font-,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) [**RectF-**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf)und [**Brush-Objekte.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush)

Im folgenden Beispiel wird ein Rechteck mit der oberen linken Ecke (30, 10), der Breite 100 und der Höhe 122 erstellt. Anschließend zeichnet der Code eine Zeichenfolge innerhalb dieses Rechtecks. Die Zeichenfolge ist auf das Rechteck beschränkt und umschließt so, dass einzelne Wörter nicht unterbrochen werden.

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

![Screenshot eines kleinen Fensters mit einer Verschränkung, in dem der erste Teil eines Satzes angezeigt wird](images/fontstext2.png)

Im vorherigen Beispiel ist das vierte Argument, das an die [**DrawString-Methode**](https://www.bing.com/search?q=**DrawString**) übergeben wird, ein [**RectF-Objekt,**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf) das das umgebende Rechteck für den Text angibt. Der fünfte Parameter ist vom Typ [**StringFormat.**](/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)Das Argument ist **NULL,** da keine spezielle Zeichenfolgenformatierung erforderlich ist.
