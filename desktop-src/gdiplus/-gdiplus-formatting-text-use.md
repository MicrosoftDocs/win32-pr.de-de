---
description: Um eine spezielle Formatierung auf Text anzuwenden, initialisieren Sie ein StringFormat-Objekt, und übergeben Sie die Adresse dieses Objekts an die DrawString-Methode der Grafikklasse.
ms.assetid: 4014a602-88f6-4fac-b4b2-3dafdcff8f33
title: Formatieren von Text (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6b2cc6109e7b946e9b4e98645c9445b8268bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551271"
---
# <a name="formatting-text-gdi"></a>Formatieren von Text (GDI+)

Um eine spezielle Formatierung auf Text anzuwenden, initialisieren Sie ein [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) -Objekt, und übergeben Sie die Adresse dieses Objekts an die [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) -Methode der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse.

Um formatierten Text in einem Rechteck zu zeichnen, benötigen Sie [**Grafiken**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)-, [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font)-, [**RectF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rectf)-, [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)-und [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) -Objekte.

-   [Ausrichten von Text](#aligning-text)
-   [Festlegen von Tabstopps](#setting-tab-stops)
-   [Zeichnen von vertikaler Text](#drawing-vertical-text)

## <a name="aligning-text"></a>Ausrichten von Text

Im folgenden Beispiel wird Text in einem Rechteck gezeichnet. Jede Textzeile wird zentriert (Seite zu Seite), und der gesamte TextBlock wird im Rechteck zentriert (von oben nach unten) zentriert.


```
WCHAR string[] = 
   L"Use StringFormat and RectF objects to center text in a rectangle.";
                       
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 12, FontStyleBold, UnitPoint);
RectF        rectF(30.0f, 10.0f, 120.0f, 140.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));

// Center-justify each line of text.
stringFormat.SetAlignment(StringAlignmentCenter);

// Center the block of text (top to bottom) in the rectangle.
stringFormat.SetLineAlignment(StringAlignmentCenter);

graphics.DrawString(string, -1, &font, rectF, &stringFormat, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
            
```



In der folgenden Abbildung werden das Rechteck und der zentrierte Text gezeigt.

![Screenshot eines Fensters mit einem Rechteck, das sechs Textzeilen enthält, die horizontal zentriert sind](images/fontstext3.png)

Der vorangehende Code ruft zwei Methoden des [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) -Objekts auf: [**StringFormat:: SetAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setalignment) und [**StringFormat:: setlinealignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setlinealignment). Der Befehl **StringFormat:: SetAlignment** gibt an, dass jede Textzeile in dem Rechteck zentriert wird, das durch das dritte an die [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) -Methode über gegebene Argument angegeben wird. Der Befehl **StringFormat:: setlinealignment** gibt an, dass der TextBlock im Rechteck zentriert (von oben nach unten) zentriert wird.

Der Wert [* * * * stringalignmentcenter * * * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringalignment) ist ein Element der **StringAlignment** -Enumeration, das in "gdiplusenums. h" deklariert wird.

## <a name="setting-tab-stops"></a>Festlegen von Tabstopps

Sie können Tabstopps für Text festlegen, indem Sie [**die StringFormat:: settabstopps**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) -Methode eines [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) -Objekts aufrufen und dann die Adresse dieses **StringFormat** -Objekts an die [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) -Methode der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse übergeben.

Im folgenden Beispiel wird der Tabstopp bei 150, 250 und 350 festgelegt. Im Code wird dann eine Liste der Namen und Testergebnisse im Registerkarten Format angezeigt.


```
WCHAR string[150] = 
   L"Name\tTest 1\tTest 2\tTest 3\n";

StringCchCatW(string, 150, L"Joe\t95\t88\t91\n");
StringCchCatW(string, 150, L"Mary\t98\t84\t90\n");
StringCchCatW(string, 150, L"Sam\t42\t76\t98\n");
StringCchCatW(string, 150, L"Jane\t65\t73\t92\n");
                       
FontFamily   fontFamily(L"Courier New");
Font         font(&fontFamily, 12, FontStyleRegular, UnitPoint);
RectF        rectF(10.0f, 10.0f, 450.0f, 100.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));
REAL         tabs[] = {150.0f, 100.0f, 100.0f};

stringFormat.SetTabStops(0.0f, 3, tabs);

graphics.DrawString(string, -1, &font, rectF, &stringFormat, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
            
```



Die folgende Abbildung zeigt den Text im Registerkarten Format.

![Abbildung eines Rechtecks, das vier Textspalten enthält. jede Spalte ist linksbündig.](images/fontstext4.png)

Der vorangehende Code übergibt drei Argumente an die [**StringFormat:: SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) -Methode. Das dritte Argument ist die Adresse eines Arrays, das die Tabulator Offsets enthält. Das zweite Argument gibt an, dass es drei Offsets in diesem Array gibt. Das erste Argument, das an **StringFormat:: settabstopps** übergeben wird, ist 0 (null) und gibt an, dass der erste Offset im Array von Position 0, dem linken Rand des umgebenden Rechtecks, gemessen wird.

## <a name="drawing-vertical-text"></a>Zeichnen von vertikaler Text

Sie können ein [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) -Objekt verwenden, um anzugeben, dass Text vertikal und nicht horizontal gezeichnet werden soll.

Im folgenden Beispiel wird der Wert [* * * * stringformatflagsdirectionvertical * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) * * an die [**StringFormat:: setformatflags**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setformatflags) -Methode eines [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) -Objekts übergeben. Die Adresse dieses **StringFormat** -Objekts wird an die [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) -Methode der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse übergeben. Der Wert [* * * * stringformatflagsdirectionvertical * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) * * ist ein Element der **StringFormatFlags** -Enumeration, das in "gdiplusenums. h" deklariert wird.


```
WCHAR string[] = L"Vertical text";
                     
FontFamily   fontFamily(L"Lucida Console");
Font         font(&fontFamily, 14, FontStyleRegular, UnitPoint);
PointF       pointF(40.0f, 10.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));

stringFormat.SetFormatFlags(StringFormatFlagsDirectionVertical);

graphics.DrawString(string, -1, &font, pointF, &stringFormat, &solidBrush);
            
```



In der folgenden Abbildung ist der vertikale Text dargestellt.

![Abbildung mit einem Fenster, das im Uhrzeigersinn 90 gedreht Text enthält](images/fontstext5.png)

 

 



