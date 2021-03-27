---
description: Das Thema Zeichnen einer Linie zeigt, wie Sie eine Windows-Anwendung schreiben, die Windows GDI+ verwendet, um eine Linie zu zeichnen.
ms.assetid: fcf45b19-456c-4551-8901-d587a73a5638
title: Zeichnen einer Zeichenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a88e76fd38dd640a402edf202dc6cdbd3008a76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215589"
---
# <a name="drawing-a-string"></a><span data-ttu-id="72e53-103">Zeichnen einer Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="72e53-103">Drawing a String</span></span>

<span data-ttu-id="72e53-104">Das Thema [Zeichnen einer Linie](-gdiplus-drawing-a-line-use.md) zeigt, wie Sie eine Windows-Anwendung schreiben, die Windows GDI+ verwendet, um eine Linie zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="72e53-104">The topic [Drawing a Line](-gdiplus-drawing-a-line-use.md) shows how to write a Windows application that uses Windows GDI+ to draw a line.</span></span> <span data-ttu-id="72e53-105">Um eine Zeichenfolge zu zeichnen, ersetzen Sie die in diesem Thema gezeigte **OnPaint** -Funktion durch die folgende **OnPaint** -Funktion:</span><span class="sxs-lookup"><span data-stu-id="72e53-105">To draw a string, replace the **OnPaint** function shown in that topic with the following **OnPaint** function:</span></span>


```
VOID OnPaint(HDC hdc)
{
   Graphics    graphics(hdc);
   SolidBrush  brush(Color(255, 0, 0, 255));
   FontFamily  fontFamily(L"Times New Roman");
   Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
   PointF      pointF(10.0f, 20.0f);
   
   graphics.DrawString(L"Hello World!", -1, &font, pointF, &brush);
}
```



<span data-ttu-id="72e53-106">Der vorherige Code erstellt mehrere GDI+-Objekte.</span><span class="sxs-lookup"><span data-stu-id="72e53-106">The previous code creates several GDI+ objects.</span></span> <span data-ttu-id="72e53-107">Das [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt stellt die [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) -Methode bereit, die die eigentliche Zeichnung durchführt.</span><span class="sxs-lookup"><span data-stu-id="72e53-107">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object provides the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method, which does the actual drawing.</span></span> <span data-ttu-id="72e53-108">Das [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) -Objekt gibt die Farbe der Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="72e53-108">The [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object specifies the color of the string.</span></span>

<span data-ttu-id="72e53-109">Der [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) -Konstruktor empfängt ein einzelnes Zeichen folgen Argument, das die Schriftfamilie identifiziert.</span><span class="sxs-lookup"><span data-stu-id="72e53-109">The [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) constructor receives a single, string argument that identifies the font family.</span></span> <span data-ttu-id="72e53-110">Die Adresse des **FontFamily** -Objekts ist das erste Argument, das an den [**Schriftart**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) -Konstruktor übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="72e53-110">The address of the **FontFamily** object is the first argument passed to the [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) constructor.</span></span> <span data-ttu-id="72e53-111">Das zweite Argument, das an den [Schriftart](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(constfont_)) -Konstruktor übergeben wird, gibt den Schrift Grad an, und das dritte Argument gibt den Stil an.</span><span class="sxs-lookup"><span data-stu-id="72e53-111">The second argument passed to the [Font](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(constfont_)) constructor specifies the font size, and the third argument specifies the style.</span></span> <span data-ttu-id="72e53-112">Der Wert **fontstyleregfeiner** ist ein Member der [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) -Enumeration, der in "gdiplusenums. h" deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="72e53-112">The value **FontStyleRegular** is a member of the [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) enumeration, which is declared in Gdiplusenums.h.</span></span> <span data-ttu-id="72e53-113">Das letzte Argument für den **Schriftart** -Konstruktor gibt an, dass die Größe der Schriftart (in diesem Fall 24) in Pixel gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="72e53-113">The last argument to the **Font** constructor indicates that the size of the font (24 in this case) is measured in pixels.</span></span> <span data-ttu-id="72e53-114">Der Wert **unitpixel** ist ein Member der [**Unit**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-unit) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="72e53-114">The value **UnitPixel** is a member of the [**Unit**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-unit) enumeration.</span></span>

<span data-ttu-id="72e53-115">Das erste Argument, das an die [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) -Methode weitergegeben wird, ist die Adresse einer Zeichenfolge mit breit Zeichen.</span><span class="sxs-lookup"><span data-stu-id="72e53-115">The first argument passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method is the address of a wide-character string.</span></span> <span data-ttu-id="72e53-116">Das zweite Argument, – 1, gibt an, dass die Zeichenfolge NULL ist.</span><span class="sxs-lookup"><span data-stu-id="72e53-116">The second argument, –1, specifies that the string is null terminated.</span></span> <span data-ttu-id="72e53-117">(Wenn die Zeichenfolge nicht NULL endet, sollte das zweite Argument die Anzahl der breit Zeichen in der Zeichenfolge angeben.) Das dritte Argument ist die Adresse des [**Schriftart**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) Objekts.</span><span class="sxs-lookup"><span data-stu-id="72e53-117">(If the string is not null terminated, the second argument should specify the number of wide characters in the string.) The third argument is the address of the [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) object.</span></span> <span data-ttu-id="72e53-118">Das vierte Argument ist ein Verweis auf ein [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf) -Objekt, das den Speicherort angibt, an dem die Zeichenfolge gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="72e53-118">The fourth argument is a reference to a [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf) object that specifies the location where the string will be drawn.</span></span> <span data-ttu-id="72e53-119">Das letzte Argument ist die Adresse des [**Pinsel**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) Objekts, das die Farbe der Zeichenfolge angibt.</span><span class="sxs-lookup"><span data-stu-id="72e53-119">The last argument is the address of the [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) object, which specifies the color of the string.</span></span>

 

 
