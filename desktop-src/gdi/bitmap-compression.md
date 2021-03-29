---
description: Windows unterstützt Formate zum Komprimieren von Bitmaps, die ihre Farben mit 8 oder 4 Bits pro Pixel definieren. Durch die Komprimierung wird der für die Bitmap erforderliche Datenträger-und Speicher Speicher reduziert.
ms.assetid: 14d14662-910a-4f3f-914e-6ccfc602c822
title: Bitmapkomprimierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38739f0e33f095b8eff567fc63b57db96b8cdc66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130853"
---
# <a name="bitmap-compression"></a><span data-ttu-id="39a37-104">Bitmapkomprimierung</span><span class="sxs-lookup"><span data-stu-id="39a37-104">Bitmap Compression</span></span>

<span data-ttu-id="39a37-105">Windows unterstützt Formate zum Komprimieren von Bitmaps, die ihre Farben mit 8 oder 4 Bits pro Pixel definieren.</span><span class="sxs-lookup"><span data-stu-id="39a37-105">Windows supports formats for compressing bitmaps that define their colors with 8 or 4 bits-per-pixel.</span></span> <span data-ttu-id="39a37-106">Durch die Komprimierung wird der für die Bitmap erforderliche Datenträger-und Speicher Speicher reduziert.</span><span class="sxs-lookup"><span data-stu-id="39a37-106">Compression reduces the disk and memory storage required for the bitmap.</span></span>

<span data-ttu-id="39a37-107">Wenn das **Komprimierungs** Element der Bitmap-Informations Header Struktur BI \_ RLE8 ist, wird ein RLE-Format (Run-Length Encoding) zum Komprimieren einer 8-Bit-Bitmap verwendet.</span><span class="sxs-lookup"><span data-stu-id="39a37-107">When the **Compression** member of the bitmap information header structure is BI\_RLE8, a run-length encoding (RLE) format is used to compress an 8-bit bitmap.</span></span> <span data-ttu-id="39a37-108">Dieses Format kann im codierten oder absoluten Modus komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="39a37-108">This format can be compressed in encoded or absolute modes.</span></span> <span data-ttu-id="39a37-109">Beide Modi können an beliebiger Stelle in der gleichen Bitmap vorkommen:</span><span class="sxs-lookup"><span data-stu-id="39a37-109">Both modes can occur anywhere in the same bitmap:</span></span>

-   <span data-ttu-id="39a37-110">Der *codierte Modus* besteht aus zwei Bytes: mit dem ersten Byte wird die Anzahl der aufeinander folgenden Pixel angegeben, die mit dem im zweiten Byte enthaltenen Farb Index gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="39a37-110">*Encoded mode* consists of two bytes: the first byte specifies the number of consecutive pixels to be drawn using the color index contained in the second byte.</span></span> <span data-ttu-id="39a37-111">Außerdem kann das erste Byte des Paars auf 0 (null) festgelegt werden, um ein Escapezeichen anzugeben, das das Ende einer Zeile, das Ende einer Bitmap oder ein Delta angibt, abhängig vom Wert des zweiten bytes.</span><span class="sxs-lookup"><span data-stu-id="39a37-111">In addition, the first byte of the pair can be set to zero to indicate an escape character that denotes the end of a line, the end of a bitmap, or a delta, depending on the value of the second byte.</span></span> <span data-ttu-id="39a37-112">Die Interpretation der Escapesequenz hängt vom Wert des zweiten Bytes des Paars ab, bei dem es sich um einen der folgenden Werte handeln kann.</span><span class="sxs-lookup"><span data-stu-id="39a37-112">The interpretation of the escape depends on the value of the second byte of the pair, which can be one of the following values.</span></span>



| <span data-ttu-id="39a37-113">Wert</span><span class="sxs-lookup"><span data-stu-id="39a37-113">Value</span></span> | <span data-ttu-id="39a37-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="39a37-114">Meaning</span></span>                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39a37-115">0</span><span class="sxs-lookup"><span data-stu-id="39a37-115">0</span></span>     | <span data-ttu-id="39a37-116">Zeilenende.</span><span class="sxs-lookup"><span data-stu-id="39a37-116">End of line.</span></span>                                                                                                                                                |
| <span data-ttu-id="39a37-117">1</span><span class="sxs-lookup"><span data-stu-id="39a37-117">1</span></span>     | <span data-ttu-id="39a37-118">Ende der Bitmap.</span><span class="sxs-lookup"><span data-stu-id="39a37-118">End of bitmap.</span></span>                                                                                                                                              |
| <span data-ttu-id="39a37-119">2</span><span class="sxs-lookup"><span data-stu-id="39a37-119">2</span></span>     | <span data-ttu-id="39a37-120">SS.</span><span class="sxs-lookup"><span data-stu-id="39a37-120">Delta.</span></span> <span data-ttu-id="39a37-121">Die 2 Bytes nach dem Escapezeichen enthalten nicht signierte Werte, die die horizontale und vertikale Offsets des nächsten Pixels von der aktuellen Position angeben.</span><span class="sxs-lookup"><span data-stu-id="39a37-121">The 2 bytes following the escape contain unsigned values indicating the horizontal and vertical offsets of the next pixel from the current position.</span></span> |



 

-   <span data-ttu-id="39a37-122">Im *absoluten Modus* ist das erste Byte 0 (null), und das zweite Byte ist ein Wert im Bereich 03h bis FFH.</span><span class="sxs-lookup"><span data-stu-id="39a37-122">In *absolute mode*, the first byte is zero and the second byte is a value in the range 03H through FFH.</span></span> <span data-ttu-id="39a37-123">Das zweite Byte stellt die Anzahl der folgenden Bytes dar, von denen jeder den Farbindex eines einzelnen Pixels enthält.</span><span class="sxs-lookup"><span data-stu-id="39a37-123">The second byte represents the number of bytes that follow, each of which contains the color index of a single pixel.</span></span> <span data-ttu-id="39a37-124">Wenn das zweite Byte zwei oder weniger ist, hat der Escape die gleiche Bedeutung wie der codierte Modus.</span><span class="sxs-lookup"><span data-stu-id="39a37-124">When the second byte is two or less, the escape has the same meaning as encoded mode.</span></span> <span data-ttu-id="39a37-125">Im absoluten Modus muss jede ausführen an einer Wort Grenze ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="39a37-125">In absolute mode, each run must be aligned on a word boundary.</span></span>

<span data-ttu-id="39a37-126">Das folgende Beispiel zeigt die hexadezimalen Werte einer komprimierten 8-Bit-Bitmap:</span><span class="sxs-lookup"><span data-stu-id="39a37-126">The following example shows the hexadecimal values of an 8-bit compressed bitmap:</span></span>


```C++
[03 04] [05 06] [00 03 45 56 67] [02 78] [00 02 05 01] 
[02 78] [00 00] [09 1E] [00 01] 
```



<span data-ttu-id="39a37-127">Die Bitmap wird wie folgt erweitert (zweistellige Werte stellen einen Farbindex für ein einzelnes Pixel dar):</span><span class="sxs-lookup"><span data-stu-id="39a37-127">The bitmap expands as follows (two-digit values represent a color index for a single pixel):</span></span>


```C++
04 04 04 
06 06 06 06 06 
45 56 67 
78 78 
move current position 5 right and 1 down 
78 78 
end of line 
1E 1E 1E 1E 1E 1E 1E 1E 1E 
end of RLE bitmap 
```



<span data-ttu-id="39a37-128">Wenn das **Komprimierungs** Element "BI RLE4" ist \_ , wird die Bitmap mithilfe eines Codierungs Formats der Laufzeit für eine 4-Bit-Bitmap komprimiert, das auch codierte und absolute Modi verwendet:</span><span class="sxs-lookup"><span data-stu-id="39a37-128">When the **Compression** member is BI\_RLE4, the bitmap is compressed by using a run-length encoding format for a 4-bit bitmap, which also uses encoded and absolute modes:</span></span>

-   <span data-ttu-id="39a37-129">Im codierten Modus enthält das erste Byte des Paars die Anzahl der Pixel, die mit den Farbindizes im zweiten Byte gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="39a37-129">In encoded mode, the first byte of the pair contains the number of pixels to be drawn using the color indexes in the second byte.</span></span> <span data-ttu-id="39a37-130">Das zweite Byte enthält zwei Farbindizes, eine in den hochwertigen 4 Bits und eine in den nieder wertigen 4 Bits.</span><span class="sxs-lookup"><span data-stu-id="39a37-130">The second byte contains two color indexes, one in its high-order 4 bits and one in its low-order 4 bits.</span></span> <span data-ttu-id="39a37-131">Der erste der Pixel wird mit der Farbe gezeichnet, die von den vier Bits mit hoher Reihenfolge angegeben wird, die zweite wird mit der Farbe in den niedriger Reihenfolge 4 Bits gezeichnet, die dritte mit der Farbe in den vier Bits mit hoher Reihenfolge usw., bis alle durch das erste Byte angegebenen Pixel gezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="39a37-131">The first of the pixels is drawn using the color specified by the high-order 4 bits, the second is drawn using the color in the low-order 4 bits, the third is drawn using the color in the high-order 4 bits, and so on, until all the pixels specified by the first byte have been drawn.</span></span>
-   <span data-ttu-id="39a37-132">Im absoluten Modus ist das erste Byte gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="39a37-132">In absolute mode, the first byte is zero.</span></span> <span data-ttu-id="39a37-133">Das zweite Byte enthält die Anzahl der folgenden Farbindizes.</span><span class="sxs-lookup"><span data-stu-id="39a37-133">The second byte contains the number of color indexes that follow.</span></span> <span data-ttu-id="39a37-134">Nachfolgende Bytes enthalten Farbindizes in ihren High-und Low-Order 4-Bits, einen Farbindex für jedes Pixel.</span><span class="sxs-lookup"><span data-stu-id="39a37-134">Subsequent bytes contain color indexes in their high- and low-order 4 bits, one color index for each pixel.</span></span> <span data-ttu-id="39a37-135">Im absoluten Modus muss jede ausführen an einer Wort Grenze ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="39a37-135">In absolute mode, each run must be aligned on a word boundary.</span></span> <span data-ttu-id="39a37-136">Die für BI-RLE8 beschriebenen End-of-Line-, End-of-Bitmap-und Delta-Escapezeichen \_ gelten auch für die BI \_ RLE4-Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="39a37-136">The end-of-line, end-of-bitmap, and delta escapes described for BI\_RLE8 also apply to BI\_RLE4 compression.</span></span>

<span data-ttu-id="39a37-137">Das folgende Beispiel zeigt die hexadezimalen Werte einer komprimierten 4-Bit-Bitmap:</span><span class="sxs-lookup"><span data-stu-id="39a37-137">The following example shows the hexadecimal values of a 4-bit compressed bitmap:</span></span>


```C++
03 04 05 06 00 06 45 56 67 00 04 78 00 02 05 01 
04 78 00 00 09 1E 00 01 
```



<span data-ttu-id="39a37-138">Die Bitmap wird wie folgt erweitert (einstellige Werte stellen einen Farbindex für ein einzelnes Pixel dar):</span><span class="sxs-lookup"><span data-stu-id="39a37-138">The bitmap expands as follows (single-digit values represent a color index for a single pixel):</span></span>


```C++
0 4 0 
0 6 0 6 0 
4 5 5 6 6 7 
7 8 7 8 
move current position 5 right and 1 down 
7 8 7 8 
end of line 
1 E 1 E 1 E 1 E 1 
end of RLE bitmap 
```



 

 



