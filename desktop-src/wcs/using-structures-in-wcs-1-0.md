---
title: Verwenden von Strukturen in WCS 1.0
description: Die meisten der von WCS 1,0 verwendeten Strukturen sind sehr unkompliziert und erfordern wenig Erläuterungen. Sie sind im Abschnitt "WCS 1,0 Reference" mit dem Titel "Strukturen" dokumentiert.
ms.assetid: 8d3682e2-38fd-4a33-b386-ab0716bb6972
keywords:
- Windows Color System (WCS), Strukturen
- WCS (Windows Color System), Strukturen
- Bild Farbverwaltung, Strukturen
- Farbverwaltung, Strukturen
- Farben, Strukturen
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d6e434ccfa6d96aa815f0c1997dc7f34178a32
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106354922"
---
# <a name="using-structures-in-wcs-10"></a><span data-ttu-id="ef7cd-109">Verwenden von Strukturen in WCS 1.0</span><span class="sxs-lookup"><span data-stu-id="ef7cd-109">Using Structures in WCS 1.0</span></span>

<span data-ttu-id="ef7cd-110">Die meisten der von WCS 1,0 verwendeten Strukturen sind sehr unkompliziert und erfordern wenig Erläuterungen.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-110">Most of the structures used by WCS 1.0 are very straightforward and require little explanation.</span></span> <span data-ttu-id="ef7cd-111">Sie sind im Abschnitt "WCS 1,0 Reference" mit dem Titel " [Strukturen](structures.md)" dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-111">They are documented in the WCS 1.0 Reference section entitled [Structures](structures.md).</span></span>

<span data-ttu-id="ef7cd-112">Ausnahmen sind die [**colormatchsetupw**](/windows/win32/api/icm/ns-icm-colormatchsetupw) -Struktur, die von der [**setupcolormatchingw**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) -Funktion verwendet wird, und die folgenden Windows-Strukturen, die in WinGDI. h definiert sind:</span><span class="sxs-lookup"><span data-stu-id="ef7cd-112">Exceptions are the [**COLORMATCHSETUPW**](/windows/win32/api/icm/ns-icm-colormatchsetupw) structure used by the [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) function, and the following Windows structures defined in Wingdi.h:</span></span>

-   [<span data-ttu-id="ef7cd-113">BITMAPV5HEADER</span><span class="sxs-lookup"><span data-stu-id="ef7cd-113">BITMAPV5HEADER</span></span>](#windows-bitmap-header-structures)
-   [<span data-ttu-id="ef7cd-114">**Logcolorspace**</span><span class="sxs-lookup"><span data-stu-id="ef7cd-114">**LOGCOLORSPACE**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea)
-   [<span data-ttu-id="ef7cd-115">**CIEXYZ**</span><span class="sxs-lookup"><span data-stu-id="ef7cd-115">**CIEXYZ**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-tagciexyz)
-   [<span data-ttu-id="ef7cd-116">**Ciexyztriple**</span><span class="sxs-lookup"><span data-stu-id="ef7cd-116">**CIEXYZTRIPLE**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-tagicexyztriple)

<span data-ttu-id="ef7cd-117">Die folgenden Themen werden in größerem Umfang behandelt:</span><span class="sxs-lookup"><span data-stu-id="ef7cd-117">The following topics are discussed at greater length:</span></span>

-   [<span data-ttu-id="ef7cd-118">Windows-Bitmap-Header Strukturen</span><span class="sxs-lookup"><span data-stu-id="ef7cd-118">Windows Bitmap Header Structures</span></span>](#windows-bitmap-header-structures)
-   [<span data-ttu-id="ef7cd-119">Unterschiede zwischen v4-und V5-Headern</span><span class="sxs-lookup"><span data-stu-id="ef7cd-119">Differences Between V4 and V5 Headers</span></span>](#differences-between-v4-and-v5-headers)
-   [<span data-ttu-id="ef7cd-120">Bitmap.exe: ein Command-Line Hilfsprogramm zum Umrechnen von bitmapheadern.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-120">Bitmap.exe: a Command-Line Utility for Converting Bitmap Headers</span></span>](#bitmapexe-a-command-line-utility-for-converting-bitmap-headers)

## <a name="windows-bitmap-header-structures"></a><span data-ttu-id="ef7cd-121">Windows-Bitmap-Header Strukturen</span><span class="sxs-lookup"><span data-stu-id="ef7cd-121">Windows Bitmap Header Structures</span></span>

<span data-ttu-id="ef7cd-122">Mit WCS 1,0 können Sie die Verknüpfung von "ICC"-Farbprofilen in geräteunabhängigen Bitmaps (Disb) ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-122">WCS 1.0 allows ICC color profiles to be linked or embedded in device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="ef7cd-123">Dadurch können DIB-Farben präziser als die Verwendung von WCS in Windows 95 gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-123">This allows DIB colors to be characterized more accurately than was possible using WCS in Windows 95.</span></span> <span data-ttu-id="ef7cd-124">[BITMAPV5HEADER](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) , die neue Bitmap-Header Struktur, wird in WinGDI. h in der-Version von Windows 98 definiert.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-124">[BITMAPV5HEADER](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) , the new bitmap header structure, is defined in Wingdi.h in the release of Windows 98.</span></span> <span data-ttu-id="ef7cd-125">Zu Entwicklungszwecken ist es auch in der Datei "ICM. h" mit der Referenz dieses Programmierers enthalten.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-125">For development purposes, it is also included in the file Icm.h with this Programmer's Reference.</span></span> <span data-ttu-id="ef7cd-126">Die **BITMAPV5HEADER** -Struktur sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="ef7cd-126">The **BITMAPV5HEADER** structure is as follows:</span></span>


```C++
typedef struct {
    DWORD        bV5Size;
    LONG         bV5Width;
    LONG         bV5Height;
    WORD         bV5Planes;
    WORD         bV5BitCount;
    DWORD        bV5Compression;
    DWORD        bV5SizeImage;
    LONG         bV5XPelsPerMeter;
    LONG         bV5YPelsPerMeter;
    DWORD        bV5ClrUsed;
    DWORD        bV5ClrImportant;
    DWORD        bV5RedMask;
    DWORD        bV5GreenMask;
    DWORD        bV5BlueMask;
    DWORD        bV5AlphaMask;
    DWORD        bV5CSType;
    CIEXYZTRIPLE bV5Endpoints;
    DWORD        bV5GammaRed;
    DWORD        bV5GammaGreen;
    DWORD        bV5GammaBlue;
    DWORD        bV5Intent;         // Rendering intent for bitmap 
    DWORD        bV5ProfileData;    // Offset to profile data 
    DWORD        bV5ProfileSize;    // Size of embedded profile data 
    DWORD        bV5Reserved;       // Should be zero 
} BITMAPV5HEADER, FAR *LPBITMAPV5HEADER, *PBITMAPV5HEADER;
```



<span data-ttu-id="ef7cd-127">Der Member **bV5CSType** kann die Werte profile \_ Embedded oder Profile \_ Linked aufweisen, um anzugeben, ob ein Profil eingebettet oder mit dem DIB verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-127">The member **bV5CSType** can have the values PROFILE\_EMBEDDED or PROFILE\_LINKED to specify whether a profile is embedded or linked with the DIB.</span></span> <span data-ttu-id="ef7cd-128">Der Member **bV5ProfileData** ist der Offset in Bytes vom Anfang der **BITMAPV5HEADER** -Struktur bis zum Anfang der Profildaten.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-128">The member **bV5ProfileData** is the offset in bytes from the beginning of the **BITMAPV5HEADER** structure to the start of the profile data.</span></span> <span data-ttu-id="ef7cd-129">Wenn das Profil eingebettet ist, handelt es sich bei den Profildaten um das tatsächliche Profil, und wenn es verknüpft ist, ist die Profildaten der mit NULL endenden Dateiname des Profils.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-129">If the profile is embedded, profile data is the actual profile, and if it is linked, the profile data is the null-terminated file name of the profile.</span></span> <span data-ttu-id="ef7cd-130">Dies darf keine Unicode-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-130">This cannot be a Unicode string.</span></span> <span data-ttu-id="ef7cd-131">Sie muss ausschließlich aus Zeichen aus dem Windows-Zeichensatz (Codepage 1252) bestehen.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-131">It must be composed exclusively of characters from the Windows character set (code page 1252).</span></span>

<span data-ttu-id="ef7cd-132">Wenn ein DIB in den Arbeitsspeicher geladen wird, sollten die Profildaten (falls vorhanden) der Farbtabelle folgen, und **bV5ProfileData** sollte den Offset der Profildaten vom Anfang der **BITMAPV5HEADER** -Struktur erhalten.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-132">When a DIB is loaded into memory, the profile data (if present) should follow the color table, and **bV5ProfileData** should give the offset of the profile data from the beginning of the **BITMAPV5HEADER** structure.</span></span> <span data-ttu-id="ef7cd-133">Der Wert dieses Members ist nun anders, da die Bitmapbits nicht der Farbtabelle im Arbeitsspeicher folgen.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-133">The value of this member will be different now, as the bitmap bits do not follow the color table in memory.</span></span> <span data-ttu-id="ef7cd-134">Anwendungen sollten den **bV5ProfileData** -Member ändern, nachdem der DIB in den Arbeitsspeicher geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-134">Applications should modify the **bV5ProfileData** member after loading the DIB into memory.</span></span>

<span data-ttu-id="ef7cd-135">Für gepackte Disb sollten die Profildaten den Bitmapbits folgen, die dem Dateiformat ähneln.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-135">For packed DIBs, the profile data should follow the bitmap bits similar to the file format.</span></span> <span data-ttu-id="ef7cd-136">Der **bV5ProfileData** -Member sollte weiterhin den Offset der Profildaten vom Anfang der **BITMAPV5HEADER** -Struktur abgeben.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-136">The **bV5ProfileData** member should still give the offset of the profile data from the beginning of the **BITMAPV5HEADER** structure.</span></span>

<span data-ttu-id="ef7cd-137">Anwendungen sollten nur auf die Profildaten zugreifen, wenn **bV5Size**  ==  **sizeof** ( **BITMAPV5HEADER** ) **ANDbV5CSType** profile \_ Embedded oder Profile \_ verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-137">Applications should access the profile data only when **bV5Size** == **sizeof** ( **BITMAPV5HEADER** ) **ANDbV5CSType** is PROFILE\_EMBEDDED or PROFILE\_LINKED.</span></span>

<span data-ttu-id="ef7cd-138">Wenn ein Profil verknüpft ist, kann der Pfad des Profils ein beliebiger voll qualifizierter Name (einschließlich eines Netzwerk Pfads) sein, der mithilfe der Win32-Funktion " **deatefile** " geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-138">If a profile is linked, the path of the profile can be any fully qualified name (including a network path) that can be opened using the Win32 **CreateFile** function.</span></span>

## <a name="differences-between-v4-and-v5-headers"></a><span data-ttu-id="ef7cd-139">Unterschiede zwischen v4-und V5-Headern</span><span class="sxs-lookup"><span data-stu-id="ef7cd-139">Differences Between V4 and V5 Headers</span></span>

<span data-ttu-id="ef7cd-140">Beim Arbeiten mit der neuen Bitmap-Struktur ist es sinnvoll, Unterschiede in der Einrichtung von **BITMAPV4HEADER** -und **BITMAPV5HEADER** -Strukturen zu erkennen:</span><span class="sxs-lookup"><span data-stu-id="ef7cd-140">In working with the new bitmap structure, it is useful to recognize differences in how **BITMAPV4HEADER** and **BITMAPV5HEADER** structures are set up:</span></span>



| <span data-ttu-id="ef7cd-141">V4-Header</span><span class="sxs-lookup"><span data-stu-id="ef7cd-141">V4 Header</span></span>     | <span data-ttu-id="ef7cd-142">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ef7cd-142">Meaning</span></span>                                                                                                                              |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef7cd-143">**bV4CSType**</span><span class="sxs-lookup"><span data-stu-id="ef7cd-143">**bV4CSType**</span></span> | <span data-ttu-id="ef7cd-144">LCS- \_ kalibrierte \_ RGB.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-144">LCS\_CALIBRATED\_RGB.</span></span> <span data-ttu-id="ef7cd-145">Dieser Wert impliziert, dass Endpunkte und Gammas in den entsprechenden Feldern angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-145">This value implies that end points and gammas are given in the appropriate fields.</span></span> <span data-ttu-id="ef7cd-146">Falsche Werte verursachen Probleme.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-146">Bogus values cause trouble.</span></span> |
| <span data-ttu-id="ef7cd-147">**bV4CSType**</span><span class="sxs-lookup"><span data-stu-id="ef7cd-147">**bV4CSType**</span></span> | <span data-ttu-id="ef7cd-148">LCS \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-148">LCS\_sRGB.</span></span> <span data-ttu-id="ef7cd-149">Dieser Wert impliziert, dass die Bitmap den sRGB-Farbraum aufweist (Gammas und Endpunkte werden ignoriert).</span><span class="sxs-lookup"><span data-stu-id="ef7cd-149">This value implies that the bitmap is in sRGB color space (gammas and endpoints ignored).</span></span>                                 |
| <span data-ttu-id="ef7cd-150">**bV4CSType**</span><span class="sxs-lookup"><span data-stu-id="ef7cd-150">**bV4CSType**</span></span> | <span data-ttu-id="ef7cd-151">LCS \_ Windows- \_ Farbraum \_ .</span><span class="sxs-lookup"><span data-stu-id="ef7cd-151">LCS\_WINDOWS\_COLOR\_SPACE.</span></span> <span data-ttu-id="ef7cd-152">Dieser Wert impliziert, dass die Bitmap in Windows-Standard Farbraum ist.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-152">This value implies that the bitmap is in Windows default color space.</span></span>                                    |



 



| <span data-ttu-id="ef7cd-153">V5-Header</span><span class="sxs-lookup"><span data-stu-id="ef7cd-153">V5 Header</span></span>     | <span data-ttu-id="ef7cd-154">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ef7cd-154">Meaning</span></span>                                                                                                                                                      |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef7cd-155">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="ef7cd-155">**bV5CSType**</span></span> | <span data-ttu-id="ef7cd-156">LCS- \_ kalibrierte \_ RGB.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-156">LCS\_CALIBRATED\_RGB.</span></span> <span data-ttu-id="ef7cd-157">Dieser Wert impliziert, dass Endpunkte und Gammas in den entsprechenden Feldern angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-157">This value implies that end points and gammas are given in the appropriate fields.</span></span> <span data-ttu-id="ef7cd-158">Falsche Werte verursachen Probleme.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-158">Bogus values cause trouble.</span></span>                         |
| <span data-ttu-id="ef7cd-159">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="ef7cd-159">**bV5CSType**</span></span> | <span data-ttu-id="ef7cd-160">LCS \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-160">LCS\_sRGB.</span></span> <span data-ttu-id="ef7cd-161">Dieser Wert impliziert, dass die Bitmap den sRGB-Farbraum aufweist (Gammas und Endpunkte werden ignoriert).</span><span class="sxs-lookup"><span data-stu-id="ef7cd-161">This value implies that the bitmap is in sRGB color space (gammas and endpoints ignored).</span></span>                                                         |
| <span data-ttu-id="ef7cd-162">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="ef7cd-162">**bV5CSType**</span></span> | <span data-ttu-id="ef7cd-163">Profil \_ eingebettet.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-163">PROFILE\_EMBEDDED.</span></span> <span data-ttu-id="ef7cd-164">Dieser Wert impliziert, dass **bV5ProfileData** auf einen Arbeitsspeicher Puffer verweist, der das zu verwendende Profil enthält (Gammas und Endpunkte werden ignoriert).</span><span class="sxs-lookup"><span data-stu-id="ef7cd-164">This value implies that **bV5ProfileData** points to a memory buffer that contains the profile to use (gammas and endpoints are ignored).</span></span> |
| <span data-ttu-id="ef7cd-165">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="ef7cd-165">**bV5CSType**</span></span> | <span data-ttu-id="ef7cd-166">Profil \_ verknüpft.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-166">PROFILE\_LINKED.</span></span> <span data-ttu-id="ef7cd-167">Dieser Wert impliziert, dass **bV5ProfileData** auf den Dateinamen des zu verwendenden Profils zeigt (Gammas und Endpunkte werden ignoriert).</span><span class="sxs-lookup"><span data-stu-id="ef7cd-167">This value implies that **bV5ProfileData** points to the file name of the profile to use (gammas and endpoints are ignored).</span></span>                |
| <span data-ttu-id="ef7cd-168">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="ef7cd-168">**bV5CSType**</span></span> | <span data-ttu-id="ef7cd-169">LCS \_ Windows- \_ Farbraum \_ .</span><span class="sxs-lookup"><span data-stu-id="ef7cd-169">LCS\_WINDOWS\_COLOR\_SPACE.</span></span> <span data-ttu-id="ef7cd-170">Dieser Wert impliziert, dass die Bitmap in Windows-Standard Farbraum ist.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-170">This value implies that the bitmap is in Windows default color space.</span></span>                                                            |



 

<span data-ttu-id="ef7cd-171">Um ältere Bitmaps in und aus der neuen **BITMAPV5HEADER** -Struktur zu konvertieren, ist eine Befehlszeilen-Konvertierungsprogramm Datei mit dem Namen Bitmap.exe in der WCS 1,0-Programmier Referenz enthalten.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-171">In order to convert older bitmaps to and from the new **BITMAPV5HEADER** structure, a command-line conversion utility file named Bitmap.exe is included in the WCS 1.0 Programmer's Reference.</span></span>

## <a name="bitmapexe-a-command-line-utility-for-converting-bitmap-headers"></a><span data-ttu-id="ef7cd-172">BitMap.exe: ein Command-Line Hilfsprogramm zum Umrechnen von bitmapheadern.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-172">BitMap.exe: a Command-Line Utility for Converting Bitmap Headers</span></span>

<span data-ttu-id="ef7cd-173">Bitmap.exe ist ein Befehlszeilenprogramm, das sich im \\ Ordner "bin" unter dem von Ihnen angegebenen Installationsordner befindet.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-173">Bitmap.exe is a command-line utility located in the \\Bin folder under the installation folder that you specified.</span></span> <span data-ttu-id="ef7cd-174">Er ändert die Header von Windows-Bitmaps, sodass Sie vorhandene Bitmaps aus **BITMAPINFOHEADER** -und **BITMAPV4HEADER** -Header Strukturen in die neuere **BITMAPV5HEADER** -Struktur und wieder zurück konvertieren können.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-174">It modifies the headers of Windows bitmaps, allowing you to convert existing bitmaps from **BITMAPINFOHEADER** and **BITMAPV4HEADER** header structures to the newer **BITMAPV5HEADER** structure and back again.</span></span> <span data-ttu-id="ef7cd-175">Die Befehlszeilen Syntax lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ef7cd-175">The command-line syntax is as follows:</span></span>


```C++
BITMAP [/d] [/1|4|5] [/s] [/f] 
filename
```



<span data-ttu-id="ef7cd-176">Die Befehls Zeilenschalter haben folgende Auswirkungen:</span><span class="sxs-lookup"><span data-stu-id="ef7cd-176">The command-line switches have the following effects.</span></span>



| <span data-ttu-id="ef7cd-177">Schalter</span><span class="sxs-lookup"><span data-stu-id="ef7cd-177">Switch</span></span> | <span data-ttu-id="ef7cd-178">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ef7cd-178">Meaning</span></span>                                                                  |
|--------|--------------------------------------------------------------------------|
| <span data-ttu-id="ef7cd-179">/d</span><span class="sxs-lookup"><span data-stu-id="ef7cd-179">/d</span></span>     | <span data-ttu-id="ef7cd-180">Standardwerte werden automatisch in den konvertierten Headern eingegeben.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-180">Default values are automatically entered in the converted headers.</span></span>       |
| <span data-ttu-id="ef7cd-181">/1</span><span class="sxs-lookup"><span data-stu-id="ef7cd-181">/1</span></span>     | <span data-ttu-id="ef7cd-182">Die angegebenen Bitmaps werden in **BITMAPINFOHEADER** konvertiert.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-182">Convert the specified bitmaps to **BITMAPINFOHEADER**</span></span>                    |
| <span data-ttu-id="ef7cd-183">/4</span><span class="sxs-lookup"><span data-stu-id="ef7cd-183">/4</span></span>     | <span data-ttu-id="ef7cd-184">Die angegebenen Bitmaps werden in **BITMAPV4HEADER** konvertiert.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-184">Convert the specified bitmaps to **BITMAPV4HEADER**</span></span>                      |
| <span data-ttu-id="ef7cd-185">/5</span><span class="sxs-lookup"><span data-stu-id="ef7cd-185">/5</span></span>     | <span data-ttu-id="ef7cd-186">Die angegebenen Bitmaps werden in **BITMAPV5HEADER** konvertiert.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-186">Convert the specified bitmaps to **BITMAPV5HEADER**</span></span>                      |
| <span data-ttu-id="ef7cd-187">/f</span><span class="sxs-lookup"><span data-stu-id="ef7cd-187">/f</span></span>     | <span data-ttu-id="ef7cd-188">Erzwingt die Konvertierung, auch wenn die Bitmap bereits über den rechten Header verfügt.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-188">Forces conversion, even if the bitmap already has the right header</span></span>       |
| <span data-ttu-id="ef7cd-189">/s</span><span class="sxs-lookup"><span data-stu-id="ef7cd-189">/s</span></span>     | <span data-ttu-id="ef7cd-190">Konvertiert Bitmaps im angegebenen Ordner und in allen Unterverzeichnissen darunter.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-190">Converts bitmaps in the specified folder and all subdirectories under it</span></span> |



 

 

 