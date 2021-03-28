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
# <a name="formatting-text-gdi"></a><span data-ttu-id="77b81-103">Formatieren von Text (GDI+)</span><span class="sxs-lookup"><span data-stu-id="77b81-103">Formatting Text (GDI+)</span></span>

<span data-ttu-id="77b81-104">Um eine spezielle Formatierung auf Text anzuwenden, initialisieren Sie ein [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) -Objekt, und übergeben Sie die Adresse dieses Objekts an die [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) -Methode der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse.</span><span class="sxs-lookup"><span data-stu-id="77b81-104">To apply special formatting to text, initialize a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object and pass the address of that object to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span>

<span data-ttu-id="77b81-105">Um formatierten Text in einem Rechteck zu zeichnen, benötigen Sie [**Grafiken**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)-, [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font)-, [**RectF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rectf)-, [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)-und [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) -Objekte.</span><span class="sxs-lookup"><span data-stu-id="77b81-105">To draw formatted text in a rectangle, you need [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rectf), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), and [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) objects.</span></span>

-   [<span data-ttu-id="77b81-106">Ausrichten von Text</span><span class="sxs-lookup"><span data-stu-id="77b81-106">Aligning Text</span></span>](#aligning-text)
-   [<span data-ttu-id="77b81-107">Festlegen von Tabstopps</span><span class="sxs-lookup"><span data-stu-id="77b81-107">Setting Tab Stops</span></span>](#setting-tab-stops)
-   [<span data-ttu-id="77b81-108">Zeichnen von vertikaler Text</span><span class="sxs-lookup"><span data-stu-id="77b81-108">Drawing Vertical Text</span></span>](#drawing-vertical-text)

## <a name="aligning-text"></a><span data-ttu-id="77b81-109">Ausrichten von Text</span><span class="sxs-lookup"><span data-stu-id="77b81-109">Aligning Text</span></span>

<span data-ttu-id="77b81-110">Im folgenden Beispiel wird Text in einem Rechteck gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="77b81-110">The following example draws text in a rectangle.</span></span> <span data-ttu-id="77b81-111">Jede Textzeile wird zentriert (Seite zu Seite), und der gesamte TextBlock wird im Rechteck zentriert (von oben nach unten) zentriert.</span><span class="sxs-lookup"><span data-stu-id="77b81-111">Each line of text is centered (side to side), and the entire block of text is centered (top to bottom) in the rectangle.</span></span>


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



<span data-ttu-id="77b81-112">In der folgenden Abbildung werden das Rechteck und der zentrierte Text gezeigt.</span><span class="sxs-lookup"><span data-stu-id="77b81-112">The following illustration shows the rectangle and the centered text.</span></span>

![Screenshot eines Fensters mit einem Rechteck, das sechs Textzeilen enthält, die horizontal zentriert sind](images/fontstext3.png)

<span data-ttu-id="77b81-114">Der vorangehende Code ruft zwei Methoden des [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) -Objekts auf: [**StringFormat:: SetAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setalignment) und [**StringFormat:: setlinealignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setlinealignment).</span><span class="sxs-lookup"><span data-stu-id="77b81-114">The preceding code calls two methods of the [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object: [**StringFormat::SetAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setalignment) and [**StringFormat::SetLineAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setlinealignment).</span></span> <span data-ttu-id="77b81-115">Der Befehl **StringFormat:: SetAlignment** gibt an, dass jede Textzeile in dem Rechteck zentriert wird, das durch das dritte an die [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) -Methode über gegebene Argument angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="77b81-115">The call to **StringFormat::SetAlignment** specifies that each line of text is centered in the rectangle given by the third argument passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method.</span></span> <span data-ttu-id="77b81-116">Der Befehl **StringFormat:: setlinealignment** gibt an, dass der TextBlock im Rechteck zentriert (von oben nach unten) zentriert wird.</span><span class="sxs-lookup"><span data-stu-id="77b81-116">The call to **StringFormat::SetLineAlignment** specifies that the block of text is centered (top to bottom) in the rectangle.</span></span>

<span data-ttu-id="77b81-117">Der Wert [\* \* \* \* stringalignmentcenter \* \* \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringalignment) ist ein Element der **StringAlignment** -Enumeration, das in "gdiplusenums. h" deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="77b81-117">The value [\*\*\*\*StringAlignmentCenter\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringalignment) is an element of the **StringAlignment** enumeration, which is declared in Gdiplusenums.h.</span></span>

## <a name="setting-tab-stops"></a><span data-ttu-id="77b81-118">Festlegen von Tabstopps</span><span class="sxs-lookup"><span data-stu-id="77b81-118">Setting Tab Stops</span></span>

<span data-ttu-id="77b81-119">Sie können Tabstopps für Text festlegen, indem Sie [**die StringFormat:: settabstopps**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) -Methode eines [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) -Objekts aufrufen und dann die Adresse dieses **StringFormat** -Objekts an die [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) -Methode der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse übergeben.</span><span class="sxs-lookup"><span data-stu-id="77b81-119">You can set tab stops for text by calling the [**StringFormat::SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) method of a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object and then passing the address of that **StringFormat** object to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span>

<span data-ttu-id="77b81-120">Im folgenden Beispiel wird der Tabstopp bei 150, 250 und 350 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="77b81-120">The following example sets tab stops at 150, 250, and 350.</span></span> <span data-ttu-id="77b81-121">Im Code wird dann eine Liste der Namen und Testergebnisse im Registerkarten Format angezeigt.</span><span class="sxs-lookup"><span data-stu-id="77b81-121">Then the code displays a tabbed list of names and test scores.</span></span>


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



<span data-ttu-id="77b81-122">Die folgende Abbildung zeigt den Text im Registerkarten Format.</span><span class="sxs-lookup"><span data-stu-id="77b81-122">The following illustration shows the tabbed text.</span></span>

![Abbildung eines Rechtecks, das vier Textspalten enthält. jede Spalte ist linksbündig.](images/fontstext4.png)

<span data-ttu-id="77b81-124">Der vorangehende Code übergibt drei Argumente an die [**StringFormat:: SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) -Methode.</span><span class="sxs-lookup"><span data-stu-id="77b81-124">The preceding code passes three arguments to the [**StringFormat::SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) method.</span></span> <span data-ttu-id="77b81-125">Das dritte Argument ist die Adresse eines Arrays, das die Tabulator Offsets enthält.</span><span class="sxs-lookup"><span data-stu-id="77b81-125">The third argument is the address of an array containing the tab offsets.</span></span> <span data-ttu-id="77b81-126">Das zweite Argument gibt an, dass es drei Offsets in diesem Array gibt.</span><span class="sxs-lookup"><span data-stu-id="77b81-126">The second argument indicates that there are three offsets in that array.</span></span> <span data-ttu-id="77b81-127">Das erste Argument, das an **StringFormat:: settabstopps** übergeben wird, ist 0 (null) und gibt an, dass der erste Offset im Array von Position 0, dem linken Rand des umgebenden Rechtecks, gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="77b81-127">The first argument passed to **StringFormat::SetTabStops** is 0, which indicates that the first offset in the array is measured from position 0, the left edge of the bounding rectangle.</span></span>

## <a name="drawing-vertical-text"></a><span data-ttu-id="77b81-128">Zeichnen von vertikaler Text</span><span class="sxs-lookup"><span data-stu-id="77b81-128">Drawing Vertical Text</span></span>

<span data-ttu-id="77b81-129">Sie können ein [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) -Objekt verwenden, um anzugeben, dass Text vertikal und nicht horizontal gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="77b81-129">You can use a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object to specify that text be drawn vertically rather than horizontally.</span></span>

<span data-ttu-id="77b81-130">Im folgenden Beispiel wird der Wert [\* \* \* \* stringformatflagsdirectionvertical \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) \* \* an die [**StringFormat:: setformatflags**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setformatflags) -Methode eines [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) -Objekts übergeben.</span><span class="sxs-lookup"><span data-stu-id="77b81-130">The following example passes the value [\*\*\*\*StringFormatFlagsDirectionVertical\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) to the [**StringFormat::SetFormatFlags**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setformatflags) method of a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object.</span></span> <span data-ttu-id="77b81-131">Die Adresse dieses **StringFormat** -Objekts wird an die [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) -Methode der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse übergeben.</span><span class="sxs-lookup"><span data-stu-id="77b81-131">The address of that **StringFormat** object is passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="77b81-132">Der Wert [\* \* \* \* stringformatflagsdirectionvertical \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) \* \* ist ein Element der **StringFormatFlags** -Enumeration, das in "gdiplusenums. h" deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="77b81-132">The value [\*\*\*\*StringFormatFlagsDirectionVertical\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) is an element of the **StringFormatFlags** enumeration, which is declared in Gdiplusenums.h.</span></span>


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



<span data-ttu-id="77b81-133">In der folgenden Abbildung ist der vertikale Text dargestellt.</span><span class="sxs-lookup"><span data-stu-id="77b81-133">The following illustration shows the vertical text.</span></span>

![Abbildung mit einem Fenster, das im Uhrzeigersinn 90 gedreht Text enthält](images/fontstext5.png)

 

 



