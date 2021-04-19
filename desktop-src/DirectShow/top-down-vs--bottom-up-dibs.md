---
description: Top-Down im Vergleich zu
ms.assetid: c292f145-f385-4f18-8f98-e414d86860e2
title: Top-Down im Vergleich zu Bottom-Up Disb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e719bea5923aeccc4a0a92b5f73a253e13d2e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373093"
---
# <a name="top-down-vs-bottom-up-dibs"></a><span data-ttu-id="84dc4-103">Top-Down im Vergleich zu Bottom-Up Disb</span><span class="sxs-lookup"><span data-stu-id="84dc4-103">Top-Down vs. Bottom-Up DIBs</span></span>

<span data-ttu-id="84dc4-104">Wenn Sie mit der Grafik Programmierung noch nicht vertraut sind, können Sie davon ausgehen, dass eine Bitmap im Arbeitsspeicher angeordnet wäre, sodass die obere Zeile des Bilds am Anfang des Puffers, gefolgt von der nächsten Zeile usw. angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="84dc4-104">If you are new to graphics programming, you might expect that a bitmap would be arranged in memory so that the top row of the image appeared at the start of the buffer, followed by the next row, and so forth.</span></span> <span data-ttu-id="84dc4-105">Dies ist jedoch nicht unbedingt der Fall.</span><span class="sxs-lookup"><span data-stu-id="84dc4-105">However, this is not necessarily the case.</span></span> <span data-ttu-id="84dc4-106">In Windows können geräteunabhängige Bitmaps (Disb) in zwei verschiedenen Ausrichtungen, von unten nach oben und von oben nach unten, in den Arbeitsspeicher eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="84dc4-106">In Windows, device-independent bitmaps (DIBs) can be placed in memory in two different orientations, bottom-up and top-down.</span></span>

<span data-ttu-id="84dc4-107">In einem Bottom-up-DIB beginnt der Bild Puffer mit der untersten Zeile der Pixel, gefolgt von der nächsten Zeile nach oben usw.</span><span class="sxs-lookup"><span data-stu-id="84dc4-107">In a bottom-up DIB, the image buffer starts with the bottom row of pixels, followed by the next row up, and so forth.</span></span> <span data-ttu-id="84dc4-108">Die oberste Zeile des Bilds ist die letzte Zeile im Puffer.</span><span class="sxs-lookup"><span data-stu-id="84dc4-108">The top row of the image is the last row in the buffer.</span></span> <span data-ttu-id="84dc4-109">Daher ist das erste Byte im Speicher das untere linke Pixel des Bilds.</span><span class="sxs-lookup"><span data-stu-id="84dc4-109">Therefore, the first byte in memory is the bottom-left pixel of the image.</span></span> <span data-ttu-id="84dc4-110">In GDI sind alle Disb im unteren Bereich.</span><span class="sxs-lookup"><span data-stu-id="84dc4-110">In GDI, all DIBs are bottom-up.</span></span> <span data-ttu-id="84dc4-111">Das folgende Diagramm zeigt das physische Layout eines Bottom-up-DIB.</span><span class="sxs-lookup"><span data-stu-id="84dc4-111">The following diagram shows the physical layout of a bottom-up DIB.</span></span>

![Unterer DIB](images/pixel-layout-bottomup.png)

<span data-ttu-id="84dc4-113">In einem DIB von oben nach unten wird die Reihenfolge der Zeilen umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="84dc4-113">In a top-down DIB, the order of the rows is reversed.</span></span> <span data-ttu-id="84dc4-114">Die oberste Zeile des Bilds ist die erste Zeile im Arbeitsspeicher, gefolgt von der nächsten Zeile nach unten.</span><span class="sxs-lookup"><span data-stu-id="84dc4-114">The top row of the image is the first row in memory, followed by the next row down.</span></span> <span data-ttu-id="84dc4-115">Die untere Zeile des Bilds ist die letzte Zeile im Puffer.</span><span class="sxs-lookup"><span data-stu-id="84dc4-115">The bottom row of the image is the last row in the buffer.</span></span> <span data-ttu-id="84dc4-116">Bei einem Top-Down-DIB ist das erste Byte im Speicher das linke obere Pixel des Bilds.</span><span class="sxs-lookup"><span data-stu-id="84dc4-116">With a top-down DIB, the first byte in memory is the top-left pixel of the image.</span></span> <span data-ttu-id="84dc4-117">DirectDraw verwendet Top-Down-Disb.</span><span class="sxs-lookup"><span data-stu-id="84dc4-117">DirectDraw uses top-down DIBs.</span></span> <span data-ttu-id="84dc4-118">Das folgende Diagramm zeigt das physische Layout eines Top-Down-DIB:</span><span class="sxs-lookup"><span data-stu-id="84dc4-118">The following diagram shows the physical layout of a top-down DIB:</span></span>

![DIB von oben nach unten](images/pixel-layout-topdown.png)

<span data-ttu-id="84dc4-120">Bei RGB-Distributionen wird die Bild Ausrichtung durch den **biheight** -Member der [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="84dc4-120">For RGB DIBs, the image orientation is indicated by the **biHeight** member of the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span> <span data-ttu-id="84dc4-121">Wenn **biheight** positiv ist, wird das Bild von unten nach oben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84dc4-121">If **biHeight** is positive, the image is bottom-up.</span></span> <span data-ttu-id="84dc4-122">Wenn **biheight** negativ ist, wird das Bild von oben nach unten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84dc4-122">If **biHeight** is negative, the image is top-down.</span></span>

<span data-ttu-id="84dc4-123">Disb in YUV-Formaten sind immer von oben nach unten, und das Vorzeichen des Elements **biheight** wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="84dc4-123">DIBs in YUV formats are always top-down, and the sign of the **biHeight** member is ignored.</span></span> <span data-ttu-id="84dc4-124">Decoders sollten YUV-Formaten mit positiver **biheight** anbieten, Sie sollten jedoch auch YUV-Formate mit negativer **biheight** akzeptieren und das Vorzeichen ignorieren.</span><span class="sxs-lookup"><span data-stu-id="84dc4-124">Decoders should offer YUV formats with positive **biHeight**, but they should also accept YUV formats with negative **biHeight** and ignore the sign.</span></span>

<span data-ttu-id="84dc4-125">Außerdem sollte jeder DIB-Typ, der ein **FourCC** im **bicompression** -Member verwendet, seine **biheight** als positive Zahl ausdrücken, unabhängig davon, was seine Ausrichtung ist, da der **FourCC** selbst ein Komprimierungs Schema identifiziert, dessen Bild Ausrichtung von einem beliebigen kompatiblen Filter verstanden werden sollte.</span><span class="sxs-lookup"><span data-stu-id="84dc4-125">Also, any DIB type that uses a **FOURCC** in the **biCompression** member, should express its **biHeight** as a positive number no matter what its orientation is, since the **FOURCC** itself identifies a compression scheme whose image orientation should be understood by any compatible filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84dc4-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="84dc4-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84dc4-127">Arbeiten mit Video Frames</span><span class="sxs-lookup"><span data-stu-id="84dc4-127">Working with Video Frames</span></span>](working-with-video-frames.md)
</dt> </dl>

 

 



