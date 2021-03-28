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
# <a name="drawing-text-gdi"></a><span data-ttu-id="5c6f3-103">Zeichnen von Text (GDI+)</span><span class="sxs-lookup"><span data-stu-id="5c6f3-103">Drawing Text (GDI+)</span></span>

<span data-ttu-id="5c6f3-104">Sie können die [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) -Methode der [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse verwenden, um Text an einer angegebenen Position oder innerhalb eines angegebenen Rechtecks zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-104">You can use the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to draw text at a specified location or within a specified rectangle.</span></span>

-   [<span data-ttu-id="5c6f3-105">Zeichnen von Text an einer angegebenen Position</span><span class="sxs-lookup"><span data-stu-id="5c6f3-105">Drawing Text at a Specified Location</span></span>](#drawing-text-at-a-specified-location)
-   [<span data-ttu-id="5c6f3-106">Zeichnen von Text in einem Rechteck</span><span class="sxs-lookup"><span data-stu-id="5c6f3-106">Drawing Text in a Rectangle</span></span>](#drawing-text-in-a-rectangle)

## <a name="drawing-text-at-a-specified-location"></a><span data-ttu-id="5c6f3-107">Zeichnen von Text an einer angegebenen Position</span><span class="sxs-lookup"><span data-stu-id="5c6f3-107">Drawing Text at a Specified Location</span></span>

<span data-ttu-id="5c6f3-108">Zum Zeichnen von Text an einer angegebenen Position benötigen Sie [**Grafiken**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)-, [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font)-, [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf)-und [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) -Objekte.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-108">To draw text at a specified location, you need [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf), and [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) objects.</span></span>

<span data-ttu-id="5c6f3-109">Im folgenden Beispiel wird die Zeichenfolge "Hello" an Position (30, 10) gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-109">The following example draws the string "Hello" at location (30, 10).</span></span> <span data-ttu-id="5c6f3-110">Die Schriftfamilie ist Times New Roman.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-110">The font family is Times New Roman.</span></span> <span data-ttu-id="5c6f3-111">Die Schriftart, bei der es sich um einen einzelnen Member der Schriftfamilie handelt, ist Times New Roman, die Größe 24 Pixel, regulärer Stil.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-111">The font, which is an individual member of the font family, is Times New Roman, size 24 pixels, regular style.</span></span> <span data-ttu-id="5c6f3-112">Angenommen, die **Grafik** ist ein vorhandenes [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-112">Assume that **graphics** is an existing [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
PointF      pointF(30.0f, 10.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(L"Hello", -1, &font, pointF, &solidBrush);

```

<span data-ttu-id="5c6f3-113">Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-113">The following illustration shows the output of the preceding code.</span></span>

![Screenshot eines kleinen Fensters mit dem Text "Hello"](images/fontstext1.png)

<span data-ttu-id="5c6f3-115">Im vorherigen Beispiel erhält der [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) -Konstruktor eine Zeichenfolge, die die Schriftfamilie identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-115">In the preceding example, the [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) constructor receives a string that identifies the font family.</span></span> <span data-ttu-id="5c6f3-116">Die Adresse des **FontFamily** -Objekts wird als erstes Argument an den [**Schriftart**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) -Konstruktor übergeben.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-116">The address of the **FontFamily** object is passed as the first argument to the [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) constructor.</span></span> <span data-ttu-id="5c6f3-117">Das zweite Argument, das an den **Schriftart** -Konstruktor übergeben wird, gibt die Größe der Schriftart an, gemessen in Einheiten, die vom vierten Argument angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-117">The second argument passed to the **Font** constructor specifies the size of the font measured in units given by the fourth argument.</span></span> <span data-ttu-id="5c6f3-118">Das dritte Argument gibt den Stil der Schriftart an (regulär, Fett, kursiv usw.).</span><span class="sxs-lookup"><span data-stu-id="5c6f3-118">The third argument specifies the style (regular, bold, italic, and so on) of the font.</span></span>

<span data-ttu-id="5c6f3-119">Die [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) -Methode empfängt fünf Argumente.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-119">The [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method receives five arguments.</span></span> <span data-ttu-id="5c6f3-120">Das erste Argument ist die Zeichenfolge, die gezeichnet werden soll, und das zweite Argument ist die Länge (in Zeichen, nicht Bytes) dieser Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-120">The first argument is the string to be drawn, and the second argument is the length (in characters, not bytes) of that string.</span></span> <span data-ttu-id="5c6f3-121">Wenn die Zeichenfolge NULL-terminiert ist, können Sie – 1 als Länge übergeben.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-121">If the string is null-terminated, you can pass –1 for the length.</span></span> <span data-ttu-id="5c6f3-122">Das dritte Argument ist die Adresse des zuvor erstellten [**Schriftart**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) Objekts.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-122">The third argument is the address of the [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object that was constructed previously.</span></span> <span data-ttu-id="5c6f3-123">Das vierte Argument ist ein [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) -Objekt, das die Koordinaten der linken oberen Ecke der Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-123">The fourth argument is a [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) object that contains the coordinates of the upper-left corner of the string.</span></span> <span data-ttu-id="5c6f3-124">Das fünfte Argument ist die Adresse eines [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) -Objekts, das zum Ausfüllen der Zeichen der Zeichenfolge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-124">The fifth argument is the address of a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object that will be used to fill the characters of the string.</span></span>

## <a name="drawing-text-in-a-rectangle"></a><span data-ttu-id="5c6f3-125">Zeichnen von Text in einem Rechteck</span><span class="sxs-lookup"><span data-stu-id="5c6f3-125">Drawing Text in a Rectangle</span></span>

<span data-ttu-id="5c6f3-126">Eine der [**DrawString**](https://www.bing.com/search?q=**DrawString**) -Methoden der [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse verfügt über einen *RectF* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-126">One of the [**DrawString**](https://www.bing.com/search?q=**DrawString**) methods of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class has a *RectF* parameter.</span></span> <span data-ttu-id="5c6f3-127">Indem Sie diese **DrawString** -Methode aufrufen, können Sie Text zeichnen, der in einem angegebenen Rechteck umbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-127">By calling that **DrawString** method, you can draw text that wraps in a specified rectangle.</span></span> <span data-ttu-id="5c6f3-128">Zum Zeichnen von Text in einem Rechteck benötigen Sie **Grafiken**, [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)-, [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font)-, [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf)-und [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) -Objekte.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-128">To draw text in a rectangle, you need **Graphics**, [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf), and [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) objects.</span></span>

<span data-ttu-id="5c6f3-129">Im folgenden Beispiel wird ein Rechteck mit der oberen linken Ecke (30, 10), der Breite 100 und der Höhe 122 erstellt.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-129">The following example creates a rectangle with upper-left corner (30, 10), width 100, and height 122.</span></span> <span data-ttu-id="5c6f3-130">Anschließend zeichnet der Code eine Zeichenfolge innerhalb dieses Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-130">Then the code draws a string inside that rectangle.</span></span> <span data-ttu-id="5c6f3-131">Die Zeichenfolge ist auf das Rechteck beschränkt und wird so umschlossen, dass einzelne Wörter nicht beschädigt werden.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-131">The string is restricted to the rectangle and wraps in such a way that individual words are not broken.</span></span>

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

<span data-ttu-id="5c6f3-132">Die folgende Abbildung zeigt den im Rechteck gezeichneten Text.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-132">The following illustration shows the text drawn in the rectangle.</span></span>

![Screenshot eines kleinen Fensters mit einem Winkel, in dem der erste Teil eines Satzes angezeigt wird](images/fontstext2.png)

<span data-ttu-id="5c6f3-134">Im vorherigen Beispiel ist das vierte Argument, das an die [**DrawString**](https://www.bing.com/search?q=**DrawString**) -Methode übermittelt wurde, ein [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf) -Objekt, das das umgebende Rechteck für den Text angibt.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-134">In the preceding example, the fourth argument passed to the [**DrawString**](https://www.bing.com/search?q=**DrawString**) method is a [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf) object that specifies the bounding rectangle for the text.</span></span> <span data-ttu-id="5c6f3-135">Der fünfte Parameter weist den Typ [**StringFormat**](/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)auf – das Argument ist **null** , da keine besondere Zeichen folgen Formatierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-135">The fifth parameter is of type [**StringFormat**](/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)— the argument is **NULL** because no special string formatting is required.</span></span>
