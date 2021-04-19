---
title: _BITMAPINFOHEADER Struktur
description: Die \_ BITMAPINFOHEADER-Struktur definiert das Format eines Video Frames.
ms.assetid: 394b8ded-81db-4ad3-8cf7-086f1e832771
keywords:
- _BITMAPINFOHEADER Struktur von Windows-Medien Device Manager
topic_type:
- apiref
api_name:
- _BITMAPINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481c80b6d209e0da8d00ef06d88392504bcae8e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362076"
---
# <a name="_bitmapinfoheader-structure"></a><span data-ttu-id="1dbe9-104">\_BITMAPINFOHEADER-Struktur</span><span class="sxs-lookup"><span data-stu-id="1dbe9-104">\_BITMAPINFOHEADER structure</span></span>

<span data-ttu-id="1dbe9-105">Die **\_ BITMAPINFOHEADER** -Struktur definiert das Format eines Video Frames.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-105">The **\_BITMAPINFOHEADER** structure defines the format of a video frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dbe9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1dbe9-106">Syntax</span></span>


```C++
typedef struct _tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} _BITMAPINFOHEADER;
```



## <a name="members"></a><span data-ttu-id="1dbe9-107">Member</span><span class="sxs-lookup"><span data-stu-id="1dbe9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1dbe9-108">**bisize**</span><span class="sxs-lookup"><span data-stu-id="1dbe9-108">**biSize**</span></span>
</dt> <dd>

<span data-ttu-id="1dbe9-109">Gibt die Anzahl der Bytes an, die für die Struktur erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-109">Specifies the number of bytes required by the structure.</span></span>

</dd> <dt>

<span data-ttu-id="1dbe9-110">**biwidth**</span><span class="sxs-lookup"><span data-stu-id="1dbe9-110">**biWidth**</span></span>
</dt> <dd>

<span data-ttu-id="1dbe9-111">Gibt die Breite der Bitmap in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-111">Specifies the width of the bitmap, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="1dbe9-112">**biheight**</span><span class="sxs-lookup"><span data-stu-id="1dbe9-112">**biHeight**</span></span>
</dt> <dd>

<span data-ttu-id="1dbe9-113">Gibt die Höhe der Bitmap in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-113">Specifies the height of the bitmap, in pixels.</span></span> <span data-ttu-id="1dbe9-114">Wenn **biheight** positiv ist, ist die Bitmap ein Bottom-up-DIB, und der Ursprung ist die untere linke Ecke.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-114">If **biHeight** is positive, the bitmap is a bottom-up DIB and its origin is the lower-left corner.</span></span> <span data-ttu-id="1dbe9-115">Wenn **biheight** negativ ist, ist die Bitmap eine Top-Down-DIB, und Ihr Ursprung ist die linke obere Ecke.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-115">If **biHeight** is negative, the bitmap is a top-down DIB and its origin is the upper-left corner.</span></span> <span data-ttu-id="1dbe9-116">Wenn **biheight** auf einen negativen Wert festgelegt ist, der einen Top-Down-DIB anzeigt, muss die **bikomprimierung** entweder BI \_ RGB oder BI- \_ Bitfields sein</span><span class="sxs-lookup"><span data-stu-id="1dbe9-116">If **biHeight** is negative, indicating a top-down DIB, **biCompression** must be either BI\_RGB or BI\_BITFIELDS.</span></span> <span data-ttu-id="1dbe9-117">Top-Down-Disb können nicht komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-117">Top-down DIBs cannot be compressed.</span></span>

</dd> <dt>

<span data-ttu-id="1dbe9-118">**zwei Ebenen**</span><span class="sxs-lookup"><span data-stu-id="1dbe9-118">**biPlanes**</span></span>
</dt> <dd>

<span data-ttu-id="1dbe9-119">Gibt die Anzahl der Ebenen für das Zielgerät an.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-119">Specifies the number of planes for the target device.</span></span> <span data-ttu-id="1dbe9-120">Dieser Wert muss auf 1 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-120">This value must be set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="1dbe9-121">**biBitCount**</span><span class="sxs-lookup"><span data-stu-id="1dbe9-121">**biBitCount**</span></span>
</dt> <dd>

<span data-ttu-id="1dbe9-122">Gibt die Anzahl der Bits pro Pixel an.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-122">Specifies the number of bits per pixel.</span></span> <span data-ttu-id="1dbe9-123">Der **biBitCount** -Member der **BITMAPINFOHEADER** -Struktur bestimmt die Anzahl der Bits, die jedes Pixel definieren, sowie die maximale Anzahl von Farben in der Bitmap.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-123">The **biBitCount** member of the **BITMAPINFOHEADER** structure determines the number of bits that define each pixel and the maximum number of colors in the bitmap.</span></span> <span data-ttu-id="1dbe9-124">Dieser Member muss einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-124">This member must be one of the following values.</span></span>



| <span data-ttu-id="1dbe9-125">Wert</span><span class="sxs-lookup"><span data-stu-id="1dbe9-125">Value</span></span> | <span data-ttu-id="1dbe9-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1dbe9-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dbe9-127">1</span><span class="sxs-lookup"><span data-stu-id="1dbe9-127">1</span></span>     | <span data-ttu-id="1dbe9-128">Die Bitmap ist Monochrom und der bmicolors-Member enthält zwei Einträge.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-128">The bitmap is monochrome, and the bmiColors member contains two entries.</span></span> <span data-ttu-id="1dbe9-129">Jedes Bit im Bitmap-Array stellt ein Pixel dar.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-129">Each bit in the bitmap array represents a pixel.</span></span> <span data-ttu-id="1dbe9-130">Wenn das Bit eindeutig ist, wird das Pixel mit der Farbe des ersten Eintrags in der Tabelle bmicolors angezeigt. Wenn das-Bit festgelegt ist, hat das Pixel die Farbe des zweiten Eintrags in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-130">If the bit is clear, the pixel is displayed with the color of the first entry in the bmiColors table; if the bit is set, the pixel has the color of the second entry in the table.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="1dbe9-131">2</span><span class="sxs-lookup"><span data-stu-id="1dbe9-131">2</span></span>     | <span data-ttu-id="1dbe9-132">Die Bitmap verfügt über vier mögliche Farbwerte.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-132">The bitmap has four possible color values.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="1dbe9-133">4</span><span class="sxs-lookup"><span data-stu-id="1dbe9-133">4</span></span>     | <span data-ttu-id="1dbe9-134">Die Bitmap hat maximal 16 Farben, und der bmicolors-Member enthält bis zu 16 Einträge.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-134">The bitmap has a maximum of 16 colors, and the bmiColors member contains up to 16 entries.</span></span> <span data-ttu-id="1dbe9-135">Jedes Pixel in der Bitmap wird durch einen 4-Bit-Index in der Farbtabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-135">Each pixel in the bitmap is represented by a 4-bit index into the color table.</span></span> <span data-ttu-id="1dbe9-136">Wenn das erste Byte in der Bitmap z. b. 0x1F ist, stellt das Byte zwei Pixel dar.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-136">For example, if the first byte in the bitmap is 0x1F, the byte represents two pixels.</span></span> <span data-ttu-id="1dbe9-137">Das erste Pixel enthält die Farbe im zweiten Tabelleneintrag, und das zweite Pixel enthält die Farbe in der zehnten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-137">The first pixel contains the color in the second table entry, and the second pixel contains the color in the sixteenth table entry.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="1dbe9-138">8</span><span class="sxs-lookup"><span data-stu-id="1dbe9-138">8</span></span>     | <span data-ttu-id="1dbe9-139">Die Bitmap hat maximal 256 Farben, und der bmicolors-Member enthält bis zu 256 Einträge.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-139">The bitmap has a maximum of 256 colors, and the bmiColors member contains up to 256 entries.</span></span> <span data-ttu-id="1dbe9-140">In diesem Fall stellt jedes Byte im Array ein einzelnes Pixel dar.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-140">In this case, each byte in the array represents a single pixel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="1dbe9-141">16</span><span class="sxs-lookup"><span data-stu-id="1dbe9-141">16</span></span>    | <span data-ttu-id="1dbe9-142">Die Bitmap hat maximal 2 ^ 16 Farben.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-142">The bitmap has a maximum of 2^16 colors.</span></span> <span data-ttu-id="1dbe9-143">Wenn der bicompression-Member von BITMAPINFOHEADER BI \_ RGB ist, ist der bmicolors-Member **null**.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-143">If the biCompression member of the BITMAPINFOHEADER is BI\_RGB, the bmiColors member is **NULL**.</span></span> <span data-ttu-id="1dbe9-144">Jedes Wort im bitmaparray stellt ein einzelnes Pixel dar.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-144">Each WORD in the bitmap array represents a single pixel.</span></span> <span data-ttu-id="1dbe9-145">Die relativen Intensitäten von rot, grün und blau werden für jede Farbkomponente mit 5 Bits dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-145">The relative intensities of red, green, and blue are represented with 5 bits for each color component.</span></span> <span data-ttu-id="1dbe9-146">Der Wert für blau liegt in den geringsten 5 Bits, gefolgt von 5 Bits für Grün und rot.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-146">The value for blue is in the least significant 5 bits, followed by 5 bits each for green and red.</span></span> <span data-ttu-id="1dbe9-147">Das signifikanteste Bit wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-147">The most significant bit is not used.</span></span> <span data-ttu-id="1dbe9-148">Die Farbtabelle bmicolors dient zum Optimieren von Farben, die auf palettenbasierten Geräten verwendet werden, und muss die Anzahl der Einträge enthalten, die vom biclrused-Member angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-148">The bmiColors color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the biClrUsed member.</span></span> |
| <span data-ttu-id="1dbe9-149">24</span><span class="sxs-lookup"><span data-stu-id="1dbe9-149">24</span></span>    | <span data-ttu-id="1dbe9-150">Die Bitmap hat maximal 2 ^ 24 Farben, und der bmicolors-Member ist **null**.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-150">The bitmap has a maximum of 2^24 colors, and the bmiColors member is **NULL**.</span></span> <span data-ttu-id="1dbe9-151">Jede 3-Byte-Zahl im Bitmap-Array stellt die relativen Intensitäten von blau, grün und rot für ein Pixel dar.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-151">Each 3-byte triplet in the bitmap array represents the relative intensities of blue, green, and red, respectively, for a pixel.</span></span> <span data-ttu-id="1dbe9-152">Die Farbtabelle bmicolors dient zum Optimieren von Farben, die auf palettenbasierten Geräten verwendet werden, und muss die Anzahl der Einträge enthalten, die vom biclrused-Member angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-152">The bmiColors color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the biClrUsed member.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="1dbe9-153">32</span><span class="sxs-lookup"><span data-stu-id="1dbe9-153">32</span></span>    | <span data-ttu-id="1dbe9-154">Die Bitmap hat maximal 2 ^ 32 Farben.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-154">The bitmap has a maximum of 2^32 colors.</span></span> <span data-ttu-id="1dbe9-155">Wenn der bicompression-Member BI \_ RGB ist, ist der bmicolors-Member **null**.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-155">If the biCompression member is BI\_RGB, the bmiColors member is **NULL**.</span></span> <span data-ttu-id="1dbe9-156">Jedes DWORD im Bitmap-Array stellt die relativen Intensitäten von blau, grün und rot für ein Pixel dar.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-156">Each DWORD in the bitmap array represents the relative intensities of blue, green, and red, respectively, for a pixel.</span></span> <span data-ttu-id="1dbe9-157">Das hohe Byte in jedem DWORD wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-157">The high byte in each DWORD is not used.</span></span> <span data-ttu-id="1dbe9-158">Die Farbtabelle bmicolors dient zum Optimieren von Farben, die auf palettenbasierten Geräten verwendet werden, und muss die Anzahl der Einträge enthalten, die vom biclrused-Member angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-158">The bmiColors color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the biClrUsed member.</span></span>                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="1dbe9-159">**bikomprimierung**</span><span class="sxs-lookup"><span data-stu-id="1dbe9-159">**biCompression**</span></span>
</dt> <dd>

<span data-ttu-id="1dbe9-160">Gibt den Komprimierungstyp für eine komprimierte Bottom-up-Bitmap an (Top-Down-Disb können nicht komprimiert werden).</span><span class="sxs-lookup"><span data-stu-id="1dbe9-160">Specifies the type of compression for a compressed bottom-up bitmap (top-down DIBs cannot be compressed).</span></span> <span data-ttu-id="1dbe9-161">Dieser Member kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-161">This member can be the one of the following values.</span></span>



| <span data-ttu-id="1dbe9-162">Wert</span><span class="sxs-lookup"><span data-stu-id="1dbe9-162">Value</span></span>         | <span data-ttu-id="1dbe9-163">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1dbe9-163">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dbe9-164">BI \_ RGB</span><span class="sxs-lookup"><span data-stu-id="1dbe9-164">BI\_RGB</span></span>       | <span data-ttu-id="1dbe9-165">Ein unkomprimiertes Format.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-165">An uncompressed format.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="1dbe9-166">BI- \_ Bitfields</span><span class="sxs-lookup"><span data-stu-id="1dbe9-166">BI\_BITFIELDS</span></span> | <span data-ttu-id="1dbe9-167">Gibt an, dass die Bitmap nicht komprimiert ist und dass die Farbtabelle aus drei DWORD-Farb Masken besteht, die jeweils die roten, grünen und blauen Komponenten der einzelnen Pixel angeben.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-167">Specifies that the bitmap is not compressed and that the color table consists of three DWORD color masks that specify the red, green, and blue components, respectively, of each pixel.</span></span> <span data-ttu-id="1dbe9-168">Dies ist gültig bei Verwendung mit 16-bpp-und 32-bpp-Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-168">This is valid when used with 16-bpp and 32-bpp bitmaps.</span></span> <span data-ttu-id="1dbe9-169">Dieser Wert ist in Microsoft Windows CE Version 2,0 und höher gültig.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-169">This value is valid in Microsoft Windows CE version 2.0 and later.</span></span> |



 

</dd> <dt>

<span data-ttu-id="1dbe9-170">**bisizeimage**</span><span class="sxs-lookup"><span data-stu-id="1dbe9-170">**biSizeImage**</span></span>
</dt> <dd>

<span data-ttu-id="1dbe9-171">Gibt die Größe des Bilds in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-171">Specifies the size of the image, in bytes.</span></span> <span data-ttu-id="1dbe9-172">Dieser Wert kann für BI RGB-Bitmaps auf 0 (null) festgelegt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="1dbe9-172">This may be set to zero for BI\_RGB bitmaps.</span></span>

</dd> <dt>

<span data-ttu-id="1dbe9-173">**bixpelspermeter**</span><span class="sxs-lookup"><span data-stu-id="1dbe9-173">**biXPelsPerMeter**</span></span>
</dt> <dd>

<span data-ttu-id="1dbe9-174">Gibt die horizontale Auflösung des Zielgeräts für die Bitmap in Pixel pro Meter an.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-174">Specifies the horizontal resolution, in pixels per meter, of the target device for the bitmap.</span></span> <span data-ttu-id="1dbe9-175">Mit diesem Wert kann eine Anwendung eine Bitmap aus einer Ressourcengruppe auswählen, die den Merkmalen des aktuellen Geräts am besten entspricht.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-175">An application can use this value to select a bitmap from a resource group that best matches the characteristics of the current device.</span></span>

</dd> <dt>

<span data-ttu-id="1dbe9-176">**biypelspermeter**</span><span class="sxs-lookup"><span data-stu-id="1dbe9-176">**biYPelsPerMeter**</span></span>
</dt> <dd>

<span data-ttu-id="1dbe9-177">Gibt die vertikale Auflösung des Zielgeräts für die Bitmap in Pixel pro Meter an.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-177">Specifies the vertical resolution, in pixels per meter, of the target device for the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="1dbe9-178">**biclrused**</span><span class="sxs-lookup"><span data-stu-id="1dbe9-178">**biClrUsed**</span></span>
</dt> <dd>

<span data-ttu-id="1dbe9-179">Gibt die Anzahl der Farbindizes in der Farbtabelle an, die tatsächlich von der Bitmap verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-179">Specifies the number of color indexes in the color table that are actually used by the bitmap.</span></span> <span data-ttu-id="1dbe9-180">Wenn dieser Wert 0 (null) ist, verwendet die Bitmap die maximale Anzahl von Farben, die dem Wert des **biBitCount** -Members für den durch die **bikomprimierung** angegebenen Komprimierungs Modus entspricht.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-180">If this value is zero, the bitmap uses the maximum number of colors corresponding to the value of the **biBitCount** member for the compression mode specified by **biCompression**.</span></span>

</dd> <dt>

<span data-ttu-id="1dbe9-181">**biclrimportant**</span><span class="sxs-lookup"><span data-stu-id="1dbe9-181">**biClrImportant**</span></span>
</dt> <dd>

<span data-ttu-id="1dbe9-182">Gibt die Anzahl der für die Anzeige der Bitmap erforderlichen Farbindizes an.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-182">Specifies the number of color indexes required for displaying the bitmap.</span></span> <span data-ttu-id="1dbe9-183">Wenn dieser Wert 0 (null) ist, sind alle Farben erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-183">If this value is zero, all colors are required.</span></span>

<span data-ttu-id="1dbe9-184">Wenn der biclrused-Wert ungleich 0 (null) und der biBitCount-Member kleiner als 16 ist, gibt der biclrused-Member die tatsächliche Anzahl der Farben an, auf die das Grafik Modul oder der Gerätetreiber zugreift</span><span class="sxs-lookup"><span data-stu-id="1dbe9-184">If biClrUsed is nonzero and the biBitCount member is less than 16, the biClrUsed member specifies the actual number of colors the graphics engine or device driver accesses.</span></span> <span data-ttu-id="1dbe9-185">Wenn biBitCount 16 oder größer ist, gibt der biclrused-Member die Größe der Farbtabelle an, die zum Optimieren der Leistung der System Farbpaletten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-185">If biBitCount is 16 or greater, the biClrUsed member specifies the size of the color table used to optimize performance of the system color palettes.</span></span> <span data-ttu-id="1dbe9-186">Wenn biBitCount gleich 16 oder 32 ist, beginnt die optimale Farbpalette unmittelbar nach den drei DWORD-Masken.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-186">If biBitCount equals 16 or 32, the optimal color palette starts immediately following the three DWORD masks.</span></span>

<span data-ttu-id="1dbe9-187">Wenn es sich bei der Bitmap um eine gepackte Bitmap handelt (eine Bitmap, in der das bitmaparray unmittelbar auf die \_ BITMAPINFOHEADER-Struktur folgt und von einem einzelnen Zeiger referenziert wird), muss der biclrused-Member entweder 0 (null) oder die tatsächliche Größe der Farbtabelle aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-187">If the bitmap is a packed bitmap (a bitmap in which the bitmap array immediately follows the \_BITMAPINFOHEADER structure and is referenced by a single pointer), the biClrUsed member must be either zero or the actual size of the color table.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1dbe9-188">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1dbe9-188">Remarks</span></span>

<span data-ttu-id="1dbe9-189">Diese Struktur ist in einer **\_ videoinfoheader** -Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="1dbe9-189">This structure is contained within a **\_VIDEOINFOHEADER** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dbe9-190">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1dbe9-190">Requirements</span></span>



| <span data-ttu-id="1dbe9-191">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1dbe9-191">Requirement</span></span> | <span data-ttu-id="1dbe9-192">Wert</span><span class="sxs-lookup"><span data-stu-id="1dbe9-192">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1dbe9-193">Header</span><span class="sxs-lookup"><span data-stu-id="1dbe9-193">Header</span></span><br/> | <dl> <span data-ttu-id="1dbe9-194"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1dbe9-194"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dbe9-195">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1dbe9-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dbe9-196">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="1dbe9-196">**Structures**</span></span>](structures.md)
</dt> <dt>

[<span data-ttu-id="1dbe9-197">**\_Videoinfoheader**</span><span class="sxs-lookup"><span data-stu-id="1dbe9-197">**\_VIDEOINFOHEADER**</span></span>](-videoinfoheader.md)
</dt> </dl>

 

 





