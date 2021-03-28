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
# <a name="enumerating-the-installed-fonts"></a><span data-ttu-id="fdd74-103">Auflisten der installierten Schriftarten</span><span class="sxs-lookup"><span data-stu-id="fdd74-103">Enumerating the Installed Fonts</span></span>

<span data-ttu-id="fdd74-104">In einigen Fällen muss eine Anwendung in der Lage sein, die verfügbaren Schriftarten aufzulisten und die für einen bestimmten Vorgang am besten geeignete auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="fdd74-104">In some instances, an application must be able to enumerate the available fonts and select the one most appropriate for a particular operation.</span></span> <span data-ttu-id="fdd74-105">Eine Anwendung kann die verfügbaren Schriftarten durch Aufrufen der [enumfonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) -oder [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) -Funktion auflisten.</span><span class="sxs-lookup"><span data-stu-id="fdd74-105">An application can enumerate the available fonts by calling the [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) or [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) function.</span></span> <span data-ttu-id="fdd74-106">Diese Funktionen senden Informationen zu den verfügbaren Schriftarten an eine Rückruffunktion, die von der Anwendung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fdd74-106">These functions send information about the available fonts to a callback function that the application supplies.</span></span> <span data-ttu-id="fdd74-107">Die Rückruffunktion empfängt Informationen in den Strukturen [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) und [newtextmetric](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) .</span><span class="sxs-lookup"><span data-stu-id="fdd74-107">The callback function receives information in [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) and [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structures.</span></span> <span data-ttu-id="fdd74-108">(Die [**newtextmetric**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) -Struktur enthält Informationen über eine TrueType-Schriftart.</span><span class="sxs-lookup"><span data-stu-id="fdd74-108">(The [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure contains information about a TrueType font.</span></span> <span data-ttu-id="fdd74-109">Wenn die Rückruffunktion Informationen zu einer nicht-TrueType-Schriftart empfängt, sind die Informationen in einer [TextMetric](/windows/win32/api/wingdi/ns-wingdi-textmetrica) -Struktur enthalten.) Mithilfe dieser Informationen kann eine Anwendung die Auswahl des Benutzers auf die verfügbaren Schriftarten beschränken.</span><span class="sxs-lookup"><span data-stu-id="fdd74-109">When the callback function receives information about a non-TrueType font, the information is contained in a [TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure.) By using this information, an application can limit the user's choices to only those fonts that are available.</span></span>

<span data-ttu-id="fdd74-110">Die Funktion " [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) " ähnelt der Funktion " [**enumfonts**](/windows/win32/api/wingdi/nf-wingdi-enumfontsa) ", bietet aber einige zusätzliche Funktionen.</span><span class="sxs-lookup"><span data-stu-id="fdd74-110">The [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) function is similar to the [**EnumFonts**](/windows/win32/api/wingdi/nf-wingdi-enumfontsa) function but includes some extra functionality.</span></span> <span data-ttu-id="fdd74-111">**EnumFontFamilies** ermöglicht es einer Anwendung, die in TrueType-Schriftarten verfügbaren Stile zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="fdd74-111">**EnumFontFamilies** allows an application to take advantage of styles available with TrueType fonts.</span></span> <span data-ttu-id="fdd74-112">Für neue und aktualisierte Anwendungen sollten **EnumFontFamilies** anstelle von **enumfonts** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fdd74-112">New and upgraded applications should use **EnumFontFamilies** instead of **EnumFonts**.</span></span>

<span data-ttu-id="fdd74-113">TrueType-Schriftarten werden um einen Schriftart Namen (z. b. Courier New) und Stil Namen organisiert (z. b. kursiv, Fett und Extra Fett).</span><span class="sxs-lookup"><span data-stu-id="fdd74-113">TrueType fonts are organized around a typeface name (for example, Courier New) and style names (for example, italic, bold, and extra-bold).</span></span> <span data-ttu-id="fdd74-114">Die [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) -Funktion Listet alle Stile auf, die einem angegebenen Familiennamen zugeordnet sind, und nicht nur die fett formatierten und kursiv formatierten Attribute.</span><span class="sxs-lookup"><span data-stu-id="fdd74-114">The [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) function enumerates all the styles associated with a specified family name, not simply the bold and italic attributes.</span></span> <span data-ttu-id="fdd74-115">Wenn das System z. b. eine TrueType-Schriftart namens Courier New Extra-Bold enthält, listet **EnumFontFamilies** Sie mit den anderen Courier New-Schriftarten auf.</span><span class="sxs-lookup"><span data-stu-id="fdd74-115">For example, when the system includes a TrueType font called Courier New Extra-Bold, **EnumFontFamilies** lists it with the other Courier New fonts.</span></span> <span data-ttu-id="fdd74-116">Die Funktionen von **EnumFontFamilies** sind hilfreich für Schriftarten mit vielen oder ungewöhnlichen Stilen und für Schriftarten, die internationale Grenzen überschreiten.</span><span class="sxs-lookup"><span data-stu-id="fdd74-116">The capabilities of **EnumFontFamilies** are helpful for fonts with many or unusual styles and for fonts that cross international borders.</span></span>

<span data-ttu-id="fdd74-117">Wenn eine Anwendung keinen Schriftart Namen bereitstellt, stellen die Funktionen " [enumfonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) " und " [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) " Informationen zu einer Schriftart in jeder verfügbaren Familie bereit.</span><span class="sxs-lookup"><span data-stu-id="fdd74-117">If an application does not supply a typeface name, the [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) and [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) functions supply information about one font in each available family.</span></span> <span data-ttu-id="fdd74-118">Um alle Schriftarten in einem Gerätekontext aufzulisten, kann die Anwendung für den Namen der Schriftart **null** angeben, eine Liste der verfügbaren typegesichter kompilieren und dann jede Schriftart in jeder Schriftart auflisten.</span><span class="sxs-lookup"><span data-stu-id="fdd74-118">To enumerate all the fonts in a device context, the application can specify **NULL** for the typeface name, compile a list of the available typefaces, and then enumerate each font in each typeface.</span></span>

<span data-ttu-id="fdd74-119">Im folgenden Beispiel wird die-Funktion von [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) verwendet, um die Anzahl der verfügbaren Schriftfamilien für Raster, Vector und TrueType abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fdd74-119">The following example uses the [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) function to retrieve the number of available raster, vector, and TrueType font families.</span></span>


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



<span data-ttu-id="fdd74-120">In diesem Beispiel werden zwei Masken, Raster \_ -fonttype und TrueType \_ fonttype, verwendet, um den Typ der aufzuzählenden Schriftart zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="fdd74-120">This example uses two masks, RASTER\_FONTTYPE and TRUETYPE\_FONTTYPE, to determine the type of font being enumerated.</span></span> <span data-ttu-id="fdd74-121">Wenn das Raster- \_ fonttype-Bit festgelegt ist, ist die Schriftart eine Raster Schriftart.</span><span class="sxs-lookup"><span data-stu-id="fdd74-121">If the RASTER\_FONTTYPE bit is set, the font is a raster font.</span></span> <span data-ttu-id="fdd74-122">Wenn das "TrueType \_ fonttype"-Bit festgelegt ist, ist die Schriftart eine TrueType-Schriftart.</span><span class="sxs-lookup"><span data-stu-id="fdd74-122">If the TRUETYPE\_FONTTYPE bit is set, the font is a TrueType font.</span></span> <span data-ttu-id="fdd74-123">Wenn keines der beiden Bits festgelegt ist, ist die Schriftart eine Vektor Schriftart.</span><span class="sxs-lookup"><span data-stu-id="fdd74-123">If neither bit is set, the font is a vector font.</span></span> <span data-ttu-id="fdd74-124">Eine dritte Maske, Device \_ fonttype, wird festgelegt, wenn ein Gerät (z. b. ein Laserdrucker) das Herunterladen von TrueType-Schriftarten unterstützt. es ist 0 (null), wenn das Gerät ein Anzeige Adapter, ein Punkt/Matrix-Drucker oder ein anderes rastergerät ist</span><span class="sxs-lookup"><span data-stu-id="fdd74-124">A third mask, DEVICE\_FONTTYPE, is set when a device (for example, a laser printer) supports downloading TrueType fonts; it is zero if the device is a display adapter, dot-matrix printer, or other raster device.</span></span> <span data-ttu-id="fdd74-125">Eine Anwendung kann auch die Geräte \_ -fonttype-Maske verwenden, um vom Gerät bereitgestellte Raster Schriftarten von Geräten bereitgestellten Schriftarten zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="fdd74-125">An application can also use the DEVICE\_FONTTYPE mask to distinguish GDI-supplied raster fonts from device-supplied fonts.</span></span> <span data-ttu-id="fdd74-126">Das System kann Fett-, kursiv-, unterstrichen-und durchgestrichen-Attribute für die von GDI bereitgestellten Raster Schriftarten, jedoch nicht für vom Gerät bereitgestellte Schriftarten simulieren.</span><span class="sxs-lookup"><span data-stu-id="fdd74-126">The system can simulate bold, italic, underline, and strikeout attributes for GDI-supplied raster fonts, but not for device-supplied fonts.</span></span>

<span data-ttu-id="fdd74-127">Eine Anwendung kann auch Bits 1 und 2 im **tmpitchandfamily** -Member der [newtextmetric](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) -Struktur überprüfen, um eine TrueType-Schriftart zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fdd74-127">An application can also check bits 1 and 2 in the **tmPitchAndFamily** member of the [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure to identify a TrueType font.</span></span> <span data-ttu-id="fdd74-128">Wenn Bit 1 0 und Bit 2 1 ist, ist die Schriftart eine TrueType-Schriftart.</span><span class="sxs-lookup"><span data-stu-id="fdd74-128">If bit 1 is 0 and bit 2 is 1, the font is a TrueType font.</span></span>

<span data-ttu-id="fdd74-129">Vektor Schriftarten werden als OEM-Zeichen \_ Satz anstelle von ANSI-Zeichensatz kategorisiert \_ .</span><span class="sxs-lookup"><span data-stu-id="fdd74-129">Vector fonts are categorized as OEM\_CHARSET instead of ANSI\_CHARSET.</span></span> <span data-ttu-id="fdd74-130">Einige Anwendungen identifizieren Vektor Schriftarten mithilfe dieser Informationen und überprüfen den **tmcharset** -Member der [**newtextmetric**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="fdd74-130">Some applications identify vector fonts by using this information, checking the **tmCharSet** member of the [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure.</span></span> <span data-ttu-id="fdd74-131">Diese Kategorisierung verhindert in der Regel, dass die Schriftart Mapper Vektor Schriftarten auswählen, es sei denn, Sie werden ausdrücklich angefordert.</span><span class="sxs-lookup"><span data-stu-id="fdd74-131">This categorization usually prevents the font mapper from choosing vector fonts unless they are specifically requested.</span></span> <span data-ttu-id="fdd74-132">(Die meisten Anwendungen verwenden keine Vektor Schriftarten mehr, da ihre Striche eine einzelne Zeile sind und Sie mehr Zeit benötigen als TrueType-Schriftarten, die viele der gleichen Skalierungs-und Rotations Features bieten, die Vektor Schriftarten erforderten.)</span><span class="sxs-lookup"><span data-stu-id="fdd74-132">(Most applications no longer use vector fonts because their strokes are single lines and they take longer to draw than TrueType fonts, which offer many of the same scaling and rotation features that required vector fonts.)</span></span>

 

 
