---
description: FourCC-Codes
ms.assetid: 7627b580-4119-48e2-88b7-51b714b5d5b2
title: FourCC-Codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb789bc16a1643ee737c1c1a63bdbc5704567931
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123566"
---
# <a name="fourcc-codes"></a><span data-ttu-id="b0d6a-103">FourCC-Codes</span><span class="sxs-lookup"><span data-stu-id="b0d6a-103">FOURCC Codes</span></span>

<span data-ttu-id="b0d6a-104">Vielen digitalen Medienformaten werden FOURCC-Codes zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-104">Many digital media formats have FOURCC codes assigned to them.</span></span> <span data-ttu-id="b0d6a-105">Bei einem FourCC-Code handelt es sich um eine 32-Bit-Ganzzahl ohne Vorzeichen, die durch Verkettung von vier ASCII-Zeichen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-105">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span> <span data-ttu-id="b0d6a-106">Der FourCC-Code für im YUY2 Video lautet beispielsweise "im YUY2".</span><span class="sxs-lookup"><span data-stu-id="b0d6a-106">For example, the FOURCC code for YUY2 video is 'YUY2'.</span></span> <span data-ttu-id="b0d6a-107">Für komprimierte Videoformate und nicht-RGB-Videoformate (z. b. YUV) sollte der **bicompression** -Member der [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur auf den FourCC-Code festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-107">For compressed video formats and non-RGB video formats (such as YUV), the **biCompression** member of the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure should be set to the FOURCC code.</span></span>

<span data-ttu-id="b0d6a-108">Es gibt verschiedene C/C++-Makros, die das Deklarieren von FourCC-Werten im Quellcode vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-108">There are various C/C++ macros that make it easier to declare FOURCC values in source code.</span></span> <span data-ttu-id="b0d6a-109">Beispielsweise wird das **makefourcc** -Makro in MMSYSTEM. h deklariert, und das **FCC** -Makro wird in aviriff. h deklariert.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-109">For example, the **MAKEFOURCC** macro is declared in Mmsystem.h, and the **FCC** macro is declared in Aviriff.h.</span></span> <span data-ttu-id="b0d6a-110">Verwenden Sie diese wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b0d6a-110">Use them as follows:</span></span>


```C++
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```



<span data-ttu-id="b0d6a-111">Sie können einen FourCC-Code auch direkt als Zeichenfolgenliterale deklarieren, indem Sie einfach die Reihenfolge der Zeichen umkehren.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-111">You can also declare a FOURCC code directly as a string literal simply by reversing the order of the characters.</span></span> <span data-ttu-id="b0d6a-112">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="b0d6a-112">For example:</span></span>


```C++
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```



<span data-ttu-id="b0d6a-113">Das Umkehren der Reihenfolge ist erforderlich, da das Microsoft Windows-Betriebssystem eine Little-Endian-Architektur verwendet.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-113">Reversing the order is necessary because the Microsoft Windows operating system uses a little-endian architecture.</span></span> <span data-ttu-id="b0d6a-114">' Y ' = 0x59, ' U ' = 0x55 und ' 2 ' = 0x32, daher ist ' 2yuy ' 0x32595559.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-114">'Y' = 0x59, 'U' = 0x55, and '2' = 0x32, so '2YUY' is 0x32595559.</span></span>

### <a name="converting-fourcc-codes-to-subtype-guids"></a><span data-ttu-id="b0d6a-115">Umstellen von FOURCC-Codes in Untertyp-GUIDs</span><span class="sxs-lookup"><span data-stu-id="b0d6a-115">Converting FOURCC Codes to Subtype GUIDs</span></span>

<span data-ttu-id="b0d6a-116">Ein Bereich von 2 \* 32 GUIDs ist für die Darstellung von fourccs reserviert.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-116">A range of 2\*32 GUIDs is reserved for representing FOURCCs.</span></span> <span data-ttu-id="b0d6a-117">Diese GUIDs sind in der Form, `XXXXXXXX-0000-0010-8000-00AA00389B71` in der `XXXXXXXX` der FourCC-Code ist.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-117">These GUIDs are all of the form `XXXXXXXX-0000-0010-8000-00AA00389B71` where `XXXXXXXX` is the FOURCC code.</span></span> <span data-ttu-id="b0d6a-118">Daher ist die Untertyp-GUID für im YUY2 `32595559-0000-0010-8000-00AA00389B71` .</span><span class="sxs-lookup"><span data-stu-id="b0d6a-118">Thus, the subtype GUID for YUY2 is `32595559-0000-0010-8000-00AA00389B71`.</span></span>

<span data-ttu-id="b0d6a-119">Viele dieser GUIDs sind bereits in der Header Datei "UUIDs. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-119">Many of these GUIDs are defined already in the header file Uuids.h.</span></span> <span data-ttu-id="b0d6a-120">Beispielsweise ist der im YUY2-Untertyp als mediasubtype \_ im YUY2 definiert.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-120">For example, the YUY2 subtype is defined as MEDIASUBTYPE\_YUY2.</span></span> <span data-ttu-id="b0d6a-121">Die DirectShow-Basisklassen Bibliothek bietet auch eine Hilfsklasse, " [**fourccmap**](fourccmap.md)", die zum Konvertieren von FOURCC-Codes in GUID-Werte verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-121">The DirectShow base class library also provides a helper class, [**FOURCCMap**](fourccmap.md), which can be used to convert FOURCC codes into GUID values.</span></span> <span data-ttu-id="b0d6a-122">Der **fourccmap** -Konstruktor nimmt einen FourCC-Code als Eingabeparameter an.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-122">The **FOURCCMap** constructor takes a FOURCC code as an input parameter.</span></span> <span data-ttu-id="b0d6a-123">Anschließend können Sie das **fourccmap** -Objekt in die entsprechende GUID umwandeln:</span><span class="sxs-lookup"><span data-stu-id="b0d6a-123">You can then cast the **FOURCCMap** object to the corresponding GUID:</span></span>


```C++
FOURCCMap fccMap(FCC('YUY2'));
GUID g1 = (GUID)fccMap;

// Equivalent:
GUID g2 = (GUID)FOURCCMap(FCC('YUY2'));
```



## <a name="related-topics"></a><span data-ttu-id="b0d6a-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b0d6a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0d6a-125">**Audiountertypen**</span><span class="sxs-lookup"><span data-stu-id="b0d6a-125">**Audio Subtypes**</span></span>](audio-subtypes.md)
</dt> <dt>

[<span data-ttu-id="b0d6a-126">Video Untertypen</span><span class="sxs-lookup"><span data-stu-id="b0d6a-126">Video Subtypes</span></span>](video-subtypes.md)
</dt> <dt>

[<span data-ttu-id="b0d6a-127">Arbeiten mit Codecs</span><span class="sxs-lookup"><span data-stu-id="b0d6a-127">Working with Codecs</span></span>](working-with-codecs.md)
</dt> </dl>

 

 



