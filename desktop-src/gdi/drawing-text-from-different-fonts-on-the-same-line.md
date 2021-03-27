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
# <a name="drawing-text-from-different-fonts-on-the-same-line"></a><span data-ttu-id="585a7-103">Zeichnen von Text aus verschiedenen Schriftarten in derselben Zeile</span><span class="sxs-lookup"><span data-stu-id="585a7-103">Drawing Text from Different Fonts on the Same Line</span></span>

<span data-ttu-id="585a7-104">Verschiedene typstile innerhalb einer Schriftfamilie können unterschiedliche Breiten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="585a7-104">Different type styles within a font family can have different widths.</span></span> <span data-ttu-id="585a7-105">Fett formatierte und kursiv formatierte Stile einer Familie sind z. b. für eine angegebene Punktgröße immer breiter als der römische Stil.</span><span class="sxs-lookup"><span data-stu-id="585a7-105">For example, bold and italic styles of a family are always wider than the roman style for a specified point size.</span></span> <span data-ttu-id="585a7-106">Wenn Sie mehrere typstile in einer einzelnen Zeile anzeigen oder drucken, müssen Sie die Breite der Linie nachverfolgen, um zu vermeiden, dass Zeichen aufeinander angezeigt oder gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="585a7-106">When you display or print several type styles on a single line, you must keep track of the width of the line to avoid having characters displayed or printed on top of one another.</span></span>

<span data-ttu-id="585a7-107">Sie können zwei-Funktionen verwenden, um die Breite (oder den Umfang) von Text in der aktuellen Schriftart abzurufen.</span><span class="sxs-lookup"><span data-stu-id="585a7-107">You can use two functions to retrieve the width (or extent) of text in the current font.</span></span> <span data-ttu-id="585a7-108">Die [gettabbedtextextent](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) -Funktion berechnet die Breite und Höhe einer Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="585a7-108">The [GetTabbedTextExtent](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) function computes the width and height of a character string.</span></span> <span data-ttu-id="585a7-109">Wenn die Zeichenfolge ein oder mehrere Tabstopp Zeichen enthält, basiert die Breite der Zeichenfolge auf einem angegebenen Array von Tabstopp Positionen.</span><span class="sxs-lookup"><span data-stu-id="585a7-109">If the string contains one or more tab characters, the width of the string is based upon a specified array of tab-stop positions.</span></span> <span data-ttu-id="585a7-110">Die [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) -Funktion berechnet die Breite und Höhe einer Textzeile.</span><span class="sxs-lookup"><span data-stu-id="585a7-110">The [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) function computes the width and height of a line of text.</span></span>

<span data-ttu-id="585a7-111">Bei Bedarf synthetisiert das System eine Schriftart durch Ändern der Zeichen Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="585a7-111">When necessary, the system synthesizes a font by changing the character bitmaps.</span></span> <span data-ttu-id="585a7-112">Um ein Zeichen in einer Fett Schrift zu synthetisieren, zeichnet das System das Zeichen zweimal: am Anfangspunkt und erneut mit einem Pixel rechts vom Startpunkt.</span><span class="sxs-lookup"><span data-stu-id="585a7-112">To synthesize a character in a bold font, the system draws the character twice: at the starting point, and again one pixel to the right of the starting point.</span></span> <span data-ttu-id="585a7-113">Um ein Zeichen in einer kursiv Formatierung zu erstellen, zeichnet das System zwei Zeilen von Pixeln am unteren Rand der Zeichen Zelle, verschiebt den Anfangspunkt um ein Pixel nach rechts, zeichnet die nächsten beiden Zeilen und wird fortgesetzt, bis das Zeichen gezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="585a7-113">To synthesize a character in an italic font, the system draws two rows of pixels at the bottom of the character cell, moves the starting point one pixel to the right, draws the next two rows, and continues until the character has been drawn.</span></span> <span data-ttu-id="585a7-114">Durch das Verschieben von Pixeln erscheint jedes Zeichen nach rechts.</span><span class="sxs-lookup"><span data-stu-id="585a7-114">By shifting pixels, each character appears to be sheared to the right.</span></span> <span data-ttu-id="585a7-115">Die Anzahl der Scheren ist eine Funktion der Höhe des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="585a7-115">The amount of shear is a function of the height of the character.</span></span>

<span data-ttu-id="585a7-116">Eine Möglichkeit, eine Textzeile zu schreiben, die mehrere Schriftarten enthält, besteht darin, die [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) -Funktion nach jedem aufzurufenden [Text aufzurufen](/windows/desktop/api/Wingdi/nf-wingdi-textouta) und die Länge einer aktuellen Position hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="585a7-116">One way to write a line of text that contains multiple fonts is to use the [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) function after each call to [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) and add the length to a current position.</span></span> <span data-ttu-id="585a7-117">Im folgenden Beispiel wird die Zeile "This is a sample string" geschrieben.</span><span class="sxs-lookup"><span data-stu-id="585a7-117">The following example writes the line "This is a sample string."</span></span> <span data-ttu-id="585a7-118">Wenn Sie Fett formatierte Zeichen für "This is a" verwenden, wechselt zu "Sample" zu kursiv formatierten Zeichen und kehrt dann zu fett formatierten Zeichen für "String" zurück.</span><span class="sxs-lookup"><span data-stu-id="585a7-118">using bold characters for "This is a", switches to italic characters for "sample", then returns to bold characters for "string."</span></span> <span data-ttu-id="585a7-119">Nach dem Drucken aller Zeichen folgen werden die System Standardzeichen wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="585a7-119">After printing all the strings, it restores the system default characters.</span></span>


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



<span data-ttu-id="585a7-120">In diesem Beispiel Initialisiert die [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) -Funktion die Elemente einer [Größen](/previous-versions//dd145106(v=vs.85)) Struktur mit der Länge und Höhe der angegebenen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="585a7-120">In this example, the [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) function initializes the members of a [SIZE](/previous-versions//dd145106(v=vs.85)) structure with the length and height of the specified string.</span></span> <span data-ttu-id="585a7-121">Die [GetTextMetrics](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) -Funktion Ruft den Überlauf der aktuellen Schriftart ab.</span><span class="sxs-lookup"><span data-stu-id="585a7-121">The [GetTextMetrics](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) function retrieves the overhang for the current font.</span></span> <span data-ttu-id="585a7-122">Da der Überhang 0 (null) ist, wenn die Schriftart eine TrueType-Schriftart ist, ändert der overstillstandwert die Zeichen folgen Platzierung nicht.</span><span class="sxs-lookup"><span data-stu-id="585a7-122">Because the overhang is zero if the font is a TrueType font, the overhang value does not change the string placement.</span></span> <span data-ttu-id="585a7-123">Bei Raster Schriftarten ist es jedoch wichtig, den overstillstandwert zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="585a7-123">For raster fonts, however, it is important to use the overhang value.</span></span>

<span data-ttu-id="585a7-124">Der über Hang wird einmal von der fett formatierten Zeichenfolge subtrahiert, um nachfolgende Zeichen näher am Ende der Zeichenfolge zu bringen, wenn die Schriftart eine Raster Schriftart ist.</span><span class="sxs-lookup"><span data-stu-id="585a7-124">The overhang is subtracted from the bold string once, to bring subsequent characters closer to the end of the string if the font is a raster font.</span></span> <span data-ttu-id="585a7-125">Da overhing sowohl den Anfang als auch das Ende der kursiv Zeichenfolge in einer Raster Schriftart beeinflusst, werden die Glyphen auf der rechten Seite des angegebenen Speicher Orts gestartet und Links vom Endpunkt der letzten Zeichen Zelle enden.</span><span class="sxs-lookup"><span data-stu-id="585a7-125">Because overhang affects both the beginning and end of the italic string in a raster font, the glyphs start at the right of the specified location and end at the left of the endpoint of the last character cell.</span></span> <span data-ttu-id="585a7-126">(Die [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) -Funktion Ruft den Umfang der Zeichen Zellen ab, nicht den Block der Symbole.) Um den Überlauf in der kursiv formatiert-Zeichenfolge zu berücksichtigen, subtrahiert das Beispiel die Überschreibung vor dem Platzieren der Zeichenfolge und subtrahiert Sie, bevor nachfolgende Zeichen abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="585a7-126">(The [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) function retrieves the extent of the character cells, not the extent of the glyphs.) To account for the overhang in the raster italic string, the example subtracts the overhang before placing the string and subtracts it again before placing subsequent characters.</span></span>

<span data-ttu-id="585a7-127">Die [settextbegrün](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) gerfunktion fügt den Break-Zeichen in einer Textzeile zusätzlichen Platz hinzu.</span><span class="sxs-lookup"><span data-stu-id="585a7-127">The [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) function adds extra space to the break characters in a line of text.</span></span> <span data-ttu-id="585a7-128">Sie können die [GetTextExtentPoint](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) -Funktion verwenden, um den Umfang einer Zeichenfolge zu bestimmen, dann den Block von der Gesamtmenge des Speicherplatzes, die die Zeile belegen soll, zu subtrahieren und mithilfe der [**settextbegrün dung**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) -Funktion den zusätzlichen Platz zwischen den Break-Zeichen in der Zeichenfolge zu verteilen.</span><span class="sxs-lookup"><span data-stu-id="585a7-128">You can use the [GetTextExtentPoint](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) function to determine the extent of a string, then subtract that extent from the total amount of space the line should occupy, and use the [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) function to distribute the extra space among the break characters in the string.</span></span> <span data-ttu-id="585a7-129">Die Funktion " [settextcharacter extra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) " fügt jeder Zeichen Zelle in der ausgewählten Schriftart, einschließlich des Break-Zeichens, zusätzlichen Platz hinzu.</span><span class="sxs-lookup"><span data-stu-id="585a7-129">The [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) function adds extra space to every character cell in the selected font, including the break character.</span></span> <span data-ttu-id="585a7-130">(Sie können die [gettextcharacter extra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) -Funktion verwenden, um die aktuelle Menge an zusätzlichem Speicherplatz zu ermitteln, der den Zeichen Zellen hinzugefügt wird. die Standardeinstellung ist 0 (null).)</span><span class="sxs-lookup"><span data-stu-id="585a7-130">(You can use the [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) function to determine the current amount of extra space being added to the character cells; the default setting is zero.)</span></span>

<span data-ttu-id="585a7-131">Sie können Zeichen mit größerer Genauigkeit platzieren, indem Sie die [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) -Funktion oder die [getcharabcbreiten](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) -Funktion verwenden, um die Breite der einzelnen Zeichen in einer Schriftart abzurufen.</span><span class="sxs-lookup"><span data-stu-id="585a7-131">You can place characters with greater precision by using the [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) or [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) function to retrieve the widths of individual characters in a font.</span></span> <span data-ttu-id="585a7-132">Die [**getcharabcbreiten**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) -Funktion ist präziser als die [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) -Funktion, aber Sie kann nur mit TrueType-Schriftarten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="585a7-132">The [**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) function is more accurate than the [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) function, but it can only be used with TrueType fonts.</span></span>

<span data-ttu-id="585a7-133">Der ABC-Abstand ermöglicht es einer Anwendung auch, eine sehr genaue Textausrichtung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="585a7-133">ABC spacing also allows an application to perform very accurate text alignment.</span></span> <span data-ttu-id="585a7-134">Wenn die Anwendung z. b. eine Raster römische Schriftart ohne Verwendung von ABC-Abstand anpasst, wird die erweiterte Breite als Zeichenbreite berechnet.</span><span class="sxs-lookup"><span data-stu-id="585a7-134">For example, when the application right aligns a raster roman font without using ABC spacing, the advance width is calculated as the character width.</span></span> <span data-ttu-id="585a7-135">Dies bedeutet, dass der Leerraum rechts neben dem Symbol in der Bitmap ausgerichtet ist, nicht jedoch das Symbol selbst.</span><span class="sxs-lookup"><span data-stu-id="585a7-135">This means the white space to the right of the glyph in the bitmap is aligned, not the glyph itself.</span></span> <span data-ttu-id="585a7-136">Durch die Verwendung von ABC-breiten haben Anwendungen bei der Ausrichtung von Text mehr Flexibilität bei der Platzierung und Entfernung von Leerraum, da Sie über Informationen verfügen, mit denen Sie den Abstand zwischen Zeichen fein steuern können.</span><span class="sxs-lookup"><span data-stu-id="585a7-136">By using ABC widths, applications have more flexibility in the placement and removal of white space when aligning text, because they have information that allows them to finely control intercharacter spacing.</span></span>

 

 
