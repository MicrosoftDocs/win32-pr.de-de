---
description: In einigen Fällen muss eine Anwendung in der Lage sein, die verfügbaren Schriftarten aufzulisten und die für einen bestimmten Vorgang am besten geeignete auszuwählen.
ms.assetid: 18db1b03-6e3c-4be3-b637-a21bf41cc080
title: Auflisten der installierten Schriftarten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dee38ccf9807371181388536f1230d222d448bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215203"
---
# <a name="enumerating-the-installed-fonts"></a>Auflisten der installierten Schriftarten

In einigen Fällen muss eine Anwendung in der Lage sein, die verfügbaren Schriftarten aufzulisten und die für einen bestimmten Vorgang am besten geeignete auszuwählen. Eine Anwendung kann die verfügbaren Schriftarten durch Aufrufen der [enumfonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) -oder [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) -Funktion auflisten. Diese Funktionen senden Informationen zu den verfügbaren Schriftarten an eine Rückruffunktion, die von der Anwendung bereitgestellt wird. Die Rückruffunktion empfängt Informationen in den Strukturen [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) und [newtextmetric](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) . (Die [**newtextmetric**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) -Struktur enthält Informationen über eine TrueType-Schriftart. Wenn die Rückruffunktion Informationen zu einer nicht-TrueType-Schriftart empfängt, sind die Informationen in einer [TextMetric](/windows/win32/api/wingdi/ns-wingdi-textmetrica) -Struktur enthalten.) Mithilfe dieser Informationen kann eine Anwendung die Auswahl des Benutzers auf die verfügbaren Schriftarten beschränken.

Die Funktion " [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) " ähnelt der Funktion " [**enumfonts**](/windows/win32/api/wingdi/nf-wingdi-enumfontsa) ", bietet aber einige zusätzliche Funktionen. **EnumFontFamilies** ermöglicht es einer Anwendung, die in TrueType-Schriftarten verfügbaren Stile zu nutzen. Für neue und aktualisierte Anwendungen sollten **EnumFontFamilies** anstelle von **enumfonts** verwendet werden.

TrueType-Schriftarten werden um einen Schriftart Namen (z. b. Courier New) und Stil Namen organisiert (z. b. kursiv, Fett und Extra Fett). Die [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) -Funktion Listet alle Stile auf, die einem angegebenen Familiennamen zugeordnet sind, und nicht nur die fett formatierten und kursiv formatierten Attribute. Wenn das System z. b. eine TrueType-Schriftart namens Courier New Extra-Bold enthält, listet **EnumFontFamilies** Sie mit den anderen Courier New-Schriftarten auf. Die Funktionen von **EnumFontFamilies** sind hilfreich für Schriftarten mit vielen oder ungewöhnlichen Stilen und für Schriftarten, die internationale Grenzen überschreiten.

Wenn eine Anwendung keinen Schriftart Namen bereitstellt, stellen die Funktionen " [enumfonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) " und " [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) " Informationen zu einer Schriftart in jeder verfügbaren Familie bereit. Um alle Schriftarten in einem Gerätekontext aufzulisten, kann die Anwendung für den Namen der Schriftart **null** angeben, eine Liste der verfügbaren typegesichter kompilieren und dann jede Schriftart in jeder Schriftart auflisten.

Im folgenden Beispiel wird die-Funktion von [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) verwendet, um die Anzahl der verfügbaren Schriftfamilien für Raster, Vector und TrueType abzurufen.


```C++
    UINT uAlignPrev; 
    int aFontCount[] = { 0, 0, 0 }; 
    char szCount[8];
        HRESULT hr;
        size_t * pcch; 
 
    EnumFontFamilies(hdc, (LPCTSTR) NULL, 
        (FONTENUMPROC) EnumFamCallBack, (LPARAM) aFontCount); 
 
    uAlignPrev = SetTextAlign(hdc, TA_UPDATECP); 
 
    MoveToEx(hdc, 10, 50, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of raster fonts: ", 24); 
    itoa(aFontCount[0], szCount, 10); 
        
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    MoveToEx(hdc, 10, 75, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of vector fonts: ", 24); 
    itoa(aFontCount[1], szCount, 10);
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    MoveToEx(hdc, 10, 100, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of TrueType fonts: ", 26); 
    itoa(aFontCount[2], szCount, 10);
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    SetTextAlign(hdc, uAlignPrev); 
 
BOOL CALLBACK EnumFamCallBack(LPLOGFONT lplf, LPNEWTEXTMETRIC lpntm, DWORD FontType, LPVOID aFontCount) 
{ 
    int far * aiFontCount = (int far *) aFontCount; 
 
    // Record the number of raster, TrueType, and vector  
    // fonts in the font-count array.  
 
    if (FontType & RASTER_FONTTYPE) 
        aiFontCount[0]++; 
    else if (FontType & TRUETYPE_FONTTYPE) 
        aiFontCount[2]++; 
    else 
        aiFontCount[1]++; 
 
    if (aiFontCount[0] || aiFontCount[1] || aiFontCount[2]) 
        return TRUE; 
    else 
        return FALSE; 
 
    UNREFERENCED_PARAMETER( lplf ); 
    UNREFERENCED_PARAMETER( lpntm ); 
} 
```



In diesem Beispiel werden zwei Masken, Raster \_ -fonttype und TrueType \_ fonttype, verwendet, um den Typ der aufzuzählenden Schriftart zu ermitteln. Wenn das Raster- \_ fonttype-Bit festgelegt ist, ist die Schriftart eine Raster Schriftart. Wenn das "TrueType \_ fonttype"-Bit festgelegt ist, ist die Schriftart eine TrueType-Schriftart. Wenn keines der beiden Bits festgelegt ist, ist die Schriftart eine Vektor Schriftart. Eine dritte Maske, Device \_ fonttype, wird festgelegt, wenn ein Gerät (z. b. ein Laserdrucker) das Herunterladen von TrueType-Schriftarten unterstützt. es ist 0 (null), wenn das Gerät ein Anzeige Adapter, ein Punkt/Matrix-Drucker oder ein anderes rastergerät ist Eine Anwendung kann auch die Geräte \_ -fonttype-Maske verwenden, um vom Gerät bereitgestellte Raster Schriftarten von Geräten bereitgestellten Schriftarten zu unterscheiden. Das System kann Fett-, kursiv-, unterstrichen-und durchgestrichen-Attribute für die von GDI bereitgestellten Raster Schriftarten, jedoch nicht für vom Gerät bereitgestellte Schriftarten simulieren.

Eine Anwendung kann auch Bits 1 und 2 im **tmpitchandfamily** -Member der [newtextmetric](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) -Struktur überprüfen, um eine TrueType-Schriftart zu identifizieren. Wenn Bit 1 0 und Bit 2 1 ist, ist die Schriftart eine TrueType-Schriftart.

Vektor Schriftarten werden als OEM-Zeichen \_ Satz anstelle von ANSI-Zeichensatz kategorisiert \_ . Einige Anwendungen identifizieren Vektor Schriftarten mithilfe dieser Informationen und überprüfen den **tmcharset** -Member der [**newtextmetric**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) -Struktur. Diese Kategorisierung verhindert in der Regel, dass die Schriftart Mapper Vektor Schriftarten auswählen, es sei denn, Sie werden ausdrücklich angefordert. (Die meisten Anwendungen verwenden keine Vektor Schriftarten mehr, da ihre Striche eine einzelne Zeile sind und Sie mehr Zeit benötigen als TrueType-Schriftarten, die viele der gleichen Skalierungs-und Rotations Features bieten, die Vektor Schriftarten erforderten.)

 

 
