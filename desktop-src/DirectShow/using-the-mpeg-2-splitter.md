---
description: Verwenden des MPEG-2-Splitters
ms.assetid: a08e079c-41be-475a-9e88-ee46d17fe938
title: Verwenden des MPEG-2-Splitters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60505ef242c2ed9c1eab3031a005a2582b99608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358573"
---
# <a name="using-the-mpeg-2-splitter"></a><span data-ttu-id="f36f0-103">Verwenden des MPEG-2-Splitters</span><span class="sxs-lookup"><span data-stu-id="f36f0-103">Using the MPEG-2 Splitter</span></span>

> [!Note]  
> <span data-ttu-id="f36f0-104">Ab Microsoft® Windows® XP ist der MPEG-2-Splitter Filter veraltet.</span><span class="sxs-lookup"><span data-stu-id="f36f0-104">Starting in Microsoft® Windows® XP, the MPEG-2 Splitter filter is deprecated.</span></span> <span data-ttu-id="f36f0-105">Verwenden Sie stattdessen den [MPEG-2-Demultiplexer](mpeg-2-demultiplexer.md) .</span><span class="sxs-lookup"><span data-stu-id="f36f0-105">Use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) instead.</span></span>

 

<span data-ttu-id="f36f0-106">Der MPEG-2-Splitter Filter unterstützt die Wiedergabe von MPEG-2-Programmstreams im Pull-Modus, die mindestens einen der folgenden Streamtypen enthalten.</span><span class="sxs-lookup"><span data-stu-id="f36f0-106">The MPEG-2 Splitter filter supports pull-mode playback of MPEG-2 program streams that contain at least one of the following stream types.</span></span>

-   <span data-ttu-id="f36f0-107">MPEG-2-Video</span><span class="sxs-lookup"><span data-stu-id="f36f0-107">MPEG-2 video</span></span>
-   <span data-ttu-id="f36f0-108">MPEG-2-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="f36f0-108">MPEG-2 audio</span></span>
-   <span data-ttu-id="f36f0-109">Dolby AC-3-Audiocodierung, wie für DVD-Video definiert</span><span class="sxs-lookup"><span data-stu-id="f36f0-109">Dolby AC-3 audio encoded as defined for DVD-Video</span></span>
-   <span data-ttu-id="f36f0-110">LPCM (Linear Pulse Code moduliert) audiocodiert, wie für DVD-Video definiert</span><span class="sxs-lookup"><span data-stu-id="f36f0-110">LPCM (Linear Pulse Code Modulated) audio encoded as defined for DVD-Video</span></span>

<span data-ttu-id="f36f0-111">Eine Liste der Medientypen, die der MPEG-2-Splitter unterstützt, finden Sie unter [MPEG-2 Splitter Medien Types](mpeg-2-splitter-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="f36f0-111">For a list of media types that the MPEG-2 Splitter supports, see [MPEG-2 Splitter Media Types](mpeg-2-splitter-media-types.md).</span></span>

<span data-ttu-id="f36f0-112">Der MPEG-2-Splitter analysiert keine Transportdaten Ströme.</span><span class="sxs-lookup"><span data-stu-id="f36f0-112">The MPEG-2 Splitter does not parse transport streams.</span></span> <span data-ttu-id="f36f0-113">Verwenden Sie den MPEG-2 Demultiplexer-Filter für Transport Datenströme (nur Pushmodus).</span><span class="sxs-lookup"><span data-stu-id="f36f0-113">Use the MPEG-2 Demultiplexer filter for transport streams (push mode only).</span></span>

<span data-ttu-id="f36f0-114">**Zeitstempel**</span><span class="sxs-lookup"><span data-stu-id="f36f0-114">**Time Stamps**</span></span>

<span data-ttu-id="f36f0-115">Bei der Wiedergabe von MPEG-2-Programmstreams behandelt der MPEG-2-Splitter Filter den ersten systemtaktsverweis, der als Zeit Ursprung eines beliebigen Streams auftritt.</span><span class="sxs-lookup"><span data-stu-id="f36f0-115">When playing back MPEG-2 program streams, the MPEG-2 Splitter filter treats the first system clock reference it encounters as the time origin of any stream.</span></span> <span data-ttu-id="f36f0-116">Dies unterscheidet sich vom [MPEG-1-Datenstrom Splitter](mpeg-1-stream-splitter-filter.md), der Präsentationszeit Stempel verwendet.</span><span class="sxs-lookup"><span data-stu-id="f36f0-116">This differs from the [MPEG-1 Stream Splitter](mpeg-1-stream-splitter-filter.md), which uses presentation time stamps.</span></span> <span data-ttu-id="f36f0-117">Die [**iamparser:: getsamantime**](/previous-versions/windows/desktop/api/Amparse/nf-amparse-iamparse-getparsetime) -Methode gibt die (möglicherweise geschätzte) Datenstrom System-Uhrzeitangabe für die verarbeiteten Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="f36f0-117">The [**IAMParse::GetParseTime**](/previous-versions/windows/desktop/api/Amparse/nf-amparse-iamparse-getparsetime) method returns the (possibly estimated) stream system clock time for the data it has processed.</span></span>

<span data-ttu-id="f36f0-118">Wenn der MPEG-2-Splitter Filter ein Eingabe Beispiel mit der Diskontinuität-Eigenschaft festgelegt hat (die Diskontinuität-Eigenschaft kann mithilfe von [**imediasample festgelegt werden: setdiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) oder [**IMediaSample2:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties)) überspringt die Daten, bis das erste Paket in den Daten gefunden wird, und passt die Zeitstempel so an, dass der System Takt Verweis (SCR) für dieses Paket vor der Diskontinuität als identisch mit der SCR-Zeit gilt.</span><span class="sxs-lookup"><span data-stu-id="f36f0-118">If the MPEG-2 splitter filter encounters an input sample with the discontinuity property set (the discontinuity property can be set by using [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) or [**IMediaSample2::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties)), it skips data until it finds the first pack in the data and adjusts its time stamps so that the system clock reference (SCR) for that pack is considered identical to the SCR time before the discontinuity.</span></span> <span data-ttu-id="f36f0-119">Wenn die SCR-Uhr angezeigt wird, um mehr als eine Sekunde rückwärts zu springen oder um mehr als eine Sekunde zu springen, wird dies (in Verbindung mit der MPEG-2-Programm Datenstrom Spezifikation) ebenfalls als Zeit Abweichung der Uhr behandelt, und die offensichtliche Takt Abweichung wird von den Zeitstempeln subtrahiert, die an downstreamfilter weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="f36f0-119">If the SCR clock appears either to jump backward or to jump forward by more than a second, then (in line with the MPEG-2 program stream specification), this is also treated as a clock discontinuity and the apparent clock discrepancy is subtracted from the time stamps passed to downstream filters.</span></span>

<span data-ttu-id="f36f0-120">**Streamauswahl**</span><span class="sxs-lookup"><span data-stu-id="f36f0-120">**Stream Selection**</span></span>

<span data-ttu-id="f36f0-121">Bei der Wiedergabe des MPEG-2-Programm Datenstroms werden der erste Videostream und der erste Audiostream, der durchlaufen des Programm Datenstroms gefunden wird, ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="f36f0-121">When playing back the MPEG-2 program stream, the first video stream and first audio stream found traversing the program stream are chosen.</span></span> <span data-ttu-id="f36f0-122">Bis zu eine Audiodatei und eine Videoausgabe-PIN werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f36f0-122">Up to one audio and one video output pin are supported.</span></span> <span data-ttu-id="f36f0-123">Über die [**iamstreamselect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect) -Schnittstelle können unterschiedliche Streams desselben Typs bis zu der Zahl ausgewählt werden, die durch das audiolimit im System Header angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f36f0-123">Through the [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect) interface, different streams of the same type can be selected up to the number specified by the audio limit in the system header.</span></span> <span data-ttu-id="f36f0-124">Bei MPEG-2-Audiodaten wird derzeit angenommen, dass die Streams einen zusammenhängenden Bereich bilden, beginnend bei Stream 0xC0.</span><span class="sxs-lookup"><span data-stu-id="f36f0-124">For MPEG-2 audio, it is currently assumed the streams form a contiguous range starting at stream 0xC0.</span></span>

<span data-ttu-id="f36f0-125">**Unterstützte Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="f36f0-125">**Supported Interfaces**</span></span>

<span data-ttu-id="f36f0-126">Der MPEG-2-Splitter Filter unterstützt die folgenden Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="f36f0-126">The MPEG-2 splitter filter supports the following interfaces.</span></span>

-   <span data-ttu-id="f36f0-127">[**Iamanalysieren**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse).</span><span class="sxs-lookup"><span data-stu-id="f36f0-127">[**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse).</span></span> <span data-ttu-id="f36f0-128">Nur MPEG-2-Programm Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="f36f0-128">MPEG-2 program stream only.</span></span>
-   <span data-ttu-id="f36f0-129">[**Iamstreamselect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect).</span><span class="sxs-lookup"><span data-stu-id="f36f0-129">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect).</span></span> <span data-ttu-id="f36f0-130">Nur MPEG-2-Programmstream, nur Audiostreams.</span><span class="sxs-lookup"><span data-stu-id="f36f0-130">MPEG-2 program stream only, audio streams only.</span></span>
-   <span data-ttu-id="f36f0-131">[**Imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking).</span><span class="sxs-lookup"><span data-stu-id="f36f0-131">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking).</span></span> <span data-ttu-id="f36f0-132">Schließt bytemodusansuchen ein.</span><span class="sxs-lookup"><span data-stu-id="f36f0-132">Includes byte mode seeking.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f36f0-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f36f0-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f36f0-134">MPEG-2-Unterstützung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="f36f0-134">MPEG-2 Support in DirectShow</span></span>](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



