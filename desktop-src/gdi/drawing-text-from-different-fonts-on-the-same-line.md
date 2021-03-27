---
description: Verschiedene typstile innerhalb einer Schriftfamilie können unterschiedliche Breiten aufweisen.
ms.assetid: d21613ef-1ba4-40bb-b922-afe287556441
title: Zeichnen von Text aus verschiedenen Schriftarten in derselben Zeile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2eae2a7a332bd929b9a965462ce802734679f9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215205"
---
# <a name="drawing-text-from-different-fonts-on-the-same-line"></a>Zeichnen von Text aus verschiedenen Schriftarten in derselben Zeile

Verschiedene typstile innerhalb einer Schriftfamilie können unterschiedliche Breiten aufweisen. Fett formatierte und kursiv formatierte Stile einer Familie sind z. b. für eine angegebene Punktgröße immer breiter als der römische Stil. Wenn Sie mehrere typstile in einer einzelnen Zeile anzeigen oder drucken, müssen Sie die Breite der Linie nachverfolgen, um zu vermeiden, dass Zeichen aufeinander angezeigt oder gedruckt werden.

Sie können zwei-Funktionen verwenden, um die Breite (oder den Umfang) von Text in der aktuellen Schriftart abzurufen. Die [gettabbedtextextent](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) -Funktion berechnet die Breite und Höhe einer Zeichenfolge. Wenn die Zeichenfolge ein oder mehrere Tabstopp Zeichen enthält, basiert die Breite der Zeichenfolge auf einem angegebenen Array von Tabstopp Positionen. Die [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) -Funktion berechnet die Breite und Höhe einer Textzeile.

Bei Bedarf synthetisiert das System eine Schriftart durch Ändern der Zeichen Bitmaps. Um ein Zeichen in einer Fett Schrift zu synthetisieren, zeichnet das System das Zeichen zweimal: am Anfangspunkt und erneut mit einem Pixel rechts vom Startpunkt. Um ein Zeichen in einer kursiv Formatierung zu erstellen, zeichnet das System zwei Zeilen von Pixeln am unteren Rand der Zeichen Zelle, verschiebt den Anfangspunkt um ein Pixel nach rechts, zeichnet die nächsten beiden Zeilen und wird fortgesetzt, bis das Zeichen gezeichnet wurde. Durch das Verschieben von Pixeln erscheint jedes Zeichen nach rechts. Die Anzahl der Scheren ist eine Funktion der Höhe des Zeichens.

Eine Möglichkeit, eine Textzeile zu schreiben, die mehrere Schriftarten enthält, besteht darin, die [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) -Funktion nach jedem aufzurufenden [Text aufzurufen](/windows/desktop/api/Wingdi/nf-wingdi-textouta) und die Länge einer aktuellen Position hinzuzufügen. Im folgenden Beispiel wird die Zeile "This is a sample string" geschrieben. Wenn Sie Fett formatierte Zeichen für "This is a" verwenden, wechselt zu "Sample" zu kursiv formatierten Zeichen und kehrt dann zu fett formatierten Zeichen für "String" zurück. Nach dem Drucken aller Zeichen folgen werden die System Standardzeichen wieder hergestellt.


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



In diesem Beispiel Initialisiert die [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) -Funktion die Elemente einer [Größen](/previous-versions//dd145106(v=vs.85)) Struktur mit der Länge und Höhe der angegebenen Zeichenfolge. Die [GetTextMetrics](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) -Funktion Ruft den Überlauf der aktuellen Schriftart ab. Da der Überhang 0 (null) ist, wenn die Schriftart eine TrueType-Schriftart ist, ändert der overstillstandwert die Zeichen folgen Platzierung nicht. Bei Raster Schriftarten ist es jedoch wichtig, den overstillstandwert zu verwenden.

Der über Hang wird einmal von der fett formatierten Zeichenfolge subtrahiert, um nachfolgende Zeichen näher am Ende der Zeichenfolge zu bringen, wenn die Schriftart eine Raster Schriftart ist. Da overhing sowohl den Anfang als auch das Ende der kursiv Zeichenfolge in einer Raster Schriftart beeinflusst, werden die Glyphen auf der rechten Seite des angegebenen Speicher Orts gestartet und Links vom Endpunkt der letzten Zeichen Zelle enden. (Die [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) -Funktion Ruft den Umfang der Zeichen Zellen ab, nicht den Block der Symbole.) Um den Überlauf in der kursiv formatiert-Zeichenfolge zu berücksichtigen, subtrahiert das Beispiel die Überschreibung vor dem Platzieren der Zeichenfolge und subtrahiert Sie, bevor nachfolgende Zeichen abgelegt werden.

Die [settextbegrün](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) gerfunktion fügt den Break-Zeichen in einer Textzeile zusätzlichen Platz hinzu. Sie können die [GetTextExtentPoint](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) -Funktion verwenden, um den Umfang einer Zeichenfolge zu bestimmen, dann den Block von der Gesamtmenge des Speicherplatzes, die die Zeile belegen soll, zu subtrahieren und mithilfe der [**settextbegrün dung**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) -Funktion den zusätzlichen Platz zwischen den Break-Zeichen in der Zeichenfolge zu verteilen. Die Funktion " [settextcharacter extra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) " fügt jeder Zeichen Zelle in der ausgewählten Schriftart, einschließlich des Break-Zeichens, zusätzlichen Platz hinzu. (Sie können die [gettextcharacter extra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) -Funktion verwenden, um die aktuelle Menge an zusätzlichem Speicherplatz zu ermitteln, der den Zeichen Zellen hinzugefügt wird. die Standardeinstellung ist 0 (null).)

Sie können Zeichen mit größerer Genauigkeit platzieren, indem Sie die [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) -Funktion oder die [getcharabcbreiten](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) -Funktion verwenden, um die Breite der einzelnen Zeichen in einer Schriftart abzurufen. Die [**getcharabcbreiten**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) -Funktion ist präziser als die [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) -Funktion, aber Sie kann nur mit TrueType-Schriftarten verwendet werden.

Der ABC-Abstand ermöglicht es einer Anwendung auch, eine sehr genaue Textausrichtung auszuführen. Wenn die Anwendung z. b. eine Raster römische Schriftart ohne Verwendung von ABC-Abstand anpasst, wird die erweiterte Breite als Zeichenbreite berechnet. Dies bedeutet, dass der Leerraum rechts neben dem Symbol in der Bitmap ausgerichtet ist, nicht jedoch das Symbol selbst. Durch die Verwendung von ABC-breiten haben Anwendungen bei der Ausrichtung von Text mehr Flexibilität bei der Platzierung und Entfernung von Leerraum, da Sie über Informationen verfügen, mit denen Sie den Abstand zwischen Zeichen fein steuern können.

 

 
