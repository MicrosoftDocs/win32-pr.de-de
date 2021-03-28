---
description: Bitmaps sollten in einer Datei gespeichert werden, die das festgelegte Bitmapdateiformat verwendet, und mit der Erweiterung "drei Zeichen. bmp" einen Namen zugewiesen.
ms.assetid: 44f19d14-4e0e-4512-8c86-6bd34ca4e87b
title: Bitmapspeicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28046f6d78f5137d0dfc5b1396bbf76be318daa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130845"
---
# <a name="bitmap-storage"></a><span data-ttu-id="88902-103">Bitmapspeicher</span><span class="sxs-lookup"><span data-stu-id="88902-103">Bitmap Storage</span></span>

<span data-ttu-id="88902-104">Bitmaps sollten in einer Datei gespeichert werden, die das festgelegte Bitmapdateiformat verwendet, und mit der Erweiterung "drei Zeichen. bmp" einen Namen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="88902-104">Bitmaps should be saved in a file that uses the established bitmap file format and assigned a name with the three-character .bmp extension.</span></span> <span data-ttu-id="88902-105">Das festgelegte Bitmapdateiformat besteht aus einer [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) -Struktur, gefolgt von einer [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))-, [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)-oder [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="88902-105">The established bitmap file format consists of a [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) structure followed by a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header), or [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) structure.</span></span> <span data-ttu-id="88902-106">Ein Array aus [**rgbquad**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) -Strukturen (auch als Farbtabelle bezeichnet) folgt der Struktur der bitmapinformationsheader.</span><span class="sxs-lookup"><span data-stu-id="88902-106">An array of [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structures (also called a color table) follows the bitmap information header structure.</span></span> <span data-ttu-id="88902-107">Auf die Farbtabelle folgt ein zweites Array von Indizes in die Farbtabelle (die eigentlichen Bitmapdaten).</span><span class="sxs-lookup"><span data-stu-id="88902-107">The color table is followed by a second array of indexes into the color table (the actual bitmap data).</span></span>

<span data-ttu-id="88902-108">Das Bitmapdateiformat ist in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="88902-108">The bitmap file format is shown in the following illustration.</span></span>

![Diagramm des bitmapdateiformats, das BITMAPFILEHEADER, BITMAPINFOHEADER, rgbquad Array und Farb Index Array anzeigt](images/csbmp-02.png)

<span data-ttu-id="88902-110">Die Elemente der [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) -Struktur identifizieren die Datei. Geben Sie die Größe der Datei in Bytes an. und geben den Offset vom ersten Byte in der Kopfzeile bis zum ersten Byte der Bitmapdaten an.</span><span class="sxs-lookup"><span data-stu-id="88902-110">The members of the [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) structure identify the file; specify the size of the file, in bytes; and specify the offset from the first byte in the header to the first byte of bitmap data.</span></span> <span data-ttu-id="88902-111">Die Elemente der [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))-, [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)-oder [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) -Struktur geben die Breite und Höhe der Bitmap in Pixel an. das Farb Format (Anzahl von Farbebenen und Farbbits pro Pixel) des Anzeige Geräts, auf dem die Bitmap erstellt wurde. Gibt an, ob die Bitmapdaten vor dem Speicher und dem verwendeten Komprimierungstyp komprimiert wurden. die Anzahl der Bytes von Bitmapdaten. die Auflösung des Anzeige Geräts, auf dem die Bitmap erstellt wurde. und die Anzahl der in den Daten dargestellten Farben.</span><span class="sxs-lookup"><span data-stu-id="88902-111">The members of the [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header), or [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) structure specify the width and height of the bitmap, in pixels; the color format (count of color planes and color bits-per-pixel) of the display device on which the bitmap was created; whether the bitmap data was compressed before storage and the type of compression used; the number of bytes of bitmap data; the resolution of the display device on which the bitmap was created; and the number of colors represented in the data.</span></span> <span data-ttu-id="88902-112">Die [**rgbquad**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) -Strukturen geben die RGB-Intensitätswerte für die einzelnen Farben in der Palette des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="88902-112">The [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structures specify the RGB intensity values for each of the colors in the device's palette.</span></span>

<span data-ttu-id="88902-113">Das Farb Index Array ordnet eine Farbe in Form eines Indexes einer [**rgbquad**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) -Struktur zu, wobei jedes Pixel in einer Bitmap angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="88902-113">The color-index array associates a color, in the form of an index to an [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure, with each pixel in a bitmap.</span></span> <span data-ttu-id="88902-114">Daher entspricht die Anzahl der Bits im Farb Index Array der Anzahl der Pixel, die für die Indizierung der **rgbquad** -Strukturen benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="88902-114">Thus, the number of bits in the color-index array equals the number of pixels times the number of bits needed to index the **RGBQUAD** structures.</span></span> <span data-ttu-id="88902-115">Beispielsweise verfügt eine "8x8 Black-and-White"-Bitmap über ein Farb Index Array von 8 \* 8 \* 1 = 64 Bits, da ein Bit erforderlich ist, um zwei Farben zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="88902-115">For example, an 8x8 black-and-white bitmap has a color-index array of 8 \* 8 \* 1 = 64 bits, because one bit is needed to index two colors.</span></span> <span data-ttu-id="88902-116">Der in [Informationen zu Bitmaps](about-bitmaps.md)erwähnte Redbrick.bmp ist eine 32 x 32-Bitmap mit 16 Farben. das Farb Index Array ist 32 \* 32 \* 4 = 4096 Bits, da vier Bits den Wert 16 Farben haben.</span><span class="sxs-lookup"><span data-stu-id="88902-116">The Redbrick.bmp, mentioned in [About Bitmaps](about-bitmaps.md), is a 32x32 bitmap with 16 colors; its color-index array is 32 \* 32 \* 4 = 4096 bits because four bits index 16 colors.</span></span>

<span data-ttu-id="88902-117">Zum Erstellen eines Farb Index Arrays für eine Top-Down-Bitmap beginnen Sie in der obersten Zeile in der Bitmap.</span><span class="sxs-lookup"><span data-stu-id="88902-117">To create a color-index array for a top-down bitmap, start at the top line in the bitmap.</span></span> <span data-ttu-id="88902-118">Der Index von [**rgbquad**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) für die Farbe des äußersten linken Pixels ist die erste *n* Bits im Farb Index Array (wobei *n* die Anzahl der Bits ist, die zum Angeben aller **rgbquad** -Strukturen benötigt werden).</span><span class="sxs-lookup"><span data-stu-id="88902-118">The index of the [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) for the color of the left-most pixel is the first *n* bits in the color-index array (where *n* is the number of bits needed to indicate all of the **RGBQUAD** structures).</span></span> <span data-ttu-id="88902-119">Die Farbe des nächsten Pixels auf der rechten Seite entspricht den nächsten *n* Bits im Array usw.</span><span class="sxs-lookup"><span data-stu-id="88902-119">The color of the next pixel to the right is the next *n* bits in the array, and so forth.</span></span> <span data-ttu-id="88902-120">Nachdem Sie das ganz rechts Pixel in der Linie erreicht haben, fahren Sie mit dem äußersten linken Pixel in der folgenden Zeile fort.</span><span class="sxs-lookup"><span data-stu-id="88902-120">After you reach the right-most pixel in the line, continue with the left-most pixel in the line below.</span></span> <span data-ttu-id="88902-121">Fahren Sie fort, bis die gesamte Bitmap abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="88902-121">Continue until you finish with the entire bitmap.</span></span> <span data-ttu-id="88902-122">Wenn es sich um eine untere Bitmap handelt, starten Sie in der unteren Zeile der Bitmap statt in der oberen Zeile, und fahren Sie von links nach rechts fort, und fahren Sie mit der obersten Zeile der Bitmap fort.</span><span class="sxs-lookup"><span data-stu-id="88902-122">If it is a bottom-up bitmap, start at the bottom line of the bitmap instead of the top line, still going from left to right, and continue to the top line of the bitmap.</span></span>

<span data-ttu-id="88902-123">In der folgenden hexadezimalen Ausgabe wird der Inhalt der Datei Redbrick.bmp angezeigt.</span><span class="sxs-lookup"><span data-stu-id="88902-123">The following hexadecimal output shows the contents of the file Redbrick.bmp.</span></span>


```C++
0000    42 4d 76 02 00 00 00 00  00 00 76 00 00 00 28 00 
0010    00 00 20 00 00 00 20 00  00 00 01 00 04 00 00 00 
0020    00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00 
0030    00 00 00 00 00 00 00 00  00 00 00 00 80 00 00 80 
0040    00 00 00 80 80 00 80 00  00 00 80 00 80 00 80 80 
0050    00 00 80 80 80 00 c0 c0  c0 00 00 00 ff 00 00 ff 
0060    00 00 00 ff ff 00 ff 00  00 00 ff 00 ff 00 ff ff 
0070    00 00 ff ff ff 00 00 00  00 00 00 00 00 00 00 00 
0080    00 00 00 00 00 00 00 00  00 00 00 00 00 00 09 00 
0090    00 00 00 00 00 00 11 11  01 19 11 01 10 10 09 09 
00a0    01 09 11 11 01 90 11 01  19 09 09 91 11 10 09 11 
00b0    09 11 19 10 90 11 19 01  19 19 10 10 11 10 09 01 
00c0    91 10 91 09 10 10 90 99  11 11 11 11 19 00 09 01 
00d0    91 01 01 19 00 99 11 10  11 91 99 11 09 90 09 91 
00e0    01 11 11 11 91 10 09 19  01 00 11 90 91 10 09 01 
00f0    11 99 10 01 11 11 91 11  11 19 10 11 99 10 09 10 
0100    01 11 11 11 19 10 11 09  09 10 19 10 10 10 09 01 
0110    11 19 00 01 10 19 10 11  11 01 99 01 11 90 09 19 
0120    11 91 11 91 01 11 19 10  99 00 01 19 09 10 09 19 
0130    10 91 11 01 11 11 91 01  91 19 11 00 99 90 09 01 
0140    01 99 19 01 91 10 19 91  91 09 11 99 11 10 09 91 
0150    11 10 11 91 99 10 90 11  01 11 11 19 11 90 09 11 
0160    00 19 10 11 01 11 99 99  99 99 99 99 99 99 09 99 
0170    99 99 99 99 99 99 00 00  00 00 00 00 00 00 00 00 
0180    00 00 00 00 00 00 90 00  00 00 00 00 00 00 00 00 
0190    00 00 00 00 00 00 99 11  11 11 19 10 19 19 11 09 
01a0    10 90 91 90 91 00 91 19  19 09 01 10 09 01 11 11 
01b0    91 11 11 11 10 00 91 11  01 19 10 11 10 01 01 11 
01c0    90 11 11 11 91 00 99 09  19 10 11 90 09 90 91 01 
01d0    19 09 91 11 01 00 90 10  19 11 00 11 11 00 10 11 
01e0    01 10 11 19 11 00 90 19  10 91 01 90 19 99 00 11 
01f0    91 01 11 01 91 00 99 09  09 01 10 11 91 01 10 91 
0200    99 11 10 90 91 00 91 11  00 10 11 01 10 19 19 09 
0210    10 00 99 01 01 00 91 01  19 91 19 91 11 09 10 11 
0220    00 91 00 10 90 00 99 01  11 10 09 10 10 19 09 01 
0230    91 90 11 09 11 00 90 99  11 11 11 90 19 01 19 01 
0240    91 01 01 19 09 00 91 10  11 91 99 09 09 90 11 91 
0250    01 19 11 11 91 00 91 19  01 00 11 00 91 10 11 01 
0260    11 11 10 01 11 00 99 99  99 99 99 99 99 99 99 99 
0270    99 99 99 99 99 90 
```



<span data-ttu-id="88902-124">In der folgenden Tabelle werden die Daten Bytes angezeigt, die den Strukturen in einer Bitmapdatei zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="88902-124">The following table shows the data bytes associated with the structures in a bitmap file.</span></span>



| <span data-ttu-id="88902-125">Struktur</span><span class="sxs-lookup"><span data-stu-id="88902-125">Structure</span></span>                                    | <span data-ttu-id="88902-126">Entsprechende bytes</span><span class="sxs-lookup"><span data-stu-id="88902-126">Corresponding bytes</span></span> |
|----------------------------------------------|---------------------|
| [<span data-ttu-id="88902-127">**BITMAPFILEHEADER**</span><span class="sxs-lookup"><span data-stu-id="88902-127">**BITMAPFILEHEADER**</span></span>](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) | <span data-ttu-id="88902-128">0x00 0x0D</span><span class="sxs-lookup"><span data-stu-id="88902-128">0x00 0x0D</span></span>           |
| <span data-ttu-id="88902-129">[**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="88902-129">[**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))</span></span> | <span data-ttu-id="88902-130">0x0E 0x35</span><span class="sxs-lookup"><span data-stu-id="88902-130">0x0E 0x35</span></span>           |
| <span data-ttu-id="88902-131">[**Rgbquad**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) -Array</span><span class="sxs-lookup"><span data-stu-id="88902-131">[**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) array</span></span>             | <span data-ttu-id="88902-132">0x36 0x75</span><span class="sxs-lookup"><span data-stu-id="88902-132">0x36 0x75</span></span>           |
| <span data-ttu-id="88902-133">Farb Index Array</span><span class="sxs-lookup"><span data-stu-id="88902-133">Color-index array</span></span>                            | <span data-ttu-id="88902-134">0x76 0x275</span><span class="sxs-lookup"><span data-stu-id="88902-134">0x76 0x275</span></span>          |



 

 

 
