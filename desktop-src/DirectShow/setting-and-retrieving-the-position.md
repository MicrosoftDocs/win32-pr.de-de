---
description: Festlegen und Abrufen der Position
ms.assetid: 06b0e2d7-9539-41ad-a631-7e8da556feeb
title: Festlegen und Abrufen der Position
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776a32eb6193ef456d693b5a133c87d800a0b64e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745409"
---
# <a name="setting-and-retrieving-the-position"></a><span data-ttu-id="f0ff5-103">Festlegen und Abrufen der Position</span><span class="sxs-lookup"><span data-stu-id="f0ff5-103">Setting and Retrieving the Position</span></span>

<span data-ttu-id="f0ff5-104">Im Filter Diagramm werden zwei Positionswerte, die aktuelle Position und die Position des Stopps, beibehalten.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-104">The filter graph maintains two position values, current position and stop position.</span></span> <span data-ttu-id="f0ff5-105">Diese werden wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="f0ff5-105">These are defined as follows:</span></span>

-   <span data-ttu-id="f0ff5-106">Wenn das Diagramm ausgeführt wird, ist die aktuelle Position die aktuelle Wiedergabe Position relativ zum Anfang der Quelle.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-106">When the graph is running, the current position is the current playback position, relative to the beginning of the source.</span></span> <span data-ttu-id="f0ff5-107">Wenn das Diagramm beendet oder angehalten wird, ist die aktuelle Position der Punkt, an dem das Streaming mit dem Befehl für die nächste Ausführung beginnt.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-107">When the graph is stopped or paused, the current position is the point where streaming will begin on the next run command.</span></span>
-   <span data-ttu-id="f0ff5-108">Die Position des Stopps ist der Punkt, an dem der Stream endet.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-108">The stop position is the point where the stream will end.</span></span> <span data-ttu-id="f0ff5-109">Wenn das Diagramm die Stoppposition erreicht, werden keine weiteren Daten gestreamt, und der Filter Graph-Manager stellt ein [**EC \_ Complete**](ec-complete.md) -Ereignis zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-109">When the graph reaches the stop position, no more data is streamed, and the filter graph manager posts an [**EC\_COMPLETE**](ec-complete.md) event.</span></span> <span data-ttu-id="f0ff5-110">(Das Diagramm wechselt jedoch nicht automatisch in den Zustand "beendet".</span><span class="sxs-lookup"><span data-stu-id="f0ff5-110">(The graph does not automatically switch to a stopped state, however.</span></span> <span data-ttu-id="f0ff5-111">Weitere Informationen finden Sie unter [reagieren auf Ereignisse](responding-to-events.md).)</span><span class="sxs-lookup"><span data-stu-id="f0ff5-111">For more information, see [Responding to Events](responding-to-events.md).)</span></span>

<span data-ttu-id="f0ff5-112">Um diese Werte abzurufen, rufen Sie die [**imediaseeking:: getpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-112">To retrieve these values, call the [**IMediaSeeking::GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) method.</span></span> <span data-ttu-id="f0ff5-113">Die zurückgegebenen Werte sind immer relativ zur ursprünglichen Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-113">The returned values are always relative to the original media source.</span></span> <span data-ttu-id="f0ff5-114">Standardmäßig befinden sich die Werte in den Bezugszeit Einheiten.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-114">By default, the values are in reference time units.</span></span> <span data-ttu-id="f0ff5-115">In einigen Fällen können Sie die Zeiteinheiten ändern. Weitere Informationen finden Sie unter [Zeitformate für Such Befehle](time-formats-for-seek-commands.md).</span><span class="sxs-lookup"><span data-stu-id="f0ff5-115">In some cases, you can change the time units; for more information, see [Time Formats For Seek Commands](time-formats-for-seek-commands.md).</span></span>

<span data-ttu-id="f0ff5-116">Um an einer neuen Position zu suchen oder eine neue Halteposition festzulegen, rufen Sie die [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) -Methode auf, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="f0ff5-116">To seek to a new position or set a new stop position, call the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method, as shown in the following example:</span></span>


```C++
#define ONE_SECOND 10000000
REFERENCE_TIME rtNow  = 2 * ONE_SECOND, 
               rtStop = 5 * ONE_SECOND;

hr = pSeek->SetPositions(
    &rtNow,  AM_SEEKING_AbsolutePositioning, 
    &rtStop, AM_SEEKING_AbsolutePositioning
    );
```



> [!Note]  
> <span data-ttu-id="f0ff5-117">Eine Sekunde ist 10 Millionen Einheiten der Verweis Zeit.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-117">One second is 10,000,000 units of reference time.</span></span> <span data-ttu-id="f0ff5-118">Der praktische Wert definiert dieses Beispiel als eine \_ Sekunde.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-118">For convenience, the example defines this value as ONE\_SECOND.</span></span> <span data-ttu-id="f0ff5-119">Wenn Sie die DirectShow-Basisklassen Bibliothek verwenden, haben die Konstanten Einheiten denselben Wert.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-119">If you are using the DirectShow base-class library, the constant UNITS has the same value.</span></span>

 

<span data-ttu-id="f0ff5-120">Der *rtnow* -Parameter gibt die neue aktuelle Position an.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-120">The *rtNow* parameter specifies the new current position.</span></span> <span data-ttu-id="f0ff5-121">Der zweite Parameter ist ein Flag, das definiert, wie *rtnow* interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-121">The second parameter is a flag that defines how to interpret *rtNow*.</span></span> <span data-ttu-id="f0ff5-122">In diesem Beispiel gibt das Flag für die \_ Suche nach \_ absolutepositionierung an, dass *rtnow* eine absolute Position in der Quelle angibt.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-122">In this example, the AM\_SEEKING\_AbsolutePositioning flag indicates that *rtNow* specifies an absolute position in the source.</span></span> <span data-ttu-id="f0ff5-123">Daher sucht das Filter Diagramm zwei Sekunden vom Anfang des Streams bis zu einer Position.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-123">Therefore, the filter graph will seek to a position two seconds from the start of the stream.</span></span> <span data-ttu-id="f0ff5-124">Der *rtstoppt* -Parameter gibt die Endzeit an.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-124">The *rtStop* parameter gives the stop time.</span></span> <span data-ttu-id="f0ff5-125">Der letzte Parameter gibt an, dass *rtbeenden* auch eine absolute Position ist.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-125">The last parameter specifies that *rtStop* is also an absolute position.</span></span>

<span data-ttu-id="f0ff5-126">Um eine Position relativ zum vorherigen Positionswert anzugeben, verwenden Sie das \_ Flag zum Suchen der \_ relativepositionierung.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-126">To specify a position relative to the previous position value, use the AM\_SEEKING\_RelativePositioning flag.</span></span> <span data-ttu-id="f0ff5-127">Wenn Sie einen der Positionswerte unverändert lassen möchten, verwenden Sie das Flag für die \_ Suche nach \_ nopositionsflag.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-127">To leave one of the position values unchanged, use the AM\_SEEKING\_NoPositioning flag.</span></span> <span data-ttu-id="f0ff5-128">Der entsprechende Zeitparameter kann in diesem Fall **null** sein.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-128">The corresponding time parameter can be **NULL** in that case.</span></span> <span data-ttu-id="f0ff5-129">Im folgenden Beispiel wird die Position um 10 Sekunden Fortschritt und die Position des Stopps unverändert gelassen:</span><span class="sxs-lookup"><span data-stu-id="f0ff5-129">The following example seeks forward by 10 seconds but leaves the stop position unchanged:</span></span>


```C++
REFERENCE_TIME rtNow = 10 * ONE_SECOND;
hr = pSeek->SetPositions(
    &rtNow, AM_SEEKING_RelativePositioning, 
    NULL, AM_SEEKING_NoPositioning
    );
```



<span data-ttu-id="f0ff5-130">Wenn das Filter Diagramm angehalten wird, aktualisiert der Videorenderer das Bild nach einem Suchvorgang nicht.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-130">If the filter graph is stopped, the video renderer does not update the image after a seek operation.</span></span> <span data-ttu-id="f0ff5-131">Für den Benutzer wird er so angezeigt, als ob die Suche nicht durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-131">To the user, it will appear as if the seek did not happen.</span></span> <span data-ttu-id="f0ff5-132">Um das Bild zu aktualisieren, halten Sie das Diagramm nach dem Suchvorgang an.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-132">To update the image, pause the graph after the seek operation.</span></span> <span data-ttu-id="f0ff5-133">Durch Anhalten des Diagramms wird ein neuer Videoframe für den Videorenderer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-133">Pausing the graph cues a new video frame for the video renderer.</span></span> <span data-ttu-id="f0ff5-134">Sie können die [**IMediaControl:: stopaconready**](/windows/desktop/api/Control/nf-control-imediacontrol-stopwhenready) -Methode verwenden, die das Diagramm anhält und dann beendet.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-134">You can use the [**IMediaControl::StopWhenReady**](/windows/desktop/api/Control/nf-control-imediacontrol-stopwhenready) method, which pauses the graph and then stops it.</span></span>

 

 



