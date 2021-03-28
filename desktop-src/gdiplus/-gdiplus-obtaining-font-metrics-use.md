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
# <a name="obtaining-font-metrics"></a><span data-ttu-id="038bd-103">Abrufen von Schriftart Metriken</span><span class="sxs-lookup"><span data-stu-id="038bd-103">Obtaining Font Metrics</span></span>

<span data-ttu-id="038bd-104">Die [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) -Klasse stellt die folgenden Methoden bereit, die verschiedene Metriken für eine bestimmte Kombination aus Familie und Stil abrufen:</span><span class="sxs-lookup"><span data-stu-id="038bd-104">The [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) class provides the following methods that retrieve various metrics for a particular family/style combination:</span></span>

-   <span data-ttu-id="038bd-105">[**FontFamily:: GetEmHeight**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight)(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="038bd-105">[**FontFamily::GetEmHeight**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight)(FontStyle)</span></span>
-   <span data-ttu-id="038bd-106">[**FontFamily:: GetCellAscent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcellascent)(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="038bd-106">[**FontFamily::GetCellAscent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcellascent)(FontStyle)</span></span>
-   <span data-ttu-id="038bd-107">[**FontFamily:: GetCellDescent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent)(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="038bd-107">[**FontFamily::GetCellDescent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent)(FontStyle)</span></span>
-   <span data-ttu-id="038bd-108">[**FontFamily:: GetLineSpacing(**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getlinespacing)FontStyle)</span><span class="sxs-lookup"><span data-stu-id="038bd-108">[**FontFamily::GetLineSpacing**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getlinespacing)(FontStyle)</span></span>

<span data-ttu-id="038bd-109">Die von diesen Methoden zurückgegebenen Zahlen sind in Schriftart Entwurfs Einheiten, sodass Sie unabhängig von der Größe und den Einheiten eines bestimmten [**Schriftart**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) Objekts sind.</span><span class="sxs-lookup"><span data-stu-id="038bd-109">The numbers returned by these methods are in font design units, so they are independent of the size and units of a particular [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object.</span></span>

<span data-ttu-id="038bd-110">In der folgenden Abbildung sind die Aufstiege, der Abstieg und der Zeilenabstand dargestellt.</span><span class="sxs-lookup"><span data-stu-id="038bd-110">The following illustration shows ascent, descent, and line spacing.</span></span>

![Diagramm von zwei Zeichen in angrenzenden Zeilen, das Zellen Aufstieg, den Zell Abstieg und den Zeilenabstand anzeigt](images/fontstext7a.png)

<span data-ttu-id="038bd-112">Im folgenden Beispiel werden die Metriken für den regulären Stil der Arial-Schriftfamilie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="038bd-112">The following example displays the metrics for the regular style of the Arial font family.</span></span> <span data-ttu-id="038bd-113">Der Code erstellt auch ein [**Schriftart**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) Objekt (basierend auf der Arial-Familie) mit einer Größe von 16 Pixel und zeigt die Metriken (in Pixel) für das jeweilige **Schriftart** Objekt an.</span><span class="sxs-lookup"><span data-stu-id="038bd-113">The code also creates a [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object (based on the Arial family) with size 16 pixels and displays the metrics (in pixels) for that particular **Font** object.</span></span>


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



<span data-ttu-id="038bd-114">Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes.</span><span class="sxs-lookup"><span data-stu-id="038bd-114">The following illustration shows the output of the preceding code.</span></span>

![Screenshot eines Fensters mit Text, der die Schriftgröße und-Höhe angibt, und die Steigung, den Abstieg und den Zeilenabstand](images/fontstext8.png)

<span data-ttu-id="038bd-116">Beachten Sie die ersten beiden Zeilen der Ausgabe in der obigen Abbildung.</span><span class="sxs-lookup"><span data-stu-id="038bd-116">Note the first two lines of output in the preceding illustration.</span></span> <span data-ttu-id="038bd-117">Das [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) -Objekt gibt eine Größe von 16 zurück, und das [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) -Objekt gibt die EM-Höhe von 2.048 zurück.</span><span class="sxs-lookup"><span data-stu-id="038bd-117">The [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object returns a size of 16, and the [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object returns an em height of 2,048.</span></span> <span data-ttu-id="038bd-118">Diese beiden Zahlen (16 und 2.048) sind der Schlüssel für die Typumwandlung zwischen Schriftart Entwurfs Einheiten und den Einheiten (in diesem Fall Pixel) des **Schriftart** Objekts.</span><span class="sxs-lookup"><span data-stu-id="038bd-118">These two numbers (16 and 2,048) are the key to converting between font design units and the units (in this case pixels) of the **Font** object.</span></span>

<span data-ttu-id="038bd-119">Beispielsweise können Sie den Aufstieg wie folgt von Entwurfs Einheiten in Pixel konvertieren:</span><span class="sxs-lookup"><span data-stu-id="038bd-119">For example, you can convert the ascent from design units to pixels as follows:</span></span>

![Gleichung, bei der 1854-Entwurfs Einheiten um 16 Pixel dividiert durch 2048-Entwurfs Einheiten, gleich 14,484375 Pixel, multipliziert werden.](images/fontstext9.png)

<span data-ttu-id="038bd-121">Der vorangehende Code positioniert Text vertikal, indem der *y* -Datenmember eines [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) -Objekts festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="038bd-121">The preceding code positions text vertically by setting the *y* data member of a [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) object.</span></span> <span data-ttu-id="038bd-122">Die y-Koordinate wird von `font.GetHeight(0.0f)` für jede neue Textzeile um erweitert.</span><span class="sxs-lookup"><span data-stu-id="038bd-122">The y-coordinate is increased by `font.GetHeight(0.0f)` for each new line of text.</span></span> <span data-ttu-id="038bd-123">Die [**Schriftart:: GetHeight**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-getheight(inreal)) -Methode eines [**Schriftart**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) Objekts gibt den Zeilenabstand (in Pixel) für das jeweilige **Schriftart** Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="038bd-123">The [**Font::GetHeight**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-getheight(inreal)) method of a [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object returns the line spacing (in pixels) for that particular **Font** object.</span></span> <span data-ttu-id="038bd-124">In diesem Beispiel ist die Zahl, die von **Font:: GetHeight** zurückgegeben wird, 18,398438.</span><span class="sxs-lookup"><span data-stu-id="038bd-124">In this example, the number returned by **Font::GetHeight** is 18.398438.</span></span> <span data-ttu-id="038bd-125">Beachten Sie, dass dies mit der Zahl übereinstimmt, die durch die Umstellung der Metrik für den Zeilenabstand in Pixel erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="038bd-125">Note that this is the same as the number obtained by converting the line spacing metric to pixels.</span></span>

 

 
