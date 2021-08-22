---
description: Unterschiedliche Typstile innerhalb einer Schriftfamilie können unterschiedliche Breiten aufweisen.
ms.assetid: d21613ef-1ba4-40bb-b922-afe287556441
title: Zeichnen von Text aus verschiedenen Schriftarten in derselben Zeile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad28f13c94e568073504f07e8722e5d688cb12aa1b376b0f52fad752574e6f8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038048"
---
# <a name="drawing-text-from-different-fonts-on-the-same-line"></a>Zeichnen von Text aus verschiedenen Schriftarten in derselben Zeile

Unterschiedliche Typstile innerhalb einer Schriftfamilie können unterschiedliche Breiten aufweisen. Fett- und kursiv formatierte Stile einer Familie sind beispielsweise immer breiter als der lateinische Stil für eine angegebene Punktgröße. Wenn Sie mehrere Typformate in einer einzelnen Zeile anzeigen oder drucken, müssen Sie die Breite der Zeile nachverfolgen, um zu vermeiden, dass Zeichen angezeigt oder übereinander gedruckt werden.

Sie können zwei Funktionen verwenden, um die Breite (oder den Umfang) von Text in der aktuellen Schriftart abzurufen. Die [GetTabbedTextExtent-Funktion](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) berechnet die Breite und Höhe einer Zeichenfolge. Wenn die Zeichenfolge ein oder mehrere Tabstoppzeichen enthält, basiert die Breite der Zeichenfolge auf einem angegebenen Array von Tabstopppositionen. Die [GetTextExtentPoint32-Funktion](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) berechnet die Breite und Höhe einer Textzeile.

Bei Bedarf synthetisiert das System eine Schriftart, indem die Zeichenbitmaps geändert werden. Um ein Zeichen in fetter Schrift zu synthetisieren, zeichnet das System das Zeichen zweimal: am Anfangspunkt und erneut ein Pixel rechts vom Anfangspunkt. Um ein Zeichen in einer italischen Schriftart zu synthetisieren, zeichnet das System zwei Pixelzeilen am unteren Rand der Zeichenzelle, verschiebt den Startpunkt um ein Pixel nach rechts, zeichnet die nächsten beiden Zeilen und fährt fort, bis das Zeichen gezeichnet wurde. Durch Verschieben von Pixeln scheint jedes Zeichen nach rechts zu schubsen. Der Schrarwert ist eine Funktion der Höhe des Zeichens.

Eine Möglichkeit zum Schreiben einer Textzeile, die mehrere Schriftarten enthält, besteht darin, die [**GetTextExtentPoint32-Funktion**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) nach jedem Aufruf von [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) zu verwenden und die Länge einer aktuellen Position hinzuzufügen. Im folgenden Beispiel wird die Zeile "This is a sample string" (Dies ist eine Beispielzeichenfolge) geschrieben. mit fett formatiertem Zeichen für "This is a" wechselt zu kursiven Zeichen für "sample" und kehrt dann zu fett formatierte Zeichen für "string" zurück. Nachdem alle Zeichenfolgen gedruckt wurden, werden die Standardzeichen des Systems wiederhergestellt.


```C++
int XIncrement; 
int YStart; 
TEXTMETRIC tm; 
HFONT hfntDefault, hfntItalic, hfntBold; 
SIZE sz; 
LPSTR lpszString1 = "This is a "; 
LPSTR lpszString2 = "sample "; 
LPSTR lpszString3 = "string."; 
HRESULT hr;
size_t * pcch;
 
// Create a bold and an italic logical font.  
 
hfntItalic = MyCreateFont(); 
hfntBold = MyCreateFont(); 
 
 
// Select the bold font and draw the first string  
// beginning at the specified point (XIncrement, YStart).  
 
XIncrement = 10; 
YStart = 50; 
hfntDefault = SelectObject(hdc, hfntBold); 
hr = StringCchLength(lpszString1, 11, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
TextOut(hdc, XIncrement, YStart, lpszString1, *pcch); 
 
// Compute the length of the first string and add  
// this value to the x-increment that is used for the  
// text-output operation.  

hr = StringCchLength(lpszString1, 11, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
GetTextExtentPoint32(hdc, lpszString1, *pcch, &sz); 
XIncrement += sz.cx; 
 
// Retrieve the overhang value from the TEXTMETRIC  
// structure and subtract it from the x-increment.  
// (This is only necessary for non-TrueType raster  
// fonts.)  
 
GetTextMetrics(hdc, &tm); 
XIncrement -= tm.tmOverhang; 
 
// Select an italic font and draw the second string  
// beginning at the point (XIncrement, YStart).  
 
hfntBold = SelectObject(hdc, hfntItalic); 
GetTextMetrics(hdc, &tm); 
XIncrement -= tm.tmOverhang;
hr = StringCchLength(lpszString2, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
TextOut(hdc, XIncrement, YStart, lpszString2, *pcch); 
 
// Compute the length of the second string and add  
// this value to the x-increment that is used for the  
// text-output operation.  

hr = StringCchLength(lpszString2, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }  
GetTextExtentPoint32(hdc, lpszString2, *pcch, &sz); 
XIncrement += sz.cx; 
 
// Reselect the bold font and draw the third string  
// beginning at the point (XIncrement, YStart).  
 
SelectObject(hdc, hfntBold);
hr = StringCchLength(lpszString3, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }  
TextOut(hdc, XIncrement - tm.tmOverhang, YStart, lpszString3, 
            *pcch); 
 
// Reselect the original font.  
 
SelectObject(hdc, hfntDefault); 
 
// Delete the bold and italic fonts.  
 
DeleteObject(hfntItalic); 
DeleteObject(hfntBold); 
```



In diesem Beispiel initialisiert die [GetTextExtentPoint32-Funktion](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) die Member einer [SIZE-Struktur](/previous-versions//dd145106(v=vs.85)) mit der Länge und Höhe der angegebenen Zeichenfolge. Die [GetTextMetrics-Funktion](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) ruft den Überhänge für die aktuelle Schriftart ab. Da der Überhänge null ist, wenn es sich bei der Schriftart um eine TrueType-Schriftart handelt, ändert der Überhängewert die Zeichenfolgenplatzierung nicht. Für Rasterschriftarten ist es jedoch wichtig, den Überhängewert zu verwenden.

Der Überhang wird einmal von der fett formatierten Zeichenfolge subtrahiert, um nachfolgende Zeichen näher an das Ende der Zeichenfolge zu bringen, wenn es sich bei der Schriftart um eine Rasterschriftart handelt. Da sich overhang sowohl auf den Anfang als auch auf das Ende der italischen Zeichenfolge in einer Rasterschriftart auswirkt, beginnen die Glyphen rechts von der angegebenen Position und enden links vom Endpunkt der letzten Zeichenzelle. (Die [**GetTextExtentPoint32-Funktion**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) ruft den Umfang der Zeichenzellen ab, nicht den Umfang der Glyphen.) Um den Überhang in der italischen Rasterzeichenfolge zu berücksichtigen, subtrahiert das Beispiel den Überhang vor dem Platzieren der Zeichenfolge und subtrahiert sie erneut, bevor nachfolgende Zeichen platziert werden.

Die [SetTextJustification-Funktion](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) fügt den Unterbrechungszeichen in einer Textzeile zusätzlichen Platz hinzu. Sie können die [GetTextExtentPoint-Funktion](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) verwenden, um den Umfang einer Zeichenfolge zu bestimmen, diesen Wert dann von der Gesamtmenge des Speicherplatzes subtrahieren, den die Zeile belegen soll, und die [**SetTextJustification-Funktion**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) verwenden, um den zusätzlichen Platz auf die Haltezeichen in der Zeichenfolge zu verteilen. Die [SetTextCharacterExtra-Funktion](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) fügt jeder Zeichenzelle in der ausgewählten Schriftart zusätzlichen Platz hinzu, einschließlich des Haltezeichens. (Sie können die [GetTextCharacterExtra-Funktion](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) verwenden, um die aktuelle Menge an zusätzlichem Speicherplatz zu bestimmen, die den Zeichenzellen hinzugefügt wird. Die Standardeinstellung ist 0 (null).

Sie können Zeichen mit höherer Genauigkeit platzieren, indem Sie die [GetCharWidth32-](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) oder [GetCharABCWidths-Funktion](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) verwenden, um die Breite einzelner Zeichen in einer Schriftart abzurufen. Die [**GetCharABCWidths-Funktion**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) ist genauer als die [**GetCharWidth32-Funktion,**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) kann aber nur mit TrueType-Schriftarten verwendet werden.

Der ABC-Abstand ermöglicht einer Anwendung auch eine sehr genaue Textausrichtung. Wenn die Anwendung z. B. eine Rasterschriftart rechts ausrichtet, ohne ABC-Abstände zu verwenden, wird die Vorbreite als Zeichenbreite berechnet. Dies bedeutet, dass der Leerraum rechts neben dem Symbol in der Bitmap ausgerichtet ist, nicht das Symbol selbst. Durch die Verwendung von ABC-Breiten haben Anwendungen mehr Flexibilität bei der Platzierung und Entfernung von Leerzeichen beim Ausrichten von Text, da sie Informationen haben, mit denen sie den Abstand zwischen Zeichen präzise steuern können.

 

 
