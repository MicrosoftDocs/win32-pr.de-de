---
title: Schriftart-und Text Funktionen (OpenGL)
description: Die folgenden Funktionen können zum Verwalten von Schriftarten und Text verwendet werden.
ms.assetid: 42e16967-1eeb-4d37-bbd6-33c473eb2757
keywords:
- WGL-Funktionen, Text
- WGL-Funktionen, Schriftart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e205549346cccc2c44b7670db91530cfbc24017d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391416"
---
# <a name="font-and-text-functions-opengl"></a><span data-ttu-id="93266-105">Schriftart-und Text Funktionen (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="93266-105">Font and Text Functions (OpenGL)</span></span>

<span data-ttu-id="93266-106">Die folgenden Funktionen können zum Verwalten von Schriftarten und Text verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93266-106">The following functions can be used to manage fonts and text.</span></span>



| <span data-ttu-id="93266-107">Windows-Funktion</span><span class="sxs-lookup"><span data-stu-id="93266-107">Windows Function</span></span>                                 | <span data-ttu-id="93266-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="93266-108">Description</span></span>                                                                                                                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93266-109">**wgluseefontbitmaps**</span><span class="sxs-lookup"><span data-stu-id="93266-109">**wglUseFontBitmaps**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)   | <span data-ttu-id="93266-110">Erstellt einen Satz von Zeichen Bitmap-Anzeigelisten.</span><span class="sxs-lookup"><span data-stu-id="93266-110">Creates a set of character bitmap display lists.</span></span> <span data-ttu-id="93266-111">Zeichen stammen aus der aktuellen Schriftart eines angegebenen Geräte Kontexts.</span><span class="sxs-lookup"><span data-stu-id="93266-111">Characters come from a specified device context's current font.</span></span> <span data-ttu-id="93266-112">Zeichen werden als aufeinander folgende Laufzeiten innerhalb des Symbol Satzes der Schriftart angegeben.</span><span class="sxs-lookup"><span data-stu-id="93266-112">Characters are specified as a consecutive run within the font's glyph set.</span></span>                                      |
| [<span data-ttu-id="93266-113">**wgluseelfontgliederungen**</span><span class="sxs-lookup"><span data-stu-id="93266-113">**wglUseFontOutlines**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) | <span data-ttu-id="93266-114">Erstellt einen Satz von anzeigen Listen basierend auf den Symbolen der aktuell ausgewählten Gliederungs Schriftart eines Geräte Kontexts für die Verwendung mit dem aktuellen renderingkontext.</span><span class="sxs-lookup"><span data-stu-id="93266-114">Creates a set of display lists, based on the glyphs of the currently selected outline font of a device context, for use with the current rendering context.</span></span> <span data-ttu-id="93266-115">Die Anzeigelisten werden verwendet, um 3D-Zeichen von TrueType-Schriftarten zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="93266-115">The display lists are used to draw 3-D characters of TrueType fonts.</span></span> |



 

<span data-ttu-id="93266-116">Die **wglutarfontbitmaps** -und **wglutarfontgliedungsfunktionen** übernehmen ein Handle für einen Gerätekontext und verwenden die aktuelle Schriftart dieses Geräte Kontexts als Quelle für die Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="93266-116">The **wglUseFontBitmaps** and **wglUseFontOutlines** functions take a handle to a device context, and use that device context's current font as a source for the bitmaps.</span></span> <span data-ttu-id="93266-117">Daher ist es erforderlich, die Schriftart des Geräte Kontexts und die Schriftart Eigenschaften vor dem Aufrufen von **wglusefontbitmaps** oder **wglusefontgliederungen** festzulegen.</span><span class="sxs-lookup"><span data-stu-id="93266-117">It is therefore necessary to set the device context's font and the font's properties before calling **wglUseFontBitmaps** or **wglUseFontOutlines**.</span></span>

<span data-ttu-id="93266-118">Die Funktionen [**wgluseefontbitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) und [**wglusetfontgliederungen**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) verwenden auch einen Parameter, der das erste Symbol in der Schriftart in eine Bitmap-Anzeigeliste verwandelt, und einen Parameter, der angibt, wie viele Symbole in Anzeigelisten umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="93266-118">The [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) and [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) functions also take a parameter that turns the first glyph in the font into a bitmap display list, and a parameter that specifies how many glyphs to turn into display lists.</span></span> <span data-ttu-id="93266-119">Die-Funktion erstellt dann Anzeigelisten für die angegebene aufeinanderfolgende Durchführung von Symbolen.</span><span class="sxs-lookup"><span data-stu-id="93266-119">The function then creates display lists for the specified consecutive run of glyphs.</span></span> <span data-ttu-id="93266-120">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="93266-120">For example:</span></span>

-   <span data-ttu-id="93266-121">Legen Sie zum Erstellen eines Satzes von 224 Bitmap-Anzeigelisten für alle Symbole des Windows-Zeichensatzes diese beiden Parameter auf 32 bzw. 224 fest.</span><span class="sxs-lookup"><span data-stu-id="93266-121">To create a set of 224 bitmap display lists for all of the Windows character set glyphs, set these two parameters to 32 and 224, respectively.</span></span>
-   <span data-ttu-id="93266-122">Zum Erstellen eines Satzes von 256 Bitmap-Anzeigelisten für alle OEM-Zeichensatz Symbole legen Sie diese beiden Parameter auf 0 bzw. 256 fest.</span><span class="sxs-lookup"><span data-stu-id="93266-122">To create a set of 256 bitmap display lists for all of the OEM character set glyphs, set these two parameters to 0 and 256, respectively.</span></span>
-   <span data-ttu-id="93266-123">Legen Sie zum Erstellen einer einzelnen Bitmap-Anzeigeliste für ein beliebiges einzelnes Zeichensatz Symbol den zweiten dieser Parameter auf 1 fest.</span><span class="sxs-lookup"><span data-stu-id="93266-123">To create a single bitmap display list for any single character set glyph, set the second of these parameters to 1.</span></span>

<span data-ttu-id="93266-124">Die Funktionen **wgluseefontbitmaps** und **wgluseefontgliederungen** stellen ein NULL-Symbol in einer Schriftart mit einer leeren Anzeigeliste dar.</span><span class="sxs-lookup"><span data-stu-id="93266-124">The **wglUseFontBitmaps** and **wglUseFontOutlines** functions represent a null glyph in a font with an empty display list.</span></span>

<span data-ttu-id="93266-125">Die anzeigen Listen, die durch einen **wglu-fontbitmaps** -oder **wglusetfont-** aufrufsbefehl erstellt wurden, werden automatisch nacheinander nummeriert.</span><span class="sxs-lookup"><span data-stu-id="93266-125">The display lists created by a call to **wglUseFontBitmaps** or **wglUseFontOutlines** are automatically numbered consecutively.</span></span>

<span data-ttu-id="93266-126">Rufen Sie nach dem Aufrufen der [**wgluseefontbitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) -oder [**wglusetfontgliegerfunktion**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) " [**glcalllists**](glcalllists.md) " auf, um eine Zeichenfolge zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="93266-126">After calling the [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) or [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) function, call [**glCallLists**](glcalllists.md) to draw a string of characters.</span></span> <span data-ttu-id="93266-127">Beispielcode finden Sie [unterzeichnen von Text in einem Double-Buffered OpenGL-Fenster](drawing-text-in-a-double-buffered-opengl-window.md) .</span><span class="sxs-lookup"><span data-stu-id="93266-127">See [Drawing Text in a Double-Buffered OpenGL Window](drawing-text-in-a-double-buffered-opengl-window.md) for sample code.</span></span> <span data-ttu-id="93266-128">In diesem Kontext verwendet **glcalllists** die einzelnen Zeichen in einer Zeichenfolge als Index in das Array von in der Reihenfolge nummerierten anzeigen Listen, die von **wglutarfontbitmaps** oder **wglutarfontskizziert** erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="93266-128">In this context, **glCallLists** uses each character in a string as an index into the array of consecutively numbered display lists created by **wglUseFontBitmaps** or **wglUseFontOutlines**.</span></span>

<span data-ttu-id="93266-129">Wenn Sie das Zeichnen von Text beenden, rufen Sie die Funktion " [**gldelta etelists**](gldeletelists.md) " auf, um den zusammenhängenden Satz von anzeigen Listen freizugeben, die von **wglusefontbitmaps** und **wglusefontgliedern** erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="93266-129">When you finish drawing text, call the [**glDeleteLists**](gldeletelists.md) function to release the contiguous set of display lists created by **wglUseFontBitmaps** and **wglUseFontOutlines**.</span></span>

 

 




