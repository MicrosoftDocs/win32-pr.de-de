---
description: Video fourccs
ms.assetid: bea4835d-fd7f-4ac3-8466-7f4e0d799a12
title: Video fourccs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b804962308d0ecc5bf32fcddf5176905d0e17fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344849"
---
# <a name="video-fourccs"></a><span data-ttu-id="7216f-103">Video fourccs</span><span class="sxs-lookup"><span data-stu-id="7216f-103">Video FOURCCs</span></span>

<span data-ttu-id="7216f-104">Vielen Videoformaten werden FOURCC-Codes zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="7216f-104">Many video formats have FOURCC codes assigned to them.</span></span> <span data-ttu-id="7216f-105">Bei einem FourCC-Code handelt es sich um eine 32-Bit-Ganzzahl ohne Vorzeichen, die durch Verkettung von vier ASCII-Zeichen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7216f-105">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span> <span data-ttu-id="7216f-106">Der FourCC-Code für im YUY2 Video lautet beispielsweise "im YUY2".</span><span class="sxs-lookup"><span data-stu-id="7216f-106">For example, the FOURCC code for YUY2 video is 'YUY2'.</span></span>

<span data-ttu-id="7216f-107">Zum Deklarieren von FourCC-Werten im Quellcode sind verschiedene C/C++-Makros definiert.</span><span class="sxs-lookup"><span data-stu-id="7216f-107">Various C/C++ macros are defined for declaring FOURCC values in source code.</span></span> <span data-ttu-id="7216f-108">Das **makefourcc** -Makro ist in "MMSYSTEM. h" definiert, und das " **FCC** "-Makro wird in "aviriff. h" und verschiedenen anderen Header Dateien definiert.</span><span class="sxs-lookup"><span data-stu-id="7216f-108">The **MAKEFOURCC** macro is defined in Mmsystem.h, and the **FCC** macro is defined in Aviriff.h and various other header files.</span></span> <span data-ttu-id="7216f-109">Sie können einen FourCC-Code auch direkt als Zeichenfolgenliterale deklarieren, indem Sie einfach die Reihenfolge der Zeichen umkehren.</span><span class="sxs-lookup"><span data-stu-id="7216f-109">You can also declare a FOURCC code directly as a string literal simply by reversing the order of the characters.</span></span> <span data-ttu-id="7216f-110">Daher sind die folgenden Anweisungen äquivalent:</span><span class="sxs-lookup"><span data-stu-id="7216f-110">Thus, the following statements are equivalent:</span></span>

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```

<span data-ttu-id="7216f-111">(Im letzten Beispiel ist das Umkehren der Byte Reihenfolge erforderlich, da Windows eine Little-Endian-Architektur verwendet.</span><span class="sxs-lookup"><span data-stu-id="7216f-111">(In the last example, reversing the byte order is necessary because Windows uses a little-endian architecture.</span></span> <span data-ttu-id="7216f-112">' Y ' = 0x59, ' U ' = 0x55 und ' 2 ' = 0x32, also ' 2yuy ' ist 0x32595559.)</span><span class="sxs-lookup"><span data-stu-id="7216f-112">'Y' = 0x59, 'U' = 0x55, and '2' = 0x32, so '2YUY' is 0x32595559.)</span></span>

<span data-ttu-id="7216f-113">Einige der [DirectX Video Acceleration 2,0](directx-video-acceleration-2-0.md) -APIs verwenden einen **D3DFORMAT** -Wert, um ein Video Format zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7216f-113">Some of the [DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md) APIs use a **D3DFORMAT** value to describe a video format.</span></span> <span data-ttu-id="7216f-114">Ein FourCC-Code kann auch in diesem Kontext verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="7216f-114">A FOURCC code can be used in this context as well:</span></span>

``` syntax
D3DFORMAT fmt = (D3DFORMAT)MAKEFOURCC('Y','U','Y','2');
D3DFORMAT fmt = (D3DFORMAT)FCC('YUY2');
D3DFORMAT fmt = D3DFORMAT('2YUY'); // Coerce to D3DFORMAT type.
```

### <a name="fourcc-constants"></a><span data-ttu-id="7216f-115">FourCC-Konstanten</span><span class="sxs-lookup"><span data-stu-id="7216f-115">FOURCC Constants</span></span>

<span data-ttu-id="7216f-116">In der folgenden Tabelle sind einige gängige FOURCC-Codes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="7216f-116">The following table lists some common FOURCC codes.</span></span>



| <span data-ttu-id="7216f-117">FourCC-Wert</span><span class="sxs-lookup"><span data-stu-id="7216f-117">FOURCC value</span></span> | <span data-ttu-id="7216f-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7216f-118">Description</span></span>                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7216f-119">H264</span><span class="sxs-lookup"><span data-stu-id="7216f-119">'H264'</span></span>       | <span data-ttu-id="7216f-120">H. 264-Video.</span><span class="sxs-lookup"><span data-stu-id="7216f-120">H.264 video.</span></span>                                                                                                          |
| <span data-ttu-id="7216f-121">'I420'</span><span class="sxs-lookup"><span data-stu-id="7216f-121">'I420'</span></span>       | <span data-ttu-id="7216f-122">YUV-Video, das im planare 4:2:0-Format gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="7216f-122">YUV video stored in planar 4:2:0 format.</span></span>                                                                              |
| <span data-ttu-id="7216f-123">"IYUV"</span><span class="sxs-lookup"><span data-stu-id="7216f-123">'IYUV'</span></span>       | <span data-ttu-id="7216f-124">YUV-Video, das im planare 4:2:0-Format gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="7216f-124">YUV video stored in planar 4:2:0 format.</span></span>                                                                              |
| <span data-ttu-id="7216f-125">X 4s2 '</span><span class="sxs-lookup"><span data-stu-id="7216f-125">'M4S2'</span></span>       | <span data-ttu-id="7216f-126">MPEG-4 Part 2-Video.</span><span class="sxs-lookup"><span data-stu-id="7216f-126">MPEG-4 part 2 video.</span></span>                                                                                                  |
| <span data-ttu-id="7216f-127">MP4 Bitrate</span><span class="sxs-lookup"><span data-stu-id="7216f-127">'MP4S'</span></span>       | <span data-ttu-id="7216f-128">Microsoft MPEG 4 Codec Version 3.</span><span class="sxs-lookup"><span data-stu-id="7216f-128">Microsoft MPEG 4 codec version 3.</span></span> <span data-ttu-id="7216f-129">Dieser Codec wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7216f-129">This codec is no longer supported.</span></span>                                                  |
| <span data-ttu-id="7216f-130">MP4V</span><span class="sxs-lookup"><span data-stu-id="7216f-130">'MP4V'</span></span>       | <span data-ttu-id="7216f-131">MPEG-4 Part 2-Video.</span><span class="sxs-lookup"><span data-stu-id="7216f-131">MPEG-4 part 2 video.</span></span>                                                                                                  |
| <span data-ttu-id="7216f-132">'MPG1'</span><span class="sxs-lookup"><span data-stu-id="7216f-132">'MPG1'</span></span>       | <span data-ttu-id="7216f-133">MPEG-1-Video.</span><span class="sxs-lookup"><span data-stu-id="7216f-133">MPEG-1 video.</span></span>                                                                                                         |
| <span data-ttu-id="7216f-134">'MSS1'</span><span class="sxs-lookup"><span data-stu-id="7216f-134">'MSS1'</span></span>       | <span data-ttu-id="7216f-135">Inhalt, der mit dem Windows Media Video 7-Bildschirm Codec codiert ist.</span><span class="sxs-lookup"><span data-stu-id="7216f-135">Content encoded with the Windows Media Video 7 screen codec.</span></span>                                                          |
| <span data-ttu-id="7216f-136">'MSS2'</span><span class="sxs-lookup"><span data-stu-id="7216f-136">'MSS2'</span></span>       | <span data-ttu-id="7216f-137">Inhalt, der mit dem Windows Media Video 9-Bildschirm Codec codiert ist.</span><span class="sxs-lookup"><span data-stu-id="7216f-137">Content encoded with the Windows Media Video 9 screen codec.</span></span>                                                          |
| <span data-ttu-id="7216f-138">UYVY</span><span class="sxs-lookup"><span data-stu-id="7216f-138">'UYVY'</span></span>       | <span data-ttu-id="7216f-139">YUV-Video im gepackten 4:2:2-Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7216f-139">YUV video stored in packed 4:2:2 format.</span></span> <span data-ttu-id="7216f-140">Vergleichbar mit im YUY2, aber mit einer unterschiedlichen Datenreihen Folge.</span><span class="sxs-lookup"><span data-stu-id="7216f-140">Similar to YUY2 but with different ordering of data.</span></span>                         |
| <span data-ttu-id="7216f-141">'WMV1'</span><span class="sxs-lookup"><span data-stu-id="7216f-141">'WMV1'</span></span>       | <span data-ttu-id="7216f-142">Mit dem Windows Media Video 7-Codec codierter Inhalt.</span><span class="sxs-lookup"><span data-stu-id="7216f-142">Content encoded with the Windows Media Video 7 codec.</span></span>                                                                 |
| <span data-ttu-id="7216f-143">'WMV2'</span><span class="sxs-lookup"><span data-stu-id="7216f-143">'WMV2'</span></span>       | <span data-ttu-id="7216f-144">Mit dem Windows Media Video 8-Codec codierter Inhalt.</span><span class="sxs-lookup"><span data-stu-id="7216f-144">Content encoded with the Windows Media Video 8 codec.</span></span>                                                                 |
| <span data-ttu-id="7216f-145">'WMV3'</span><span class="sxs-lookup"><span data-stu-id="7216f-145">'WMV3'</span></span>       | <span data-ttu-id="7216f-146">Mit dem Windows Media Video 9-Codec codierter Inhalt.</span><span class="sxs-lookup"><span data-stu-id="7216f-146">Content encoded with the Windows Media Video 9 codec.</span></span>                                                                 |
| <span data-ttu-id="7216f-147">"Wmva"</span><span class="sxs-lookup"><span data-stu-id="7216f-147">'WMVA'</span></span>       | <span data-ttu-id="7216f-148">Inhalt, der mit der älteren, veralteten Version von Windows Media Video 9 Advanced Profile Codec codiert ist.</span><span class="sxs-lookup"><span data-stu-id="7216f-148">Content encoded with the older, obsolete version of the Windows Media Video 9 Advanced Profile codec.</span></span>                 |
| <span data-ttu-id="7216f-149">"Wmvp"</span><span class="sxs-lookup"><span data-stu-id="7216f-149">'WMVP'</span></span>       | <span data-ttu-id="7216f-150">Inhalt, der mit Windows Media Video dem 9,1-Bildcodec codiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7216f-150">Content encoded with the Windows Media Video 9.1 Image codec.</span></span>                                                         |
| <span data-ttu-id="7216f-151">'WVC1'</span><span class="sxs-lookup"><span data-stu-id="7216f-151">'WVC1'</span></span>       | <span data-ttu-id="7216f-152">SMPTE 421m ("VC-1").</span><span class="sxs-lookup"><span data-stu-id="7216f-152">SMPTE 421M ("VC-1").</span></span> <span data-ttu-id="7216f-153">Inhalt, der mit Windows Media Video 9 Advanced Profile codiert ist.</span><span class="sxs-lookup"><span data-stu-id="7216f-153">Content encoded with Windows Media Video 9 Advanced Profile.</span></span>                                     |
| <span data-ttu-id="7216f-154">'WVP2'</span><span class="sxs-lookup"><span data-stu-id="7216f-154">'WVP2'</span></span>       | <span data-ttu-id="7216f-155">Inhalt, der mit dem Windows Media Video 9,1 Image V2-Codec codiert ist.</span><span class="sxs-lookup"><span data-stu-id="7216f-155">Content encoded with the Windows Media Video 9.1 Image v2 codec.</span></span>                                                      |
| <span data-ttu-id="7216f-156">Im YUY2</span><span class="sxs-lookup"><span data-stu-id="7216f-156">'YUY2'</span></span>       | <span data-ttu-id="7216f-157">YUV-Video im gepackten 4:2:2-Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7216f-157">YUV video stored in packed 4:2:2 format.</span></span>                                                                              |
| <span data-ttu-id="7216f-158">'YV12'</span><span class="sxs-lookup"><span data-stu-id="7216f-158">'YV12'</span></span>       | <span data-ttu-id="7216f-159">YUV-Video, das im planare 4:2:0-oder 4:1:1-Format gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="7216f-159">YUV video stored in planar 4:2:0 or 4:1:1 format.</span></span> <span data-ttu-id="7216f-160">Identisch mit I420/IYUV, mit dem Unterschied, dass die Ebenen you und V gewechselt werden.</span><span class="sxs-lookup"><span data-stu-id="7216f-160">Identical to I420/IYUV except that the U and V planes are switched.</span></span> |
| <span data-ttu-id="7216f-161">YVU9</span><span class="sxs-lookup"><span data-stu-id="7216f-161">'YVU9'</span></span>       | <span data-ttu-id="7216f-162">YUV-Video, das im planare 16:1:1-Format gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="7216f-162">YUV video stored in planar 16:1:1 format.</span></span>                                                                             |
| <span data-ttu-id="7216f-163">Im yvyu</span><span class="sxs-lookup"><span data-stu-id="7216f-163">'YVYU'</span></span>       | <span data-ttu-id="7216f-164">YUV-Video im gepackten 4:2:2-Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7216f-164">YUV video stored in packed 4:2:2 format.</span></span> <span data-ttu-id="7216f-165">Vergleichbar mit im YUY2, aber mit einer unterschiedlichen Datenreihen Folge.</span><span class="sxs-lookup"><span data-stu-id="7216f-165">Similar to YUY2 but with different ordering of data.</span></span>                         |



 

## <a name="related-topics"></a><span data-ttu-id="7216f-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7216f-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7216f-167">Video Medientypen</span><span class="sxs-lookup"><span data-stu-id="7216f-167">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="7216f-168">Video Untertyp-GUIDs</span><span class="sxs-lookup"><span data-stu-id="7216f-168">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> </dl>

 

 



